---
title: PDF-Generierung für einzelne Themen konfigurieren
description: Erfahren Sie, wie Sie die Erstellung von PDF für einzelne Themen konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# PDF-Generierung für einzelne Themen konfigurieren {#id22ADC70M0XA}

Mit den AEM-Handbüchern können Sie die PDF einzelner Themen oder eine ganze Map-Datei generieren. Sie können Ihre Themen im PDF-Format mithilfe der nativen PDF- oder DITA-OT-Methode veröffentlichen. Verwenden Sie die native PDF-Methode, um eine funktionsreiche PDF-Ausgabe basierend auf W3C CSS3- und CSS-Medienstandards zu generieren. Sie können die DITA-OT-Methode verwenden, um eine PDF-Ausgabe für eine Zuordnung aus dem Map-Dashboard zu generieren.

>[!NOTE]
>
> Native PDF ist die Standardmethode zum Generieren einer PDF in der aktuellen Version von AEM Guides.

So aktivieren Sie die alte PDF-Generierung über DITA-OT im Themenvorschaumodus:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an und laden Sie die Konfigurationsdatei der Benutzeroberfläche herunter.

1. Klicken Sie dazu oben auf den Link Adobe Experience Manager und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die Schaltfläche **Ordnerprofile**.
1. Klicken Sie auf **Globales Profil** Kachel.
1. Wählen Sie die **Konfiguration des XML-Editors** Registerkarte und klicken Sie auf **Bearbeiten** Symbol oben
1. Klicken Sie auf **Herunterladen** -Symbol, um die Datei ui\_config.json auf Ihr lokales System herunterzuladen. Anschließend können Sie Änderungen an der Datei vornehmen und diese dann hochladen.
1. Im `ui_config.json` -Datei, suchen Sie die folgende Konfiguration:

   ```
   {
                           "component": "button",
                           "variant": "action",
                           "quiet": true,
                           "icon": "filePDF",
                           "title": "Download as PDF",
                           "on-click": "EDITOR_SAVE_AS_PDF"
                           }
   ```

   und ersetzen Sie sie durch

   ```
   {
                           "component": "button",
                           "icon": "filePDF",
                           "variant": "action",
                           "quiet": true, "title": "Export as PDF",
                           "on-click": "DOWNLOAD_TOPIC_PDF",
                           "show" : ["@isPreviewMode", "@isXmlMode"]
                           }
   ```

1. Speichern Sie die Datei und laden Sie sie hoch.

Wenn Sie nach dem Ausführen der oben genannten Schritte unter Benutzereinstellungen im Web-Editor dasselbe Ordnerprofil auswählen, wird im Vorschaumodus eines Themas die Option zum Generieren von PDF angezeigt.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
