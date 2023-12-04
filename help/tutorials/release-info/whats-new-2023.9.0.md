---
title: Versionshinweise | Neue Funktionen in Adobe Experience Manager-Handbüchern, Version September 2023
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in der Version vom September 2023 von Adobe Experience Manager Guides as a Cloud Service
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 0%

---

# Neue Funktionen in der Version September 2023 von Adobe Experience Manager Guides as a Cloud Service

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version September 2023 der Adobe Experience Manager-Handbücher (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](release-notes-2023.9.0.md).

## Herstellen einer Verbindung zu einer Datenquelle und Einfügen der Themen

AEM Guides bieten vordefinierte Connectoren, mit denen Sie eine Verbindung zu Ihren Datenquellen herstellen können, sodass AEM Guides ein echter Content-Hub werden. Dies bietet Ihnen den Vorteil, dass Sie Zeit und Mühe sparen, die andernfalls für das manuelle Hinzufügen oder die Replikation von Daten ausgegeben würden.

Neben den bereits vorhandenen nativen Connectoren wie JIRA und SQL (MySQL, PostgreSQL, SQL Server, SQLite) kann Ihr Administrator auch Connectoren für die Datenbanken MariaDB, H2DB, AdobeCommerce und Elasticsearch konfigurieren. Sie können auch andere Connectoren hinzufügen, indem sie die Standardschnittstellen erweitern.

Sie können die konfigurierten Connectoren unter dem **Data Sources** im Web Editor angezeigt.

<img src="assets/data-sources.png" alt="Liste der Datenquellen im Bereich" width="300">

*Anzeigen der verbundenen Datenquellen.*

Sie können jetzt auch ein Thema aus einer verbundenen Datenquelle erstellen. Ein Thema kann Daten in verschiedenen Formaten wie Tabellen, Listen und Absätzen enthalten. Außerdem können Sie eine DITA-Zuordnung für alle Themen erstellen. Beim Abrufen aus einer Datenquelle können Sie dem Thema Metadaten zuordnen.

Weitere Informationen finden Sie unter [Daten aus Ihrer Datenquelle verwenden](../user-guide/web-editor-content-snippet.md).

## Hinzufügen von Zitaten zu Ihrem Inhalt

Zitate sind Verweise auf die Informationsquelle, die zu Ihrem Inhalt hinzugefügt wird. Zitate helfen Ihnen dabei, Glaubwürdigkeit zu schaffen und Plagiatismus zu verhindern. Zitate helfen den Lesern, die Quelle zu finden und die im Text dargestellten Informationen zu überprüfen.

In AEM Handbüchern können Sie Zitate hinzufügen oder Zitate importieren und auf Ihren Inhalt anwenden. Sie können diese Zitate aus jeder Quelle von Büchern, Websites und Zeitschriften hinzufügen.

Nachdem Sie Ihre Zitate in Ihre Themen eingefügt haben, können Sie sie im Web-Editor in der Vorschau anzeigen. Sie können auch Inhalte mit Zitaten mithilfe des nativen PDF veröffentlichen.

![In einem Bedienfeld aufgelistete Zitate](assets/citation-panel.png){width="300" align="left"}

*Zeigen Sie die Liste der Zitate im Bereich &quot;Zitate&quot;an.*

Weitere Informationen finden Sie unter [Hinzufügen und Verwalten von Zitaten in Ihrem Inhalt](../user-guide/web-editor-apply-citations.md).


## In einem Inhaltsfragment veröffentlichen

Inhaltsfragmente sind separate Inhaltsfragmente in AEM. Sie sind strukturierte Inhalte, die auf einem Inhaltsmodell basieren. Inhaltsfragmente sind reine Inhalte ohne Design- oder Layoutinformationen. Sie können unabhängig von den von AEM unterstützten Kanälen erstellt und verwaltet werden. Die Modularität und Wiederverwendbarkeit der Inhaltsfragmente führt zu mehr Flexibilität, Konsistenz, Effizienz und einfacherer Verwaltung.

Jetzt bietet AEM Guides eine Möglichkeit, ein Thema oder die Elemente innerhalb eines Themas in einem Inhaltsfragment zu veröffentlichen. Sie können eine JSON-basierte Zuordnung zwischen einem Thema und einem Inhaltsfragmentmodell erstellen. Verwenden Sie diese Zuordnung, um Inhalte in einigen oder allen Elementen innerhalb eines Themas für ein Inhaltsfragment zu veröffentlichen.

Nutzen Sie AEM Handbücher und Inhaltsfragmente optimal und verwenden Sie Inhaltsfragmente auf jeder AEM Site. Sie können die Details auch über APIs extrahieren, die von Inhaltsfragmenten unterstützt werden.

![Option zum Veröffentlichen von Inhaltsfragmenten](assets/content-fragment-publish.png){width="550" align="left"}

*Veröffentlichen Sie ein Thema in einem Inhaltsfragment.*

