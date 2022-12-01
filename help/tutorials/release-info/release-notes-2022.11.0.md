---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version November 2022
description: Neueste Version der Adobe Experience Manager-Handbücher as a Cloud Service
source-git-commit: 549417d6a45508d0afe98574499f1694ae32e708
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 2%

---

# Neueste Version der Adobe Experience Manager-Handbücher as a Cloud Service

## Aktualisierung auf die neueste Version

Aktualisieren Sie Ihre aktuellen Adobe Experience Manager-Handbücher as a Cloud Service (später als *AEM as a Cloud Service Handbücher*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2022.11.198.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die neueste Version der as a Cloud Service AEM Guides zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts (nur, wenn Sie eine Version vor der September-Version von AEM Guides as a Cloud Service verwenden)

Führen Sie die folgenden Schritte für die Indizierung des vorhandenen Inhalts aus und verwenden Sie den neuen Suchen- und Ersetzen-Text auf Zuordnungsebene:

* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexin`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service vom November 2022 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
|  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2022.11.0 | 2,7,13 | 2,7,13 | 2.3 | 2,3 |
|  |  |  |  |


## Neue Funktionen und Erweiterungen

AEM Guides as a Cloud Service bietet Verbesserungen und neue Funktionen der neuesten Version:


### Löschen von Dateien aus dem Repository-Bereich

Jetzt können Sie Dateien (einzelne Datei pro Datei) einfach aus der **Optionen** Menü der ausgewählten Datei aus dem Repository-Bereich.
<img src="assets/repository-delete-file.png" alt="Aus Repository löschen" width="500">

Vor dem Löschen der Datei wird eine Bestätigungsaufforderung angezeigt. Wenn keine andere Datei auf die Datei verweist, wird sie gelöscht und es wird eine Erfolgsmeldung angezeigt.

Wenn die ausgewählte Datei ausgecheckt ist, kann sie nicht gelöscht werden. Eine Fehlermeldung wird angezeigt. Wenn die ausgewählte Datei zu einer Favoriten-Sammlung hinzugefügt oder aus einer anderen Datei referenziert wird, prüft AEM Guides, ob Sie Ihre Bestätigung erhalten haben, und gibt Ihnen die Möglichkeit, sie erzwungen zu löschen. Wenn Sie ein referenziertes Thema löschen und die Datei mit Verweisen zur Bearbeitung geöffnet haben, wird der fehlerhafte Link für die referenzierte Datei angezeigt.

**Hinweis**: Sie können die ausgewählte Datei auch mithilfe der Entf-Taste der Tastatur löschen.


### Ausgewählte Dateiversionen bereinigen

Beim Erstellen und Verwalten Ihres Inhalts werden möglicherweise viele Versionen für Ihre DITA-Dateien in Ihrem Repository erstellt. Mit AEM Guides können Sie ältere Versionen Ihrer DITA-Dateien aus dem Repository löschen und Speicherplatz freigeben.

<img src="assets/preview-purge-report.png" alt="Bereinigungsbericht in der Vorschau" width="500">


AEM Guides löschen nicht die erste Version der Datei oder eine Version, die in einer Grundlinie enthalten ist oder auf die eine Beschriftung angewendet wird. Der Bereinigungsvorgang löscht nicht einmal Dateien, die in einer Übersetzung oder einem Prüfungs-Workflow enthalten sind. Sie können die Anzahl der beizubehaltenden Versionen auswählen und auch die Dateien löschen, die älter als die definierte Anzahl von Tagen sind.

Bevor Sie mit dem Bereinigungsvorgang beginnen, können Sie eine Vorschau des Berichts anzeigen, um die Versionen anzuzeigen, die bereinigt werden sollen. Anschließend können Sie den Bereinigungsvorgang starten oder abbrechen.

<img src="assets/download-purge-report.png" alt="PDownload-Bereinigungsbericht" width="500">

Nach Abschluss des Bereinigungsvorgangs können Sie den Bereinigungsbericht prüfen, um die bereinigten Dateien anzuzeigen.

### Ausgabevorgaben für Global- und Ordnerprofile verwalten

AEM Handbücher bieten Ihnen die Möglichkeit, Ausgabevorgaben für die globalen und Ordnerprofile zu erstellen und zu verwalten. Dann können Sie diese Ausgabevorgaben einfach verwenden, um die Ausgabe für alle Maps zu generieren, die mit diesem Global- oder Ordnerprofil verbunden sind.

<img src="assets/add-global-output-preset.png" alt="Globales Profil hinzufügen" width="400">

**Hinweis** Nur Benutzer mit Administratorrechten auf Ordnerebene können Vorgaben für Global- und Ordnerprofile erstellen.

Diese globalen Vorgaben werden unter der **Ausgabe** -Registerkarte aller zugehörigen Maps. Sie können sie verwenden, um die Ausgabe für alle zugehörigen Maps zu generieren. Sie können die Vorgabe als standardmäßige PDF-Vorgabe auswählen, um die PDF-Ausgabe zu generieren. Sie können auch **Bearbeiten**, **Umbenennen**, **Duplizieren** oder **Löschen** eine vorhandene Ausgabevorgabe aus der **Optionen** Menü.

### Spalte &quot;Versionsbezeichnung&quot;zum Übersetzungs-Dashboard hinzugefügt

Im Übersetzungs-Dashboard wird auch die Spalte Versionsbezeichnung angezeigt. Dadurch wird der Titel der ausgewählten Version der Quelldatei angezeigt. Auf diese Weise können Sie alle Dateien mit einem bestimmten Titel auswählen und in einem Schritt übersetzen.

<img src="assets/send-translation.png" alt="Übersetzen" width="600">


## Verbesserungen der nativen PDF-Veröffentlichung

### PDF mit Änderungsleiste, die den Unterschied zwischen Dokumentversionen anzeigt

Jetzt können Sie eine PDF erstellen, die die Inhaltsunterschiede zwischen zwei Versionen mithilfe der Änderungsleiste anzeigt. Sie können die aktuelle Version mit einer Grundlinie der vorherigen Version vergleichen oder zwischen den beiden ausgewählten Grundversionen vergleichen.

<img src="assets/pdf-change-version.png" alt="spdf-change-version" width="600">

Auf der PDF wird eine Änderungsleiste angezeigt, die den geänderten, eingefügten oder gelöschten Inhalt angibt. Sie haben auch die folgenden Optionen:
* Eingefügten Inhalt in grüner Farbe anzeigen und unterstrichen
* Gelöschte Inhalte in roter Farbe anzeigen und mit einem Durchstreichen markieren

### Variablenunterstützung für Output Path und PDF File Name

Jetzt können Sie auch die folgenden vordefinierten Variablen verwenden, um den Ausgabepfad und die PDF-Datei zu definieren. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um die folgenden Optionen zu definieren:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Nur für Ausgabepfad)
* `${path_after_langfolder}` (Nur für Ausgabepfad)


### Inhaltsverzeichnis für DITA-Maps generieren und Seitenlayouts neu anordnen

Jetzt können Sie das Inhaltsverzeichnis auch in DITA-Maps generieren, indem Sie eine erweiterte PDF-Einstellung der Vorlage verwenden. Sie können die Anzeige der verschiedenen Seitenlayouts aktivieren oder deaktivieren und ihre Position neu anordnen.

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Native PDF | Eine Fußnote in der Tabellenüberschrift führt zu einem fett und zentrierten Fußnotentext in der Fußzeile in der PDF-Ausgabe. (10610)
* Native PDF | `conkeyref` wird in der generierten PDF-Ausgabe nicht aufgelöst. (10564)
* Native PDF | Beim Zugriff auf Metadaten einer Zuordnung in der PDF-Ausgabe treten Probleme auf. (10556)
* Native PDF | Inline-Stil wird zum Generieren von Tags anstelle von Klassennamen verwendet.  (10498)
* Der Web Editor lädt zeitweise eine leere Seite. (10678)
* Die PDF-Veröffentlichung schlägt fehl, wenn eine Vorgabe durch Duplizieren einer vorhandenen Vorgabe erstellt wird. (10584)
* **Protokoll anzeigen** -Schaltfläche funktioniert nicht, wenn die PDF-Generierung für eine Vorgabe fehlschlägt. (10576)
* Hinweis innerhalb eines para-Tags, das eine conref ist, wird nicht in der Vorschau angezeigt. (10559)
* Wenn Sie die Rücktaste am Ende eines Listenelements drücken, wird die gesamte Liste entfernt. (10540)
* Bei Verwendung eines nativen PDF exportieren Sie die verschachtelten `<indexterm>` sind nicht im Index verschachtelt. (10521)
* Bei der falschen Verwendung von Grundlinien-Publishing `cq:tags` werden ausgewählt (aus der aktuellen Arbeitskopie statt aus der Versionskopie ausgewählt). (10494)
* **Auto-Indent** in der Symbolleiste fehlt in der Quellansicht. (10448)
* Das erste Zeichen eines Listenelements geht verloren, während die Liste im Editor erstellt wird. (10447)
* Es werden mehrere Popups angezeigt, wenn eine DITA-Asset-Version geändert und im Fenster der Basisbearbeitung gespeichert wird. (10399)
* Anwendungsfehler beim Klicken **Bearbeiten** nach Auswahl aller Ausgabevorgaben aus dem Bereich Schnellgenerierung . (10388)
* Benutzerdefinierte Metadaten für DITA-Themen werden nicht beibehalten, wenn eine Aktion zum Kopieren und Einfügen über die Assets-Benutzeroberfläche ausgeführt wird. (10367)
* Die Nachbearbeitung wird für den gesamten Sprachordner blockiert, dessen Assets in einem aktiven Übersetzungsprojekt vorhanden sind. (10332)
* Die Registerkarte &quot;Vorlage&quot;im XML-Editor ist für Ordnerprofiladministratoren nicht sichtbar. (10266)
* Navigationsprobleme treten im Web Editor nach der Aktualisierung auf Version 4.0 auf. (10159)
* Das erste Zeichen ist beim Authoring im Web Editor in koreanischer Sprache nicht lesbar. (10049)
* SVG-Dateien werden nicht im Vorschaumodus angezeigt. (10010)
* Wenn die Registerkarte &quot;Ausgabe&quot;des Editors mehr Vorgaben enthält, kann kein Bildlauf im Bereich &quot;Vorgaben&quot;durchgeführt werden und nicht alle Vorgaben werden angezeigt. (9787)
* **Bearbeiten** und **Anmerken** -Optionen für ein Bild funktionieren in der Spaltenansicht nicht ordnungsgemäß. (8758)
* Peer-Link wird nicht aufgelöst und in der generierten Ausgabe als normaler Text angezeigt. (7774)
