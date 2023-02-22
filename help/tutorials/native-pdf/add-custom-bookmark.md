---
title: Native PDF-Veröffentlichungsfunktion | Hinzufügen eines benutzerdefinierten Lesezeichens in der PDF-Ausgabe
description: Erfahren Sie, wie Sie Stile für Ihren Inhalt erstellen und Stile erstellen.
source-git-commit: fb7ffbaefcdca4302e43d8369bc056c1f08a3ed6
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Hinzufügen eines benutzerdefinierten Lesezeichens in der PDF-Ausgabe

Im Allgemeinen wird das Inhaltsverzeichnis in einer DITA-Zuordnung als Lesezeichen in der endgültigen PDF-Ausgabe repliziert. Dieses Inhaltsverzeichnis wird aus den Themen- oder Abschnittstiteln in Ihrer DITA-Zuordnung erstellt. Sie können in der PDF-Ausgabe gelegentlich ein benutzerdefiniertes Lesezeichen zu einem bestimmten Inhalt hinzufügen, um die Navigation zu erleichtern. Dies kann durch Hinzufügen eines `outputclass` -Attribut auf das Element ein und wenden das folgende Attribut darauf an:

`bookmark-level: 3`

Hier wird die `bookmark-level` ist ein Attribut und eine Zahl `3` ist der Wert, der die Ebene in der Lesezeichenhierarchie angibt, auf der das Lesezeichen hinzugefügt wird. Im folgenden Beispiel enthält das erste Thema &quot;Kontakte&quot;eine Tabelle &quot;Kontaktliste&quot;, zu der wir eine `outputclass` -Attribut mit dem Wert von `custom-bookmark`.


<img src="./assets/custom-bookmark-attribute.png" width="500">

Die folgende Definition der `custom-bookmark` -Klasse wird in der CSS-Datei hinzugefügt:

```css
…
/*Adding a custom bookmark*/
.custom-bookmark{
    bookmark-level: 2
}
…
```

In der PDF-Ausgabe wird die *Kontaktliste* -Tabelle wird auf der zweiten Ebene in der PDF-Lesezeichenliste hinzugefügt, wie unten dargestellt:

<img src="./assets/custom-bookmark-in-pdf-output.png" width="500">

>[!NOTE]
>
>Sie müssen die richtige Ebene auswählen, auf der das benutzerdefinierte Lesezeichen hinzugefügt wird. Wenn Sie eine Zahl angeben, die kleiner als das Lesezeichen des übergeordneten Themas ist, nimmt das benutzerdefinierte Lesezeichen die Position des übergeordneten Lesezeichens an, und alle anderen Lesezeichen werden als untergeordnete Elemente angezeigt. Dies kann zu einer unerwarteten Lesezeichenstruktur führen.

