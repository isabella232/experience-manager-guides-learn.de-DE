---
title: Automatische Dateinamen basierend auf UUID konfigurieren
description: Erfahren Sie, wie Sie automatische Dateinamen basierend auf der UUID konfigurieren.
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---


# Automatische Dateinamen basierend auf UUID konfigurieren {#id205QG070D5Z}

Standardmäßig erhalten Autoren bei der Erstellung einer Themen- oder Zuordnungsdatei die Möglichkeit, auch den Dateinamen anzugeben. Autoren können die Dateinamen gemäß ihren Anforderungen zuweisen. Dies kann jedoch zu Inkonsistenz führen und eine große Bandbreite an Dateinamen kann in einem großen Dokumentationssystem angezeigt werden. Als Administrator können Sie Ihre Autoren daran hindern, Dateinamen für die Dateien zuzuweisen, die sie in Ihrem System erstellen. Für jede neue Themen- oder Zuordnungsdatei können Sie automatisch UUID-basierte Dateinamen zuweisen.

Führen Sie die folgenden Schritte aus, um automatisch den UUID-basierten Dateinamen für alle im System erstellten neuen Dateien zuzuweisen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf *com.adobe.fmdita.xmleditor.config.XmlEditorConfig* Bundle.

1. Wählen Sie die **Verwenden von UUID-basierten Systemdateinamen** -Option.

1. Klicken Sie auf **Speichern**.


>[!NOTE]
>
> Standardmäßig ist diese Option deaktiviert. Wenn diese Option aktiviert ist, sehen Autoren beim Erstellen eines neuen Themas oder einer neuen Zuordnungsdatei nicht die Option, den Dateinamen anzugeben. Eine neue Themen- oder Zuordnungsdatei kann über die Assets-Benutzeroberfläche und den Web-Editor erstellt werden.

**Übergeordnetes Thema:**[ Dateinamen konfigurieren](conf-file-names.md)

