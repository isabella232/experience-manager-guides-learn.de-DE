---
title: Versionshinweise | Upgrade-Anweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern, Version September 2023
description: Erfahren Sie mehr über die Fehlerbehebungen und wie Sie auf die Version September 2023 von Adobe Experience Manager Guides as a Cloud Service aktualisieren können
source-git-commit: 3f79dfbc747b3d2efc05608d05df6ba45e53d877
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 3%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service im September 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version September 2023 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version von AEM Guides as a Cloud Service im September 2023](whats-new-2023.9.0.md).

## Aktualisierung auf Version September 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der AEM Guides zu aktualisieren:

1. Sehen Sie sich den Git-Code des Cloud Service an und wechseln Sie zu der Verzweigung, die in der Cloud Service-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Service-Git-Codes auf 2023.9.0.359.
3. Vergeben Sie die Änderungen und führen Sie die Cloud Service-Pipeline aus, um auf die as a Cloud Service Version von AEM Guides vom September 2023 zu aktualisieren.

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

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt nachzubearbeiten und den neuen Bericht zu fehlerhaften Links zu verwenden:

1. (Optional) Wenn mehr als 100.000 Datendateien im System vorhanden sind, aktualisieren Sie die `queryLimitReads` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` auf einen größeren Wert (ein Wert, der größer ist als die Anzahl der vorhandenen Assets, z. B. 200.000), und dann erneut bereitgestellt werden.

   - Verwenden Sie die Anweisungen unter *Konfigurationsüberschreibungen* im Abschnitt Adobe Experience Manager-Handbücher as a Cloud Service installieren und konfigurieren , um die Konfigurationsdatei zu erstellen.
   - Geben Sie in der Konfigurationsdatei die folgenden (Eigenschaft-)Details an, um die Option queryLimitReads zu konfigurieren:

     | PID | Eigenschaftenschlüssel | Eigenschaftswert |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Wert: 200000 Standardwert: 100000 |

1. Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>//bin/guides/reports/upgrade`.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Sobald der Auftrag abgeschlossen ist, antwortet die vorherige GET-Anfrage erfolgreich. Wenn der Auftrag aus irgendeinem Grund fehlschlägt, kann in den Serverprotokollen ein Fehler angezeigt werden.

1. Wiederherstellen des standardmäßigen oder vorherigen vorhandenen Werts von `queryLimitReads` wenn Sie es in Schritt 1 geändert haben.

## Schritte zum Indexieren des vorhandenen Inhalts zur Verwendung der neuen Suchen- und Ersetzen- und Themenliste auf der Registerkarte Berichte :

