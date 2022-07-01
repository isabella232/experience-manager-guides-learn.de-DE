---
title: Konfigurieren zusätzlicher Sonderzeichen in der Symbolleiste des Web-Editors
description: So konfigurieren Sie zusätzliche Sonderzeichen in der Symbolleiste des Web-Editors
feature: Web Editor
role: User
exl-id: 0fbc05a5-a6b0-4f6b-bbc4-8fca03581d90
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# So konfigurieren Sie zusätzliche Sonderzeichen in der Symbolleiste des Web-Editors

In der Symbolleiste des Web-Editors gibt es eine Option zum Verknüpfen, damit der Autor die Sonderzeichen bereits einfügen kann.
Dasselbe ist im folgenden Screenshot zu sehen:

![Sonderzeichen](assets/special-chars.png)


Diese Liste von Zeichen kann hier konfiguriert werden. Wenn Sie weitere Zeichen hinzufügen müssen, führen Sie die folgenden Schritte aus:

+ Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

+ Erstellen Sie die Datei &quot;symbols.json&quot;am folgenden Speicherort: &#39;/apps/fmdita/xmleditor/&#39; (Sie können die Standardeinstellung aus dem Verzeichnis &#39;/libs/fmdita/clientlibs/clientlibs/xmleditor/symbols.json&#39; kopieren.)

+ Fügen Sie die Sonderzeichendefinition in der Datei symbols.json wie folgt hinzu:

```
{
      "label": "Logical Symbols",
      "items": [
        {
          "name": "≥",
          "title": "Greater-Than or Equal To"
        },
        {
          "name": "≤",
          "title": "Smaller-Than or Equal To"
        }
      ]
}
```

Die Struktur der Datei symbols.json wird nachfolgend beschrieben:

+ &quot;label&quot;: &quot;Logische Symbole&quot;: Gibt die Kategorie für die Sonderzeichen an. Im Snippet wird eine Kategorie mit dem Namen &quot;Logisches Symbol&quot;definiert.

+ &quot;items&quot;: Dadurch wird die Sammlung von Sonderzeichen in der Kategorie definiert.

+ &quot;name&quot;: &quot;≥&quot;, &quot;title&quot;: &quot;Größer oder gleich&quot;: Dies ist die Definition des Sonderzeichens. Sie beginnt mit der Bezeichnung &quot;name&quot;, die nicht geändert werden darf. Dem Namen folgt das Sonderzeichen. Der &quot;Titel&quot;ist der Name oder Titel des Sonderzeichens, das als QuickInfo für dieses Sonderzeichen angezeigt wird.

Sie können mehrere Definitionen von Sonderzeichen innerhalb einer Kategorie definieren.

Dadurch wird im Dialogfeld &quot;Sonderzeichen&quot;eine weitere Kategorie hinzugefügt:

![Symbolkategorie](assets/special-char-category.png)

![Sonderzeichen einfügen](assets/insert-special-char.png)

>[!MORELIKETHIS]
>
>+ [Handbuch zur Installation und Konfiguration](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-6/XML-Documentation-for-Adobe-Experience-Manager_Installation-Configuration-Guide_EN.pdf)

