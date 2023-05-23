---
title: Versionshinweise | Neue Funktionen in Version 4.2 der Adobe Experience Manager-Handbücher
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in Version 4.2 der Adobe Experience Manager-Handbücher.
source-git-commit: a54ada55dad4ff8da8eee3dccb5ad9028b4cdc9e
workflow-type: tm+mt
source-wordcount: '2417'
ht-degree: 0%

---

# Neue Funktionen in Version 4.2 der Adobe Experience Manager-Handbücher (Februar 2023)

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version 4.2 der Adobe Experience Manager-Handbücher (später auch als *AEM*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie in der [Versionshinweise](release-notes-4.2.md) Artikel.

## Generieren von Berichten über den Web-Editor

AEM Guides verfügen über eine Funktion im Web Editor, mit der Sie die Gesamtvollständigkeit Ihrer technischen Dokumente überprüfen und Berichte für diese erstellen können.
Sie können die Themenliste anzeigen und die Metadaten aller Verweise für die aktuelle Zuordnung über die
**Berichte** im Web Editor.

**Ansicht &quot;Topic List&quot;generieren**

Sie können die Themenliste generieren, die detaillierte Informationen zu Ihren Themen enthält, z. B. den Referenztyp, den Dokumentstatus und den Autor. Sie können auch die CSV-Datei generieren, um die aktuelle Momentaufnahme der Themen in der DITA-Map herunterzuladen.

**Metadaten verwalten und Dokumentstatus ändern**

Sie können Tags auf ein einzelnes Thema anwenden oder die Bulk-Tagging-Funktion verwenden, um mehrere Tags auf mehrere Themen, eine DITA-Zuordnung oder eine Unterzuordnung anzuwenden. Sie können auch den Dokumentstatus aller ausgewählten Themen in den nächsten möglichen allgemeinen Dokumentstatus ändern.

<img src="assets/web-editor-metadata-panel.png" alt="Verwalten von Metadaten" width="600">

## UX für die Überprüfungsfunktion überarbeitet

Jetzt bieten AEM Handbücher eine verbesserte UX, mit der Sie die Themen, die zur Überprüfung freigegeben wurden, überprüfen können. Im neuesten Erlebnis bietet die Überprüfungsfunktion die folgenden Verbesserungen:

* Die Benutzeroberfläche wurde aktualisiert
* Bereich &quot;Bedingungen&quot;, in dem Sie den Inhalt gemäß den verfügbaren Bedingungen im Thema hervorheben können.
* Jeder Kommentar im Kommentarbereich ist mit dem entsprechenden Text im aktuellen Thema verknüpft. Sie können damit den kommentierten Text identifizieren.
* Die Kommentare werden in der Reihenfolge des kommentierten Texts im Dokument angezeigt.
* Der Name der Prüfungsaufgabe wird im Überprüfungs-Workflow angezeigt.
* Wählen Sie die Rootmap für die Überprüfungsaufgabe aus, die zur Auflösung aller wichtigen Verweise und Glossarbegriffe verwendet wird, die im Überprüfungsinhalt verwendet werden.
* Kontextsymbolleiste, mit der Sie schnell Text hervorheben oder durchstreichen können.
* Menü &quot;Optionen&quot;, um Ihre eigenen Kommentare zu bearbeiten oder zu löschen.
* Für veraltete Kommentare haben Sie Zugriff auf eine Seitenansicht, die Ihnen hilft, die vorherige Version des Themas mit der aktuellen Reviewversion zu vergleichen
* Bei Verwendung der Filter werden die Kommentare im rechten Bereich entsprechend der Auswahl gefiltert und die Anzahl der Kommentare im linken Bereich wird entsprechend aktualisiert.


<img alt="Prüfungsaufgabe" src="assets/comment-pop-up-panel.png" width="600">


Weitere Informationen finden Sie im Abschnitt *Themen oder Karten überprüfen* im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.

## Verbesserungen bei der Übersetzung

Jetzt verfügen Sie über benutzerfreundlichere Verbesserungen im Dashboard &quot;Übersetzung&quot;, die Ihnen die einfache Übersetzung Ihrer Dokumente aus dem Web-Editor erleichtern.


**Spalte &quot;Versionsbezeichnung&quot;zum Übersetzungs-Dashboard hinzugefügt**

Im Übersetzungs-Dashboard wird auch die Spalte Versionsbezeichnung angezeigt. Dadurch wird der Titel der ausgewählten Version der Quelldatei angezeigt. Auf diese Weise können Sie alle Dateien mit einem bestimmten Titel auswählen und in einem Schritt übersetzen.

**Versionsunterschied für nicht synchronisierte Dateien im Übersetzungs-Dashboard anzeigen**

Jetzt können Sie die Unterschiede zwischen der ausgewählten Version und der zuletzt übersetzten Quellversion der Themen überprüfen. Sie können auch die **Nicht synchronisiert** -Dateien basierend auf den Änderungen, die zwischen den beiden Versionen eines Themas vorgenommen wurden.

<img src="assets/translation-version-diff.png" alt="Übersetzungsbüro" width="600">



**Übergeben der Versionsbezeichnung an die Zielversion**

Mit AEM Guides können Sie den Titel der Quelldatei an die Zieldatei übergeben. Auf diese Weise können Sie die Quellversion der übersetzten Datei leicht identifizieren.

<img alt="Übersetzungstitel" src="assets/translation-pass-source-label.png" width="600">

Wenn Sie beispielsweise Quelldateien mit der Versionsbeschriftung Release 1.0 auf sie angewendet haben, können Sie auch die Quellbeschriftung (Release 1.0) an die übersetzte Datei übergeben.

**Synchronisierung für nicht synchronisierte Assets erzwingen**

Wenn Sie Änderungen an einigen Assets vornehmen, kennzeichnet AEM Guides diese als nicht synchronisiert. Sie können die geänderten Assets entweder erneut übersetzen oder den Status Nicht synchronisiert verwerfen auswählen. Wenn Sie beispielsweise einige kleinere Änderungen vorgenommen haben, die eigentlich keine Übersetzung benötigen, können Sie ihren Status als In Sync markieren.

**In Bearbeitung befindliche Übersetzungsprojekte für ein Thema oder eine Zuordnung anzeigen**

Einige Verweise auf Ihr Übersetzungs-Dashboard werden möglicherweise ausgeführt. Jetzt bietet AEM Guides eine Funktion, mit der Sie die Liste aller laufenden Übersetzungsprojekte (zusammen mit der Zielsprache) anzeigen können, die die ausgewählte Referenz enthalten.

Weitere Informationen finden Sie im Abschnitt *Übersetzen von Dokumenten aus dem Web Editor* im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.

## Generieren von Ausgaben in verschiedenen Formaten über den Web Editor

Jetzt können Sie die Ausgabe für Ihre Themen oder DITA-Maps einfach im Web Editor generieren. Sie können verschiedene Ausgabevorgaben wie AEM Site, PDF, HTML5, JSON (Headless-Ausgabeformat) und benutzerdefinierte Ausgabe konfigurieren. Verwenden Sie diese, um die entsprechenden Ausgaben zu generieren. Sie können Attribute in Ihren DITA-Themen definieren und dann die Bedingungsvorgabe verwenden, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Sie können auch die Funktion Grundlinien-Veröffentlichung verwenden, um eine bestimmte Version Ihrer DITA-Map oder Ihres Themas selektiv zu veröffentlichen.

**Ausgabevorgaben für Global- und Ordnerprofile verwalten**

AEM Handbücher bieten Ihnen die Möglichkeit, Ausgabevorgaben für die globalen und Ordnerprofile zu erstellen und zu verwalten. Dann können Sie diese Ausgabevorgaben einfach verwenden, um die Ausgabe für alle Maps zu generieren, die mit diesem Global- oder Ordnerprofil verbunden sind.

<img alt="Vorgabe hinzufügen" src="assets/add-global-output-preset.png" width="400">


Diese globalen Vorgaben werden unter der **Ausgabe** -Registerkarte aller zugehörigen Maps. Sie können sie verwenden, um die Ausgabe für alle zugehörigen Maps zu generieren. Sie können die Vorgabe als PDF-Standardvorgabe auswählen, um die PDF-Ausgabe zu generieren. Sie können auch **Bearbeiten**, **Umbenennen**, **Duplizieren** oder **Löschen** eine vorhandene Ausgabevorgabe aus der **Optionen** Menü.

>[!NOTE]
>
>Nur Benutzer mit Administratorrechten auf Ordnerebene können Vorgaben für Global- und Ordnerprofile erstellen.

## Suchen und Ersetzen von Text auf Zuordnungsebene

Sie können jetzt nach Dateien in einer Zuordnung suchen, die bestimmten Text enthalten. Der gesuchte Text wird in den Dateien hervorgehoben. Sie können das gesuchte Wort oder die gesuchte Wortgruppe auch durch ein anderes Wort oder eine andere Wortgruppe in den Dateien ersetzen. Wählen Sie die **Einmaliges Auftreten ersetzen** -Symbol, um das aktuelle Vorkommen und das **Alle in Datei ersetzen** -Symbol, um alle Vorkommen in der ausgewählten Datei zu ersetzen. Sie können **Alle ersetzen** -Symbol, um alle Vorkommen des gesuchten Begriffs in allen Dateien zu ersetzen.

<img src="assets/map-find-replace.png" alt="map find replace" width="600">


Standardmäßig werden die Optionen **Checkout-Datei vor Ersetzen** und **Neue Version erstellen nach Ersetzen** ausgewählt sind, sodass eine Datei ausgecheckt wird, bevor Sie den Text ersetzen, und eine neue Version erstellt wird, nachdem der Text ersetzt wurde. Sie können die Zeichenfolge auch in den indirekten Verweisen in der DITA-Zuordnung durchsuchen. Standardmäßig ist dies deaktiviert, sodass die Suche nur für direkte Verweise durchgeführt wird.

## Layout-Ansicht im Map Editor


Jetzt können Sie das vollständige Layout einer DITA-Karte im Map Editor anzeigen. Wenn Sie eine Karte zur Bearbeitung öffnen, wird die Ansicht &quot;Layout&quot;des Map-Editors geöffnet. In dieser Ansicht können Sie die Zuordnungshierarchie in einer Baumansicht sehen. Sie können die Themen in einer Zuordnung auch bearbeiten, organisieren oder strukturieren.

<img src="assets/layout-view-map.png" alt=" Kartenlayout-Ansicht" width="600">

Die Ansicht &quot;Layout&quot;enthält eine separate Symbolleiste, mit der Sie viele Aufgaben zu den in einer Zuordnung vorhandenen Themen ausführen können.
Sie können Themenverweise, Themengruppen und Schlüsseldefinitionen in eine Zuordnung einfügen. Sie können die in einer Karte vorhandenen Themen neu organisieren, indem Sie sie nach oben, unten, links oder rechts verschieben. Sie können die Themen auch per Drag-and-Drop in eine Karte verschieben. Der Map Editor bietet außerdem die Symbole zum Sperren oder Entsperren von Dateien, zum Überprüfen des Versionsverlaufs und zum Verwalten von Versionsbeschriftungen.


Die Ansicht &quot;Layout&quot;bietet außerdem die **Anzeigeoptionen** um die Zeilennummer ein- oder auszublenden, das Kontrollkästchen ein- oder auszublenden oder den Dateinamen oder Titel für die Themen in einer Zuordnung anzuzeigen.
Sie können die Themen auch basierend auf den angewendeten bedingten Filtern anzeigen.

Neben der Organisation von Themen in der Map-Datei können Sie auch Verweise hinzufügen, verschieben, kopieren, einfügen oder löschen, indem Sie die **Optionen** für ein Element in der Ansicht &quot;Layout&quot;verfügbar.

<img src="assets/layout-inline-attributes.png" alt=" Zuordnungslayoutattribute" width="600">


Im rechten Bereich werden die Inhaltseigenschaften und die Zuordnungseigenschaften in der Ansicht &quot;Layout&quot;des Map-Editors angezeigt. Jetzt können Sie auch die Metadateninformationen für die Themen oder die Zuordnung festlegen. Sie können den Navigationstitel, den Linktext, die Kurzbeschreibung und die Suchbegriffe für das ausgewählte Thema oder die ausgewählte Zuordnung definieren.

Weitere Informationen finden Sie unter *Layoutansicht* im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.

## Bereich &quot;Schnellgenerierung&quot;

Jetzt stellt AEM Guides das Bedienfeld Schnellgenerierung bereit, mit dem Sie schnell die Ausgabe für Vorgaben generieren und anzeigen können, die für Ihre DITA-Zuordnung erstellt wurden.

<img src="assets/quick-generate-map-view.png" alt=" Schnellgenerierbereich" width="600">

Im **Schnellgenerierung** angezeigt, können Sie die Liste aller für Ihre DITA-Zuordnung erstellten Ausgabevorgaben sehen. Sie können auch die für die Vorgaben generierte Ausgabe schnell anzeigen. Nach der Generierung der Ausgabe wird eine Erfolgs- oder Fehlermeldung angezeigt. Sie können auch das Fehlerprotokoll anzeigen, das Details des im Generierungsprozess aufgetretenen Fehlers enthält.

## Dynamische Grundlinie basierend auf Bezeichnungen erstellen

Jetzt bietet Ihnen AEM Guides die Möglichkeit, dynamische Grundlinien basierend auf Bezeichnungen zu erstellen. Wenn Sie eine Grundlinie erstellen, eine Grundlinie herunterladen oder ein Übersetzungsprojekt mit einer Grundlinie erstellen, werden die Dateien dynamisch anhand der aktualisierten Beschriftungen ausgewählt. Diese Funktion ist praktisch, da Sie die Grundlinie bei der Aktualisierung der Beschriftungen nicht ändern müssen.

<img src="assets/dynamic-baseline.png" alt=" dynamische Grundlinie" width="400">

## Löschen und Duplizieren von Dateien aus dem Repository-Bereich

Jetzt können Sie Dateien (einzelne Datei pro Datei) einfach aus der **Optionen** Menü der ausgewählten Datei aus dem Repository-Bereich. Vor dem Löschen der Datei wird eine Bestätigungsaufforderung angezeigt. Wenn keine andere Datei auf die Datei verweist, wird sie gelöscht und es wird eine Erfolgsmeldung angezeigt.

<img src="assets/options-menu-repo-view-file-level.png" alt="Menü für Dateioptionen " width="500">

Sie können auch ein Duplikat oder eine Kopie der ausgewählten Datei erstellen. Standardmäßig wird die Datei mit einem Suffix erstellt (z. B. filename_1.extension).


## Weitere Verbesserungen am Webeditor

* In AEM Handbüchern können Sie über das Kontextmenü einige gängige Vorgänge für Bilder und Mediendateien ausführen. Jetzt können Sie auch das ausgewählte Bild oder Medium im Repository suchen oder die Vorschau der Datei in der Assets-Benutzeroberfläche anzeigen.

* Der Name des aktuellen Ordnerprofils wird als Beschriftung für das Symbol Benutzereinstellungen in der Hauptsymbolleiste angezeigt. Auf diese Weise können Sie das Ordnerprofil identifizieren, an dem Sie gerade arbeiten.

* Wenn Sie eine Karte in der Kartenansicht öffnen, wird der Titel der aktuellen Karte in der Mitte der Hauptsymbolleiste angezeigt. Dies ist hilfreich, um den Benutzern mitzuteilen, welche Karte derzeit geöffnet ist.

## Ausgewählte Dateiversionen bereinigen

Beim Erstellen und Verwalten Ihres Inhalts werden möglicherweise viele Versionen für Ihre DITA-Dateien in Ihrem Repository erstellt. Mit AEM Guides können Sie ältere Versionen Ihrer DITA-Dateien aus dem Repository löschen und Speicherplatz freigeben.

<img src="assets/preview-purge-report.png" alt="Bereinigungsbericht in der Vorschau" width="500">

AEM Guides löschen nicht die erste Version der Datei oder eine Version, die in einer Grundlinie enthalten ist oder auf die eine Beschriftung angewendet wird. Der Bereinigungsvorgang löscht nicht einmal Dateien, die in einer Übersetzung oder einem Prüfungs-Workflow enthalten sind. Sie können die Anzahl der beizubehaltenden Versionen auswählen und auch die Dateien löschen, die älter als die definierte Anzahl von Tagen sind.

Bevor Sie mit dem Bereinigungsvorgang beginnen, können Sie eine Vorschau des Berichts anzeigen, um die Versionen anzuzeigen, die bereinigt werden sollen. Anschließend können Sie den Bereinigungsvorgang starten oder abbrechen.

<img src="assets/download-purge-report.png" alt="PDownload-Bereinigungsbericht" width="500">

Nach Abschluss des Bereinigungsvorgangs können Sie den Bereinigungsbericht prüfen, um die bereinigten Dateien anzuzeigen.

## Anzeigen des Titels anstelle der UUID im Sauerstoffeditor

Jetzt können Sie AEM Guides auswählen **Verwenden von Titel in Editor und Maps Manager** in den Einstellungen. Wenn Sie diese Option auswählen, wird der Titel der Datei auf der Registerkarte der Datei angezeigt, wenn er im Editor oder im DITA Maps Manager geöffnet wird. Wenn Sie diese Option nicht auswählen, wird die UUID der Datei auf der Registerkarte der Datei angezeigt.

## Für PDF-Vorgaben verfügbare Metadaten-Benutzeroberfläche

Sie können die Metadaten aus der Ausgabevorgabe einer DITA-Zuordnung festlegen. Sie können die Metadaten Titel, Autor, Betreff und Suchbegriffe festlegen. Diese Metadaten werden den Metadaten in den Dateieigenschaften Ihrer Ausgabe-PDF zugeordnet. Diese Metadaten setzen die auf Buchebene definierten Metadaten außer Kraft. Sie können die Metadaten in jeder Ausgabevorgabe spezifisch definieren und an die Ausgabe-PDF übergeben.

## Native PDF | PDF mit Änderungsleiste, die den Unterschied zwischen Dokumentversionen anzeigt

Jetzt können Sie eine PDF erstellen, die die Inhaltsunterschiede zwischen zwei Versionen mithilfe der Änderungsleiste anzeigt. Sie können die aktuelle Version mit einer Grundlinie der vorherigen Version vergleichen oder zwischen den beiden ausgewählten Grundversionen vergleichen.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Auf der PDF wird eine Änderungsleiste angezeigt, die den geänderten, eingefügten oder gelöschten Inhalt angibt. Sie haben auch die folgenden Optionen:
* Eingefügten Inhalt in grüner Farbe anzeigen und unterstrichen
* Gelöschte Inhalte in roter Farbe anzeigen und mit einem Durchstreichen markieren

## Native PDF | Variablenunterstützung für Output Path und PDF File Name

Jetzt können Sie auch die folgenden vordefinierten Variablen verwenden, um den Ausgabepfad und die PDF-Datei zu definieren. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um die folgenden Optionen zu definieren:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Nur für Ausgabepfad)
* `${path_after_langfolder}` (Nur für Ausgabepfad)

