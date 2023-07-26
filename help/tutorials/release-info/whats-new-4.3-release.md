---
title: Versionshinweise | Neue Funktionen in Version 4.3.0 der Adobe Experience Manager-Handbücher
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in Version 4.3.0 der Adobe Experience Manager-Handbücher.
source-git-commit: ec67a3b959f9ee5b90a53134c1fe9aff8760cb6f
workflow-type: tm+mt
source-wordcount: '2638'
ht-degree: 0%

---

# Neue Funktionen in Version 4.3.0 der Adobe Experience Manager-Handbücher (Juli 2023)

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version 4.3.0 der Adobe Experience Manager-Handbücher (später auch als *AEM*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter  [Versionshinweise](./release-notes-4.3.md).


## Herstellen einer Verbindung zu einer Datenquelle und Einfügen von Daten in Ihre Themen

Jetzt können Sie über vordefinierte Connectoren aus AEM Handbüchern schnell eine Verbindung zu Ihren Datenquellen herstellen. Durch die Verbindung mit einer Datenquelle können Sie Ihre Informationen mit der Quelle synchronisieren, und alle Aktualisierungen der Daten werden automatisch übernommen, was AEM Guides zu einem echten Content-Hub macht. Mit dieser Funktion sparen Sie Zeit und Mühe beim manuellen Hinzufügen oder Kopieren der Daten.

Mit AEM Guides kann Ihr Administrator die nativen Connectoren für JIRA- und SQL-Datenbanken (MySQL, PostgreSQL, SQL Server, SQLite) konfigurieren. Sie können auch andere Connectoren hinzufügen, indem sie die Standardschnittstellen erweitern.
Nach dem Hinzufügen können Sie die konfigurierten Connectoren anzeigen, die im Web Editor im Bereich Data Sources aufgeführt sind.

<img src="assets/data-sources.png" alt="Liste der Datenquellen im Bereich" width="300">

Erstellen Sie ein Inhaltsfragment, um die Daten aus einer verbundenen Datenquelle abzurufen. Anschließend können Sie die Daten in Ihre Themen einfügen und sie bearbeiten. Nachdem Sie einen Inhaltsfragment-Generator erstellt haben, können Sie ihn wiederverwenden, um die Daten in ein beliebiges Thema einzufügen.

Jetzt können Sie auch ein Thema aus einer verbundenen Datenquelle erstellen. Ein Thema kann Daten in verschiedenen Formaten wie Tabellen, Listen und Absätzen enthalten. Außerdem können Sie eine DITA-Zuordnung für alle Themen erstellen. Beim Abrufen aus einer Datenquelle können Sie dem Thema Metadaten zuordnen.

Weitere Informationen finden Sie unter [Daten aus Ihrer Datenquelle verwenden](../user-guide/web-editor-content-snippet.md).

## Hinzufügen von Zitaten zu Ihrem Inhalt

Zitate sind Verweise auf die Informationsquelle, die zu Ihrem Inhalt hinzugefügt wird. Zitate helfen Ihnen dabei, Glaubwürdigkeit zu schaffen und Plagiatismus zu verhindern. Zitate helfen den Lesern, die Quelle zu finden und die im Text dargestellten Informationen zu überprüfen.

In AEM Handbüchern können Sie Zitate hinzufügen oder Zitate importieren und auf Ihren Inhalt anwenden. Sie können diese Zitate aus jeder Quelle von Büchern, Websites und Zeitschriften hinzufügen.

Nachdem Sie Ihre Zitate in Ihre Themen eingefügt haben, können Sie sie im Web-Editor in der Vorschau anzeigen. Sie können auch Inhalte mit Zitaten mithilfe des nativen PDF veröffentlichen.

![In einem Bedienfeld aufgelistete Zitate](assets/citation-panel.png){width="300" align="left"}


Weitere Informationen finden Sie unter [Hinzufügen und Verwalten von Zitaten in Ihrem Inhalt](../user-guide/web-editor-apply-citations.md).

## In einem Inhaltsfragment veröffentlichen

Inhaltsfragmente sind separate Inhaltsfragmente in AEM. Sie sind strukturierte Inhalte, die auf einem Inhaltsmodell basieren. Inhaltsfragmente sind reine Inhalte ohne Design- oder Layoutinformationen. Sie können unabhängig von den von AEM unterstützten Kanälen erstellt und verwaltet werden. Die Modularität und Wiederverwendbarkeit der Inhaltsfragmente führt zu mehr Flexibilität, Konsistenz, Effizienz und einfacherer Verwaltung.

Jetzt bietet AEM Guides eine Möglichkeit, ein Thema oder die Elemente innerhalb eines Themas in einem Inhaltsfragment zu veröffentlichen. Sie können eine JSON-basierte Zuordnung zwischen einem Thema und einem Inhaltsfragmentmodell erstellen. Verwenden Sie diese Zuordnung, um Inhalte in einigen oder allen Elementen innerhalb eines Themas für ein Inhaltsfragment zu veröffentlichen.

Nutzen Sie AEM Handbücher und Inhaltsfragmente optimal und verwenden Sie Inhaltsfragmente auf jeder AEM Site. Sie können die Details auch über APIs extrahieren, die von Inhaltsfragmenten unterstützt werden.

![Option zum Veröffentlichen von Inhaltsfragmenten](assets/content-fragment-publish.png){width="550" align="left"}


## Verbesserungen überprüfen

AEM Handbücher bieten jetzt eine verbesserte Überprüfungsfunktion mit den folgenden Funktionen:

### Überprüfungsfenster zur Präsentation von Überprüfungsprojekten und der aktiven Prüfungsaufgaben

Jetzt AEM Guides machen Ihre Rezensionen nahtloser. Es stellt den Bereich &quot;Bewertungen&quot;im Web Editor bereit. Im Bedienfeld &quot;Überprüfungen&quot;werden alle Überprüfungsprojekte und die aktiven Prüfungsaufgaben innerhalb der Überprüfungsprojekte angezeigt, zu denen Sie gehören.

Als Autor können Sie mit dieser Funktion die Prüfungsaufgaben einfach öffnen, die Kommentare anzeigen und die Kommentare schnell in einer zentralen Ansicht bearbeiten.
![](assets/active-review-task-comments.png){width="800" align="left"}
Weitere Informationen finden Sie unter **Überprüfen** Funktionsbeschreibung innerhalb der [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

### Suchüberprüfungsthemen

Die Durchführung von Überprüfungen ist ein wichtiges Merkmal AEM Leitfadens. Es hilft den Validierungsverantwortlichen, die ihnen zugewiesenen Dokumente zu überprüfen.
Jetzt können Sie nach einem Thema suchen, indem Sie einen Teil des Textes des Titels oder Dateipfads in die Suchleiste der Themenansicht des Prüfungsbereichs eingeben. Sie können auch alle Themen anzeigen oder Themen mit Kommentaren anzeigen. Standardmäßig können Sie alle in der Prüfungsaufgabe vorhandenen Themen anzeigen.


![Suchen im Bereich &quot;Prüfungsthemen&quot;](assets/review-search-topic.png){width="800" align="left"}

Weitere Informationen finden Sie unter [Prüfungsthemen](../user-guide/review-topics.md).

## Guides Extension Framework

Erstellen Sie benutzerdefinierte Pakete zusätzlich zu AEM Handbüchern, um die Erweiterbarkeit mit AEM Guides Extension Framework bereitzustellen. Diese Pakete sind für Entwickler und Berater nützlich und bieten ihnen Erweiterbarkeit für die Komponenten im Editor. Sie können Schaltflächen, Dialogfelder und Dropdown-Menüs auswählen und benutzerdefiniertes JavaScript hinzufügen, das einfach mit AEM Guides-Benutzeroberfläche interagieren kann.



## Native PDF-Verbesserungen

Die folgenden nativen PDF-Verbesserungen wurden in Version 4.3.0 vorgenommen, um AEM Guides zu einem robusteren Produkt zu machen:

### Unterstützung für Sprachvariablen

AEM Guides unterstützen Sprachvariablen. Sie können Sprachvariablen verwenden, um eine lokalisierte Version der vordefinierten Beschriftungen wie Hinweis, Vorsicht und Warnung oder statischen Text in der PDF-Ausgabe zu definieren.
Sie können die Sprachvariablen oder die lokalisierte Version der Titel den entsprechenden Abschnitten in Ihrer PDF-Ausgabe und in den Ausgabevorlagen hinzufügen.

#### Sprachvariablen in der PDF-Ausgabe

Sie können die Sprachvariablen verwenden, um lokalisierte Beschriftungen für Elemente wie Hinweis, Vorsicht und Warnung zu definieren. Sie können den Wert für diese Variablen in einer oder mehreren Sprachen aktualisieren und dann wird der lokalisierte Wert automatisch in der PDF-Ausgabe ausgewählt.
Beispielsweise können Sie die Beschriftung Notiz in Ihrer PDF-Ausgabe wie folgt darstellen:

* Englisch: Hinweis
* Französisch: Remarque
* Deutsch: Verweis

#### Sprachvariablen in den Ausgabevorlagen

Wenn Sie die PDF-Ausgabe in verschiedenen Sprachen erstellen wollten, mussten Sie für jede Sprache verschiedene PDF-Vorlagen mit lokalisiertem Text erstellen. Mit der Sprachvariablen-Funktion müssen Sie die Vorlage nur einmal erstellen. Anschließend können Sie für jeden statischen Text, den Sie lokalisieren müssen, entsprechende Sprachvariablen erstellen und in Ihrer Vorlage verwenden.
Sie können Sprachvariablen für längeren Text erstellen, z. B. einen ganzen Satz oder sogar einen Absatz. Sie können auch Stile anwenden und HTML Markup verwenden, um diese Sprachvariablen zu formatieren.

Weitere Informationen finden Sie unter [Unterstützung für Sprachvariablen](../native-pdf/native-pdf-language-variables.md).

### Wasserzeichen zur PDF-Ausgabe für Entwürfe hinzufügen

Jetzt können Sie ein Wasserzeichen zur PDF-Ausgabe des Dokuments hinzufügen, das noch nicht genehmigt wurde. Dieses Wasserzeichen wird nicht angezeigt, wenn Sie die PDF für das Dokument im Dokumentstatus &quot;Genehmigt&quot;generieren. Sie können beispielsweise einen Wasserzeichenentwurf für Ihre PDF-Ausgabe hinzufügen.

Weitere Informationen finden Sie unter [Hinzufügen eines Wasserzeichens zur PDF-Ausgabe für Entwurfsdokumente](../native-pdf/use-javascript-content-style.md#watermark-draft-document).

### Möglichkeit zur Verwendung AEM Metadaten in PDF-Layouts

Metadaten sind die Beschreibung oder Definition Ihres Inhalts. Diese Metadaten werden in Ihrem Quell-DITA-Map-Inhalt gespeichert.

Jetzt können Sie in AEM Handbüchern auch die Metadateneigenschaften Ihrer Assets auswählen und sie zum Seitenlayout hinzufügen. Anschließend wählt AEM Guides diese Metadateneigenschaften Ihrer Assets aus und veröffentlicht sie in Ihrer PDF-Ausgabe.


![Metadaten für natives PDF hinzufügen](assets/native-pdf-metadata-asset.png){width="300" align="left"}

>[!NOTE]
>
> AEM Guides unterstützen auch die Metadateneigenschaften für Ihre DITA-Maps.

Weitere Informationen finden Sie unter [Felder und Metadaten hinzufügen](../native-pdf/design-page-layout.md#add-fields-metadata).


### Sortieren von Seiten in der PDF-Ausgabe

Sie können die folgenden Bereiche in Ihrer PDF ein- oder ausblenden und auch die Reihenfolge anordnen, in der sie in Ihrer endgültigen PDF-Ausgabe angezeigt werden sollen:

* IHV
* Kapitel und Themen
* Bildliste
* Tabellenliste
* Index
* Glossar
* Zitat
* Seitenlayouts

Wenn Sie in Ihrer PDF-Ausgabe keinen bestimmten Bereich anzeigen möchten, können Sie dies verbergen, indem Sie den Umschalter ausschalten.

Weitere Informationen finden Sie unter [Seitenreihenfolge](../native-pdf/components-pdf-template.md#page-order).

### Seiten zusammenführen

In einer nativen PDF-Ausgabe beginnen standardmäßig alle Bereiche auf einer neuen Seite. Jetzt können Sie einen Abschnitt mit der vorherigen Seite oder der nächsten Seite zusammenführen. Dadurch wird der -Abschnitt in Weiterführung mit der ausgewählten PDF-Ausgabe veröffentlicht und es gibt keinen Seitenumbruch dazwischen.

Weitere Informationen finden Sie in der Funktionsbeschreibung der Zusammenführungsseiten unter [Seitenreihenfolge](../native-pdf/components-pdf-template.md#page-order) Abschnitt.

### Statische Seiten

Sie können auch benutzerdefinierte Seitenlayouts erstellen und diese als statische PDF-Seiten veröffentlichen. Auf diese Weise können Sie statischen Inhalt wie Notizen oder leere Seiten hinzufügen.

Weitere Informationen finden Sie in der Funktionsbeschreibung für statische Seiten unter [Seitenreihenfolge](../native-pdf/components-pdf-template.md#page-order) Abschnitt.


### Variablen in Querverweisen

Sie können Variablen verwenden, um einen Querverweis zu definieren. Wenn Sie eine Variable verwenden, wird ihr Wert aus den Eigenschaften ausgewählt.

Jetzt können Sie auch {figure} und {table}.
Verwendung {figure}um einen Querverweis zur Zahl hinzuzufügen. Sie wählt die Zahl aus den automatischen Nummernstilen aus, die Sie für die Beschriftung definiert haben.

Verwendung {table} , um der Tabellennummer einen Querverweis hinzuzufügen. Die Tabellennummer wird aus den automatischen Nummernstilen ausgewählt, die Sie für die Beschriftung definiert haben.

Weitere Informationen finden Sie unter [Querverweise](../native-pdf/components-pdf-template.md##cross-references).

### Jedes Kapitel von der aktuellen Seite aus starten

Sie können die grundlegenden Konfigurationseinstellungen für den Start eines Kapitels von einer ungeraden oder geraden Seite, die TOC-Struktur und das Füllzeichenzeilenformat für die TOC-Einträge festlegen.

Jetzt können Sie auch ein Kapitel von der aktuellen Seite aus starten. Wenn Sie sich dafür entscheiden, werden alle Kapitel als Fortsetzung und ohne Seitenumbrüche veröffentlicht. Wenn ein Kapitel beispielsweise mitten auf Seite 15 endet, beginnt das nächste Kapitel auch auf der 15. Seite selbst.


### Möglichkeit zum Zugriff auf temporäre HTML-Dateien beim Generieren der nativen PDF-Ausgabe

Jetzt können Sie AEM Guides die temporären HTML-Dateien herunterladen, die beim Generieren der nativen PDF-Ausgabe erstellt wurden. Wählen Sie in den Ausgabevorgabeneinstellungen die Option zum Herunterladen der temporären Dateien aus.  In AEM Guides können Sie die temporären Dateien herunterladen, die beim Generieren der Ausgabe mithilfe dieser Vorgabe erstellt wurden.

Diese Funktion ermöglicht bessere Einblicke in den Generierungsprozess mit Zugriff auf Zwischenstile und Layouts und hilft Ihnen, Ihre CSS-Stile gemäß Ihren Anforderungen zu korrigieren oder zu ändern.

![das Dialogfeld mit den erweiterten Einstellungen im nativen PDF-Format](assets/native-pdf-advanced-settings.png){width="800" align="left"}

Weitere Informationen finden Sie unter [Erstellen einer PDF-Ausgabevorgabe](../web-editor/native-pdf-web-editor.md#create-output-preset).


### Neugestaltung des CSS-Editors

Jetzt wurde der CSS-Editor für ein besseres Benutzererlebnis mit Selektoren und Stileigenschaften neu gestaltet.

#### Verbesserung des Dialogfelds &quot;Stil hinzufügen&quot;

Sie können jetzt benutzerdefinierte Selektoren verwenden, um komplexe Stile hinzuzufügen. Mit dem neuen Selektor-Feld können Sie benutzerdefinierte Selektoren neben der Kombination aus Klasse, Tag und Pseudo-Klasse hinzufügen. Sie können beispielsweise `table a.link` -Stil für alle Hyperlinks in einer Tabelle.

![Hinzufügen von Stilen in nativen PDF-Vorlagen](assets/add-styles-native-pdf.png){width="300" align="left"}

#### Anpassen von Stileigenschaften

Jetzt werden Sie in AEM Handbüchern in ein neues Eigenschaftenbedienfeld unter dem Vorschauabschnitt für Stile vorgestellt. Sie können die Eigenschaften der Stile effizienter und schneller im Eigenschaftenbereich bearbeiten.


## Umbenennen und Verschieben von Dateien in der Repository-Ansicht

Jetzt können Sie eine Datei auch umbenennen oder aus dem Repository-Bereich verschieben. Diese Funktion ist praktisch und erleichtert die Verwaltung Ihrer Dateien über das Repository-Bedienfeld. Sie können eine Datei auswählen und sie umbenennen oder verschieben mithilfe der **Optionen** für die ausgewählte Datei. AEM Handbücher zeigt eine Erfolgsmeldung an, wenn Sie eine Datei verschieben oder umbenennen.

![Optionen-Menü einer Datei](assets/rename-move-assets.png){width="550" align="left"}

Weitere Informationen zum Menü Optionen einer Datei finden Sie unter **Repository-Ansicht** Funktionsbeschreibung in [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

## Bericht zu fehlerhaften Links im Web-Editor

Mit AEM Guides können Sie die Gesamtvollständigkeit Ihrer technischen Dokumente überprüfen und Berichte aus dem Web-Editor erstellen. Ab der Version Juni 2023 bieten Ihnen AEM Handbücher die Möglichkeit, fehlerhafte Links anzuzeigen und zu reparieren. Dies ist ein nützlicher Bericht, der Ihnen bei der Verwaltung Ihrer fehlerhaften Links hilft. Sie können die fehlerhaften Links in Ihrer DITA-Zuordnung einfach anzeigen und sie auch beheben.
![defekter Link-Bericht](assets/broken-link-report.png){width="800" align="left"}

Wenn Sie einen Link korrigieren, wird er nicht unter der Liste der fehlerhaften Links angezeigt.

Weitere Informationen finden Sie unter [Fehlerbehebung bei fehlerhaften Links](../user-guide/reports-web-editor.md#report-broken-links).

## Verbesserungen bei Schemata

### Verwenden Sie Berichtanweisungen zur Überprüfung auf Regeln in Schema

AEM Guides unterstützen jetzt auch die Berichtanweisungen mit dem Schema. Eine Berichtanweisung generiert eine Meldung, wenn eine Testanweisung als &quot;true&quot;ausgewertet wird. Wenn Sie beispielsweise eine Kurzbeschreibung von 150 Zeichen oder weniger wünschen, können Sie eine Berichtanweisung definieren, um die Themen zu überprüfen, bei denen die Kurzbeschreibung mehr als 150 Zeichen umfasst.

Weitere Informationen finden Sie unter [Verwenden Sie Assets und Berichtanweisungen, um nach Regeln zu suchen.](../user-guide/support-schematron-file.md#schematron-assert-report).

### Verwenden von Regex-Ausdrücken

Sie können auch Regex-Ausdrücke verwenden, um eine Regel mit der Funktion matches() zu definieren und dann mithilfe der Schematron-Datei eine Validierung durchzuführen.

Weitere Informationen finden Sie unter [Verwenden von Regex-Ausdrücken](../user-guide/support-schematron-file.md#schematron-assert-report).


### Abstrakte Muster definieren

AEM Guides unterstützen auch abstrakte Muster in Schematron. Sie können allgemeine abstrakte Muster definieren und diese abstrakten Muster wiederverwenden. Abstrakte Muster können Ihr Schema vereinfachen und Ihnen auch bei der Verwaltung und Aktualisierung Ihrer Validierungslogik helfen.


Weitere Informationen finden Sie unter [Abstrakte Muster definieren](../user-guide/support-schematron-file.md#schematron-abstract-patterns).

## Unterstützung des XLIFF-Formats bei der Übersetzung

AEM Guides unterstützen auch das XLIFF-Format (XML Localization Interchange File Format) bei der Übersetzung. Jetzt können Sie auch **Erstellen eines neuen XLIFF-Übersetzungsprojekts** , um den XML-Inhalt in das XLIFF-Format zu konvertieren. AEM Guides unterstützen XLIFF-Version 1.2.

Mithilfe dieses Formats können Sie den Inhalt in das XLIFF-Format des Branchenstandards exportieren und dann den Übersetzungsanbietern dasselbe bereitstellen. Weitere Informationen finden Sie unter [Erstellen eines Übersetzungsprojekts](../user-guide/translate-documents-web-editor.md#create-translation-project).

![Arten von Übersetzungsprojekten](assets/translation-project-types.png){width="350" align="left"}


## Verbesserungen bei der Zuordnungssammlung

Mit einer Map Collection können Sie mehrere Maps organisieren und sie im Stapel veröffentlichen. An der Zuordnungssammlung wurden viele neue Verbesserungen vorgenommen:

* Jetzt können Sie einer Zuordnungssammlung native PDF-Ausgabevorgaben hinzufügen und diese zum Generieren der PDF-Ausgabe verwenden.
* Sie können die von Ihrem Administrator erstellten globalen und Ordnerprofilvorgaben anzeigen und sie zum Generieren der PDF-Ausgabe verwenden.
* Jetzt können Sie nicht nur eine einzelne Vorgabe auswählen, sondern auch alle Ordnerprofilvorgaben für eine DITA-Zuordnung in einem Schritt aktivieren.
  ![Bearbeiten einer Zuordnungssammlung](assets/edit-map-collection.png){width="800" align="left"}

Weitere Informationen finden Sie unter [Verwenden der Kartensammlung für die Ausgabegenerierung](../user-guide/generate-output-use-map-collection-output-generation.md).

## Native PDF-Unterstützung im Dashboard für die Massenveröffentlichung


Mit der Massenaktivierung von AEM Handbüchern können Sie Ihre Inhalte schnell und einfach von der Authoring- bis zur Publishing-Instanz aktivieren. Auf der Massen-Aktivierungskarte können Sie die native PDF-Ausgabevorgabe, die AEM-Site, PDF, HTML5, benutzerdefinierte und JSON-Ausgabe einbeziehen.
Weitere Informationen finden Sie unter [Massenaktivierung veröffentlichter Inhalte](../user-guide/conf-bulk-activation.md).

## Verbessertes Werkzeug zum Verschieben von Stapeln

Als Administrator können Sie jetzt das verbesserte Werkzeug zum Verschieben von Massen-Dateien verwenden, um Ordner mit vielen Dateien von einem Speicherort zum anderen zu verschieben.
Sie können das Dialogfeld Datei durchsuchen verwenden, um die Quellordner auszuwählen, die Sie verschieben möchten. Sie können auch nach dem Zielspeicherort suchen, um die Quellordner zu verschieben. Auswählen ![Infosymbol](assets/info-icon.svg) {width="25" align="left"} in der Nähe eines Felds, um weitere Informationen dazu anzuzeigen.

Weitere Informationen finden Sie unter [Stapelweises Verschieben von Dateien](../user-guide/authoring-file-management.md#move-files-bulk).

## Verbessertes Bedienfeld &quot;Favoriten&quot;

Mithilfe AEM Handbücher können Sie eine Sammlung oder Favoritenliste Ihrer Dateien und Ordner erstellen und diese einfach verwenden. Jetzt **Optionen** Menü ist auch verfügbar im **Favoriten** Bedienfeld. Sie können die ausgewählte Sammlung umbenennen oder aus der **Optionen** Menü. Sie können die **Aktualisieren** , um eine neue Liste von Dateien oder Ordnern aus dem Repository zu erhalten. Sie können den Ordnerinhalt auch in der Assets-Benutzeroberfläche anzeigen.

![das Favoriten-Bedienfeld](assets/favorites-options.png){width="650" align="left"}

>[!NOTE]
>
> Sie können die Liste auch mit dem **Aktualisieren** Symbol oben.

Weitere Informationen finden Sie unter **Optionen** Menü einer Favoriten-Sammlung, zeigen Sie die **Favoriten** Funktionsbeschreibung in [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

## Wechseln Sie zum Systemdesign

Sie können jetzt auch das Gerätedesign verwenden. Verwenden der **Benutzereinstellungen** können Sie AEM Guides so konfigurieren, dass je nach Thema Ihres Geräts automatisch zwischen hellen und dunklen Themen umgeschaltet wird.

![Benutzereinstellungen](assets/device-theme-user-preferences.png){width="550" align="left"}

Weitere Informationen finden Sie unter **Benutzereinstellungen** Funktionsbeschreibung in [Hauptleiste](../user-guide/web-editor-features.md#id2051EA0G05Z) Abschnitt.
