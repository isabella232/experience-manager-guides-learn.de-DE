---
title: Erstellen einer Karte
description: Erstellen Sie eine Karte mit dem Map Editor in AEM Handbüchern. Suchen Sie nach den Schritten zum Erstellen einer Map-Datei basierend auf einer Map-Vorlage.
exl-id: d35ee09f-f951-4866-a2b1-e4b19f76e7a1
source-git-commit: 8504a0a52d381044bf1f0d6e7de3585ebecf3a7b
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Erstellen einer Karte {#id176FEN0D05Z}

AEM Guides bietet zwei vordefinierte Zuordnungsvorlagen - DITA-Zuordnung und Lesekarte. Sie können auch eigene Zuordnungsvorlagen erstellen und diese für Ihre Autoren freigeben, um Zuordnungsdateien zu erstellen.

Führen Sie die folgenden Schritte aus, um eine Zuordnungsdatei zu erstellen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zu dem Speicherort, an dem Sie die Zuordnungsdatei erstellen möchten.

1. Klicks **Erstellen** \> **DITA Map**.

1. Wählen Sie auf der Blueprint-Seite den gewünschten Typ von Zuordnungsvorlagen aus und klicken Sie auf **Nächste**.

   >[!NOTE]
   >
   > Wie die Themen in einer Map-Datei referenziert werden, hängt von der Zuordnungsvorlage ab. Wenn Sie beispielsweise die Zuordnungsvorlage auswählen, verweist das Thema auf \(`topicref`\) werden verwendet, um auf Themen zu verweisen. Im Fall einer Bookmap werden Themenverweise mithilfe der Variablen `chapter` -Element in DITA.

   ![](images/map-template.png){width="650" align="left"}

1. Geben Sie auf der Seite Eigenschaften die Zuordnung an **Titel**.

1. \(Optional\) Geben Sie die Datei an **Name**.

   Wenn Ihr Administrator einen automatischen Dateinamen basierend auf der UUID-Einstellung konfiguriert hat, wird Ihnen die Option zum Angeben des Dateinamens nicht angezeigt. Der Datei wird automatisch ein UUID-basierter Dateiname zugewiesen.

   Wenn die Dateibenennungsoption verfügbar ist, wird automatisch auch der Name basierend auf dem Titel Ihrer Zuordnung vorgeschlagen. Wenn Sie den Namen der Zuordnungsdatei manuell angeben möchten, stellen Sie sicher, dass der Dateiname keine Leerzeichen, Apostroph oder Klammern enthält und mit `.ditamap`.

1. Klicken Sie auf **Erstellen**.

   Die Meldung Zuordnungserstellung wird angezeigt.

   Jede neue Zuordnungsdatei, die Sie über die Assets-Benutzeroberfläche erstellen **Erstellen** \> **DITA Map** oder dem Web-Editor eine eindeutige Zuordnungs-ID zugewiesen wird. Außerdem wird die neue Karte als neueste Arbeitskopie in DAM gespeichert. Bis Sie eine Revision einer neu erstellten Zuordnung speichern, wird keine Versionsnummer im Versionsverlauf angezeigt. Wenn Sie die Karte zur Bearbeitung öffnen, werden die Versionsinformationen in der rechten oberen Ecke der Registerkarte der Zuordnungsdatei angezeigt:

   ![](images/first-version-map-none.png){width="650" align="left"}

   Die Versionsinformationen für eine neu erstellte Zuordnung werden als *Keine*. Wenn Sie eine neue Version speichern, wird ihr die Versionsnummer 1.0 zugewiesen. Weitere Informationen zum Speichern einer neuen Version finden Sie unter [Als neue Version speichern](web-editor-features.md#save-as-new-version-id209ME400GXA).

   Sie können die Map zur Bearbeitung im konfigurierten Map-Editor öffnen oder die Map-Datei im AEM-Repository speichern.

   >[!NOTE]
   >
   > Um den erweiterten Map-Editor zu verwenden, greifen Sie im Web Editor auf die Map-Datei zu. Falls Ihr Administrator den erweiterten Map-Editor als Standardeditor in den Zuordnungsdateien konfiguriert hat, wird die Zuordnungsdatei direkt im erweiterten Map-Editor zur Bearbeitung geöffnet. Siehe *Festlegen des Erweiterten Map-Editors als Standard* unter Adobe Experience Manager-Handbücher installieren und konfigurieren as a Cloud Service.


**Übergeordnetes Thema:**[ Arbeiten mit dem Map Editor](map-editor.md)
