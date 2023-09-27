---
title: Versionshinweise | Neue Funktionen in Adobe Experience Manager-Handbüchern, Version Oktober 2023
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im Oktober 2023.
source-git-commit: 18adbd41370d32b183cc4828d1d79b7183453f5e
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Neue Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service vom Oktober 2023

Dieser Artikel behandelt die neuen und verbesserten Funktionen in der Version Oktober 2023 der Adobe Experience Manager-Handbücher (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](release-notes-2023.10.0.md).


## Konfigurieren eines Datenquellen-Connectors mithilfe der Tools

Experience Manager-Handbücher bieten jetzt eine **Data Sources** -Tool, mit dem Sie native Connectoren für Datenquellen konfigurieren können. Sie können die Connectoren für JIRA-, SQL- (MySQL-, PostgreSQL-, Microsoft SQL Server-, SQLite-, MariaDB-, H2DB-), AdobeCommerce- und Elasticsearch-Datenbanken einfach erstellen.

Sie können einen Datenquellen-Connector auch einfach bearbeiten, neu verbinden, duplizieren oder löschen. Erfahren Sie, wie [einen Datenquellen-Connector mithilfe der Tools konfigurieren](../install-guide/conf-data-source-connector.md).

![im Bereich &quot;Datenquellen&quot;aufgelistete Data Source Connectors](assets/data-sources-create-window.png){width="550" align="left"}

*Erstellen Sie die Data Source Connectors und zeigen Sie sie im Bereich &quot;Data Sources&quot;an.*

## Anzeigen von Protokollen für den Themengenerator

Sie können jetzt auch die Protokolldatei zur Inhaltserstellung anzeigen. Mithilfe dieser Protokolldatei können Sie die Warnungen, Fehler und Ausnahmen überprüfen.  Erfahren Sie mehr darüber, wie die [Optionen für einen Themengenerator](../user-guide/web-editor-content-snippet.md#options-for-a-topic-generator) helfen Ihnen, die Themengeneratoren einfach zu erstellen und zu verwalten.

## Unterstützung für Velocity-Tools in den Datenquellenvorlagen

Sie können jetzt die Velocity-Tools in den Vorlagen für Experience Manager-Handbücher verwenden. Mit diesen Tools können Sie verschiedene Funktionen auf die Daten anwenden, die Sie aus den Datenquellen abrufen. Sie können die Vorlagen beim Erstellen eines Inhaltsfragments oder eines Themas verwenden. Mit dieser Funktion sparen Sie Zeit und Mühe bei der manuellen Anwendung derselben Funktion auf jeden Datensatz.  Außerdem werden präzise Ergebnisse sichergestellt.
Beispielsweise können Sie das $mathematische Tool verwenden, um mathematische Funktionen auszuführen.
Erfahren Sie mehr über das [Verwenden von Velocity-Tools in Datenquellenvorlagen](../user-guide/web-editor-content-snippet.md##use-velocity-tools).


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

## Bearbeiten einer Datei im Oxygen-Connector-Plug-in

In den Experience Manager Guides können Sie jetzt eine Datei im Web Editor auswählen und die Datei dann im Oxygen-Connector-Plugin bearbeiten. Diese Option ist im Rahmen der nativen Unterstützung nicht aktiviert.

Weitere Informationen finden Sie im Abschnitt **Dateioptionen** Funktionsbeschreibung innerhalb der [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

