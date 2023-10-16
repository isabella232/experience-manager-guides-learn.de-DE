---
title: Versionshinweise | Neue Funktionen in Version 4.3.1 der Adobe Experience Manager-Handbücher
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in Version 4.3.1 der Adobe Experience Manager-Handbücher.
source-git-commit: 5c51ff7f52624c6403e5486e099d1262f324e523
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%

---

# Neue Funktionen in Version 4.3.1 der Adobe Experience Manager-Handbücher (Oktober 2023)

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version 4.3.1 der Adobe Experience Manager-Handbücher (später auch als *AEM*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](./release-notes-4.3.1.md).

## Herstellen einer Verbindung zu einer Datenquelle und Einfügen der Themen

Experience Manager-Handbücher bieten vordefinierte Connectoren, mit denen Sie eine Verbindung zu Ihren Datenquellen herstellen können. AEM Handbücher sind somit ein echter Content-Hub. Dies bietet Ihnen den Vorteil, dass Sie Zeit und Mühe sparen, die andernfalls für das manuelle Hinzufügen oder die Replikation von Daten ausgegeben würden.

Neben den bereits vorhandenen nativen Connectoren wie JIRA und SQL (MySQL, PostgreSQL, SQL Server, SQLite) kann Ihr Administrator auch Connectoren für die Datenbanken MariaDB, H2DB, AdobeCommerce und Elasticsearch konfigurieren. Sie können auch andere Connectoren hinzufügen, indem sie die Standardschnittstellen erweitern.

Sie können die konfigurierten Connectoren unter dem **Data Sources** im Web Editor angezeigt.

<img src="assets/data-sources.png" alt="Liste der Datenquellen im Bereich" width="300">

*Anzeigen der verbundenen Datenquellen.*

Sie können jetzt auch ein Thema aus einer verbundenen Datenquelle erstellen. Ein Thema kann Daten in verschiedenen Formaten wie Tabellen, Listen und Absätzen enthalten. Außerdem können Sie eine DITA-Zuordnung für alle Themen erstellen. Beim Abrufen aus einer Datenquelle können Sie dem Thema Metadaten zuordnen.

Weitere Informationen finden Sie unter [Daten aus Ihrer Datenquelle verwenden](../user-guide/web-editor-content-snippet.md).

## Konfigurieren eines Datenquellen-Connectors über die Benutzeroberfläche

Experience Manager-Handbücher bieten jetzt auch eine **Data Sources** -Tool, mit dem Sie native Connectoren für Datenquellen konfigurieren können. Sie können die Connectoren für JIRA-, SQL- (MySQL-, PostgreSQL-, Microsoft SQL Server-, SQLite-, MariaDB-, H2DB-), AdobeCommerce- und Elasticsearch-Datenbanken einfach erstellen.

Sie können einen Datenquellen-Connector auch einfach bearbeiten, neu verbinden, duplizieren oder löschen. Erfahren Sie mehr über das [einfach einen Datenquellen-Connector über die Benutzeroberfläche konfigurieren](../install-guide/conf-data-source-connector-tools.md).

![im Bereich &quot;Datenquellen&quot;aufgelistete Data Source Connectors](assets/data-sources-create-window.png){width="550" align="left"}

*Erstellen Sie die Data Source Connectors und zeigen Sie sie im Bereich &quot;Data Sources&quot;an.*

## Anzeigen von Protokollen für den Themengenerator

