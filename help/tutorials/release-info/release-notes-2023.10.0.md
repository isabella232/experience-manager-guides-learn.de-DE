---
title: Versionshinweise | Upgrade-Anweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern, Version Oktober 2023
description: Erfahren Sie mehr über die Fehlerbehebungen und wie Sie auf die Version von Adobe Experience Manager Guides vom Oktober 2023 aktualisieren as a Cloud Service
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 1%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service vom Oktober 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version Oktober 2023 der Adobe Experience Manager-Handbücher behobenen Probleme behandelt (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version von AEM Guides as a Cloud Service vom Oktober 2023](whats-new-2023.10.0.md).

## Aktualisierung auf Version Oktober 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der AEM Guides zu aktualisieren:

1. Sehen Sie sich den Git-Code des Cloud Service an und wechseln Sie zu der Verzweigung, die in der Cloud Service-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Service-Git-Codes auf 2023.10.0.373.
3. Nehmen Sie die Änderungen vor und führen Sie die Cloud Service-Pipeline aus, um auf die as a Cloud Service Version der AEM Handbücher vom Oktober 2023 zu aktualisieren.

## Schritte zum Aktivieren des Triggers eines Skripts über ein Servlet

(Nur wenn Sie eine Version vor der Version von AEM Guides im Juni 2023 as a Cloud Service haben)

Nachdem Sie die Installation abgeschlossen haben, können Sie den Trigger drücken, um den Übersetzungsauftrag zu starten:

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Antwort:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

In der vorherigen Antwort JSON, der Schlüssel `lockNodePath` enthält den Pfad zum Knoten, der im Repository erstellt wurde und auf den gesendeten Auftrag verweist. Er wird automatisch gelöscht, sobald der Auftrag abgeschlossen ist. Bis dahin können Sie den aktuellen Status des Auftrags in diesem Knoten nachlesen.

Warten Sie, bis dieser Auftrag abgeschlossen ist, bevor Sie mit den nächsten Schritten fortfahren.

>[!NOTE]
>
> Sie sollten überprüfen, ob der Knoten noch vorhanden ist, und den Status des Auftrags überprüfen.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

## Schritte zum Nachbearbeiten des vorhandenen Inhalts zur Verwendung des Berichts über einen fehlerhaften Link

(Nur wenn Sie eine Version vor der Version von AEM Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte für die Nachbearbeitung des vorhandenen Inhalts und die Verwendung des neuen Berichts über fehlerhafte Links aus:

1. (Optional) Wenn mehr als 100.000 DITA-Dateien im System vorhanden sind, aktualisieren Sie die `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` auf einen größeren Wert (ein Wert, der größer ist als die Anzahl der vorhandenen Assets, z. B. 200.000), und dann erneut bereitgestellt werden.

   - Verwenden Sie die im Abschnitt *Konfigurationsüberschreibungen* im Abschnitt Adobe Experience Manager-Handbücher as a Cloud Service installieren und konfigurieren , um die Konfigurationsdatei zu erstellen.
   - Geben Sie in der Konfigurationsdatei die folgenden (Eigenschaft-)Details an, um die Option queryLimitReads zu konfigurieren:

     | PID | Eigenschaftenschlüssel | Eigenschaftswert |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Wert: 200000 Standardwert: 100000 |

1. Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>//bin/guides/reports/upgrade`.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Nach Abschluss des Auftrags antwortet die vorherige GET-Anfrage erfolgreich. Wenn der Auftrag aus irgendeinem Grund fehlschlägt, kann in den Serverprotokollen ein Fehler angezeigt werden.

1. Auf den standardmäßigen oder vorherigen vorhandenen Wert von zurücksetzen `queryLimitReads` wenn Sie es in Schritt 1 geändert haben.

## Schritte zum Indexieren des vorhandenen Inhalts zur Verwendung der neuen Suchen- und Ersetzen- und Themenliste auf der Registerkarte Berichte :

(Nur wenn Sie eine Version vor der Version von AEM Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungs- und Themenliste auf der Registerkarte Berichte zu finden und zu ersetzen:

1. Führen Sie eine POST-Anfrage an den Server aus \(mit korrekter Authentifizierung\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert \|\| Beispiel : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. Sie können auch einen Stammordner übergeben, um die DITA-Maps eines bestimmten Ordners (und seiner Unterordner) zu indizieren. Beispiel: `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Beachten Sie, dass nur der Pfadparameter berücksichtigt wird, wenn sowohl der Pfadparameter als auch der Stammparameter übergeben werden.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Nach Abschluss des Auftrags antwortet die vorherige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guide as a Cloud Service vom Oktober 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM-Handbücher für Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.10.0 | Nicht kompatibel | 2022 oder höher |
| | | |


### Sauerstoffanschluss

| AEM-Handbücher für Cloud | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.10.0 | 3.2-uuid 5 | 3.2-uuid 5 | 2,3 | 2,3 |
|  |  |  |  |


### Knowledgebase-Vorlagenversion

| Name des Komponentenpakets | Komponentenversion | Vorlagenversion |
|---|---|---|
| Inhaltspaket für AEM Guides-Komponenten für Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

- Nachmittagsstunden werden nicht im **Datum** zur Erstellung von Grundlinien. (12712)
- Der JSON-Code kann nicht in die `<codeblock>` -Element des Web-Editors. (12326)
- Nicht gespeicherte Versionsänderungen und die zugehörigen Indikatoren werden nicht für große Dateien angezeigt. (11784)
- Bei der Bearbeitung in koreanischer Sprache wird das erste Zeichen in den Standard geändert. (10049)


### Veröffentlichung

- Native PDF | Die Reihenfolge der Themen wird nicht festgelegt, wenn die PDF-Ausgabe erzeugt wird. (13157)
- Native PDF | Es ist kein standardmäßiges Stil-Tag verfügbar für `<p>`-Element. (12559)
- Native PDF | Inline-Stile, die auf den Inhaltsbereich angewendet werden, werden nicht auf die Themen in der Vordergrund- und der RückMaterie angewendet. (13510)
- Die `DeliveryTarget` -Attribut wird beim Generieren der AEM Site-Ausgabe nicht übernommen.  (13132)
- Die **Veröffentlichen** Workflow hängt beim Generieren AEM Site-Ausgabe für Inhalte mit bestimmten Fehlern nicht mehr zusammen. (12000)

### Verwaltung

- Versionsverlauf wird nicht angezeigt, auch wenn die `dc:format` -Eigenschaft für ein Asset nicht vorhanden ist. (10463)


### Überprüfung

- Die Themenüberprüfung zeigt falsche Kommentare an. (13453)



### Übersetzung

- Die aus der **Übersetzung** Dashboard schlägt fehl und wird nicht in der Zielsprache geöffnet. (13466)

- Anstatt den ausgewählten Übersetzungsprojekten neue Aufträge hinzuzufügen, werden neue Übersetzungsprojekte erstellt.  (10214)

## Bekanntes Problem

Adobe hat das folgende bekannte Problem für die Version Oktober 2023 identifiziert.

- Das erneute Veröffentlichen von Inhaltsfragmenten schlägt fehl.
