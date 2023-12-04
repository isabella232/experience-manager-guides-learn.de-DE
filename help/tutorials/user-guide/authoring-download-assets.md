---
title: Dateien herunterladen
description: Erfahren Sie, wie Sie Dateien aus der DITA-Map-Konsole in AEM-Handbüchern herunterladen und eine DITA-Map-Datei in AEM Repository exportieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Dateien herunterladen {#id216MC0H0BE8}

Sie können Assets einschließlich DITA- und Nicht-DITA-Dateien herunterladen. Es gibt mehrere Möglichkeiten, Assets herunterzuladen, einige Methoden sind AEM nativ und andere werden von AEM Guides unterstützt. Informationen zu nativen AEM-Assets finden Sie unter [Herunterladen von Assets aus Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/download-assets-from-aem.html) in AEM Dokumentation. Im folgenden Abschnitt wird der Mechanismus zum Herunterladen von Dateien über die DITA-Zuordnungskonsole in AEM Handbüchern beschrieben.

## DITA-Map-Datei exportieren

Sobald sich die DITA-Map-Datei im AEM-Repository befindet, können Sie die Map-Datei zusammen mit den abhängigen Elementen herunterladen. So können Sie die vollständige Zuordnungsdatei für die Offline-Bearbeitung, Validierung, Überprüfung oder einfach Erstellung einer Sicherung freigeben.

Führen Sie die folgenden Schritte aus, um eine DITA-Map-Datei zusammen mit den abhängigen Dateien herunterzuladen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnung, die Sie herunterladen möchten.

1. Klicken Sie auf die DITA-Karte, um sie in der DITA-Map-Konsole zu öffnen.

1. Wählen Sie die **Themen** um eine Liste der in der DITA-Map verfügbaren Themen anzuzeigen.

1. Klicken Sie in der Symbolleiste auf **Download-Map**.

   Das Dialogfeld &quot;Karte herunterladen&quot;wird angezeigt.

   ![](images/download-map.png){width="300" align="left"}

1. Klicken Sie auf **Herunterladen**. Im Dialogfeld &quot;Karte herunterladen&quot;können Sie die folgenden Optionen auswählen:

   - **Grundlinie verwenden**: Wählen Sie diese Option aus, um eine Liste der Grundlinien für die DITA-Zuordnung zu erhalten. Wenn Sie die Zuordnungsdatei und deren Inhalt auf Grundlage einer bestimmten Grundlinie herunterladen möchten, wählen Sie die Grundlinie aus der Dropdownliste aus. Weitere Informationen zum Arbeiten mit Grundlinien finden Sie unter [Arbeiten mit Grundlinien](generate-output-use-baseline-for-publishing.md#).
   - **Reduzieren der Dateihierarchie**: Wählen Sie diese Option, um alle referenzierten Themen und Mediendateien in einem einzigen Ordner zu speichern.
   >[!NOTE]
   >
   > Sie können auch die Zuordnungsdatei herunterladen, ohne eine Option auszuwählen. In diesem Fall wird die letzte persistente Version der referenzierten Themen und Mediendateien heruntergeladen.

1. Nachdem Sie auf **Herunterladen** -Schaltfläche, wird die Anfrage zum Herunterladen der Map in die Warteschlange gestellt. Sie erhalten die folgende Benachrichtigung, sobald die Karte zum Download bereit ist.

   ![](images/download-map-prompt.png){width="550" align="left"}

   - Klicks **Herunterladen** um die Zuordnungsdatei im.zip-Format herunterzuladen.

   - Klicks **Später herunterladen** , um die Map-Datei zu einem späteren Zeitpunkt herunterzuladen. Der Downloadlink kann über den AEM Benachrichtigungs-Posteingang aufgerufen werden. Klicken Sie im Posteingang auf die Benachrichtigung zur generierten Zuordnung, um die Zuordnung im ZIP-Format herunterzuladen.

   >[!NOTE]
   >
   > Standardmäßig bleiben die heruntergeladenen Maps fünf Tage im AEM Benachrichtigungs-Posteingang.

![](images/download-map-inbox.png){width="300" align="left"}

Nachdem die Karte heruntergeladen wurde, können Sie die Karte auswählen und das Symbol Öffnen oben verwenden, um den ausgewählten Bericht zu öffnen.

**Übergeordnetes Thema:**[ Inhalt verwalten](authoring.md)
