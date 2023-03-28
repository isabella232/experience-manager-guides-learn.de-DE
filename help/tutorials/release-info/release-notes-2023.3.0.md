---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version März 2023
description: Neueste Version der Adobe Experience Manager-Handbücher as a Cloud Service
source-git-commit: 27c8c0f3ac5c6d9c318ac8fb7ed13299ac9994de
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service im März

## Aktualisierung auf die neueste Version

Aktualisieren Sie Ihre aktuellen Adobe Experience Manager-Handbücher as a Cloud Service (später als *AEM as a Cloud Service Handbücher*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2023.3.242.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die neueste Version der as a Cloud Service AEM Guides zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts (nur, wenn Sie eine Version vor der September-Version von AEM Guides as a Cloud Service verwenden)

Führen Sie die folgenden Schritte für die Indizierung des vorhandenen Inhalts aus und verwenden Sie den neuen Suchen- und Ersetzen-Text auf Zuordnungsebene:

* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service im März 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM zu Handbüchern as a Cloud - Version | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | Nicht kompatibel | 2022 oder höher |
|  |  |  |


### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Neue Funktionen und Erweiterungen

AEM Guides as a Cloud Service bietet Verbesserungen und neue Funktionen der neuesten Version:

### Öffnen und Abspielen von Video- oder Audiodateien im Web Editor

AEM Handbücher bietet jetzt die Funktion zum Öffnen und Abspielen der Audio- oder Videodateien im Web Editor. Sie können die Lautstärke oder die Ansicht des Videos ändern. Im Kontextmenü haben Sie auch die Möglichkeit, **Download**, ändern **Rückspielgeschwindigkeit** oder Ansicht **Bild im Bild**.

<img src="assets/video-web-editor.png" alt="Abspielvideo" width="600">


## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Der Download-PDF-Prozess funktioniert im Web Editor nicht ordnungsgemäß. (11496)
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

**Problemumgehung**: Bevor Sie Änderungen am doppelten Asset vornehmen, verarbeiten Sie es über die Assets-Benutzeroberfläche erneut.

