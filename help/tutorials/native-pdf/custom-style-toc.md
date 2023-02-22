---
title: Native PDF-Veröffentlichungsfunktion | Anwenden eines benutzerdefinierten Stils auf Inhaltsverzeichniseinträge und Themeninhalte
description: Erfahren Sie, wie Sie Stile für Ihren Inhalt erstellen und Stile erstellen.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Anwenden eines benutzerdefinierten Stils auf Inhaltsverzeichniseinträge und Themeninhalte

Manchmal können Sie benutzerdefinierte Stile auf die TOC-Einträge oder ein bestimmtes Thema anwenden. Dies kann durch die Verknüpfung eines `outputclass` -Attribut mit dem `<topicref>` -Element in Ihrer DITA-Zuordnung. Wenn Sie ein benutzerdefiniertes Format auf ein ganzes Thema anwenden möchten, kann dies auch durch Erweitern der Stildefinition des Attributs in der CSS erreicht werden.

Nehmen wir ein Beispiel für ein neues Thema, das Sie zur Überprüfung senden möchten. Zur einfachen Identifizierung des aktualisierten Themas müssen Sie eine `outputclass` -Attribut `<topicref>` -Element in Ihrer DITA-Zuordnung ein und definieren Sie dann einen benutzerdefinierten Stil für denselben in der CSS.

Im folgenden Beispiel wird die *Flugverlauf* dem Thema zugewiesen wurde, wurde ein `outputclass` -Attribut mit dem Wert von `new-topic`.

<img src="./assets/new-topic-attribute-in-map.png" width="500">

Die Klassendefinition der `new-topic` in einer CSS können Sie den Stil für die folgenden Elemente definieren:
* Der Haupteintrag im Inhaltsverzeichnis oder im Mini-Inhaltsverzeichnis
* Der Titel des Themas im Hauptinhalt
* Der gesamte Inhalt des Themas, einschließlich des Titels

Sehen wir uns an, wie jedes dieser Szenarien in CSS definiert werden kann. In der folgenden CSS-Definition der `new-topic` -Klasse, wurde die Textfarbe geändert.

```css
…
.new-topic {
  color: #CC5309
}
…
```

Diese Definition steuert die Farbe des Texts im Inhaltsverzeichnis und den Titel des Themas. Die folgende PDF-Ausgabe zeigt die unterschiedliche Farbe, die auf den TOC-Eintrag angewendet wird:

<img src="./assets/pdf-output-toc-entry.jpg" width="500">

Der Titel des Themas wird ebenfalls mit derselben Farbe formatiert.

<img src="./assets/pdf-output-topic-title.jpg" width="500">

Wenn Sie möchten, dass der TOC-Eintrag und der Titel des Themas unterschiedliche Stile aufweisen, können Sie sie wie unten gezeigt separat definieren:

```css
...
/*for styling TOC entry */
.new-topic {
  color: #CC3509
}

/* for styling topic's title */
.new-topic.title {
  color: #092ACC
}
...
```

Schließlich können Sie auch Stile auf den gesamten Inhalt innerhalb des Themas anwenden. Dazu müssen Sie ein Suffix hinzufügen &quot;`-content`&quot; zum Klassennamen. Im folgenden Beispiel wurde eine Änderungsleiste für den gesamten Inhalt des Themas hinzugefügt:

```css
...
/* for styling the topic's content */
.new-topic-content {
  -ro-change-bar-color: #A609CC;
}
...
```

Unter Verwendung der oben genannten Stilattribute wird links neben dem *Flugverlauf* wie unten gezeigt:

<img src="./assets/pdf-output-topic-content.jpg" width="500">