Weitere Informationen finden Sie unter [In einem Inhaltsfragment veröffentlichen](../user-guide//publish-content-fragment.md).

## Verbesserungen überprüfen

AEM Handbücher bieten jetzt eine verbesserte Überprüfungsfunktion mit den folgenden Funktionen:

### Suchüberprüfungsthemen

Die Durchführung von Überprüfungen ist ein wichtiges Merkmal AEM Leitfadens. Es hilft den Validierungsverantwortlichen, die ihnen zugewiesenen Dokumente zu überprüfen.
Jetzt können Sie nach einem Thema suchen, indem Sie einen Teil des Textes des Titels oder Dateipfads in die Suchleiste der Themenansicht des Prüfungsbereichs eingeben. Sie können auch alle Themen anzeigen oder Themen mit Kommentaren anzeigen. Standardmäßig können Sie alle in der Prüfungsaufgabe vorhandenen Themen anzeigen. Weitere Informationen finden Sie unter [Prüfungsthemen](../user-guide/review-topics.md).

![Suchen im Bereich &quot;Prüfungsthemen&quot;](assets/review-search-topic.png){width="800" align="left"}

*Suchen Sie ein Prüfungsthema im Prüfungsbereich.*



## Guides Extension Framework

Erstellen Sie benutzerdefinierte Pakete zusätzlich zu AEM Handbüchern, um die Erweiterbarkeit mit AEM Guides Extension Framework bereitzustellen. Diese Pakete sind für Entwickler und Berater nützlich und bieten ihnen Erweiterbarkeit für die Komponenten im Editor. Sie können Schaltflächen, Dialogfelder und Dropdown-Menüs auswählen und benutzerdefiniertes JavaScript hinzufügen, das einfach mit AEM Guides-Benutzeroberfläche interagieren kann.



## Native PDF-Verbesserungen

Die folgenden nativen PDF-Verbesserungen wurden in der Version vom September 2023 vorgenommen, um AEM Guides zu einem robusteren Produkt zu machen:



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

Weitere Informationen finden Sie unter **Seiten zusammenführen** Funktionsbeschreibung in [Seitenreihenfolge](../native-pdf/components-pdf-template.md#page-order) Abschnitt.

### Jedes Kapitel von der aktuellen Seite aus starten

Sie können die grundlegenden Konfigurationseinstellungen für den Start eines Kapitels von einer ungeraden oder geraden Seite, die TOC-Struktur und das Füllzeichenzeilenformat für die TOC-Einträge festlegen.

Jetzt können Sie auch ein Kapitel von der aktuellen Seite aus starten. Wenn Sie sich dafür entscheiden, werden alle Kapitel als Fortsetzung und ohne Seitenumbrüche veröffentlicht. Wenn ein Kapitel beispielsweise mitten auf Seite 15 endet, beginnt das nächste Kapitel auch auf der 15. Seite selbst.

Weitere Informationen finden Sie unter **Allgemein** Registerkartenbeschreibung in  [Erweiterte PDF-Einstellungen](../native-pdf/components-pdf-template.md#advanced-pdf-settings-advanced-pdf-settings).

### Statische Seiten

Sie können auch benutzerdefinierte Seitenlayouts erstellen und diese als statische PDF-Seiten veröffentlichen. Auf diese Weise können Sie statischen Inhalt wie Notizen oder leere Seiten hinzufügen.

Weitere Informationen finden Sie unter **Statische Seiten** Funktionsbeschreibung in [Seitenreihenfolge](../native-pdf/components-pdf-template.md#page-order) Abschnitt.


### Variablen in Querverweisen

Sie können Variablen verwenden, um einen Querverweis zu definieren. Wenn Sie eine Variable verwenden, wird ihr Wert aus den Eigenschaften ausgewählt.

Jetzt können Sie auch {figure} und {table}.
Verwendung {figure}um einen Querverweis zur Zahl hinzuzufügen. Sie wählt die Zahl aus den automatischen Nummernstilen aus, die Sie für die Beschriftung definiert haben.

Verwendung {table} , um der Tabellennummer einen Querverweis hinzuzufügen. Die Tabellennummer wird aus den automatischen Nummernstilen ausgewählt, die Sie für die Beschriftung definiert haben.

Weitere Informationen finden Sie unter [Querverweise](../native-pdf/components-pdf-template.md##cross-references).



### Neugestaltung des CSS-Editors

Jetzt wurde der CSS-Editor für ein besseres Benutzererlebnis mit Selektoren und Stileigenschaften neu gestaltet.

#### Verbesserung des Dialogfelds &quot;Stil hinzufügen&quot;

Sie können jetzt benutzerdefinierte Selektoren verwenden, um komplexe Stile hinzuzufügen. Mit dem neuen Selektor-Feld können Sie benutzerdefinierte Selektoren neben der Kombination aus Klasse, Tag und Pseudo-Klasse hinzufügen. Sie können beispielsweise `table a.link` -Stil für alle Hyperlinks in einer Tabelle.

![Hinzufügen von Stilen in nativen PDF-Vorlagen](assets/add-styles-native-pdf.png){width="300" align="left"}

*Fügen Sie die Details für den neuen Stil hinzu.*

#### Anpassen von Stileigenschaften

Jetzt werden Sie in AEM Handbüchern in ein neues Eigenschaftenbedienfeld unter dem Vorschauabschnitt für Stile vorgestellt. Sie können die Eigenschaften der Stile effizienter und schneller im Eigenschaftenbereich bearbeiten.


## Unterstützung für mehrere Themendefinitionen in einer einzelnen Auflistungsdefinition

Sie können jetzt eine oder mehrere Betreffdefinitionen in einer Zuordnung und die Auflistungsdefinitionen in einer anderen Zuordnung definieren und dann die Zuordnungsreferenz hinzufügen. Die Verweise auf die Betreffauflistung werden in derselben Zuordnung oder der referenzierten Zuordnung aufgelöst.

Sie können jetzt auch Bedingungen definieren und sie auf einige spezifische Elemente in einem Thema anwenden.  Die Bedingungen sind nur für diese spezifischen Elemente sichtbar, nicht für alle anderen Elemente.

Weitere Informationen zur Handhabung hierarchischer Definitionen von Betreffdefinitionen und Auflistungen finden Sie in der Funktionsbeschreibung des Betreffschemas im Abschnitt [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.





## Auswählen aller Vorgaben in einer Map Collection

Sie können nicht nur eine einzelne Vorgabe und alle Ordnerprofilvorgaben aktivieren, sondern auch alle Vorgaben für eine DITA-Zuordnung in einem Schritt aktivieren.
![Bearbeiten einer Zuordnungssammlung](assets/edit-map-collection-cs.png){width="800" align="left"}\
*Wählen Sie alle Vorgaben in einer Zuordnungssammlung aus.*

Weitere Informationen finden Sie unter [Verwenden der Kartensammlung für die Ausgabegenerierung](../user-guide/generate-output-use-map-collection-output-generation.md).


## Native PDF-Unterstützung im Dashboard für die Massenveröffentlichung


Mit der Massenaktivierung von AEM Handbüchern können Sie Ihre Inhalte schnell und einfach von der Authoring- bis zur Publishing-Instanz aktivieren. Auf der Massen-Aktivierungskarte können Sie die native PDF-Ausgabevorgabe, die AEM-Site, PDF, HTML5, benutzerdefinierte und JSON-Ausgabe einbeziehen.
Weitere Informationen finden Sie unter [Massenaktivierung veröffentlichter Inhalte](../user-guide/conf-bulk-activation.md).

## Verbessertes Werkzeug zum Verschieben von Stapeln

Als Administrator können Sie jetzt das verbesserte Werkzeug zum Verschieben von Massen-Dateien verwenden, um Ordner mit vielen Dateien von einem Speicherort zum anderen zu verschieben.
Sie können das Dialogfeld Datei durchsuchen verwenden, um die Quellordner auszuwählen, die Sie verschieben möchten. Sie können auch nach dem Zielspeicherort suchen, um die Quellordner zu verschieben. Auswählen ![Infosymbol](assets/info-icon.svg) {width="25" align="left"} in der Nähe eines Felds, um weitere Informationen dazu anzuzeigen.

Weitere Informationen finden Sie unter [Stapelweises Verschieben von Dateien](../user-guide/authoring-file-management.md#move-files-bulk).


## Erweiterte Funktionen zur Vorschau im Kontextmenü

Verwenden Sie das Kontextmenü, um die Datei (dita, .xml, audio, video oder image) schnell in der Vorschau anzuzeigen, ohne sie zu öffnen. Sie können jetzt die Größe des Vorschaufensters ändern. Wenn der Inhalt einen Verweis-Link enthält, können Sie ihn auswählen, um ihn in einer neuen Registerkarte zu öffnen.

![Vorschaufenster ](assets/quick-preview_cs.png){width="800" align="left"}

*Zeigen Sie eine Vorschau der Datei im Bereich an.*

Weitere Informationen zum Kontextmenü finden Sie im **Dateioptionen** Funktionsbeschreibung in [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.


## Verwenden Sie Variablen für das aktuelle Datum und die aktuelle Uhrzeit in den Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;

Beim Generieren von Ausgaben in AEM Site oder PDF können Sie Variablen zum Festlegen der Variablen **Zielpfad**, **Site-Name** oder **Dateiname** Optionen. Sie können jetzt auch die `${system_date}`und `${system_time}` Variablen. Mithilfe dieser Variablen können Sie diesen Optionen das aktuelle Datum und die aktuelle Uhrzeit anhängen.

Erfahren Sie, wie [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](../user-guide/generate-output-use-variables.md).
