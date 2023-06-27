---
title: Inhaltsfragment aus Ihrer Datenquelle einfügen
description: Erfahren Sie, wie Sie einen Inhaltsausschnitt aus Ihrer Datenquelle einfügen
source-git-commit: f01903fe9ae3d60a8b818e881fd3b1d626fcd2bc
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Inhaltsfragment aus Ihrer Datenquelle einfügen

AEM Handbücher bieten die Möglichkeit, eine Verbindung mit Ihrer Datenquelle herzustellen. Sie können Ihre Daten abrufen, in Ihre Themen einfügen und sie bearbeiten. Sie können einfach ein Inhaltsfragment mit dem Inhaltsfragment-Generator erstellen und es in Ihren Themen wiederverwenden.

Führen Sie die folgenden Schritte aus, um ein Inhaltsfragment mit dem Inhaltsfragment-Generator zu erstellen und es in Ihr Thema einzufügen:

1. Auswählen **Data Sources** ![](images/data-source-icon.svg)   im linken Bereich, um die verbundenen Datenquellen anzuzeigen. Das Bedienfeld &quot;Data Sources&quot;wird geöffnet und zeigt alle verbundenen Datenquellen an. Weitere Informationen finden Sie unter [Konfigurieren eines Datenquellen-Connectors](../cs-install-guide/conf-data-source-connector.md).
   >[!NOTE]
   >
   > Daraufhin werden die Datenquellen angezeigt, für die Ihr Administrator den Connector konfiguriert hat.

1. Wählen Sie eine Datenquelle aus, um die für die ausgewählte Datenquelle verfügbaren Inhaltsfragment-Generatoren anzuzeigen.
   ![](images/code-snippet-generator.png){width="300" align="left"}
1. Auswählen **Hinzufügen** , um einen neuen Inhaltsfragment-Generator hinzuzufügen. Die **Inhaltsfragment-Generator hinzufügen** -Bedienfeld geöffnet.

1. Geben Sie die Abfrage in das Textfeld Datenabfrage ein.
1. Wählen Sie die Vorlage aus, die Ihrer Datenquelle zugeordnet ist. **Datenzuordnungsvorlage** Dropdown-Liste.
Die nativen Vorlagen für die ausgewählte Datenquelle werden in der Dropdown-Liste angezeigt. Sie können beispielsweise die Vorlage &quot;sql-table&quot;für die Datenquelle &quot;PostgreSQL&quot;anzeigen.

   >[!NOTE]
   >  
   > Wenn Ihr Administrator benutzerdefinierte Vorlagen konfiguriert hat, werden diese Vorlagen auch in der Dropdown-Liste angezeigt (basierend auf den von Ihrem Administrator durchgeführten Vorlagenpfadkonfigurationen).
1. Klicken **Abrufen** , um die Daten aus der Datenquelle abzurufen und die Vorlage auf die Daten anzuwenden, die aus der SQL-Abfrage resultieren.
1. Sie können die Daten in der Vorschau oder in der DITA-Quellansicht anzeigen.

   1. Die Vorschau zeigt, wie die Daten beim Einfügen in den Inhalt angezeigt werden. Die Vorschau zeigt einen kleinen Teil der Daten im Format der ausgewählten Vorlage an.
Beispiel:
      * Wenn Sie die Vorlage &quot;sql-table&quot;ausgewählt haben, können Sie die SQL-Daten im Tabellenformat anzeigen.
      * Wenn Sie die Vorlage &quot;jira-ordered-list&quot;ausgewählt haben, können Sie eine geordnete Liste für die Jira-Probleme anzeigen.

   1. Die Quellansicht zeigt die Daten in der DITA-Quellansicht an.
      ![](images/add-content-snippet-generator.png){width="800" align="left"}
1. Um die Ergebnisse der Abfrage zu speichern, geben Sie den Namen des Generators ein und klicken Sie auf **HINZUFÜGEN**.   Der Liste wird ein neuer Inhaltsfragment-Generator hinzugefügt.

   >[!NOTE]
   >
   > Sie müssen die Dateibenennungskonvention für den Namen des neuen Inhaltsgenerators befolgen. Im Namen des Inhaltsfragment-Generators darf kein Leerzeichen stehen. Außerdem können Sie keinen neuen Inhaltsgenerator mit dem Namen eines vorhandenen Inhaltsgenerators speichern. Es tritt ein Fehler auf.

## Optionen für einen Inhaltsfragment-Generator

Klicken Sie mit der rechten Maustaste auf einen Inhaltsfragment-Generator, um die Optionen zu öffnen. Mithilfe der Optionen können Sie die folgenden Vorgänge ausführen:
* **Einfügen**: Verwenden Sie diese Option, um das ausgewählte Inhaltsfragment in das Thema einzufügen, das im Web Editor zur Bearbeitung geöffnet wurde. Da die Daten als Snippet eingefügt werden, können Sie die Daten in Ihrem Thema auch im Web Editor bearbeiten.

  >[!NOTE]
  > 
  > Die Option &quot;Einfügen&quot;wird nur angezeigt, wenn Sie ein Thema bearbeiten.

* **Bearbeiten**: Verwenden Sie diese Option, um Änderungen am Inhaltsfragment-Generator vorzunehmen und zu speichern.
* **Löschen**: Verwenden Sie diese Option, um den ausgewählten Inhaltsfragment-Generator zu löschen.
* **Duplizieren**: Verwenden Sie diese Option, um ein Duplikat oder eine Kopie des ausgewählten Inhaltsfragment-Generators zu erstellen. Das Duplikat wird standardmäßig mit einem Suffix (wie generator_1) erstellt.

### Abfrageausschnitt einfügen

Sie können auch die **Query Snippet einfügen** ![](images/data-source-icon.svg)   aus der Hauptsymbolleiste, um das Datenfragment in die Themen einzufügen.  Sie können einen Generator aus der Dropdown-Liste auswählen, Ihre Abfrage bearbeiten oder die Vorlage ändern und die Daten in Ihr Thema einfügen.

![](images/insert-content-snippet.png){width="800" align="left"}




