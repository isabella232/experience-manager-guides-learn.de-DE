---
title: Versionshinweise | Adobe Experience Manager-Handbücher Version 4.2
description: Aktuelle Version der Adobe Experience Manager-Handbücher
source-git-commit: 2fb46bdfb7f42fd9b3ef19343700009818c5b4f2
workflow-type: tm+mt
source-wordcount: '3681'
ht-degree: 2%

---

# Version 4.2 von Adobe Experience Manager-Handbüchern (Februar 2023)

In diesem Versionshinweis werden die Upgrade-Anweisungen, neuen Funktionen und Verbesserungen in Version 4.2 der Adobe Experience Manager-Handbücher (später auch als *AEM*).

## Aktualisierung auf die neueste Version

Sie können Ihre aktuelle Version von AEM Guides einfach auf Version 4.2 aktualisieren. Bevor Sie mit der Aktualisierung auf Version 4.2 von AEM Guides fortfahren, müssen Sie die folgenden Punkte beachten:
* Wenn Sie Version 4.0, 4.1 oder 4.1.x verwenden, können Sie direkt auf Version 4.2 aktualisieren.
* Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0 aktualisieren, bevor Sie auf Version 4.2 aktualisieren.
* Wenn Sie eine Version vor 3.8.5 verwenden, lesen Sie den Abschnitt *AEM* im produktspezifischen Installationshandbuch.

>[!NOTE]
>
>Sie müssen AEM Service Pack installieren, bevor Sie AEM Guides-Version aktualisieren.

