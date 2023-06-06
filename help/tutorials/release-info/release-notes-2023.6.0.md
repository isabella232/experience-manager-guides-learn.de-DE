---
title: Versionshinweise | Upgrade-Anweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern, Version Juni 2023
description: Erfahren Sie mehr über die Fehlerbehebungen und das Upgrade auf die Adobe Experience Manager Guides-Version vom Juni 2023 as a Cloud Service.
source-git-commit: 03d90157f7169373a287f24ab666bfea634e0ca4
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 3%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service im Juni 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version Juni 2023 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM as a Cloud Service Handbücher*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version von AEM Guides as a Cloud Service im Juni 2023](whats-new-2023.6.0.md).

## Aktualisierung auf Version Juni 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der AEM Guides zu aktualisieren:

1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2023.6.297.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die Version AEM Guides vom Juni 2023 as a Cloud Service zu aktualisieren.

## Schritte zum Aktivieren des Triggers eines Skripts über ein Servlet

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
(Beispiel: 
`http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Sobald der Auftrag abgeschlossen ist, antwortet die vorherige GET-Anfrage erfolgreich. Wenn der Auftrag aus irgendeinem Grund fehlschlägt, kann in den Serverprotokollen ein Fehler angezeigt werden.

1. Wiederherstellen des standardmäßigen oder vorherigen vorhandenen Werts von `queryLimitReads` wenn Sie es in Schritt 1 geändert haben.

## Schritte zum Indexieren des vorhandenen Inhalts zur Verwendung der neuen Suchen- und Ersetzen- und Themenliste auf der Registerkarte Berichte :

(Nur wenn Sie eine Version vor der Version von AEM Guides im September 2022 as a Cloud Service haben)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungs- und Themenliste auf der Registerkarte Berichte zu finden und zu ersetzen:

1. Führen Sie eine POST-Anfrage an den Server aus \(mit korrekter Authentifizierung\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert \|\| Beispiel : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. Sie können auch einen Stammordner übergeben, um die DITA-Maps eines bestimmten Ordners (und seiner Unterordner) zu indizieren. Beispiel: `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Beachten Sie, dass nur der Pfadparameter berücksichtigt wird, wenn sowohl der Pfadparameter als auch der Stammparameter übergeben werden.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Sobald der Auftrag abgeschlossen ist, antwortet die vorherige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service im Juni 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM zu Handbüchern as a Cloud - Version | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.06.0 | Nicht kompatibel | 2022 oder höher |
|  |  |  |


### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.06.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

- Navtitle wird beim Wechsel von der Layoutansicht zur Autoren- oder Quellansicht aus dem content33 entfernt. (12174)
- Manchmal tritt beim Klicken auf eine DITA Map ein Anwendungsfehler auf. (11842)
- Web Editor | Beim Bearbeiten eines Themas wird im XML-Editor geschütztes Leerzeichen hinzugefügt. (11786)
- Asset-Benutzeroberfläche | In der Listenansicht sind die überlagerten verfügbaren Spalten nicht zusammenführbar. (11528)
- Keyref ist in der Kartenansicht nicht aufgelöst. (11490)
- Das obere Menü wird nicht angezeigt, wenn Sie durch den XML-Editor navigieren. (10868)
- `conref` im ph-Tag | Das angezeigte Dialogfeld zum Durchsuchen ist falsch. (9481)
- Lokale Links zu anderen Elementen werden im Web Editor nicht aufgelöst. (8790)
- Die Funktion Matches() funktioniert in der Schematron-Funktion nicht. (11224)


### Verwaltung

- Auf der Registerkarte Berichte in der Web Editor-Benutzeroberfläche wird nicht die Themenliste der alten DITA-Maps angezeigt, die vor der Aktualisierung 4.2 erstellt wurden. (11708)

- Die Schaltfläche &quot;Dateien hochladen&quot;in der Assets-Benutzeroberfläche ist in Version 4.2 nicht mehr verfügbar. (11633)

### Veröffentlichung

- Das Veröffentlichen auf AEM Site schlägt fehl, wenn temporäre Dateien aus Pod gelesen werden, die möglicherweise aktualisiert oder neu gestartet wurden. (12113)
- Native PDF | Das Veröffentlichen von Inhalten mit einer Ausgabeklasse mit Klammern() führt zum Einfrieren der Veröffentlichung. (11936)
- JSON-Ausgabe | Zuordnen von Metadaten mit Eigenschaftswert als `"value in spaces and double quotes"` führt zu einem Veröffentlichungsfehler. (11933)
- Web Editor | Ausgabepfad und Vorlage können nicht in der AEM-Vorgabe ausgewählt werden. (11530)
- Native PDF | Benutzerdefinierte Attribute werden nicht an temporäre HTML- oder PDF-Engine übertragen. (DXML-12005)
- Native PDF | Java OutOfMemoryError tritt beim Veröffentlichen großer Inhalte auf. (11789)
- JSON-Ausgabe | Die `fmUuid` -Eigenschaft im Knoten jcr:content von JSON unterscheidet sich von der &quot;id&quot;innerhalb der JSON. (11564)
- JSON-Ausgabe | Wenn die Zuordnung und das Thema mit demselben Dateinamen vorhanden sind, wird JSON für die Zuordnung entfernt. (11524)
- Native PDF | Xref druckt den Inhalt des href-Thementitels anstelle der Xref-Beschriftung. (11322)
- Native PDF | Die PDF-Vorlageneinstellungen können nicht gespeichert werden. (10751)
- Native PDF | Der Text geht über die Spaltenbreite hinaus und schließt mehrere xrefs ein. (10876)
- Native PDF | `<note>``</note>` -Element generiert keinen zusätzlichen span-Titel seines Typs. (10549)



### Übersetzung

- Nach der Cloud-Version vom Februar (2302) werden alle Übersetzungsinhalte als &quot;Nicht synchronisiert&quot;oder &quot;Fehlende Kopie&quot;angezeigt. (11834)

### Überprüfung

- Neue Überprüfungsbenutzeroberfläche | Die Bedingungen markieren und zeigen Verstecken funktioniert anders als im Web-Editor. (11628)