Sie können jetzt auch die Protokolldatei zur Inhaltserstellung anzeigen. Mithilfe dieser Protokolldatei können Sie die Warnungen, Fehler und Ausnahmen überprüfen.  Erfahren Sie mehr darüber, wie die [Optionen für einen Themengenerator](../user-guide/web-editor-content-snippet.md#options-for-a-topic-generator) helfen Ihnen, die Themengeneratoren einfach zu erstellen und zu verwalten.

## Unterstützung für Velocity-Tools in den Datenquellenvorlagen

Sie können jetzt die Velocity-Tools in den Vorlagen für Experience Manager-Handbücher verwenden. Mit diesen Tools können Sie verschiedene Funktionen auf die Daten anwenden, die Sie aus den Datenquellen abrufen. Sie können die Vorlagen beim Erstellen eines Inhaltsfragments oder eines Themas verwenden. Mit dieser Funktion sparen Sie Zeit und Mühe bei der manuellen Anwendung derselben Funktion auf jeden Datensatz.  Außerdem werden präzise Ergebnisse sichergestellt.
Beispielsweise können Sie das $mathematische Tool verwenden, um mathematische Funktionen auszuführen.
Erfahren Sie mehr über das [Verwenden von Velocity-Tools in Datenquellenvorlagen](../user-guide/web-editor-content-snippet.md#use-velocity-tools).


## Native PDF-Verbesserungen

Die folgenden nativen PDF-Verbesserungen wurden in der Version vom Oktober 2023 vorgenommen:

### Seitenzahl für die erste Seite eines Layouts zurücksetzen

In der nativen PDF-Ausgabe können Sie die Seitenzahlen neu starten und die Nummer angeben, ab der die Nummerierung beginnt. Jetzt können Sie die Nummerierung auch nur für das erste Vorkommen eines Abschnitts beginnen.
Erfahren Sie mehr über das [Arbeiten mit den Seiteneigenschaften eines Seitenlayouts](../native-pdf/design-page-layout.md#page-props-page-layout).


### Anzeigen von Kapiteln ohne automatische Zahlen im Inhaltsverzeichnis

Experience Manager-Guides zeigen die Kapitelnummern zusammen mit den Kapitelnamen im Inhaltsverzeichnis an. Jetzt können Sie nur die Kapitelnamen ohne Kapitelnummern veröffentlichen. Weitere Informationen zur Konfiguration der [Erweiterte PDF-Einstellungen einer Vorlage](../native-pdf/components-pdf-template.md#advanced-pdf-settings).

## Herunterladen einer Karte vom Web-Editor

Jetzt können Sie nicht nur eine Karte in der Kartenansicht des Web-Editors bearbeiten, sondern sie auch herunterladen. Sie können die Karte mit einer bestimmten Grundlinie herunterladen. Sie können auch die Hierarchie reduzieren und alle Dateien und Ordner in einem Ordner speichern.

Weitere Informationen finden Sie im Abschnitt **Kartenansicht** Funktionsbeschreibung innerhalb der [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

![Optionen-Menü einer Datei in der Repository-Ansicht](assets/options-menu-repo-view-file-level-2310.png){width="550" align="left"}

*Wählen Sie eine Datei in der Repository-Ansicht aus und wählen Sie die Option, um eine Aktion für die Datei auszuführen.*


## Unterstützung für mehrere Themendefinitionen in einer einzelnen Auflistungsdefinition

Sie können jetzt eine oder mehrere Betreffdefinitionen in einer Zuordnung und die Auflistungsdefinitionen in einer anderen Zuordnung definieren und dann die Zuordnungsreferenz hinzufügen. Die Verweise auf die Betreffauflistung werden in derselben Zuordnung oder der referenzierten Zuordnung aufgelöst.

Sie können jetzt auch Bedingungen definieren und sie auf einige spezifische Elemente in einem Thema anwenden.  Die Bedingungen sind nur für diese spezifischen Elemente sichtbar, nicht für alle anderen Elemente.

Weitere Informationen zur Handhabung hierarchischer Definitionen von Betreffdefinitionen und Auflistungen finden Sie in der Funktionsbeschreibung des Betreffschemas im Abschnitt [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.




## Erweiterte Funktionen zur Vorschau im Kontextmenü

Verwenden Sie das Kontextmenü, um die Datei (dita, .xml, audio, video oder image) schnell in der Vorschau anzuzeigen, ohne sie zu öffnen. Sie können jetzt die Größe des Vorschaufensters ändern. Wenn der Inhalt einen Verweis-Link enthält, können Sie ihn auswählen, um ihn in einer neuen Registerkarte zu öffnen.

![Vorschaufenster ](assets/quick-preview_cs.png){width="800" align="left"}

*Zeigen Sie eine Vorschau der Datei im Bereich an.*

Weitere Informationen zum Kontextmenü finden Sie im **Dateioptionen** Funktionsbeschreibung in [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

## Bearbeiten einer Datei im Oxygen-Connector-Plug-in

In den Experience Manager Guides können Sie jetzt eine Datei im Web Editor auswählen und die Datei dann im Oxygen-Connector-Plugin bearbeiten. Diese Option ist im Rahmen der nativen Unterstützung nicht aktiviert.

Weitere Informationen finden Sie im Abschnitt **Dateioptionen** Funktionsbeschreibung innerhalb der [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

## Verwenden Sie Variablen für das aktuelle Datum und die aktuelle Uhrzeit in den Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;

Beim Generieren von Ausgaben in AEM Site oder PDF können Sie Variablen zum Festlegen der Variablen **Zielpfad**, **Site-Name** oder **Dateiname** Optionen. Sie können jetzt auch die `${system_date}`und `${system_time}` Variablen. Mithilfe dieser Variablen können Sie diesen Optionen das aktuelle Datum und die aktuelle Uhrzeit anhängen.

Erfahren Sie, wie [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](../user-guide/generate-output-use-variables.md).


## Tastaturbefehle zum Verschieben des Cursors in den Web-Editor

Experience Manager-Handbücher ermöglichen es Ihnen jetzt auch, Tastaturbefehle zu verwenden, um den Cursor in den Web-Editor zu verschieben. Sie können die Tastaturbefehle verwenden, um ein Wort schnell nach links oder rechts zu verschieben. Mithilfe der Tastaturbefehle können Sie auch zum Anfang oder Ende der Zeile wechseln.

Weitere Informationen zum [Tastaturbefehle im Web-Editor](../user-guide/web-editor-keyboard-shortcuts.md).