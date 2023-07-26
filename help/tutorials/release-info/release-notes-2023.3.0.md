---
title: Versionshinweise | Adobe Experience Manager Guides as a Cloud Service, Version März 2023
description: Version der Adobe Experience Manager-Handbücher as a Cloud Service im März
exl-id: c62a65fb-b52d-455d-b42c-f0b19b4d5f63
source-git-commit: f419281cdecb570f9e5c7ce5cd4c831cae349e11
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 2%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service im März 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version März 2023 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version AEM Guides as a Cloud Service im März 2023](whats-new-2023.3.0.md).

## Aktualisierung auf Version März 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der AEM Guides zu aktualisieren:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2023.3.242.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die Version AEM Guides im März 2023 as a Cloud Service zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts (nur, wenn Sie eine Version vor der September-Version von AEM Guides as a Cloud Service verwenden)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungsebene zu suchen und zu ersetzen:

* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: http://&lt;_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service im März 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM-Handbücher für Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | Nicht kompatibel | 2022 oder höher |
| | | |


### Sauerstoffanschluss

| AEM-Handbücher für Cloud | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Der Download-PDF-Prozess funktioniert im Web-Editor nicht ordnungsgemäß. (11496)
* JSON-Ausgabe | Zuordnen von Metadaten mit Eigenschaftswert als `"value in spaces and double quotes"` führt zu einem Veröffentlichungsfehler. (11438)
* Das Einfügen von Audio- und Video-Multimediadateien schlägt im YouTube-Format unter dem **Multimedia einfügen** Symbol. (11320)
* Der Validierungsfehler tritt auf, wenn eine Zuordnung mithilfe der Vorlage erstellt wird, die über ein spezielles Titelelement verfügt. (11212)
* Native PDF | Die Fußnote in der Tabellenüberschrift führt zu fett und zentriert ausgerichtetem Text in der entsprechenden Fußzeile der PDF-Ausgabe. (10610)
>[!NOTE]
>
>Um die Änderung der nativen PDF widerzuspiegeln, löschen Sie den Ordner PDF unter /content/dam/dita-templates und aktualisieren Sie dann auf den neuesten Build. (10610)

### Bekanntes Problem mit Problemumgehung

Adobe hat das folgende bekannte Problem für AEM Guides as a Cloud Service Version März 2023 identifiziert.

* Benutzer können keine Version eines duplizierten Assets speichern oder erstellen.

**Workaround**: Bevor Sie Änderungen am doppelten Asset vornehmen, verarbeiten Sie es über die Assets-Benutzeroberfläche erneut.
