---
title: Konfigurieren des Titels für die Symbole Einchecken und Auschecken
description: Erfahren Sie, wie Sie den Titel für die Symbole "Ein- und Auschecken"konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Konfigurieren des Titels für die Symbole &quot;Ein- und Auschecken&quot;

Mit AEM Guides können Sie den Titel für die Symbole &quot;Ein- und Auschecken&quot;im Web Editor konfigurieren. Führen Sie die folgenden Schritte aus, um den Titel für die Symbole Einchecken und Auschecken zu konfigurieren:

1. Laden Sie die Konfigurationsdatei der Benutzeroberfläche herunter, indem Sie sich bei Adobe Experience Manager als Administrator anmelden.
1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die Schaltfläche **Ordnerprofile**.
1. Klicken Sie auf **Globales Profil** Kachel.
1. Wählen Sie die **Konfiguration des XML-Editors** und klicken Sie auf **Bearbeiten** Symbol oben.
1. Im **Konfiguration der Benutzeroberfläche des XML-Editors** klicken Sie auf die **Herunterladen** zum Herunterladen des `ui_config.json` -Datei auf Ihrem lokalen System.
1. Im `ui_config.json` ändern Sie den Titel im Abschnitt &quot;topbar&quot;. Sie können die folgenden Werte ändern:

   ```json
   //Change title to "Check out" instead of "Lock"
           "title": "Check out"
   
   //Change title to "Check in" instead of "@checkOutBy
            "title": "Check in"
   ```

1. Speichern Sie die Datei und laden Sie sie hoch.
