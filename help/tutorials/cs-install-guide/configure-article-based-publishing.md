---
title: Pakete für die artikelbasierte Veröffentlichung installieren
description: Erfahren Sie, wie Sie Pakete für eine artikelbasierte Veröffentlichung installieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Pakete für die artikelbasierte Veröffentlichung installieren {#id21BNL02052Z}

AEM Handbücher bieten eine leistungsstarke artikelbasierte Veröffentlichungsfunktion, die in den Web-Editor integriert ist. Mit dieser Funktion können Sie ein oder mehrere Themen gleichzeitig veröffentlichen. Nachdem Sie eine Zuordnung im Map Editor geöffnet haben, können Sie zur Registerkarte &quot;Ausgaben&quot;navigieren, um eine Vorgabe zu erstellen, und dann ein oder mehrere Themen auswählen, um die Ausgabe zu generieren. Sie können die Funktion zur artikelbasierten Veröffentlichung verwenden, um schrittweise die Ausgabe eines oder mehrerer Themen zu generieren oder Ihre Inhalte auf einer Knowledgebase-Plattform in Artikelform zu veröffentlichen. Weitere Informationen finden Sie unter *Artikelbasierte Veröffentlichung im Web-Editor-Abschnitt* im Benutzerhandbuch.

So erstellen Sie eine AEM Site zum Veröffentlichen einer artikelbasierten Ausgabe:

1. Herunterladen **XML Documentation Components Content Package for Cloud Service** aus dem [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).
1. Öffnen Sie AEM Package Manager. Die Standard-URL für den Zugriff auf den Paketmanager lautet: `https://<hostname>/crx/packmgr/index.jsp`
1. Laden Sie das XML Documentation Components Content Package für Cloud Service hoch und installieren Sie es dann.
1. Laden Sie die `Knowledge-base-template-for-article-based-publishing-for-cloud-service.zip` -Datei [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).
1. Wählen Sie in der globalen Navigation die Option **Sites**.
1. Klicken Sie in der Sites-Benutzeroberfläche auf **Erstellen** -Schaltfläche oben rechts.
1. Auswählen **Site aus Vorlage** aus dem **Erstellen** Dropdown.
1. Klicken Sie auf **Import** und wählen Sie anschließend die `Knowledge-base-template-for-article-based-publishing-for-cloud-service.zip` auf Ihr System heruntergeladen haben. Nachdem die Site-Vorlage importiert wurde, wird sie unten aufgeführt.

   >[!NOTE]
   >
   > Sie müssen die ZIP-Datei nur zum ersten Mal importieren. Nach dem Import ist die Site-Vorlage in der Liste verfügbar.

   Auswählen **Knowledgebase-Vorlage für artikelbasierte Veröffentlichung** , um die AEM zu erstellen, und klicken Sie auf **Nächste** oben rechts.

1. Geben Sie die **Site-Titel** und **Site-Name** und klicken **Erstellen** oben rechts. Eine AEM Site wird mit der Site-Vorlage Tragopan erstellt. \(Die Site &quot;Tragopan&quot;ist eine Beispiel-Knowledgebase AEM Site mit Vorlagen für Kategorien, Abschnitte und Artikelseiten.\)

   >[!NOTE]
   >
   > Sie können mehrere AEM Sites mit derselben Vorlage erstellen.


Sie können die AEM-Website verwenden, um Ihren Artikel mithilfe der Ausgabevorgaben aus dem Web Editor zu veröffentlichen.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
