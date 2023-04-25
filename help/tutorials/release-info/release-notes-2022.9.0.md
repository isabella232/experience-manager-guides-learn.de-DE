---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version September 2022
description: September-Version der Adobe Experience Manager-Handbücher as a Cloud Service
exl-id: f6247f91-43cc-43a4-a6f8-3b1f09d0533f
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 3%

---

# September-Version der Adobe Experience Manager-Handbücher as a Cloud Service

## Aktualisierung auf die September-Version

Aktualisieren Sie Ihre aktuellen Adobe Experience Manager-Handbücher as a Cloud Service (später als *AEM as a Cloud Service Handbücher*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
1. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2022.9.178.
1. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die September-Version von AEM Guides as a Cloud Service zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts

Führen Sie die folgenden Schritte für die Indizierung des vorhandenen Inhalts aus und verwenden Sie den neuen Suchen- und Ersetzen-Text auf Zuordnungsebene:
* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexin`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel :   `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)
* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: `http://<_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)`
* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.


## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service vom September 2022 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
|  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2022.9.0 | 2.7.13 | 2.7.13 | 2.3 | 2.3 |
|  |  |  |  |


## Neue Funktionen und Erweiterungen

AEM Guides as a Cloud Service bietet viele Verbesserungen und neue Funktionen in der Septemberversion:


### Dynamische Grundlinie basierend auf Bezeichnungen erstellen

Jetzt bietet Ihnen AEM Guides die Möglichkeit, dynamische Grundlinien basierend auf Bezeichnungen zu erstellen. Wenn Sie eine Grundlinie erstellen, eine Grundlinie herunterladen oder ein Übersetzungsprojekt mit einer Grundlinie erstellen, werden die Dateien dynamisch anhand der aktualisierten Beschriftungen ausgewählt. Diese Funktion ist praktisch, da Sie die Grundlinie bei der Aktualisierung der Beschriftungen nicht ändern müssen.
Sie können die Momentaufnahme der Grundlinie auch als CSV exportieren.

![Erstellen von Grundlinien](assets/dynamic-baseline.png)

### Suchen und Ersetzen von Text auf Zuordnungsebene

Sie können jetzt nach Dateien in einer Zuordnung suchen, die bestimmten Text enthalten. Der gesuchte Text wird in den Dateien hervorgehoben. Sie können das gesuchte Wort oder die gesuchte Wortgruppe auch durch ein anderes Wort oder eine andere Wortgruppe in den Dateien ersetzen.
Wählen Sie die **Ersetzen** -Symbol, um das aktuelle Vorkommen und das **Alle in Datei ersetzen** -Symbol, um alle Vorkommen in der ausgewählten Datei zu ersetzen.

![Ersetzen in Zuordnung suchen](assets/map-find-replace.png)

Standardmäßig werden die Optionen **Checkout-Datei vor Ersetzen** und **Neue Version erstellen nach Ersetzen** ausgewählt sind, sodass eine Datei ausgecheckt wird, bevor Sie den Text ersetzen, und eine neue Version erstellt wird, nachdem der Text ersetzt wurde.

### Versionsunterschied für nicht synchronisierte Dateien im Übersetzungs-Dashboard anzeigen

Sie können jetzt wählen, ob Sie die **Nicht synchronisiert** -Dateien basierend auf den Änderungen, die zwischen den beiden Versionen eines Themas vorgenommen wurden.\
![Übersetzungs-Dashboard](assets/translation-version-diff.png)
Im Übersetzungs-Dashboard können Sie die Unterschiede zwischen der zuletzt übersetzten Version und der aktuellen Version der ausgewählten Datei leicht erkennen.

![Dialogfeld für Versionsunterschiede](assets/version-diff.png)

Je nach den Unterschieden können Sie entscheiden, ob Sie ein Thema übersetzen möchten oder nicht.

### Für PDF-Vorgaben verfügbare Metadaten-Benutzeroberfläche

Sie können die Metadaten aus der Ausgabevorgabe einer DITA-Zuordnung festlegen. Sie können die Metadaten Titel, Autor, Betreff und Suchbegriffe festlegen. Diese Metadaten werden den Metadaten in den Dateieigenschaften Ihrer Ausgabe-PDF zugeordnet.
Diese Metadaten setzen die auf Buchebene definierten Metadaten außer Kraft. Sie können die Metadaten in jeder Ausgabevorgabe spezifisch definieren und an die Ausgabe-PDF übergeben.

![Metadaten in der Vorgabe](assets/preset-metadata.png)


## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Web Editor | Beim Verschieben von Elementen innerhalb eines Themas werden die zugewiesenen IDs für Elemente durch automatisch zugewiesene IDs überschrieben. (7895)
* Änderungen verfolgen | Der Inhalt geht verloren, wenn mithilfe der Eingabetaste ein neues Element eingegeben wird. (10246)
* Die auf die Hauptkarte in dita-templates verweisende Unterkarte wird nicht erstellt. (10231)
* XML-Editor | Kopieren/Einfügen funktioniert nicht im Autorenmodus. (10309)
* Nach Auswahl mehrerer Versionsbeschriftungen wird die Auswahl nicht aufgehoben. (9561)
* Die automatische Navigation zum Pfad im Dialogfeld zum Durchsuchen der Site funktioniert nicht wie das Durchsuchen von Dateien. (9920)
* Im Bedienfeld &quot;Umrisse&quot;werden keine Inhalte angezeigt, wenn aus **Autor** nach **Quelle** -Modus. (10319)
* Conref in einem neuen Thema, das mit einem Inhalt in der Themenvorlage erstellt wurde, funktioniert nicht. Die kopierte Hash-ID wird in der Inhaltskopie nicht aktualisiert. (9890)
* Web-Editor | Beim Erstellen einer Zuordnung aus der Zuordnungsvorlage existiert kein Lader. (9891)
* Neuer Map-Editor | Formatierter oder kursiver Text im Zuordnungstitel wird nicht beibehalten, wenn Sie von **Autor** der **Layout** anzeigen. (10218)
* Neuer Map-Editor | Bedingungen, die auf einen Verweis angewendet werden, können nicht aus der Ansicht &quot;Layout&quot;entfernt werden. (10213)
* Neuer Map-Editor | Das Anwenden von Bedingungsverweisen funktioniert nicht in der Layout-Ansicht wie in der Autorenansicht. (10198)
* Neuer Map-Editor | Durch Verschieben nach links aus dem Kontextmenü wird der Verweis entfernt, wenn er nicht nach links verschoben werden kann. (10219)
* Neuer Map-Editor |Das Symbol wird für die Verweise in einer mit der Layoutansicht erstellten Zuordnung falsch angezeigt. (10197)
* Repository-Bereich | Ein Rechtsklick in das Repository-Bedienfeld erzeugt einen Anwendungsfehler. (10123)
* Suchen und Ersetzen | Dunkler Modus ist für Suchergebnisse im Web Editor nicht lesbar. (9978)
* Übersetzung | Metadaten und Tags werden nicht an die übersetzten Kopien weitergegeben. (4696)
* Beim Kopieren des Einfügeinhalts (Strg+C/Strg+V) wird im Autorenmodus ein Fehler ausgegeben. (10304)
* PDF-Vorlage | Beim Hinzufügen von Hintergrundbildern zu einem Seitenlayout wird &quot;Bildpfad absolut&quot;angezeigt, und die Bilder werden nicht auf der PDF angezeigt. (10297)
* Native PDF | Kapiteltitel und Kapitelüberschrift funktionieren nicht bei der PDF-Veröffentlichung. (9947)
* Native PDF | `xref` für ein Konzept für ein bestimmtes DITA-Thema nicht richtig aufgelöst. (10229)
* Native PDF | Beschriftungstext für eine Tabelle kann in der generierten PDF-Ausgabe nicht angezeigt werden. (9827)
* Native PDF | Verweise in Anhängen werden in der PDF-Ausgabe nicht als Anhänge angezeigt. (10182)
* Native PDF | Das Attribut &quot;Frame&quot;für eine Tabelle wird nicht auf die temporäre HTML (als Klasse) übertragen. (10353)
* Native PDF | temp HTML-Dateien fügen die Klassen colsep und rowsep zu td hinzu und die , selbst wenn ihr Wert 0 in der Quell-DITA beträgt. (10352)
* Native PDF | Metadaten für im Seitenlayout hinzugefügte Kriterien werden nicht berücksichtigt. (10377)
* Native PDF | Die Erstellung von PDF schlägt bei bestimmten Inhalten fehl. (9927)
* Native PDF | Der Inhalt über conkeyref wird nicht in der PDF-Ausgabe angezeigt. (9836)
* Native PDF | Schlüsselreferenzen für Keydefs mit Bildern oder externen Links werden nicht aufgelöst. (10063)
* Die Autorenansicht für eine Zuordnung zeigt keinen Platzhaltertext für die Tabellenliste und die Dateiliste an. (10330)
* Wenn wir eine neue Grundlinie erstellen, wird der bereits ausgewählte Grundlinienfilter nicht angewendet. (9954)
* Die Videodatei fehlt in der Grundlinie, wenn der Name des übergeordneten Ordners ein Leerzeichen hat. 10031)
* Bei der Grundlagenerstellung wird nicht die neueste Version ausgewählt, wenn sich die Zeitzone des Benutzers von der Zeitzone des Servers unterscheidet. (10190)
* Mit der Tastenkombination Strg + F wird das Browser-Suchmodul nach der Installation von AEM Guides 4.1 in AEM 6.5.12 nicht in der Konsole Assets geöffnet. (10189)


## Bekannte Probleme

Adobe hat die folgenden bekannten Probleme in der Version AEM Guides as a Cloud Service vom September 2022 identifiziert.


* Die dynamische Grundlinie ist nicht in die Knowledgebase-Veröffentlichung integriert.

* Übersetzung | Das Symbol Versionsunterschied wird für den Quellinhalt aufgrund einer Änderung des Zielinhalts angezeigt.
