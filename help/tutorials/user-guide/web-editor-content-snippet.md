---
title: Inhaltsfragment aus Ihrer Datenquelle einfügen
description: Verwenden Sie Daten aus Ihrer Datenquelle in AEM Handbüchern. Erfahren Sie, wie Sie ein Inhaltsfragment aus Ihrer Datenquelle einfügen. Erstellen Sie ein Thema mit dem Thema-Generator.
exl-id: 9d60499c-49b4-4793-b3ec-5c99b34338e0
source-git-commit: e8503e1441b7bc365d37c76ab9cf7b5f50374f10
workflow-type: tm+mt
source-wordcount: '2029'
ht-degree: 0%

---

# Daten aus Ihrer Datenquelle verwenden

A **Datenquelle** ist ein System, in dem Sie die Daten für Ihr Unternehmen speichern und verwalten. Dies sind Ihre Datensatzsysteme wie JIRA, SQL-Datenbanken, PIM oder PLM. AEM Handbücher bieten die Möglichkeit, eine Verbindung mit Ihrer Datenquelle herzustellen und die Daten daraus zu verwenden.

## Data Sources-Bedienfeld

Auswählen **Data Sources** ![](images/data-source-icon.svg) im linken Bereich, um die verbundenen Datenquellen anzuzeigen. Das Bedienfeld Data Sources wird geöffnet und zeigt alle verbundenen Datenquellen an.

Je nach Einrichtung kann Ihr Administrator einen Datenquellen-Connector konfigurieren:

<details>
<summary> Cloud Services </summary>


- Wenn Sie die Version von Oktober 2023 oder höher verwenden, erfahren Sie, wie Sie [einen Datenquellen-Connector über die Benutzeroberfläche konfigurieren](../cs-install-guide/conf-data-source-connector-tools.md) im Cloud Service-Installations- und Konfigurationshandbuch.

- Wenn Sie die Version vom Juli 2023 oder September 2023 verwenden, erfahren Sie, wie Sie [Konfigurieren eines Datenquellen-Connectors](../cs-install-guide/conf-data-source-connector.md) im Cloud Service-Installations- und Konfigurationshandbuch.

</details>

<details>    
<summary>  On-Premise Software </summary>

Erfahren Sie, wie [Konfigurieren eines Datenquellen-Connectors](../install-guide/conf-data-source-connector.md)  im On-Premise-Installations- und Konfigurationshandbuch.
</details>


>[!NOTE]
>
> Daraufhin werden die Datenquellen angezeigt, für die Ihr Administrator den Connector konfiguriert hat.


## Listenansicht oder Kachelansicht anzeigen

Sie können zwischen der Listen- oder der Kachelansicht umschalten, um die verschiedenen Datenquellen in Form einer Liste oder als Kacheln anzuzeigen.

Wählen Sie eine Datenquelle aus, um die Inhaltsfragment-Generatoren und die Themengeneratoren anzuzeigen, die für die ausgewählte Datenquelle verfügbar sind.

### Listenansicht  ![](images/data-sources-list-view-icon.svg)

![](images/data-sources-list-view.png){width="300" align="left"}

*Liste der verbundenen Datenquellen.*

### Kachelansicht   ![](images/data-sources-tile-view-icon.svg)

![](images/data-sources-tile-view.png){width="300" align="left"}

*Anzeigen der verbundenen Datenquellen als Kacheln*

Sie können die Daten aus Datenquellen auf zwei Arten verwenden:
- Inhaltsfragment einfügen
- Thema erstellen



## Inhaltsfragment aus Ihrer Datenquelle einfügen

AEM Handbücher bieten die Möglichkeit, eine Verbindung mit Ihrer Datenquelle herzustellen. Sie können Ihre Daten abrufen, in Ihre Themen einfügen und sie bearbeiten. Sie können einfach ein Inhaltsfragment mit dem Inhaltsfragment-Generator erstellen und es in Ihren Themen wiederverwenden.

Führen Sie die folgenden Schritte aus, um ein Inhaltsfragment mit dem Inhaltsfragment-Generator zu erstellen und es in Ihr Thema einzufügen:

