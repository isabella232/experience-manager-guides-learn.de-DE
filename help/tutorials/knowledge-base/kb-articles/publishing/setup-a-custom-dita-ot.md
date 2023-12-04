---
title: Einrichten von benutzerdefiniertem DITA-OT in [!DNL AEM Guides]
description: Erfahren Sie, wie Sie benutzerdefinierte DITA-OT in [!DNL Adobe Experience Manager Guides]
role: Admin
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Einrichten von benutzerdefiniertem DITA-OT in [!DNL AEM Guides] für AEM

Die Schritte zum Hinzufügen eines benutzerdefinierten DITA-OT werden im Abschnitt beschrieben _Verwenden benutzerdefinierter DITA-OT-Plug-ins_ des _Handbuch zur Installation und Konfiguration_.

Auf hoher Ebene sind die Schritte:

+ Grundlegendes DITA-OT abrufen
   + Wenn Sie eine Kopie von vordefiniertem DITA-OT von erhalten möchten [!DNL AEM Guides], laden Sie es aus dem Pfad herunter `/etc/fmdita/dita_resources/DITA-OT.zip`
   + Wenn Sie eine andere Version erhalten möchten, können Sie sie hier herunterladen: [dita-ot repo](https://www.dita-ot.org/download)
+ Nehmen Sie Änderungen in DITA-OT vor, wie [Hinzufügen eines neuen Plug-ins](https://www.dita-ot.org/dev/topics/plugins-installing.html)oder Anpassung vorhandener Plug-ins (siehe Beispiel im Abschnitt zu verwandten Links unten)
+ Hochladen `DITA-OT.zip` empfangen von `/apps/<project-folder>/dita_resources` (Es wird empfohlen, einen benutzerdefinierten Projektordner zu erstellen.)
+ Hinzufügen eines DITA-Profils durch **[!UICONTROL Instrumente]** > **[!UICONTROL Handbücher]** > **[!UICONTROL DITA-Profile]** (Verwenden Sie den DITA-OT-Pfad, in den das benutzerdefinierte DITA-OT hochgeladen wird, siehe Screenshot unten).
  ![DITA-Profile](assets/dita-profile.png)

>[!MORELIKETHIS]
>
>+ [DITA-OT-Plug-in-Beispiele anpassen](https://www.dita-ot.org/dev/topics/pdf-customization.html)