Weitere Informationen finden Sie unter [Upgrade-Anweisungen](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4,2 | Versionshinweise

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.2 unterstützt werden.

### Adobe Experience Manager

**Nicht-UUID**
Version 6.5 Service Pack 15, 14, 13 oder 12

**UUID**
Version 6.5 Service Pack 15, 14, 13 oder 12

Weitere Informationen finden Sie unter *Technische Anforderungen* im Handbuch &quot;Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern&quot;.

### FrameMaker und FrameMaker Publishing Server

| Release | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (Nicht-UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.3 oder höher |
| 4.2 (UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.4 oder höher |
|  |  |  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Release | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.2 (Nicht-UUID) | 2.1-normal-4 | 2.1-normal-4 | 1,6 | 1,6 |
| 4.2 (UUID) | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |


## Neue Funktionen und Erweiterungen

AEM-Handbücher bieten viele Verbesserungen und neue Funktionen in Version 4.2:

### Generieren von Berichten über den Web-Editor

AEM Guides verfügen über eine Funktion im Web Editor, mit der Sie die Gesamtvollständigkeit Ihrer technischen Dokumente überprüfen und Berichte für diese erstellen können.
Sie können die Themenliste anzeigen und die Metadaten aller Verweise für die aktuelle Zuordnung über die
**Berichte** im Web Editor.

**Ansicht &quot;Topic List&quot;generieren**

Sie können die Themenliste generieren, die detaillierte Informationen zu Ihren Themen enthält, z. B. den Referenztyp, den Dokumentstatus und den Autor. Sie können auch die CSV-Datei generieren, um die aktuelle Momentaufnahme der Themen in der DITA-Map herunterzuladen.

**Metadaten verwalten und Dokumentstatus ändern**

Sie können Tags auf ein einzelnes Thema anwenden oder die Bulk-Tagging-Funktion verwenden, um mehrere Tags auf mehrere Themen, eine DITA-Zuordnung oder eine Unterzuordnung anzuwenden. Sie können auch den Dokumentstatus aller ausgewählten Themen in den nächsten möglichen allgemeinen Dokumentstatus ändern.

<img src="assets/web-editor-metadata-panel.png" alt="Verwalten von Metadaten" width="600">

### UX für die Überprüfungsfunktion überarbeitet

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

### Verbesserungen bei der Übersetzung

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

### Generieren von Ausgaben in verschiedenen Formaten über den Web Editor

Jetzt können Sie die Ausgabe für Ihre Themen oder DITA-Maps einfach im Web Editor generieren. Sie können verschiedene Ausgabevorgaben wie AEM Site, PDF, HTML5, JSON (Headless-Ausgabeformat) und benutzerdefinierte Ausgabe konfigurieren. Verwenden Sie diese, um die entsprechenden Ausgaben zu generieren. Sie können Attribute in Ihren DITA-Themen definieren und dann die Bedingungsvorgabe verwenden, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Sie können auch die Funktion Grundlinien-Veröffentlichung verwenden, um eine bestimmte Version Ihrer DITA-Map oder Ihres Themas selektiv zu veröffentlichen.

**Ausgabevorgaben für Global- und Ordnerprofile verwalten**

AEM Handbücher bieten Ihnen die Möglichkeit, Ausgabevorgaben für die globalen und Ordnerprofile zu erstellen und zu verwalten. Dann können Sie diese Ausgabevorgaben einfach verwenden, um die Ausgabe für alle Maps zu generieren, die mit diesem Global- oder Ordnerprofil verbunden sind.

<img alt="Vorgabe hinzufügen" src="assets/add-global-output-preset.png" width="400">


Diese globalen Vorgaben werden unter der **Ausgabe** -Registerkarte aller zugehörigen Maps. Sie können sie verwenden, um die Ausgabe für alle zugehörigen Maps zu generieren. Sie können die Vorgabe als PDF-Standardvorgabe auswählen, um die PDF-Ausgabe zu generieren. Sie können auch **Bearbeiten**, **Umbenennen**, **Duplizieren** oder **Löschen** eine vorhandene Ausgabevorgabe aus der **Optionen** Menü.

>[!NOTE]
>
>Nur Benutzer mit Administratorrechten auf Ordnerebene können Vorgaben für Global- und Ordnerprofile erstellen.

### Suchen und Ersetzen von Text auf Zuordnungsebene

Sie können jetzt nach Dateien in einer Zuordnung suchen, die bestimmten Text enthalten. Der gesuchte Text wird in den Dateien hervorgehoben. Sie können das gesuchte Wort oder die gesuchte Wortgruppe auch durch ein anderes Wort oder eine andere Wortgruppe in den Dateien ersetzen. Wählen Sie die **Einmaliges Auftreten ersetzen** -Symbol, um das aktuelle Vorkommen und das **Alle in Datei ersetzen** -Symbol, um alle Vorkommen in der ausgewählten Datei zu ersetzen. Sie können **Alle ersetzen** -Symbol, um alle Vorkommen des gesuchten Begriffs in allen Dateien zu ersetzen.

<img src="assets/map-find-replace.png" alt="map find replace" width="600">


Standardmäßig werden die Optionen **Checkout-Datei vor Ersetzen** und **Neue Version erstellen nach Ersetzen** ausgewählt sind, sodass eine Datei ausgecheckt wird, bevor Sie den Text ersetzen, und eine neue Version erstellt wird, nachdem der Text ersetzt wurde. Sie können die Zeichenfolge auch in den indirekten Verweisen in der DITA-Zuordnung durchsuchen. Standardmäßig ist dies deaktiviert, sodass die Suche nur für direkte Verweise durchgeführt wird.

### Layout-Ansicht im Map Editor


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

### Bereich &quot;Schnellgenerierung&quot;

Jetzt stellt AEM Guides das Bedienfeld Schnellgenerierung bereit, mit dem Sie schnell die Ausgabe für Vorgaben generieren und anzeigen können, die für Ihre DITA-Zuordnung erstellt wurden.

<img src="assets/quick-generate-map-view.png" alt=" Schnellgenerierbereich" width="600">

Im **Schnellgenerierung** angezeigt, können Sie die Liste aller für Ihre DITA-Zuordnung erstellten Ausgabevorgaben sehen. Sie können auch die für die Vorgaben generierte Ausgabe schnell anzeigen. Nach der Generierung der Ausgabe wird eine Erfolgs- oder Fehlermeldung angezeigt. Sie können auch das Fehlerprotokoll anzeigen, das Details des im Generierungsprozess aufgetretenen Fehlers enthält.

### Dynamische Grundlinie basierend auf Bezeichnungen erstellen

Jetzt bietet Ihnen AEM Guides die Möglichkeit, dynamische Grundlinien basierend auf Bezeichnungen zu erstellen. Wenn Sie eine Grundlinie erstellen, eine Grundlinie herunterladen oder ein Übersetzungsprojekt mit einer Grundlinie erstellen, werden die Dateien dynamisch anhand der aktualisierten Beschriftungen ausgewählt. Diese Funktion ist praktisch, da Sie die Grundlinie bei der Aktualisierung der Beschriftungen nicht ändern müssen.

<img src="assets/dynamic-baseline.png" alt=" dynamische Grundlinie" width="400">

### Löschen und Duplizieren von Dateien aus dem Repository-Bereich

Jetzt können Sie Dateien (einzelne Datei pro Datei) einfach aus der **Optionen** Menü der ausgewählten Datei aus dem Repository-Bereich. Vor dem Löschen der Datei wird eine Bestätigungsaufforderung angezeigt. Wenn keine andere Datei auf die Datei verweist, wird sie gelöscht und es wird eine Erfolgsmeldung angezeigt.

<img src="assets/options-menu-repo-view-file-level.png" alt="Menü für Dateioptionen " width="500">

Sie können auch ein Duplikat oder eine Kopie der ausgewählten Datei erstellen. Standardmäßig wird die Datei mit einem Suffix erstellt (z. B. filename_1.extension).


### Weitere Verbesserungen am Webeditor

* In AEM Handbüchern können Sie über das Kontextmenü einige gängige Vorgänge für Bilder und Mediendateien ausführen. Jetzt können Sie auch das ausgewählte Bild oder Medium im Repository suchen oder die Vorschau der Datei in der Assets-Benutzeroberfläche anzeigen.

* Der Name des aktuellen Ordnerprofils wird als Beschriftung für das Symbol Benutzereinstellungen in der Hauptsymbolleiste angezeigt. Auf diese Weise können Sie das Ordnerprofil identifizieren, an dem Sie gerade arbeiten.

* Wenn Sie eine Karte in der Kartenansicht öffnen, wird der Titel der aktuellen Karte in der Mitte der Hauptsymbolleiste angezeigt. Dies ist hilfreich, um den Benutzern mitzuteilen, welche Karte derzeit geöffnet ist.

### Ausgewählte Dateiversionen bereinigen

Beim Erstellen und Verwalten Ihres Inhalts werden möglicherweise viele Versionen für Ihre DITA-Dateien in Ihrem Repository erstellt. Mit AEM Guides können Sie ältere Versionen Ihrer DITA-Dateien aus dem Repository löschen und Speicherplatz freigeben.

<img src="assets/preview-purge-report.png" alt="Bereinigungsbericht in der Vorschau" width="500">

AEM Guides löschen nicht die erste Version der Datei oder eine Version, die in einer Grundlinie enthalten ist oder auf die eine Beschriftung angewendet wird. Der Bereinigungsvorgang löscht nicht einmal Dateien, die in einer Übersetzung oder einem Prüfungs-Workflow enthalten sind. Sie können die Anzahl der beizubehaltenden Versionen auswählen und auch die Dateien löschen, die älter als die definierte Anzahl von Tagen sind.

Bevor Sie mit dem Bereinigungsvorgang beginnen, können Sie eine Vorschau des Berichts anzeigen, um die Versionen anzuzeigen, die bereinigt werden sollen. Anschließend können Sie den Bereinigungsvorgang starten oder abbrechen.

<img src="assets/download-purge-report.png" alt="PDownload-Bereinigungsbericht" width="500">

Nach Abschluss des Bereinigungsvorgangs können Sie den Bereinigungsbericht prüfen, um die bereinigten Dateien anzuzeigen.

### Anzeigen des Titels anstelle der UUID im Sauerstoffeditor

Jetzt können Sie AEM Guides auswählen **Verwenden von Titel in Editor und Maps Manager** in den Einstellungen. Wenn Sie diese Option auswählen, wird der Titel der Datei auf der Registerkarte der Datei angezeigt, wenn er im Editor oder im DITA Maps Manager geöffnet wird. Wenn Sie diese Option nicht auswählen, wird die UUID der Datei auf der Registerkarte der Datei angezeigt.

### Für PDF-Vorgaben verfügbare Metadaten-Benutzeroberfläche

Sie können die Metadaten aus der Ausgabevorgabe einer DITA-Zuordnung festlegen. Sie können die Metadaten Titel, Autor, Betreff und Suchbegriffe festlegen. Diese Metadaten werden den Metadaten in den Dateieigenschaften Ihrer Ausgabe-PDF zugeordnet. Diese Metadaten setzen die auf Buchebene definierten Metadaten außer Kraft. Sie können die Metadaten in jeder Ausgabevorgabe spezifisch definieren und an die Ausgabe-PDF übergeben.

### Native PDF | PDF mit Änderungsleiste, die den Unterschied zwischen Dokumentversionen anzeigt

Jetzt können Sie eine PDF erstellen, die die Inhaltsunterschiede zwischen zwei Versionen mithilfe der Änderungsleiste anzeigt. Sie können die aktuelle Version mit einer Grundlinie der vorherigen Version vergleichen oder zwischen den beiden ausgewählten Grundversionen vergleichen.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Auf der PDF wird eine Änderungsleiste angezeigt, die den geänderten, eingefügten oder gelöschten Inhalt angibt. Sie haben auch die folgenden Optionen:
* Eingefügten Inhalt in grüner Farbe anzeigen und unterstrichen
* Gelöschte Inhalte in roter Farbe anzeigen und mit einem Durchstreichen markieren

### Native PDF | Variablenunterstützung für Output Path und PDF File Name

Jetzt können Sie auch die folgenden vordefinierten Variablen verwenden, um den Ausgabepfad und die PDF-Datei zu definieren. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um die folgenden Optionen zu definieren:
* ${map_filename}
* ${map_title}
* ${preset_name}
* ${language_code}
* ${map_parentpath} (Nur für Ausgabepfad)
* ${path_after_langfolder} (nur für Ausgabepfad)

### Native PDF | Inhaltsverzeichnis für DITA-Maps generieren und Seitenlayouts neu anordnen

Jetzt können Sie das Inhaltsverzeichnis auch in DITA-Maps generieren, indem Sie eine erweiterte PDF-Einstellung der Vorlage verwenden. Sie können die Anzeige der verschiedenen Seitenlayouts aktivieren oder deaktivieren und ihre Position neu anordnen.

### Native PDF | Hinzufügen eines benutzerdefinierten Lesezeichens in der PDF-Ausgabe

Jetzt können Sie ein benutzerdefiniertes Lesezeichen zu einem bestimmten Inhalt in Ihrer endgültigen PDF-Ausgabe hinzufügen, um die Navigation zu erleichtern. Dies würde zum TOC hinzugefügt, das aus den Themen- oder Abschnittstiteln in Ihrer DITA-Map erstellt wird.

### Native PDF | Anwenden eines benutzerdefinierten Stils auf Inhaltsverzeichniseinträge und Themeninhalte

AEM Guides bieten die Möglichkeit, benutzerdefinierte Stile auf die TOC-Einträge oder ein bestimmtes Thema in der PDF-Ausgabe anzuwenden. Sie können beispielsweise die Textfarbe im Inhaltsverzeichnis und den Titel des Themas ändern. Sie können auch Stile auf den gesamten Inhalt innerhalb des Themas anwenden.




## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring –

* Beim Hinzufügen einer Registerkarte wird der linke Bereich umgebrochen. (11126)
* Änderungen im HTML-Code des Web Editors verursachen Probleme mit `<dl>` und `<dlentry>`. (11024)
* Einige Attribute werden nicht als bedingt behandelt und verursachen Probleme. (10895)
* Drei Ebenen oder mehr verschachtelt `<indexterm>` sind beim nativen PDF-Export nicht verschachtelt. (10799)
* Der Inhalt verschwindet beim Wechsel von der Autoren- zur Quellansicht im Hauptteil einer Aufgabe. (10735)
* Überprüfungskommentare werden in einer Prüfungsaufgabe nicht platziert. (10625)
* `<conref>` Hinweis innerhalb eines para-Tags wird nicht im Vorschaumodus angezeigt. (10559)
* Wenn Sie die Rücktaste am Ende eines Listenelements drücken, wird die gesamte Liste entfernt. (10540)
* Der Bildschirm wird in Chrome v106 beim Ziehen und Ablegen eines Elements aus der Benutzeroberfläche (z. B. aus dem Bedienfeld &quot;Bedingungen&quot;) als leer angezeigt. (10524)
* Die Schaltfläche &quot;Automatischer Einzug&quot;fehlt in der Symbolleiste in **Quelle** anzeigen. (10448)
* Das erste Zeichen eines Listenelements geht manchmal verloren, wenn die Liste im Editor erstellt wird.( 10447)
* **Rückgängig** oder **Wiederholen** funktioniert bei einigen Dateien nicht richtig. (10373)
* Benutzerdefinierte Metadaten werden beim Kopieren und Einfügen nicht beibehalten. (10367)
* Beim Kopieren (Strg+C) und Einfügen (Strg+V) des Inhalts tritt ein Fehler auf. (10304)
* Im Bedienfeld &quot;Kontur&quot;werden keine Inhalte angezeigt, wenn von der Autoreninstanz in den Quellmodus gewechselt wird. (10296)
* Submap wird nicht erstellt, wenn sie auf eine Hauptkarte in DITA-Vorlagen verweist. (10231)
* Navigationsprobleme treten im Web Editor nach der Aktualisierung auf Version 4.0 auf. (10159)
* Die Option &quot;Rückgängig&quot;im XML-Editor bringt den Benutzer zum Anfang der Seite. (10091)
* Knoteneigenschaften werden nach dem Kopieren und Einfügen eines Assets entfernt. (10053)
* SVG-Dateien, die zu DITA-Themen hinzugefügt wurden, werden im Vorschaumodus des Editors nicht angezeigt. (10010)
* Suchergebnisse für Suchen und Ersetzen im Web Editor sind im Dunkelmodus nicht lesbar. (9978)
* Beim Erstellen einer Zuordnung aus der Zuordnungsvorlage existiert kein Ladeprogramm. (9891)
* Conref in der Themenvorlage funktioniert nicht und die kopierte Hash-ID wird in der Inhaltskopie nicht aktualisiert. (9890)
* Es wird keine Option zum Durchsuchen der Themen oder Zuordnungsvorlagen in den Unterordnern des Themen- oder Zuordnungsordners angezeigt. (9889)
* Keine Option zum Erstellen einer neuen Vorlage in den Unterordnern von Themen oder Maps. (9888)
* Der XML-Editor aktualisiert die Bilder nicht zu Themen. (9500)
* mimeType ist für die Erstellung und Aktualisierung von DITA-Assets hartcodiert. (8979)
* Ein normaler Bindestrich wird bei der Auswahl von geschützten Bindestrichen im **Sonderzeichen einfügen** angezeigt. (8919)
* Der Name des Erstellers der Version im Versionsverlauf ist &quot;fmdita-service-user&quot;für die Dateien, die über die Assets-Benutzeroberfläche hochgeladen wurden. (8910)
* Die Option &quot;Bearbeiten&quot;funktioniert nicht für Bilder, während Sie in der Spaltenansicht der Assets-Benutzeroberfläche arbeiten. (8758)
* DITA-Thema wird nicht automatisch mit Änderungen aktualisiert, die am **Eigenschaften** Seite. (8745)
* Beim Verschieben von Elementen innerhalb des Themas im Web Editor werden die zugewiesenen IDs für Elemente durch automatisch zugewiesene IDs überschrieben. (7895)

### Verwaltung

* Das Kopieren eines DITA-Map-Assets (aus der Asset-Benutzeroberfläche ) verursacht fehlerhafte Grundlinien im kopierten Asset. (11218)
* Beim Hochladen einer Datei, die die in AEM zulässige Größe überschreitet, wird keine Warnmeldung angezeigt (standardmäßig 2 GB). (10817)
* Web Editor-Grundlinie | Das Verhalten der Spalte &quot;Neueste&quot;unterscheidet sich im neuen Dashboard für die Grundlinie im Web Editor. (10808)
* Übersetzung | Der Übersetzungsauftrag wird aufgrund von ungültigen /libs/fmdita/i18n/ja.json nicht gestartet. (10543)
* Übersetzung | In einem Scoping-Übersetzungsprojekt, das über das Übersetzungs-Dashboard (Menschliche Übersetzung) erstellt wurde, tritt ein Fehler auf. (10526)
* Übersetzung | Die Nachbearbeitung wird für den gesamten Sprachordner blockiert, dessen Assets in einem aktiven Übersetzungsprojekt vorhanden sind. (10332)
* Übersetzung | Metadaten und Tags werden nicht an die übersetzten Kopien weitergegeben. (4696)
* Für jedes Asset werden mehrere Popups angezeigt, wenn die Version geändert und im Baseline-Editor gespeichert wird. (10399)
* SitzungsLeak tritt unter com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210) auf. (10279)
* Die Videodatei fehlt in der Grundlinie, wenn der übergeordnete Ordner Leerzeichen im Namen enthält. (10031)

### Veröffentlichung

* Die Themenregenerierung funktioniert in einigen Szenarien nicht. (10635)
* PDF-Publishing schlägt beim Generieren der Ausgabe für eine Vorgabe (einer vorhandenen Vorgabe) fehl. (10584)
* Die Schaltfläche Protokoll anzeigen funktioniert nicht, falls die PDF-Erstellung für eine Vorgabe fehlschlägt. (10576)
* Der Herausgeber zeigt die angeforderten Daten nicht in den Infoprotokollen an und enthält auch einige Junk-Protokolle.( 10567)
* Native PDF | PDF-Generierung schlägt mit einer Nullzeiger-Ausnahme fehl. (10950)
* Native PDF | conkeyref wird in der generierten Ausgabe nicht aufgelöst. (10564)
* Native PDF | Probleme treten mit den Metadaten einer Zuordnung auf, auf die in der PDF-Ausgabe verwiesen werden muss.( 10556)
* Native PDF | Beim Drehen der Tabellenüberschrift treten Probleme auf. (10555)
* Native PDF | Beim Entfernen von Themen mit Verarbeitungsrolle=&#39;resource-only&#39; treten Probleme auf. (10554)
* Native PDF | Leere Keyrefs werden in der PDF-Ausgabe angezeigt. (10553)
* Native PDF | Verschachtelt `<indexterm>` sind beim nativen PDF-Export nicht verschachtelt. (10521)
* Native PDF | Native PDF verwendet für die generierten Tags den Inline-Stil anstelle des Klassennamens. (10498)
* Native PDF | Verschachtelte topicref in Anhängen werden alle in der temporären HTML in h1 umgewandelt.( 10454)
* Native PDF | Frontmatter-Themen können nicht aus dem Inhaltsverzeichnis ausgeblendet werden. (10355)
* Native PDF | Tabellenframe-Attribut wird nicht auf die temporäre HTML übertragen (als Klasse). (10353)
* Native PDF | Temporäre HTML-Dateien fügen die Klassen colsep und rowsep zu <td> und <th> auch wenn ihr Wert 0 in der Quell-DITA beträgt. (10352)
* Native PDF | Beim Neustarten von Seitennummern im Kapitel-Layout wird die Nummerierung nach dem Zufallsprinzip am Ende des vorherigen Kapitels begonnen. (10154)
* Native PDF | Schlüsselreferenzen für Keydefs mit Bild- oder externen Links werden nicht aufgelöst. (10063)
* Native PDF | Anlage wird als Kapitel in der generierten PDF angezeigt. (9829)
* Die Registerkarte &quot;Vorlage&quot;im XML-Editor wird den Ordnerprofil-Administratoren nicht angezeigt. (10266)
* Die Grundlinienveröffentlichung schlägt bei PDF fehl, die mit FrameMaker Publishing Server 2020 erstellt wurden. (10551)
* Anwendungsfehler tritt beim Klicken auf die Schaltfläche &quot;Bearbeiten&quot;auf, nachdem im Popup &quot;Quick Generate&quot;das Kontrollkästchen Alle Vorgaben über Ausgabevorgaben ausgewählt wurden. (10388)
* Wenn die Registerkarte &quot;Ausgabe&quot;im Web Editor über mehr Vorgaben verfügt, ist der Bereich &quot;Vorgaben&quot;nicht vertikal durchlaufbar und zeigt nicht alle verfügbaren Vorgaben an. (9787)
* Vorgaben können beim Veröffentlichen über den Editor nicht aus dem Output-Workflow gelöscht werden. (9100)
* Peer-Link wird als normaler Text statt als Link auf der generierten Seite gerendert. (7774)

### Bekanntes Problem

Adobe hat das folgende bekannte Problem für AEM Guides 4.2-Version identifiziert:

* Benutzer können Überprüfungsvorgänge auch nach Abschluss der Prüfungsaufgabe durchführen.
