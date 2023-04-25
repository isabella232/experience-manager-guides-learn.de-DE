---
title: Erstellen von Ausgabevorgaben aus dem Web-Editor
description: Erfahren Sie, wie Sie im Web Editor Ausgabevorgaben erstellen
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---


# Erstellen von Ausgabevorgaben aus dem Web-Editor {#id218CL400JW3}

Führen Sie die folgenden Schritte aus, um Ausgabevorgaben für Ihre DITA-Zuordnung zu erstellen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur Zuordnungsdatei, die Sie bearbeiten möchten.

1. Um eine exklusive Sperre für die Zuordnungsdatei zu erhalten, wählen Sie die Zuordnungsdatei aus und klicken Sie auf **Auschecken**.

1. Wählen Sie die **Themen bearbeiten** im Aktionsmenü der Zuordnungsdatei.

   Die Zuordnungsdatei wird zur Bearbeitung im Web-Editor geöffnet.

   >[!NOTE]
   >
   > Sie können jedes Thema mit dem erweiterten Map-Editor hinzufügen oder aus der Zuordnung löschen. Weitere Informationen finden Sie unter [Arbeiten mit dem erweiterten Map Editor](map-editor-advanced-map-editor.md#).

1. Im **Ausgabe** klicken Sie auf das Symbol + , um eine Ausgabevorgabe für Ihre DITA-Zuordnung zu erstellen.

   ![](images/output-tab-preset_cs.png)

1. Geben Sie den Namen der Vorgabe im Dialogfeld Vorgabe hinzufügen ein und klicken Sie auf **Hinzufügen**.

1. Geben Sie die folgenden Konfigurationsdetails ein.

   1. Wählen Sie die erforderlichen Optionen im **Allgemein** Registerkarte. Sie können eine Ausgabevorgabe mit oder ohne Bedingungen erstellen. Sie können auch eine DITVAL-Datei verwenden. Mit AEM Guides können Sie auch eine Grundlinie für die Veröffentlichung einer bestimmten Version Ihrer DITA-Map auswählen.
   1. Geben Sie die AEM Site-Details im **AEM** Registerkarte. **Site** zeigt die Liste der AEM Sites an, die in Ihrem AEM Repository verfügbar sind. **Kategorie**, **Bereichsvorlage** und **Artikelvorlage** sind die Strukturkomponenten, die verwendet werden, um das Erscheinungsbild Ihrer Ausgabe zu organisieren. Diese sind in der Vorlage AEM Site vordefiniert.

      >[!NOTE]
      >
      > Aktualisieren Sie jedes Dropdown-Menü, um die weitere Klassifizierung in der nächsten Dropdown-Liste zu erhalten.

   1. Aus dem **Artikel** die Themen, für die Sie die Ausgabe generieren möchten.
1. Wählen Sie die **Vorgabe generieren** -Symbol oben, um die Ausgabe zu generieren.

   ![](images/add-preset-articles-tab_cs.png)

1. Sie sehen den Status des Generierungsprozesses der Ausgabe. Die **Themen** enthält die Themen, für die die Ausgabe generiert wird, während die **Status** zeigt den Veröffentlichungsstatus der einzelnen Themen an.

   Um die Ausgabe anzuzeigen, bewegen Sie den Mauszeiger über das Thema und klicken Sie auf &quot;Ausgabe anzeigen&quot;.

   ![](images/add-preset-output-generated_cs.png)


>[!NOTE]
>
> Sie können eine vorhandene Ausgabevorgabe auch im Menü &quot;Optionen&quot;bearbeiten, umbenennen, duplizieren oder löschen.

![](images/edit-preset_cs.png)

**Übergeordnetes Thema:**[ Artikelbasierte Veröffentlichung im Web Editor](web-editor-article-publishing.md)

