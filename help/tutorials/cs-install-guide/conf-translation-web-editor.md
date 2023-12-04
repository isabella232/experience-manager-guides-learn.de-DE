---
title: Übersetzungsfunktion im Web-Editor konfigurieren
description: Erfahren Sie, wie Sie die Übersetzungsfunktion im Web Editor konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Übersetzungsfunktion im Web-Editor konfigurieren {#id21BONI0J0YR}

Der Web-Editor bietet eine leistungsstarke Übersetzungsfunktion, mit der Sie Ihre Inhalte in mehrere Sprachen übersetzen können.

Sie können die **Verwalten** im Web Editor, um Ihren Inhalt zu übersetzen. Diese Registerkarte ist standardmäßig verfügbar.

So blenden Sie die **Verwalten** im Web Editor die folgenden Schritte ausführen:

1. Anmelden **Adobe Experience Manager** als Administrator.
1. Klicken Sie auf **Adobe Experience Manager** links oben und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die Schaltfläche **Ordnerprofile**.
1. Klicken Sie auf **Globales Profil** Kachel.
1. Klicken Sie auf **Konfiguration des XML-Editors**.
1. Klicken Sie auf **Bearbeiten** Symbol oben.
1. Laden Sie die `ui\_config.json` file.Entfernen Sie das folgende Codefragment aus der heruntergeladenen Datei:

   ```json
   {
       "component":"tab",
       "id":"workflow",
       "title":"Manage",
       "on-click":"APP_MODE_CHANGE",
       "items":
       [
           {
               "component":"label",
               "label":"Manage"
           }
       ]
   },
   ```

1. Laden Sie die aktualisierte Datei ui\_config.json hoch.

Beachten Sie Folgendes: **Verwalten** -Filter nicht mehr verfügbar ist.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
