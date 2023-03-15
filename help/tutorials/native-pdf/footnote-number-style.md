---
title: Native PDF-Veröffentlichungsfunktion | Verwenden benutzerdefinierter Stile in Fußnoten
description: Erfahren Sie, wie Sie Stile auf die Zahlen in Fußnoten anwenden.
source-git-commit: ef562c43f5b70d3fe425427108ad8277e1456f24
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Verwenden benutzerdefinierter Stile in Fußnoten

Fußnoten sind Notizen, die am unteren Rand einer Seite platziert werden, auf der ein Verweis für einen bestimmten Teil des Textes kommentiert oder zitiert wird.

Sie können die Zahlen im Fußnotenaufruf im Themeninhalt und die Fußnotenmarkierung unten auf der Seite formatieren. Sie können beispielsweise Klammern um die Zahl setzen oder deren Farbe ändern. Mithilfe dieser Stile können Sie die Fußnoten im Dokument leicht identifizieren.

```css
...
.footnote::footnote-call { 
content: "(" counter(footnote, decimal) ")"; 
} 

.footnote::footnote-marker { 
content: "(" counter(footnote, decimal) ")"; 
} 

...
```

Im vorliegenden Beispiel wird eine Klammer vor und nach dem Fußnotenaufruf und der -Markierung hinzugefügt:

* Fügen Sie das Präfix &quot;(&quot;und das Suffix &quot;)&quot;mithilfe des Inhaltsattributs im `footnote-call` -Stil verwenden, um die Klammern um die Fußnotennummer im Themeninhalt hinzuzufügen.
* Fügen Sie das Präfix &quot;(&quot;und das Suffix &quot;)&quot;mithilfe des Inhaltsattributs im `footnote-marker` -Stil verwenden, um die Klammern um die Fußnotennummer am unteren Rand der Seite hinzuzufügen.

<img src="./assets/pdf-output-footer-numbers.png" alt="Fußzeile in PDF-Ausgabe" width="500">
