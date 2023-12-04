---
title: Native PDF-Veröffentlichungsfunktion | Arbeiten mit benutzerdefinierten Änderungsbalkenstilen
description: Erfahren Sie, wie Sie Stile auf Änderungsleisten anwenden.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Arbeiten mit benutzerdefinierten Änderungsbalkenstilen

Ein Änderungsbalken ist eine vertikale Linie, die neue oder überarbeitete Inhalte visuell identifiziert. In AEM Guides können Sie eine Änderungsleiste links neben dem geänderten Inhalt in den Themen und auch die geänderten Themen im Inhaltsverzeichnis der PDF-Ausgabe anzeigen.

Weitere Informationen zum Anzeigen der Änderungsleiste finden Sie unter *PDF mit Änderungsleiste zwischen veröffentlichten Versionen erstellen* Einstellung in [PDF-Ausgabe veröffentlichen](../web-editor/native-pdf-web-editor.md).

## Inhalt innerhalb von Themen geändert

Die Änderungsleiste wird links neben dem Inhalt in den Themen angezeigt, die eingefügt, geändert oder gelöscht wurden.

Sie können die folgenden Stile ändern, um den geänderten Inhalt und darunter mit den Änderungsleisten anzuzeigen.


>[!NOTE]
>
>Diese Stile sind Teil von `layout.css` und Sie können sie nach Bedarf bearbeiten.

Beispielsweise können Sie das Farbattribut im `.inserted-block` Stil , um festzulegen, wie der eingefügte Inhalt in der veröffentlichten PDF-Ausgabe angezeigt wird.


```css
...
.inserted-block { 
  color: #2ECC40; 
  display: inline; 
  -ro-comment-content: " "; 
  -ro-comment-style: underline; 
  -ro-comment-title: "Inserted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Auf ähnliche Weise können Sie die `.deleted-block` Stil , um festzulegen, wie der gelöschte Inhalt in der veröffentlichten PDF-Ausgabe angezeigt wird.

```css
...
.deleted-block { 
  display: inline; 
  color: #FF6961; 
  text-decoration: line-through; 
  -ro-comment-content: " "; 
  -ro-comment-style: strikeout; 
  -ro-comment-title: "Deleted"; 
  -ro-comment-date: attr(data-time); 
  -ro-comment-dateformat: "yyyy/dd/MM HH:mm:ss"; 
} 
...
```

Sie können `.inserted-change-bar` und `.deleted-change-bar` -Stil, um das Erscheinungsbild der Änderungsbalken zu ändern, die links neben dem aktualisierten Inhalt angezeigt werden.

Sie können beispielsweise `-ro-change-bar-color` -Attribut in `.inserted-change-bar` Stil, um die eingefügte Änderungsleiste in grüner Farbe anzuzeigen. Sie können auch `-ro-change-bar-color` -Attribut in `.deleted-change-bar` Stil, um die gelöschte Änderungsleiste in roter Farbe anzuzeigen.

```css
...
.inserted-change-bar { 
  -ro-change-bar-color: #2ECC40; 
} 

.deleted-change-bar { 
  -ro-change-bar-color: #FF6961; 
  } 
...
```

<img src="./assets/changed-bar-content.png" alt="Geänderter Inhalt des Balkendiagramms" width="500">

## Geändertes Thema im Inhaltsverzeichnis (Inhaltsverzeichnis)

Sie können auch eine Änderungsleiste links von den geänderten Themen im Inhaltsverzeichnis der PDF-Ausgabe hinzufügen. Sie können `-ro-change-bar-color` -Attribut im `.changed-topic` Stil , um eine Änderungsleiste in der Farbe Ihrer Wahl für die aktualisierten Themen in der Liste &quot;Inhaltsverzeichnis&quot;hinzuzufügen.

Sie können beispielsweise einen Änderungsbalken mit grüner Farbe hinzufügen.

```css
...
.changed-topic { 
 -ro-change-bar-color: #2ECC40; 
}  
...
```


Dies zeigt eine grüne Änderungsleiste für alle Themen im Inhaltsverzeichnis, an denen einige Änderungen vorgenommen wurden. Sie können auf das geänderte Thema im Inhaltsverzeichnis klicken und die detaillierten Änderungen anzeigen.

<img src="./assets/changed-bar-TOC.png" alt="Inhaltsverzeichnis der geänderten Leiste" width="500">
