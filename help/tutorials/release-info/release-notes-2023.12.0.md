---
title: Versionshinweise | Upgrade-Anweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern, Version Dezember 2023
description: Erfahren Sie mehr über die Fehlerbehebungen und wie Sie auf die Version von Adobe Experience Manager Guides vom Dezember 2023 as a Cloud Service aktualisieren können.
source-git-commit: 9fcc8faec4631d710dbdfd7e4f8567069d0ba120
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 3%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service vom Dezember 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version Dezember 2023 der Adobe Experience Manager-Handbücher as a Cloud Service behobenen Probleme behandelt (später als *Experience Manager Guides as a Cloud Service*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version von Experience Manager Guides as a Cloud Service vom Dezember 2023](whats-new-2023.12.0.md).

## Aktualisierung auf Version Dezember 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der Experience Manager-Handbücher zu aktualisieren:

1. Sehen Sie sich den Git-Code des Cloud Service an und wechseln Sie zu der Verzweigung, die in der Cloud Service-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Service-Git-Codes auf 2023.12.0.15.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Service-Pipeline aus, um auf die Version der Experience Manager-Handbücher vom Dezember 2023 as a Cloud Service zu aktualisieren.

## Schritte zum Aktivieren des Triggers eines Skripts über ein Servlet

(Nur wenn Sie eine Version vor der Version von Experience Manager Guides im Juni 2023 as a Cloud Service haben)

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

In der vorherigen Antwort JSON, der Schlüssel `lockNodePath` enthält den Pfad zum Knoten, der im Repository erstellt wurde und auf den gesendeten Auftrag verweist. Sobald der Auftrag abgeschlossen ist, wird er automatisch gelöscht. In diesem Knoten können Sie den Status des Auftrags nachlesen.

Warten Sie, bis dieser Auftrag abgeschlossen ist, bevor Sie mit den nächsten Schritten fortfahren.

>[!NOTE]
>
> Sie sollten überprüfen, ob der Knoten noch vorhanden ist, und den Status des Auftrags überprüfen.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

## Schritte zum Nachbearbeiten des vorhandenen Inhalts zur Verwendung des Berichts über einen fehlerhaften Link