1. Auswählen **Data Sources** ![](images/data-source-icon.svg)   im linken Bereich, um die verbundenen Datenquellen anzuzeigen.

1. Wählen Sie eine Datenquelle aus, um die für die ausgewählte Datenquelle verfügbaren Inhaltsfragment-Generatoren anzuzeigen.

   ![](images/code-snippet-generator.png){width="300" align="left"}
   *Im Bereich &quot;Data Sources&quot;werden die verfügbaren Inhaltsfragment-Generatoren aufgelistet.*

1. Auswählen **Hinzufügen** , um einen neuen Inhaltsfragment-Generator hinzuzufügen. Die **Inhaltsfragment-Generator hinzufügen** -Bedienfeld geöffnet.

1. Geben Sie die Abfrage in das Textfeld Datenabfrage ein.
1. Wählen Sie die Vorlage aus, die Ihrer Datenquelle zugeordnet ist. **Datenzuordnungsvorlage** Dropdown.
Die nativen Vorlagen für die ausgewählte Datenquelle werden in der Dropdown-Liste angezeigt. Sie können beispielsweise die Vorlage &quot;sql-table&quot;für die Datenquelle &quot;PostgreSQL&quot;anzeigen.

   >[!NOTE]
   >  
   > Wenn Ihr Administrator benutzerdefinierte Vorlagen konfiguriert hat, werden diese Vorlagen auch in der Dropdown-Liste angezeigt (basierend auf den von Ihrem Administrator durchgeführten Vorlagenpfadkonfigurationen).
   >   
   >Sie können auch Velocity-Tools in den Vorlagen verwenden. Erfahren Sie mehr über das [Verwenden von Velocity-Tools](#use-velocity-tools).

1. Klicks **Abrufen** , um die Daten aus der Datenquelle abzurufen und die Vorlage auf die Daten anzuwenden, die aus der SQL-Abfrage resultieren.

1. Sie können die Daten in der Vorschau oder in der DITA-Quellansicht anzeigen.

   1. Die Vorschau zeigt an, wie die Daten beim Einfügen in den Inhalt angezeigt werden. Die Vorschau zeigt einen kleinen Teil der Daten im Format der ausgewählten Vorlage an.
Zum Beispiel:
      - Wenn Sie die Vorlage &quot;sql-table&quot;ausgewählt haben, können Sie die SQL-Daten im Tabellenformat anzeigen.
      - Wenn Sie die Vorlage &quot;jira-ordered-list&quot;ausgewählt haben, können Sie eine geordnete Liste für die Jira-Probleme anzeigen.

   1. Die Quellansicht zeigt die Daten in der DITA-Quellansicht an.
      ![](images/add-content-snippet-generator.png){width="800" align="left"}
      *Fügen Sie einen Inhaltsfragment-Generator hinzu. Daten im Quell- oder Vorschaumodus anzeigen.*

1. Um die Ergebnisse der Abfrage zu speichern, geben Sie den Namen des Generators ein und klicken Sie auf **HINZUFÜGEN**.   Der Liste wird ein neuer Inhaltsfragment-Generator hinzugefügt.

   >[!NOTE]
   >
   > Sie müssen die Dateibenennungskonvention für den Namen des neuen Inhaltsgenerators befolgen. Im Namen des Inhaltsfragment-Generators darf kein Leerzeichen stehen. Außerdem können Sie keinen neuen Inhaltsgenerator mit dem Namen eines vorhandenen Inhaltsgenerators speichern. Es tritt ein Fehler auf.

### Optionen für einen Inhaltsfragment-Generator

Klicken Sie mit der rechten Maustaste auf einen Inhaltsfragment-Generator, um die Optionen zu öffnen. Mithilfe der Optionen können Sie die folgenden Vorgänge ausführen:

- **Vorschau**: Verwenden Sie diese Option, um einen Bereich zu öffnen und einen kleinen Teil der Anzeige der Daten in der Ausgabe anzuzeigen.
- **Einfügen**: Verwenden Sie diese Option, um das ausgewählte Inhaltsfragment in das Thema einzufügen, das im Web Editor zur Bearbeitung geöffnet wurde. Da die Daten als Snippet eingefügt werden, können Sie die Daten in Ihrem Thema auch im Web Editor bearbeiten.

  >[!NOTE]
  > 
  > Die Option &quot;Einfügen&quot;wird nur angezeigt, wenn Sie ein Thema bearbeiten.

- **Bearbeiten**: Verwenden Sie diese Option, um Änderungen am Inhaltsfragment-Generator vorzunehmen und zu speichern.
- **Löschen**: Mit dieser Option können Sie den ausgewählten Inhaltsfragment-Generator löschen.
- **Duplizieren**: Verwenden Sie diese Option, um ein Duplikat oder eine Kopie des ausgewählten Inhaltsfragment-Generators zu erstellen. Das Duplikat wird standardmäßig mit einem Suffix (wie generator_1) erstellt.

### Abfrageausschnitt einfügen

Sie können auch die **Query Snippet einfügen** ![](images/data-source-icon.svg)   aus der Hauptsymbolleiste, um das Datenfragment in die Themen einzufügen.  Sie können einen Generator aus der Dropdown-Liste auswählen, Ihre Abfrage bearbeiten oder die Vorlage ändern und die Daten in Ihr Thema einfügen.

![](images/insert-content-snippet.png){width="800" align="left"}

*Bearbeiten und fügen Sie ein Datenfragment ein.*

## Erstellen eines Themas mit dem Themengenerator

Mit einem Themengenerator können Sie Themen erstellen, die Daten aus Ihren Quellen enthalten. Sie können schnell einen Themengenerator erstellen und dann die Themen mithilfe des Generators generieren. Jedes Thema kann Daten in verschiedenen Formaten wie Tabellen, Listen und Absätzen enthalten.   In einem Thema können Sie beispielsweise eine Tabelle mit Details zu allen neuen Produkten und eine Liste aller Produkte hinzufügen, die nicht mehr zum Verkauf angeboten werden.

Der Themengenerator kann die Themen mit den Daten und eine DITA-Zuordnung für alle Themen erstellen. Sie können auch `<conref>` diese Themen in Ihrem Inhalt. Auf diese Weise können Sie Ihre Daten mit der Datenquelle synchronisieren und sie einfach aktualisieren.



### Thema erstellen

Führen Sie die folgenden Schritte aus, um ein Thema mit dem Themengenerator zu erstellen:

1. Wählen Sie eine Datenquelle aus, um die Inhaltsfragment-Generatoren und die Themengeneratoren anzuzeigen, die für die ausgewählte Datenquelle verfügbar sind.

   ![](images/data-sources.png){width="300" align="left"}

   *Fügen Sie einen Themengenerator für eine verbundene Datenquelle hinzu.*

1. Auswählen **Hinzufügen** ![](images/Add_icon.svg) und wählen **Themengenerator** aus der Dropdown-Liste, um einen neuen Themengenerator hinzuzufügen. Die **Themengenerator hinzufügen** -Bedienfeld geöffnet.



1. Geben Sie die Werte in die Felder unter den folgenden drei Registerkarten der **Themengenerator hinzufügen** Bereich:

   **Abrufen der Konfiguration**

   ![](images/topic-generator-fetch-configuration.png){width="300" align="left"}

   *Fügen Sie die Datenabfrage, die Vorlage für die Datenzuordnung und die Details des Stammknotens für den Themengenerator hinzu und geben Sie ihm im Bereich &quot;Fetch Configuration&quot;einen eindeutigen Namen.*

   1. Geben Sie die Abfrage im **Datenabfrage** Textfeld.
   1. Wählen Sie die Vorlage aus, die Ihrer Datenquelle zugeordnet ist. **Datenzuordnungsvorlage** Dropdown.

      >[!NOTE]
      >
      > Wenn Ihr Administrator benutzerdefinierte Vorlagen konfiguriert hat, werden diese Vorlagen auch in der Dropdown-Liste angezeigt (basierend auf den von Ihrem Administrator durchgeführten Vorlagenpfadkonfigurationen). Sie können beispielsweise eine Themenvorlage erstellen, die eine geordnete Liste, Tabellen, Absätze oder andere DITA-Elemente enthält.

   1. Geben Sie die **Stammknoten**. Dies ist der Knoten, unter dem Sie auf Ihre Daten zugreifen möchten. Der Themengenerator erstellt dann jedes Thema auf der im Stammknoten definierten Ebene. Sie können beispielsweise &quot;issues&quot;als Stammknoten in Jira hinzufügen. Wenn also eine Abfrage 13 Probleme zurückgibt, erhalten Sie 13 Themen, ein Thema für jedes Problem.

   1. Klicks **Abrufen** , um die Daten aus der Datenquelle abzurufen und die Vorlage auf die Daten anzuwenden, die aus der SQL-Abfrage resultieren. Die Vorschau zeigt einen kleinen Bruchteil der Darstellung des Themas im Format der ausgewählten Vorlage. Beispielsweise können Sie ein einzelnes Jira-Problem mit allen Feldern anzeigen, die aus der Abfrage resultieren.
   1. Geben Sie den Namen des Thema-Generators ein.

      >[!NOTE]
      > 
      > Sie müssen die Dateibenennungskonvention für den Namen des neuen Themengenerators befolgen. Im Namen des Thema-Generators darf kein Leerzeichen stehen. Außerdem können Sie keinen neuen Themengenerator mit dem Namen eines vorhandenen Themengenerators speichern. Es tritt ein Fehler auf.

   **Ausgabe-Konfiguration**

   ![](images/topic-generator-output-configuration.png){width="300" align="left"}

   *Geben Sie die Details zum Ausgabepfad und zur Themenbenennungskonvention im Bereich Ausgabekonfiguration ein. Erstellen Sie eine DITA-Zuordnung und benennen Sie sie.*

   1. Geben Sie die **Ausgabepfad** Details, in denen Sie Ihre Themen speichern möchten.
   1. Im **Namenskonvention für Themen** können Sie einen Wert oder eine Variable mit Velocity-Tags eingeben. Die neuen Themen folgen dem Konvent. Sie können beispielsweise die Variable `$key` um Themen zu erstellen, die auf Jira-Schlüsseln basieren.
   1. Aktivieren Sie die Option **Erstellen einer Zuordnung** , wenn Sie eine Zuordnung erstellen möchten, die alle generierten Themen enthält.
   1. Geben Sie den Namen der neuen DITA-Zuordnung ein.

   >[!NOTE]
   >
   > Der Themengenerator generiert die DITA-Zuordnung auf demselben Ausgabepfad wie die Themen.

   **Metadaten**

   Wählen Sie die Metadateneigenschaften aus der Dropdown-Liste aus, um sie an die Themen zu übergeben. **Name** in der Dropdown-Liste werden sowohl die benutzerdefinierten Eigenschaften als auch die Standardeigenschaften aufgeführt.

   Im folgenden Screenshot sehen Sie beispielsweise Folgendes: `dc:description`, `dc:language`, `dc:title`, und `docstate` sind die Standardeigenschaften, für die Sie die Werte definieren können. Sie können eine benutzerdefinierte Eigenschaft wie &quot;author&quot;erstellen und ihren Wert definieren.

   ![](images/topic-generator-metadata.png){width="300" align="left"}

   *Fügen Sie die Metadateneigenschaften im Metadatenbedienfeld hinzu, um sie an die Themen zu übergeben.*

1. Geben Sie den Namen des Generators ein und klicken Sie auf **Speichern** , um die Abfrageergebnisse zu speichern. Der Liste wird ein neuer Themengenerator hinzugefügt.

1. Klicks **Speichern und generieren** , um den Themengenerator zu speichern und neue Themen aus dem Themengenerator zu generieren.



   ![](images/edit-topic-generator.png){width="650" align="left"}

   *Generieren Sie neue Themen aus einem vorhandenen Themengenerator.*

   >[!NOTE]
   >
   > Wenn die Themen bereits vorhanden sind, aktualisiert der Generator die Daten in den vorhandenen Themen.

### Optionen für einen Themengenerator

Klicken Sie mit der rechten Maustaste auf einen Themengenerator, um den **Optionen**. Mithilfe der Optionen können Sie die folgenden Vorgänge ausführen:

- **Erzeugen**: Diese Option generiert die Themen für den ausgewählten Themengenerator. Sie können diese Option auch verwenden, um die vorhandenen Themen zu aktualisieren. Es stellt eine Verbindung zur Datenquelle her und ruft die aktualisierten Daten ab. Beim Generieren des Inhalts ist diese Option deaktiviert und Sie sehen einen Lader.
  >[!NOTE]
  >
  >Wenn Ihr Thema bereits vorhanden ist, können Sie die Daten im Thema überschreiben oder als neue Version speichern.

  ![](images/generate-topic-options.png)

  *Erstellen Sie ein Thema. Wenn die Datei bereits vorhanden ist, speichern Sie es als neue Version oder überschreiben Sie es.*
- **Protokoll anzeigen**: Wählen Sie diese Option, um die Protokolldatei zur Inhaltserstellung anzuzeigen. Die Protokolldatei wird in einer neuen Registerkarte geöffnet. Sie können die Fehler, Warnungen, Informationsmeldungen und Ausnahmen in der Protokolldatei anzeigen. Diese Option ist aktiviert, wenn Sie den Inhalt für den ausgewählten Themengenerator generiert haben.

- **Vorschau**: Verwenden Sie diese Option, um einen Bereich zu öffnen und einen kleinen Teil der Anzeige der Daten in der Ausgabe anzuzeigen.



- **Bearbeiten**: Verwenden Sie diese Option, um den Themengenerator zu ändern und zu speichern. Diese Option ist während der Inhaltserstellung deaktiviert.
- **Löschen**: Mit dieser Option können Sie den ausgewählten Themengenerator löschen. Diese Option ist während der Inhaltserstellung deaktiviert.
- **Duplizieren**: Diese Option erstellt ein Duplikat oder eine Kopie des ausgewählten Thema-Generators. Das Duplikat wird mit einem Suffix erstellt (wie `topic-sample_1`).



## Verwenden von Velocity-Tools in Datenquellenvorlagen {#use-velocity-tools}

Experience Manager-Vorlagen unterstützen auch die Velocity-Tools (Version 2.0). Mit diesen Tools können Sie verschiedene Funktionen auf die Daten anwenden, die Sie aus den Datenquellen abrufen. Erfahren Sie mehr über die Verwendung des [Velocity-Tools](https://velocity.apache.org/tools/2.0/generic.html) und die Funktionen, die Sie anwenden können.

Führen Sie die folgenden Schritte aus, um ein Velocity-Tool in einer Vorlage zu verwenden:
1. Bearbeiten Sie eine Velocity-Vorlage im Web-Editor.
1. Fügen Sie ein Tool und dessen Funktion in der `<tool.function>` Format. Zum Beispiel:
   - Verwenden Sie zum Generieren einer zufälligen Nummer mit dem Mathematik-Tool `$mathTool.random`.
   - Verwenden Sie zum Generieren der Summe der Zahlen mit dem mathematischen Werkzeug `$mathTool.add(num1, num2)`.
1. Verwenden Sie die Vorlage, um einen Inhaltsausschnitt oder ein Thema zu erstellen.
1. Nachdem Sie die Vorlage auf die Daten angewendet haben, können Sie die Daten in der Vorschau oder in der DITA-Quellansicht anzeigen.




Sie können die folgenden Tools in den Velocity-Vorlagen verwenden, um verschiedene Funktionen auf die Daten anzuwenden, die Sie aus dem Connector abrufen: -`$alternatorTool`
- `$classTool`
- `$contextTool`
- `$conversionTool`
- `$dateTool`
- `$comparisonDateTool`
- `$displayTool`
- `$escapeTool`
- `$fieldTool`
- `$loopTool`
- `$linkTool`
- `$listTool`
- `$mathTool`
- `$numberTool`
- `$renderTool`
- `$resourceTool`
- `$sortTool`
