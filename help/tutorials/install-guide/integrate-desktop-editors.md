---
title: Integrieren von Desktop-basierten XML-Editoren
description: Erfahren Sie, wie Sie Desktop-basierte XML-Editoren integrieren.
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Integrieren von Desktop-basierten XML-Editoren {#id181GB01G0HS}

Es gibt viele XML-Editoren, die auf dem Markt verfügbar sind, und Sie könnten bereits einen verwenden. Adobe FrameMaker ist einer der leistungsfähigsten XML-Editoren, die mit AEM Connector geliefert werden. Mithilfe des AEM-Connectors in FrameMaker können Sie einfach eine Verbindung zum AEM-Repository herstellen, Dateien auschecken und einchecken und Dateien direkt in FrameMaker bearbeiten. Sie können auch AEM Handbücher konfigurieren, um FrameMaker über den Web-Editor zu starten. Nachdem Sie die Datei in FrameMaker geöffnet haben, können Sie sie bearbeiten und wieder in das AEM Repository einchecken.

## Aktivieren Sie die Dateibearbeitung in FrameMaker über den Web-Editor

Sie können FrameMaker oder einen anderen DITA-Editor verwenden, um DITA-Inhalte zu erstellen und zu aktualisieren. Wenn Ihr Unternehmen jedoch FrameMaker als DITA-Editor verwendet, können Sie Ihren Benutzern die Möglichkeit geben, DITA-Dokumente direkt in FrameMaker von AEM aus zu öffnen.

Standardmäßig wird Ihren Benutzern die Variable **Öffnen in FrameMaker** in der AEM Symbolleiste. Führen Sie die folgenden Schritte aus, um diese Schaltfläche in der AEM-Symbolleiste hinzuzufügen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** Bundle.

   ![](assets/open-in-fm-toolbar.png){width="550" align="left"}

1. Wählen Sie die **Öffnen in FrameMaker-Schaltfläche anzeigen** -Option.

1. Klicken Sie auf **Speichern**.


Wenn Sie die **Öffnen in FrameMaker-Schaltfläche anzeigen** -Option, dann die **Öffnen in FrameMaker** bei Auswahl einer DITA-Datei im AEM Repository angezeigt. Wenn diese Option *nicht aktiviert*, die **Öffnen in FrameMaker** -Schaltfläche wird nur angezeigt, wenn Sie eine FM- oder eine .book-Datei im Repository auswählen.

