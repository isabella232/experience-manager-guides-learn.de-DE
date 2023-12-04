---
title: Ausschluss von Absätzen innerhalb eines Themas aus der Übersetzung
description: So schließen Sie Absätze innerhalb eines Themas aus der Übersetzung aus
feature: Translation
role: User
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# So schließen Sie Absätze innerhalb eines Themas aus der Übersetzung aus

Am einfachsten ist es, das Attribut translation=no zu verwenden.

+ Autoren können das zusätzliche Attribut als **translation=no** zu den Absätzen, die sie nicht übersetzen möchten. Der Übersetzungsanbieter muss informiert werden und er kann am Ende eine Konfiguration vornehmen, um den Text mit diesem Attribut zu ignorieren.
+ Die maschinelle OOTB-Übersetzung (mit Microsoft Translation Connector zum Testen) weist das gleiche Verhalten auf.
+ Testen mit Microsoft-Übersetzung : Wenn Sie **translate=no** auf Absatzebene zuordnen, wird der vollständige Absatz nicht übersetzt. Dieses Attribut kann für jedes Element definiert werden und der Inhalt innerhalb dieses Elements wird nicht übersetzt.


Im Folgenden finden Sie einige Screenshots, die dies weiter erklären:

**Quellinhalt**

![Quellinhalt](assets/source-content.jpg)

**Übersetzter Inhalt auf Spanisch**

![Übersetzter Inhalt auf Spanisch](assets/trans-content.jpg)