(Nur wenn Sie eine Version vor der Version von AEM Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungs- und Themenliste auf der Registerkarte Berichte zu finden und zu ersetzen:

1. Führen Sie eine POST-Anfrage an den Server aus \(mit korrekter Authentifizierung\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert \|\| Beispiel : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. Sie können auch einen Stammordner übergeben, um die DITA-Maps eines bestimmten Ordners (und seiner Unterordner) zu indizieren. Beispiel: `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Beachten Sie, dass nur der Pfadparameter berücksichtigt wird, wenn sowohl der Pfadparameter als auch der Stammparameter übergeben werden.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Sobald der Auftrag abgeschlossen ist, antwortet die vorherige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service vom September 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM-Handbücher für Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.09.0 | Nicht kompatibel | 2022 oder höher |
| | | |


### Sauerstoffanschluss

| AEM-Handbücher für Cloud | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.09.0 | 3.1-uuid 17 | 3.1-uuid 17 | 2.3 | 2.3 |
|  |  |  |  |


### Knowledgebase-Vorlagenversion

| Name des Komponentenpakets | Komponentenversion | Vorlagenversion |
|---|---|---|
| Inhaltspaket für AEM Guides-Komponenten für Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

- Die Themendatei ist im Web Editor nicht entsperrt, obwohl die Option Datei entsperren und die Option Nicht speichern ausgewählt sind. (12558)
- Eine Datei kann nicht im Web Editor ausgecheckt werden, obwohl die Option NO ausgewählt wurde, um die Änderungen vor dem Einchecken zu verwerfen. (12557)
- Die QuickInfos für die Symbole zum Sperren und Entsperren von Dateien in der Hauptsymbolleiste des Web-Editors stimmen nicht mit den in der Repository-Ansicht angezeigten Symbolen überein.(12555)
- Die Option Auschecken abbrechen und Entsperren wird für eine Datei im Web Editor angezeigt, die noch nicht in der Kartenansicht ausgecheckt ist. (12556)
- Die PDF-Assets können nicht in den vorhandenen &quot;topicref&quot;-Links ausgewählt werden. (12477).
- In der Repository-Ansicht können Themen oder Bilder nicht nach Verwendung der Such-/Filterfunktion gezogen werden. (12396)
- Suchergebnisse werden im Bereich Suchen und Ersetzen deaktiviert, nachdem eine durchsuchte Datei geöffnet wurde. (12142)
- Die 8-Taste auf der Seitentastatur funktioniert nicht im AEM Guides-Editor. (12106)

- Das Präfix wird im Vorschaumodus des Web-Editors dupliziert. (13133)
- `Choicetable` -Zeilen nicht angezeigt werden oder nicht ausgewählt werden können. (12616)
- Der Web Editor gibt bei der Erstellung eines Themas mit einem benutzerdefinierten Schema in bestimmten Szenarien Validierungsfehler aus. (12576)
- Die Referenzen der Ditaval-Themenvorlage erstellen beim Erstellen einer Zuordnung aus der Zuordnungsvorlage keine Kopie im Inhaltsordner. (12150)
- Das Suchfeld in DITA-Maps hat keine Schließen-Schaltfläche. (11867)
- Beim Speichern langer Dateien im Web-Editor `DirtyChecker` gibt eine Ausnahme mit einer langen Stacktrace aus und füllt die Protokolldateien. (11860)
- Für das Erstellen von DITA-Themen ist eine Löschberechtigung für den entsprechenden Ordnerknoten erforderlich, obwohl die Zuordnung mit Schreibberechtigung erstellt werden kann. (11706)
- Der Web Editor zeigt einen falschen Titel an, wenn ein Schrägstrich vorhanden ist. (10949)


### Verwaltung

- Das Feld &quot;title&quot;in den Metadateneigenschaften von DITA-Maps wird von `<title>` -Element für die Zuordnung. (10702)
- Der Inhaltsverweis ist beim Kopieren und Einfügen von DITA-Dateien beschädigt, wenn die Themen-ID nicht mit der GUID übereinstimmt. (12614)
- In dynamischen Grundlinien wird die Liste der Beschriftungen nicht aus den direkten Verweisen der Arbeitskopie einer DITA-Zuordnung abgerufen. (11917)

### Veröffentlichung

- Die Veröffentlichung schlägt beim Umbenennen einer nativen PDF-Vorgabe fehl. (12564)
- Beim Duplizieren einer nativen PDF-Vorlage wird der Standardspeicherort der Vorlage anstelle des angegebenen benutzerdefinierten Vorlagenspeicherorts übernommen. (12563)

- Native PDF | Durch die Verwendung mehrerer xrefs wird der Text über die Spaltenbreite hinaus erweitert. (13004)
- Native PDF | Wenn das Thema und der Titel dieselbe ID aufweisen, führt dies zu einer fehlerhaften Generierung der PDF-Ausgabe. (12644)
- Native PDF | Beim Hinzufügen einer Ausgabeklasse zu einer übergeordneten Klasse `<topicref>` -Element in einer DITA-Zuordnung und durch Anwendung eines benutzerdefinierten Stils auf die Ausgabeklasse wird die Formatierung auf Elemente im Themenhauptteil angewendet, einschließlich Abschnittstitel.(12166)
- Inkrementelle Veröffentlichung funktioniert nicht, wenn eine DITA-Map über mehrere Ditavalrefs verfügt. (12117)
- AEM Site | Beim Erstellen einer Zuordnung mit Keydef, die auf ein Thema als Variable verweist, und beim Hinzufügen von processing-role=resource-only werden einige unerwartete Seiten erstellt. (12099)
- Wenn Assets aus AEM DAM in einer anderen Ausgabe als der AEM-Site verwendet werden, spiegeln die Metadaten &quot;jcr:createdBy&quot;nicht den Namen des Herausgebers oder den Namen des Benutzers wider, der die DITA-Map oder das Thema zuletzt geändert hat. (12090)
- AEM Sites | DITA-Zuordnung mit topichead im Navigationstitel (mit nicht unterstützten Zeichen) führt zu fehlerhaften Seiten-URLs. (11978)
- Native PDF | Probleme treten zur Unterstützung von topichead/topicmeta/navtitle in Frontmatter und Backmatter auf. (11969)
- Native PDF | Das Generieren von PDF für große Dokumente ist zeitaufwendig. (11955)
- Native PDF | Beim Umbenennen einer Vorgabe wird beim Generieren einer PDF-Ausgabe eine NullPointerException ausgelöst. (11889)
- Die `<conref>` -Inhalt wird nicht in der PDF-Ausgabe angezeigt. (11131)
- Innerhalb der `<div>` Elemente zum Wechseln zwischen der Autoren- und der Quellansicht im Seitenlayout-Editor. (10750)
- Der im AEM Cloud Manager replizierte Inhalt ist nicht in der Veröffentlichungsinstanz sichtbar. (9564)

### Übersetzung

- Der Prozess zum Exportieren einer umbenannten Grundlinie für eine Übersetzung schlägt fehl. (12993)
- Der Titel der übersetzten Datei wird anstelle des Titels der Quelldatei angezeigt. (11630)




