---
title: Standardmäßig Attribut @navtitle einschließen
description: Erfahren Sie, wie Sie standardmäßig das Attribut @navtitle einschließen.
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---


# Standardmäßig Attribut @navtitle einschließen {#id2115BC0J0XA}

Sie können verschiedene Arten von Referenzdateien zu einer Zuordnung hinzufügen, z. B. Themen-, Referenz-, Aufgaben-, \(Unter-)Maps usw. Die meisten dieser Dateien unterstützen die `@navtitle` -Attribut. Es wird jedoch nicht von vielen Autoren konsistent verwendet. Wenn Sie die Verwendung der `@navtitle` -Attribut in allen referenzierten Dateien in einer Zuordnung verwenden, können Sie dies mit einer einfachen Konfiguration tun.

Nach der Aktivierung erhält jede Referenzdatei, die Sie in einer Zuordnung hinzufügen, automatisch die `@navtitle` -Attribut zu seinen Eigenschaften hinzugefügt. Die `@navtitle` erhält auch den Wert der `title` -Element des referenzierten Inhalts.

Einbeziehen `@navtitle` -Attribut in den Eigenschaften der Referenzdateien standardmäßig festgelegt ist, führen Sie die folgenden Schritte aus:

1. Laden Sie die Datei ui\_config.json herunter.

   Sie können diese Änderung auf globaler Ebene oder auf Ordnerebene vornehmen. Abhängig davon, wo Sie diese Änderung vornehmen möchten, müssen Sie die entsprechende Datei ui\_config.json herunterladen. Weitere Informationen zum Herunterladen der Datei ui\_config.json finden Sie unter [Konfigurieren und Anpassen des XML-Web-Editors](conf-folder-level.md#id2065G300O5Z).

1. Suchen Sie nach `ditaAttributes` Definition.

   Die Standarddefinition von `ditaAttributes` ist:

   ```json
   "ditaAttributes": {
   "attributes": [],
   "constraint": false,
   "required": {}
   },
   ```

1. Ändern Sie die `required` Parameter wie:

   ```json
   "required": {"navtitle": true}
   ```

1. Speichern Sie die Datei.

1. Laden Sie die Datei im entsprechenden Profil hoch \(Global oder Ordner\).


Mit dieser Konfiguration enthält jede Referenzdatei, die Sie einer Zuordnung hinzufügen, die `@navtitle` -Attribut.

