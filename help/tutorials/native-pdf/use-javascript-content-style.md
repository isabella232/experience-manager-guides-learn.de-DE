---
title: Native PDF-Veröffentlichungsfunktion | Verwenden von JavaScript zum Arbeiten mit Inhalt oder Stil
description: Erfahren Sie, wie Sie Stile für Ihren Inhalt erstellen und Stile erstellen.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---

# Verwenden von JavaScript zum Arbeiten mit Inhalt oder Stil

Mit der nativen PDF-Veröffentlichungsfunktion können Sie JavaScript ausführen, um Inhalte oder Stile zu bearbeiten, die auf Inhalte angewendet werden, bevor die endgültige PDF generiert wird. Diese Funktion gibt Ihnen die vollständige Kontrolle darüber, wie Ihre endgültige Ausgabe generiert wird. Beispielsweise können Sie der PDF-Ausgabe, die sich in einer anderen PDF befindet, rechtliche Hinweise hinzufügen. Mit JavaScript können Sie die rechtlichen Hinweise hinzufügen, sobald die PDF für den Basisinhalt erstellt wurde, aber bevor die endgültige PDF generiert wird.\
Um die Ausführung von JavaScript zu unterstützen, bietet Ihnen die Funktion Native PDF Publishing die folgenden Callback-Funktionen:

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Diese Rückruffunktion wird ausgeführt, bevor das Inhaltsverzeichnis generiert wird.
* `window.pdfLayout.onBeforePagination(callback)`: Diese Rückruffunktion wird ausgeführt, nachdem das Inhaltsverzeichnis generiert wurde, aber bevor Seitenumbrüche in der PDF hinzugefügt werden.
* `window.pdfLayout.onAfterPagination(callback)`: Diese Rückruffunktion wird ausgeführt, nachdem das Inhaltsverzeichnis und die Seitenumbrüche im PDF hinzugefügt wurden.

>[!NOTE]
>
>Intern wird eine Ausführungssequenz für diese Aufruffunktionen beibehalten. Zunächst wird onBeforeCreateTOC, dann onBeforePagination und schließlich onAfterPagination ausgeführt.

Je nach Art der Inhalts- oder Stiländerung, die Sie durchführen möchten, können Sie auswählen, welche Callback-Funktion verwendet werden soll. Wenn Sie beispielsweise Inhalte hinzufügen möchten, wird empfohlen, dies vor der Erstellung des Inhaltsverzeichnisses durchzuführen. Wenn Sie Stilaktualisierungen vornehmen möchten, können diese entweder vor oder nach der Paginierung durchgeführt werden.

Im folgenden Beispiel wird die Position der Titel der Abbildung von über den Bildern in unterhalb der Bilder geändert. Dazu müssen Sie die JavaScript-Ausführungsoption in der Vorgabe aktivieren. Führen Sie dazu die folgenden Schritte aus:

1. Öffnen Sie die Vorgabe zur Bearbeitung.
1. Navigieren Sie zu **Erweitert** Registerkarte.
1. Wählen Sie die **JavaScript aktivieren** -Option.
1. Speichern und schließen Sie die Vorgabe.

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

## Hinzufügen eines Wasserzeichens zur PDF-Ausgabe für Entwurfsdokumente {#watermark-draft-document}

Sie können auch JavaScript verwenden, um bedingte Wasserzeichen hinzuzufügen. Diese Wasserzeichen werden Ihrem Dokument hinzugefügt, wenn die definierte Bedingung erfüllt ist.\
Sie können beispielsweise eine JavaScript-Datei mit folgendem Code erstellen, um ein Wasserzeichen für die PDF-Ausgabe des Dokuments zu erstellen, das noch nicht genehmigt wurde. Dieses Wasserzeichen wird nicht angezeigt, wenn Sie die PDF für das Dokument im Dokumentstatus &quot;Genehmigt&quot;generieren.

```css
...
/*
* This file can be used to add a watermark to the PDF output
* */

window.addEventListener('DOMContentLoaded', function () {
    var watermark = 'Draft'
    var metaTag = document.getElementsByTagName('meta')
    css = "@page {\n  @left-middle {\n    content: \"".concat(watermark, "\";\n    z-index: 100;\n    font-family: sans-serif;\n    font-size: 80pt;\n    font-weight: bold;\n    color: gray(0, 0.3);\n    text-align: center;\n    transform: rotate(-54.7deg);\n    position: absolute;\n    left: 0;\n    top: 0;\n    width: 100%;\n    height: 100%;\n  }\n}")
    head = document.head || document.getElementsByTagName('head')[0], style = document.createElement('style');
    style.appendChild(document.createTextNode(css));
    window.pdfLayout.onBeforePagination(function () {
        for (let i = 0; i < metaTag.length; i++) {
            if (metaTag[i].getAttribute('name') === 'docstate' && metaTag[i].getAttribute('value') !== 'Approved') {
                head.appendChild(style);
            }
        }
    })
});
...
```

Die mit diesem Code generierte PDF-Ausgabe zeigt ein Wasserzeichen an *Entwurf* auf der Titelseite Ihres Dokuments:

<img src="./assets/draft-watermark.png" width="500">
