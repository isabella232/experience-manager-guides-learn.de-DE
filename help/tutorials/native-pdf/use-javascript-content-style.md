---
title: Native PDF-Veröffentlichungsfunktion | Verwenden von JavaScript zum Arbeiten mit Inhalt oder Stil
description: Erfahren Sie, wie Sie Stile für Ihren Inhalt erstellen und Stile erstellen.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---


# Verwenden von JavaScript zum Arbeiten mit Inhalt oder Stil

Mit der nativen PDF-Veröffentlichungsfunktion können Sie JavaScript ausführen, um Inhalte oder Stile zu bearbeiten, die auf Inhalte angewendet werden, bevor die endgültige PDF generiert wird. Diese Funktion gibt Ihnen die vollständige Kontrolle darüber, wie Ihre endgültige Ausgabe generiert wird. Beispielsweise können Sie der PDF-Ausgabe, die sich in einer anderen PDF befindet, rechtliche Hinweise hinzufügen. Mit JavaScript können Sie die rechtlichen Hinweise hinzufügen, sobald die PDF für den Basisinhalt erstellt wurde, aber bevor die endgültige PDF generiert wird.\
Um die Ausführung von JavaScript zu unterstützen, bietet Ihnen die Funktion Native PDF Publishing die folgenden Callback-Funktionen:

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Diese Rückruffunktion wird ausgeführt, bevor das Inhaltsverzeichnis generiert wird.
* `window.pdfLayout.onBeforePagination(callback)`: Diese Rückruffunktion wird ausgeführt, nachdem das Inhaltsverzeichnis generiert wurde, aber bevor Seitenumbrüche zum PDF hinzugefügt werden.
* `window.pdfLayout.onAfterPagination(callback)`: Diese Rückruffunktion wird ausgeführt, nachdem das Inhaltsverzeichnis und die Seitenumbrüche im PDF hinzugefügt wurden.

>[!NOTE]
>
>Intern wird eine Ausführungssequenz für diese Aufruffunktionen beibehalten. Zunächst wird onBeforeCreateTOC, dann onBeforePagination und schließlich onAfterPagination ausgeführt.

Je nach Art der Inhalts- oder Stiländerung, die Sie durchführen möchten, können Sie auswählen, welche Callback-Funktion verwendet werden soll. Wenn Sie beispielsweise Inhalte hinzufügen möchten, wird empfohlen, dies vor der Erstellung des Inhaltsverzeichnisses durchzuführen. Wenn Sie Stilaktualisierungen vornehmen möchten, können diese entweder vor oder nach der Paginierung durchgeführt werden.

Im folgenden Beispiel wird die Position der Titel der Abbildung von über den Bildern in unterhalb der Bilder geändert. Dazu müssen Sie die JavaScript-Ausführungsoption in der Vorgabe aktivieren. Führen Sie hierfür die folgenden Schritte aus:

1. Öffnen Sie die Vorgabe zur Bearbeitung.
1. Navigieren Sie zu **Erweitert** Registerkarte.
1. Wählen Sie die **JavaScript aktivieren** -Option.
1. Speichern Sie die Vorgabe und schließen Sie sie.

Erstellen Sie anschließend eine JavaScript-Datei mit dem folgenden Code und speichern Sie sie im Ordner Ressourcen Ihrer Vorlage:

```css
...
/*
* DITA only allows the figure title to be placed above images 
* This JavaScript code is used to move the figure title below the image
* */
window.addEventListener('DOMContentLoaded', function () {
    window.pdfLayout.onBeforeCreateTOC(function() {
        var titleNodes = document.querySelectorAll('.fig > .title')
        for (var i = 0; i < titleNodes.length; i++) {
            var titleNode = titleNodes[i]
            var figNode = titleNode.parentNode
            var imageNode = figNode.querySelector('.image')
            if(imageNode && imageNode.parentNode !== figNode) {
              imageNode = imageNode.parentNode
            }
            if (figNode && imageNode && imageNode.parentNode === figNode) {
                figNode.insertBefore(imageNode, titleNode)
            }
        }
    })
});
...
```

>[!NOTE]
>
>Die `window.addEventListener('DOMContentLoaded', function ()` -Funktion aufgerufen werden, bevor die Callback-Funktionen verwendet werden.

Als Nächstes muss dieses Skript aus einer Vorlagendatei aufgerufen werden, die zum Generieren der PDF-Ausgabe verwendet wird. Für unser Beispiel fügen wir es der TOC-Vorlage hinzu. Stellen Sie sicher, dass `<script>` -Tag innerhalb eines vordefinierten `<div>` -Tag in `<body>` -Tag. Wenn Sie sie in der `<head>` -Tag oder außerhalb von `<body>` -Tag, wird das Skript nicht ausgeführt.

<img src="./assets/js-added-resources-template.png" width="500">

Die mithilfe dieses Codes generierte Ausgabe und die Vorlage zeigt den Titel der Abbildung unter dem Bild an:

<img src="./assets/fig-title-below-image.png" width="500">
