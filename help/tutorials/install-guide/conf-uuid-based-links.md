---
title: Anzeige von UUID-basierten Links konfigurieren
description: Erfahren Sie, wie Sie die Anzeige von UUID-basierten Links konfigurieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Anzeige von UUID-basierten Links konfigurieren {#id2035G20M0QN}

Wenn Sie einen Link mit der Option Verweis einfügen oder Inhalt wiederverwenden im Web-Editor einfügen erstellen, wird der Link standardmäßig mit der UUID des referenzierten Inhalts erstellt. Die **Link** -Eigenschaft \(im Bereich Eigenschaften\) des referenzierten Inhalts kann so konfiguriert werden, dass der relative Dateipfad des referenzierten Inhalts oder der UUID angezeigt wird. Diese Anzeige wird von der **Aktivieren von UUIDs** in der configMgr. Standardmäßig ist sie aktiviert, was bedeutet, dass die UUID des referenzierten Inhalts im Bereich Eigenschaften angezeigt wird.

Führen Sie die folgenden Schritte aus, um den relativen Pfad oder die UUID des referenzierten Inhalts im Web Editor anzuzeigen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** Bundle

1. Im *XmlEditorConfig* -Einstellungen **Aktivieren von UUIDs** ist standardmäßig aktiviert. Dies bedeutet, dass die UUID des referenzierten Inhalts im **Link** -Eigenschaft im Bereich &quot;Eigenschaften&quot;.

   Wenn Sie den relativen Pfad des verknüpften Inhalts anzeigen möchten, deaktivieren Sie die Option **Aktivieren von UUIDs** -Option.

1. Klicken Sie auf **Speichern**.


**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
