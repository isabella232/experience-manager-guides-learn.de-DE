---
sidebar_position: 4
source-git-commit: 0f20681fa4de859053c8d2baae0e53f347ce5859
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---


# Symbol

Um ein Symbol anzuzeigen, verwenden wir die Komponente, das Symbol .
Die Textbereichskomponente in JUI stellt einen HTML-Code dar `<icon/>`.

Die unter verfügbaren Symbole [Adobe Spectrum-Symbole](https://spectrum.adobe.com/page/icons/) sind mit unserer App kompatibel.

```js title="icon.js"
const iconJSON =  {
    "component": "icon", //tells the component name
    "icon": "info", // name of the icon to be used
    "size": "S", // size of the icon
    "title": "Information" // tooltip corresponding to the icon.
},
```

Schaltflächen können auch Symbole hinzugefügt werden.

Das gerenderte Symbol sieht wie folgt aus:

![icon](./imgs/info_icon.png "Symbol")
