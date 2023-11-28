---
sidebar_position: 2
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# Rendering-Widgets

Ein Widget kann gerendert werden, indem es mithilfe seiner `id`

So rendern Sie das Widget `widget_languages` überall in der App können wir die einfache Syntax verwenden:

```json
{
    "component": "widget",
    "id": "widget_languages"
}
```

Widgets können auch zum Rendern komplexer Elemente verwendet werden, z. B. zum Rendern der Liste der Mitwirkenden für jede Datei.
Hier kann das Widget wie folgt erstellt werden:

```js title="fileContributorsWidget.js"
const widgetJSON =  {
    component: "div", 
    id: "file_contributors", 
    items: [ // adding components to the widget
        {
            component: "div",
            items: [
                {
                    component: "icon",
                    icon: "file"
                },
                {
                    component: "label",
                    label: "@fileName"
                }
            ]
        },
        {
            component: "list",
            data: "@contributors",
            itemConfig: {
                component: "label"
            }
        }
    ]
},
```

Um nun eine Liste der Beitragenden für jede Datei zu rendern, schreiben wir die Liste wie folgt:

```js title="fileContributorsList.js"
const listJSON = {
    component: "list"
    data: "@files"
    itemConfig: {
        component: "widget",
        id: "file_contributors"
    }
}
```

Hier `@files` ist eine Liste von Dateiobjekten mit Feldern

```typescript
- fileName: string
- contributors: Array<String>
```