## Native PDF | Inhaltsverzeichnis für DITA-Maps generieren und Seitenlayouts neu anordnen

Jetzt können Sie das Inhaltsverzeichnis auch in DITA-Maps generieren, indem Sie eine erweiterte PDF-Einstellung der Vorlage verwenden. Sie können die Anzeige der verschiedenen Seitenlayouts aktivieren oder deaktivieren und ihre Position neu anordnen.

## Native PDF | Hinzufügen eines benutzerdefinierten Lesezeichens in der PDF-Ausgabe

Jetzt können Sie ein benutzerdefiniertes Lesezeichen zu einem bestimmten Inhalt in Ihrer endgültigen PDF-Ausgabe hinzufügen, um die Navigation zu erleichtern. Dies würde zum TOC hinzugefügt, das aus den Themen- oder Abschnittstiteln in Ihrer DITA-Map erstellt wird.

## Native PDF | Anwenden eines benutzerdefinierten Stils auf Inhaltsverzeichniseinträge und Themeninhalte

AEM Guides bieten die Möglichkeit, benutzerdefinierte Stile auf die TOC-Einträge oder ein bestimmtes Thema in der PDF-Ausgabe anzuwenden. Sie können beispielsweise die Textfarbe im Inhaltsverzeichnis und den Titel des Themas ändern. Sie können auch Stile auf den gesamten Inhalt innerhalb des Themas anwenden.
