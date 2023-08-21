---
title: Versionshinweise | Neue Funktionen in Adobe Experience Manager-Handbüchern, Version September 2023
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in der Version vom September 2023 von Adobe Experience Manager Guides as a Cloud Service
source-git-commit: c01c3500b55f3579633ad1a954f9010783365add
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# Neue Funktionen in der Version September 2023 von Adobe Experience Manager Guides as a Cloud Service

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version September 2023 der Adobe Experience Manager-Handbücher (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](release-notes-2023.7.0.md).

## Herstellen einer Verbindung zu einer Datenquelle und Einfügen von Daten in Ihre Themen

Jetzt können Sie über vordefinierte Connectoren aus AEM Handbüchern schnell eine Verbindung zu Ihren Datenquellen herstellen. Durch die Verbindung mit einer Datenquelle können Sie Ihre Informationen mit der Quelle synchronisieren, und alle Aktualisierungen der Daten werden automatisch übernommen, was AEM Guides zu einem echten Content-Hub macht. Mit dieser Funktion sparen Sie Zeit und Mühe beim manuellen Hinzufügen oder Kopieren der Daten.

Mit AEM Guides kann Ihr Administrator die nativen Connectoren für JIRA- und SQL-Datenbanken (MySQL, PostgreSQL, SQL Server, SQLite) konfigurieren. Sie können auch andere Connectoren hinzufügen, indem sie die Standardschnittstellen erweitern.
Nach dem Hinzufügen können Sie die konfigurierten Connectoren anzeigen, die im Web Editor im Bereich Data Sources aufgeführt sind.

<img src="assets/data-sources.png" alt="Liste der Datenquellen im Bereich" width="300">

*Anzeigen der verbundenen Datenquellen.*

Erstellen Sie ein Inhaltsfragment, um die Daten aus einer verbundenen Datenquelle abzurufen. Anschließend können Sie die Daten in Ihre Themen einfügen und sie bearbeiten. Nachdem Sie einen Inhaltsfragment-Generator erstellt haben, können Sie ihn wiederverwenden, um die Daten in ein beliebiges Thema einzufügen.

Jetzt können Sie auch ein Thema aus einer verbundenen Datenquelle erstellen. Ein Thema kann Daten in verschiedenen Formaten wie Tabellen, Listen und Absätzen enthalten. Außerdem können Sie eine DITA-Zuordnung für alle Themen erstellen. Beim Abrufen aus einer Datenquelle können Sie dem Thema Metadaten zuordnen.

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

Die folgenden nativen PDF-Verbesserungen wurden in Version 4.3.0 vorgenommen, um AEM Guides zu einem robusteren Produkt zu machen:



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



### Neugestaltung des CSS-Editors

Jetzt wurde der CSS-Editor für ein besseres Benutzererlebnis mit Selektoren und Stileigenschaften neu gestaltet.

#### Verbesserung des Dialogfelds &quot;Stil hinzufügen&quot;

Sie können jetzt benutzerdefinierte Selektoren verwenden, um komplexe Stile hinzuzufügen. Mit dem neuen Selektor-Feld können Sie benutzerdefinierte Selektoren neben der Kombination aus Klasse, Tag und Pseudo-Klasse hinzufügen. Sie können beispielsweise `table a.link` -Stil für alle Hyperlinks in einer Tabelle.

![Hinzufügen von Stilen in nativen PDF-Vorlagen](assets/add-styles-native-pdf.png){width="300" align="left"}

#### Anpassen von Stileigenschaften

Jetzt werden Sie in AEM Handbüchern in ein neues Eigenschaftenbedienfeld unter dem Vorschauabschnitt für Stile vorgestellt. Sie können die Eigenschaften der Stile effizienter und schneller im Eigenschaftenbereich bearbeiten.



## Auswählen aller Vorgaben in einer Map Collection

Sie können nicht nur eine einzelne Vorgabe auswählen, sondern auch alle Vorgaben für eine DITA-Zuordnung in einem Schritt aktivieren.
![Bearbeiten einer Zuordnungssammlung](assets/edit-map-collection.png){width="800" align="left"}\
*Wählen Sie alle Vorgaben in einer Zuordnungssammlung aus.*

Weitere Informationen finden Sie unter [Verwenden der Kartensammlung für die Ausgabegenerierung](../user-guide/generate-output-use-map-collection-output-generation.md).


## Native PDF-Unterstützung im Dashboard für die Massenveröffentlichung


Mit der Massenaktivierung von AEM Handbüchern können Sie Ihre Inhalte schnell und einfach von der Authoring- bis zur Publishing-Instanz aktivieren. Auf der Massen-Aktivierungskarte können Sie die native PDF-Ausgabevorgabe, die AEM-Site, PDF, HTML5, benutzerdefinierte und JSON-Ausgabe einbeziehen.
Weitere Informationen finden Sie unter [Massenaktivierung veröffentlichter Inhalte](../user-guide/conf-bulk-activation.md).

## Verbessertes Werkzeug zum Verschieben von Stapeln

Als Administrator können Sie jetzt das verbesserte Werkzeug zum Verschieben von Massen-Dateien verwenden, um Ordner mit vielen Dateien von einem Speicherort zum anderen zu verschieben.
Sie können das Dialogfeld Datei durchsuchen verwenden, um die Quellordner auszuwählen, die Sie verschieben möchten. Sie können auch nach dem Zielspeicherort suchen, um die Quellordner zu verschieben. Auswählen ![Infosymbol](assets/info-icon.svg) {width="25" align="left"} in der Nähe eines Felds, um weitere Informationen dazu anzuzeigen.

Weitere Informationen finden Sie unter [Stapelweises Verschieben von Dateien](../user-guide/authoring-file-management.md#move-files-bulk).


