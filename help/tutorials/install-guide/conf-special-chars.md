---
title: Zulässige Sonderzeichen konfigurieren
description: Erfahren Sie, wie Sie zulässige Sonderzeichen konfigurieren
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Zulässige Sonderzeichen konfigurieren {#id20CIL600035}

Mit dem Web Editor können Sie einige Sonderzeichen direkt einfügen. Sie können jedoch die Liste der Sonderzeichen anpassen, die Ihre Autoren in ihre Dokumente einfügen können. Wenn Sie die Liste der Sonderzeichen anpassen, wird der Standardsatz der Sonderzeichen überschrieben. Den Autoren werden nur die Sonderzeichen zur Verfügung gestellt, die Sie in Ihrer Konfiguration hinzufügen.

Führen Sie die folgenden Schritte aus, um die Standardliste mit Sonderzeichen zu überschreiben:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. erstellen `symbols.json` Datei am folgenden Speicherort:

   ```json
   /apps/fmdita/xmleditor/
   ```

1. Fügen Sie die Definition von Sonderzeichen im `symbols.json` Datei als:

   ```json
   {"symbols": [{"label": "Arrows",
      "items": [
      {   "name": "←",   "title": "Left Arrow"   } 
      ,   
      {   "name": "↑",   "title": "Up Arrow"      } 
      ]   
      }   ]   }
   ```


Die Struktur der `symbols.json` -Datei wird nachfolgend erläutert:

- `"label": "Arrows"`: Gibt die Kategorie für die Sonderzeichen an. Im Snippet eine Kategorie mit dem Namen `"Arrows"` definiert ist.
- `"items"`: Dadurch wird die Sammlung von Sonderzeichen in der Kategorie definiert.
- `"name": "←", "title": "Left Arrow"`: Dies ist die Definition des Sonderzeichens. Sie beginnt mit dem `"name"` -Beschriftung, die nicht geändert werden darf. Dem Namen folgt das Sonderzeichen. Die `"title"` ist der Name oder Titel des Sonderzeichens, das als QuickInfo für dieses Sonderzeichen angezeigt wird.

   Sie können mehrere Definitionen von Sonderzeichen innerhalb einer Kategorie definieren.


**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)

