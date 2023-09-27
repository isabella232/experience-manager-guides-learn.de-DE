---
title: Konfigurieren eines Datenquellen-Connectors mit Tools
description: Erfahren Sie, wie Sie mithilfe der Tools einen Datenquellen-Connector konfigurieren.
source-git-commit: 87e907a1fbc27c9b3f8db5e4ab3c78143b03001e
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---


# Konfigurieren eines Datenquellen-Connectors mithilfe der Tools

Experience Manager-Handbücher enthalten die **Data Sources** -Tool, mit dem Sie native Connectoren für Datenquellen konfigurieren können. Sie können Connectoren für die Datenbanken JIRA, SQL (MySQL, PostgreSQL, Microsoft SQL Server, SQLite, MariaDB, H2DB), AdobeCommerce und Elasticsearch einrichten.

Um einen Connector zu konfigurieren, führen Sie die folgenden Schritte aus:

1. Wählen Sie die **Adobe Experience Manager** oben klicken und &quot;Tools&quot;auswählen.
1. Auswählen **Handbücher** aus der Liste der Tools.
1. Wählen Sie die **Data Sources** Kachel. Die **Data Sources** angezeigt. Sie können die verbundenen Datenquellen anzeigen.

   Sie können zwischen **Listenansicht** oder **Kachelansicht** um die verschiedenen verbundenen Datenquellen als Liste oder Kacheln anzuzeigen.

   <img src="./assets/data-sources-create-window.png" alt= "Datenquellen, die auf der Seite &quot;Datenquellen&quot;aufgelistet sind" width="800">

   *Anzeigen oder Erstellen eines Datenquellen-Connectors*
1. Klicken Sie auf **Erstellen**.
1. Wählen Sie die Datenbank aus, für die Sie den Connector erstellen möchten. Beispielsweise der Elasticsearch-Connector.
   >[!NOTE]
   >
   >Alle verfügbaren nativen Datenbanken werden aufgelistet.

1. Klicken Sie auf **Weiter**.
1. Geben Sie die Konfigurations- und Verbindungsdetails gemäß der Datenbank ein.

   >[!TIP]
   >* Bewegen <img src="./assets/info-details.svg" alt= "Infosymbol" width="25"> neben dem Feld, um weitere Details dazu anzuzeigen.
   > * Felder mit * sind obligatorisch. Sie können beispielsweise die folgenden Details für den Elasticsearch-Connector eingeben.

   * **Name**: Geben Sie den Namen der Datenquelle ein.
   * Authentifizierungstyp: Wählen Sie in der Dropdown-Liste den Authentifizierungstyp aus. Beispiel: Grundlegende Authentifizierung mit Benutzername und Kennwort
   * **Benutzername**: Geben Sie Ihren Benutzernamen ein.
   * **Passwort**: Geben Sie Ihren Benutzernamen und Ihr Kennwort ein.
   * **URL**: Hinzufügen der API-URL.

1. Auswählen **Verbindung testen**. Sie können die **Verbindung testen** -Schaltfläche nur aktiviert ist, nachdem Sie die erforderlichen Details hinzugefügt haben. Zeigen Sie eine Erfolgsmeldung an, wenn die Verbindungsdetails korrekt sind. Andernfalls wird möglicherweise eine Fehlermeldung angezeigt.



1. Auswählen **Speichern** oben, um den Connector zu speichern.     Anzeigen der **Speichern** -Schaltfläche aktiviert, nachdem Sie alle Details ausgefüllt haben und die Verbindung erfolgreich hergestellt wurde.


   Wenn der Connector erfolgreich gespeichert wurde, können Sie die verbundene Datenquelle auf der Seite anzeigen.

## Für einen Connector verfügbare Funktionen

* Zwischen den **Listenansicht** oder **Kachelansicht**  um die verschiedenen verbundenen Datenquellen als Liste oder Kacheln anzuzeigen.
* Aktivieren Sie das Kontrollkästchen für einen einzelnen Connector. Klicks **Alle auswählen** , um alle Connectoren auszuwählen. Sie können auf **Auswahl für alle aufheben** wenn alle Connectoren ausgewählt sind.

<img src="./assets/data-sources-features.png" alt= "Funktionen der Datenquellen auf der Seite &quot;Datenquellen&quot;" width="800">

*Bearbeiten, erneutes Verbinden, Duplizieren oder Löschen eines Datenquellen-Connectors.*

Sie können die folgenden Funktionen für den Connector auf der **Data Sources** Seite:

* **Bearbeiten**: Bearbeiten Sie die Konfigurationsdetails für den ausgewählten Connector.

* **Wiederholen**: Schließen Sie eine Verbindung zu einem getrennten Connector wieder her.

* **Duplizieren**: Erstellen Sie einen neuen doppelten Connector mit dem aktuellen Connector als Basis. Der doppelte Connector wird standardmäßig mit einem Suffix (wie connectorname_1) erstellt. Beispiel: sample-elastisches-search_1.
Wenn der Connector mit demselben Namen vorhanden ist, wird ein Fehler angezeigt.

* **Löschen**: Löschen Sie den ausgewählten Connector.


Nachdem Sie die Datenquelle konfiguriert haben, wird der Connector unter der **Data Sources-Bedienfeld** im Web-Editor. Anschließend können Sie eine Verbindung zur Datenquelle herstellen und ein Inhaltsfragment in Ihre Themen einfügen. Weitere Informationen finden Sie unter [Inhaltsfragment aus Ihrer Datenquelle einfügen](../user-guide/web-editor-content-snippet.md).




