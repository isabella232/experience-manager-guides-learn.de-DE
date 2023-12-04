---
title: Filter für Dialogfeld "Dateisuche"konfigurieren
description: Erfahren Sie, wie Sie Filter für das Dialogfeld zum Durchsuchen von Dateien konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Filter für Dialogfeld &quot;Dateisuche&quot;konfigurieren {#id20CIL7009GN}

Bei der Arbeit im Web Editor müssen Sie das Dialogfeld zum Durchsuchen von Dateien verwenden, um Elemente wie Bilder, Verweise oder wichtige Verweise einzufügen. Das Standarddialogfeld zum Durchsuchen von Dateien bietet keine Filteroption für Dateien. Sie können eigene Filter hinzufügen, mit denen Sie schnell und einfach auf die gewünschten Dateien zugreifen können.

Führen Sie die folgenden Schritte aus, um Ihre benutzerdefinierten Dateifilteroptionen zum Dialogfeld &quot;Dateisuche&quot;hinzuzufügen:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zur Standardkonfigurationsdatei, die unter folgendem Speicherort verfügbar ist:

   `/libs/fmdita/clientlibs/clientlibs/xmleditor/ui_config.json`

1. Erstellen Sie eine Kopie der Standardkonfigurationsdatei an folgendem Speicherort:

   `/apps/fmdita/xmleditor/ui_config.json`

1. Navigieren Sie zu und öffnen Sie die `ui_config.json` in der Datei `apps` Knoten zur Bearbeitung.

1. Im `ui_config.json` -Datei, fügen Sie die Definition der Filter hinzu, die Sie hinzufügen möchten.

   Das folgende Codefragment zeigt, wie zwei Filteroptionen hinzugefügt werden: DITA-Dateien und Bilddateien.

   ```json
   "browseFilters": [
       {
         "title": "DITA Files",
         "property": "jcr:content/metadata/dita_class",
         "operation": "exists"
       },
       {
         "title": "Image Files",
         "property": "jcr:content/metadata/dc:format",
         "value": [        
           "image/jpeg",
           "image/gif",
           "image/png"
         ]
       }
   ]
   ```

   Im obigen Codefragment ist der erste Filter für DITA-Dateien. Die Filterdefinition akzeptiert die folgenden Parameter:

   - **title:**   Der Anzeigename des Filters. Dieser Titel wird als Filteroption im Dialogfeld zum Durchsuchen von Dateien angezeigt.

   - **Eigenschaft:**   Die Eigenschaft, die in den Metadaten der Datei übereinstimmen soll. So lassen Sie beispielsweise nur die Dateien zu, bei denen die `dita_class` Metadaten in ihrer Eigenschaft verwendet der Eigenschaftsfilter &quot;`jcr:content/metadata/dita_class`&quot; als Wert.

   - **-Vorgang:**   Geben Sie &quot;`exists`&quot;, um für das Vorhandensein des im Eigenschaftsparameter angegebenen Werts zu stimmen.

   Der zweite Filter ist für Bilddateien vorgesehen. Die Parameter ähneln dem ersten Filter mit Ausnahme der `value` -Parameter. Die `value` -Parameter verwendet ein Array von Bildtypen als Wert. Alle im Parameter value angegebenen Dateitypen werden gesucht und im Dialogfeld zum Durchsuchen von Dateien angezeigt. Alle anderen Dateitypen werden ignoriert.

1. Speichern Sie die *ui\_config.json* und laden Sie den Web Editor neu.

   Wenn Sie das Dialogfeld zum Durchsuchen der Datei starten, werden die in der Datei ui\_config.json konfigurierten Filteroptionen angezeigt.

   ![](assets/file-browse-custom-filters.png){width="300" align="left"}
