---
sidebar_position: 3
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Anpassen der App

Unsere App folgt einer MVC-Struktur (Modell, Ansicht, Controller)

## Modell

Das Modell definiert die verschiedenen Attribute und speichert deren Werte. Auf die Werte der verschiedenen im Modell gespeicherten Attribute kann vom Controller mithilfe der Syntax zugegriffen werden

```typescript
this.model.attributeName
```

Zur Anpassung in der App werden alle neu erstellten Attribute unter einer Zuordnung im Modell hinzugefügt.
Um ein neues Attribut im Modell festzulegen, verwenden wir die folgende Syntax im Controller:

```typescript
this.model.extraProps.set("key", value)
```

Um auf ein Attribut zuzugreifen, das dem Modell hinzugefügt wurde, verwenden wir die folgende Syntax:

```typescript
const value = this.model.extraProps.get("key")
```

## Anzeigen

Die Ansicht definiert die Benutzeroberfläche der App. Wir verwenden JSON-Dateien, um die Ansicht unserer Dateien zu definieren. In unserem Beispiel definieren wir die Komponenten, den CSS (wie in der Extraklasse der Komponenten angegeben) und rendern die im Modell gespeicherten Werte.
In unserer App wird jede Ansicht mithilfe einer JSON definiert. Auf die JSONs wird anhand ihrer eindeutigen IDs verwiesen, die als `id`.

## Controller

Der Controller wird verwendet, um Ereignisse zu verarbeiten und die Daten zu verarbeiten. Der Controller wird verwendet, um Daten vom Server abzurufen und zu senden. Es ist die Schnittstelle zwischen dem, was auf der Benutzeroberfläche angezeigt und im Backend gespeichert wird.

- Zum Festlegen von Werten bei der Initialisierung verwenden wir die `init` -Funktion.
- Um eine Methode zum Controller hinzuzufügen, verwenden wir die folgende Syntax:

```typescript
methodName: function(args){
    // functionality
}
```

Die `methodName` dient hier als `key` , um auf die Methode in der JSON-Datei (Ansicht) oder in anderen Funktionen zu verweisen

- Um eine Methode im Controller aufzurufen, verwenden wir die Syntax

```typescript
this.next('methodName', args)
```

## Beispiel

Verwenden wir nun ein einfaches Beispiel, um zu zeigen, wie diese drei Komponenten miteinander interagieren.
Wir fügen eine Schaltfläche hinzu, mit der der Beschriftungswert eines Klicks geändert wird.

### Beispiel anzeigen

Unten definieren wir die JSON für eine Schaltfläche, die einen dynamischen Text anzeigt, der im Modell unter dem Variablennamen gespeichert ist. `buttonLabel`.
In diesem Beispiel ändert sich der Titel der Schaltfläche.

```JSON
{
    "component": "button",
    "label": "@extraProps.buttonLabel",
    "variant": "cta",
    "on-click": "switchButtonLabel",
}
```

### Modellbeispiel

in diesem Fall `extraProps.buttonLabel` enthält den Titel der Schaltfläche

### Controller-Beispiel

```typescript
  controller: {
    init: function () {
      this.model.extraProps.set("buttonLabel", "Submit")
    },

    switchButtonLabel(){
        const buttonLabel = this.model.extraProps.get("buttonLabel") === "Submit"? "Cancel" : "Submit"
        this.model.extraProps.set("buttonLabel", buttonLabel)
    }
  }
```

Unter GIF wird der oben stehende Code in Aktion angezeigt.
![basic_customization](imgs/basic_customisation.gif "Schaltfläche &quot;Grundlegende Anpassung&quot;")