(Nur wenn Sie eine Version vor der Version von Experience Manager Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte für die Nachbearbeitung des vorhandenen Inhalts und die Verwendung des neuen Berichts über fehlerhafte Links aus:

1. (Optional) Wenn mehr als 100.000 DITA-Dateien im System vorhanden sind, aktualisieren Sie die `queryLimitReads` und `queryLimitInMemory` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` auf einen größeren Wert (ein Wert, der größer ist als die Anzahl der vorhandenen Assets, z. B. 200.000), und dann erneut bereitgestellt werden.

   - Verwenden Sie die im Abschnitt *Konfigurationsüberschreibungen* im Abschnitt Adobe Experience Manager-Handbücher as a Cloud Service installieren und konfigurieren , um die Konfigurationsdatei zu erstellen.
   - Geben Sie in der Konfigurationsdatei die folgenden (Eigenschaft-)Details an, um die `queryLimitReads` und `queryLimitInMemory` Option:

     | PID | Eigenschaftenschlüssel | Eigenschaftswert |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Wert: 200000 Standardwert: 100000 |
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitInMemory | Wert: 200000 Standardwert: 100000 |

1. Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server>//bin/guides/reports/upgrade`.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server>/bin/guides/reports/upgrade?jobId= {jobId}`
(Beispiel: `http://localhost:8080/bin/guides/reports/upgrade?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Nach Abschluss des Auftrags antwortet die vorherige GET-Anfrage erfolgreich. Wenn der Auftrag aus irgendeinem Grund fehlschlägt, kann in den Serverprotokollen ein Fehler angezeigt werden.

1. Auf den standardmäßigen oder vorherigen vorhandenen Wert von zurücksetzen `queryLimitReads` wenn Sie es in Schritt 1 geändert haben.

## Schritte zum Indexieren des vorhandenen Inhalts zur Verwendung der neuen Suchen- und Ersetzen- und Themenliste auf der Registerkarte Berichte :

(Nur wenn Sie eine Version vor der Version von Experience Manager Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungs- und Themenliste auf der Registerkarte Berichte zu finden und zu ersetzen:

1. Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexing`. (Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert|| Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

1. Sie können auch einen Stammordner übergeben, um die DITA-Maps eines bestimmten Ordners (und seiner Unterordner) zu indizieren. Beispiel: `http://<server:port>/bin/guides/map-find/indexing?root=/content/dam/test`. Beachten Sie, dass nur der Pfadparameter berücksichtigt wird, wenn sowohl der Pfadparameter als auch der Stammparameter übergeben werden.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)


1. Nach Abschluss des Auftrags antwortet die vorherige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Schritte zum Verarbeiten der `'fmdita rewriter'` Konflikt

Experience Manager-Handbücher verfügen über eine [**benutzerdefinierte Sling-Rewriter**](../cs-install-guide/conf-output-generation.md#custom-rewriter) -Modul zur Behandlung der im Fall von Querkarten generierten Links (Verknüpfungen zwischen den Themen zweier verschiedener Karten).

Wenn Sie einen anderen benutzerdefinierten Sling-Rewriter in Ihrer Codebase haben, verwenden Sie eine `'order'` Wert größer als 50, da der Experience Manager Guides Sling Rewriter verwendet `'order'` 50.  Um dies zu überschreiben, benötigen Sie einen Wert > 50. Weitere Informationen finden Sie unter [Pipelines zum Neuschreiben der Ausgabe](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Während dieses Upgrades, seit der `'order'` -Wert von 1000 auf 50 geändert wird, müssen Sie die vorhandene benutzerdefinierte Rewriter, sofern vorhanden, mit `'fmdita-rewriter'`.


## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von der Experience Manager Guides-Version vom as a Cloud Service Dezember 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| Experience Manager-Handbücher für as a Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.12.0 | Nicht kompatibel | 2022 oder höher |
| | | |


### Sauerstoffanschluss

| Experience Manager-Handbücher für as a Cloud | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.12.0 | 3.3-uuid.5 | 3.3-uuid.5 | 2.3 | 2.3 |
|  |  |  |  |


### Knowledgebase-Vorlagenversion

| Name des Komponentenpakets | Komponentenversion | Vorlagenversion |
|---|---|---|
| Experience Manager Guides-Komponenteninhaltspaket für Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:



### Authoring

- Die **Titel** auf der Registerkarte &quot;Web Editor&quot;wird nach einem Punkt(.) abgeschnitten Zeichen. (14372)
- Fehlermeldungen für doppelte Zuordnungsnamen in der Assets-Benutzeroberfläche werden nicht aktualisiert. (14320)
- Bei der Versionserstellungslogik tritt beim Ziehen und Ablegen von Assets ein Fehler auf. (14291)
- Wiederverwendbare Inhalte überspringen die Element-IDs. (14213)
- Das Einstellungssteuerelement zum Ausblenden **Sprachvariablen** Bereich unter **Ausgabe** fehlt. (14194)
- Der Web Editor gibt Anwendungsfehler aus, wenn ein neuer Verweis oder Thema mithilfe eines speziellen Schemas in der Layout-Ansicht hinzugefügt wird. (14094)
- Ein Ankerlink zu `<dlentry>` oder `<dt>` -Element kann den Link-Text nicht anzeigen. (13543)
- Die **Favoriten** -Sammlung im Web-Editor kann nicht geladen werden. (13495)
- Zitate zeigen nicht anklickbare Links an, wenn sie mit einer eindeutigen ID mit Leerzeichen erstellt werden. (13447)
- Im **Layout** Ansicht für eine Lesekarte mit **Nach rechts** , um ein ausgewähltes Kapitel zu einem Unterelement zu machen, das nicht funktioniert. (12567)
- Das Vorschaufenster des XML-Editors wird in Google Chrome- und Microsoft Edge-Browsern abgeschnitten. (10755)
- Der Web Editor kann ein Element nicht in die möglichen übergeordneten Elemente einschließen. (8791)

### Veröffentlichung

- Fmdita-Komponenten haben einen fest programmierten Pfad von `delegator.jsp`verhindert die Überlagerung von AEM Sites-Komponenten. (13993)
- Die getaggte Ansicht des PDF-Reaktors in der Ausgabe der nativen PDF-Veröffentlichung funktioniert nicht erwartungsgemäß. (13622)
- AEM Site-Veröffentlichung tritt beim Übertragen an den Datenspeicher für große Maps mit Perimeter-Peer-Links auf ein Problem auf. (13531)
- Eine Site kann nicht über das Dashboard &quot;Massenveröffentlichung&quot;des Experience Manager Guides aktiviert werden. (13439)
- Die Lokalisierung der Elementbeschriftungen funktioniert in der AEM Sites-Ausgabe nicht ordnungsgemäß. (12144)
- Fehlt **Ditaval** -Option in Ausgabevorgaben auf Ordnerprofilebene, die über die Benutzeroberfläche des Web-Editors erstellt wurden. (11903)

### Verwaltung

- AEM Cloud-Umgebungen stoßen aufgrund von großen Knoten auf eine MongoWrite-Ausnahme. (13509)

### Übersetzung

- Die **Akzeptieren/Ablehnen** Fehlerhafte Schaltflächen werden für die automatische menschliche Übersetzung angezeigt. (14318)
- Internationalisierungsprobleme (i18n) treten während der Transformation nicht-englischer DITA-Dateien auf AEM Seiten auf. (14286)
- Übersetzte Inhalte können nicht mit temporären Übersetzungsprojekten synchronisiert werden, und der DITA XML-Editor-Übersetzungs-Assistent zeigt fälschlicherweise **Gestartet** Status für genehmigte Aufträge. (9938)

### Barrierefreiheit

- Die Benutzeroberfläche der Autorenarbeitsfläche kann nicht durchsucht werden, da der Fokus im Themeneditor gefangen wird. (13517)

## Bekanntes Problem

Adobe hat das folgende bekannte Problem für die Version Dezember 2023 identifiziert:
- Beim Upgrade auf die Version vom Dezember 2023 tritt zeitweise der Fehler &quot;Ungültige DTD-Fehler erhalten&quot;auf.