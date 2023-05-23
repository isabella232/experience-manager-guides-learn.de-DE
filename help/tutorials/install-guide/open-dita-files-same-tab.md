---
title: DITA-Themen- oder Zuordnungsdateien auf derselben Registerkarte öffnen
description: Erfahren Sie, wie Sie DITA-Themen oder -Zuordnungsdateien auf derselben Registerkarte öffnen
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# DITA-Themen- oder Zuordnungsdateien auf derselben Registerkarte öffnen {#id223HI0P202H}

Wenn Sie in einigen Workflows auf einen Link eines Themas oder einer Zuordnungsdatei klicken, wird dieser in einer neuen Registerkarte geöffnet. Dies kann dazu führen, dass in Ihrem Browser viele Tabs geöffnet werden, was sich auf Ihre Produktivität auswirken könnte. Sie können dieses Verhalten beim Öffnen einer Themen- oder Zuordnungsdatei in einer neuen Registerkarte ändern und das Öffnen auf der aktuellen Registerkarte erzwingen. Führen Sie dazu die folgenden Konfigurationsänderungen durch:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** Bundle.

1. Wählen Sie die **DITA-Thema/Karte auf derselben Registerkarte öffnen** -Option.

1. Klicken Sie auf **Speichern**.


Diese Einstellung wirkt sich auf die folgenden Stellen aus, an denen Sie auf die Themen- oder Zuordnungsdateien zugreifen können:

- DITA-Thema erstellen \(am Ende des Workflows, wenn Sie auf das **Thema öffnen** button\)

- DITA-Map erstellen \(am Ende des Workflows, wenn Sie auf die **Open Map** button\)

- Registerkarte &quot;Themen&quot;in der DITA-Map-Konsole

- Registerkarte &quot;Grundlinien&quot;in der DITA-Map-Konsole

- Registerkarte &quot;Berichte&quot;in der DITA-Map-Konsole


**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)

