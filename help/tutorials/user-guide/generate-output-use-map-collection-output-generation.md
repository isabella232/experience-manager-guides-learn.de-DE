---
title: Verwenden der Kartensammlung für die Ausgabegenerierung
description: Erfahren Sie, wie Sie die Map Collection für die Ausgabegenerierung verwenden.
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 1%

---


# Verwenden der Kartensammlung für die Ausgabegenerierung {#id1723F20G0HS}

In jeder Organisation kann ein Produkt über mehrere Arten von Dokumentation verfügen. Als Publishing-Spezialist möchten Sie steuern, welche Ausgabe Sie für welches Dokument generieren möchten. Außerdem sollte es eine Möglichkeit geben, mehrere Dokumente mit einem einzigen Klick im Batch-Modus zu veröffentlichen.

AEM Guides bieten Ihnen die Möglichkeit, Ihre Inhalte für die Veröffentlichung mithilfe eines Dashboards namens Map Collection zu organisieren. Mit einer Kartensammlung können Sie alle verschiedenen Arten von Dokumenten in einer Einheit zusammenführen. Sie können festlegen, welche Art von Ausgabe Sie für jedes Dokument in Ihrer Map Collection generieren möchten. Darüber hinaus können Sie die Ausgabe generieren und den Fortschritt der Ausgabenerstellung im Publishing-Dashboard anzeigen.

Mit der Sammlung &quot;Karte&quot;können Sie anzeigen, ob sich eine Karte von der letzten veröffentlichten Ausgabe ändert. Sie können die Details auf der Registerkarte Karten und Vorgaben Ihrer Map-Sammlung anzeigen und die Ausgabe dann bei Bedarf erneut veröffentlichen. Weitere Informationen finden Sie unter Hinzufügen einer Zuordnung zu einer Map-Sammlung.

## Erstellen einer Zuordnungssammlung und Hinzufügen von DITA-Maps

So erstellen Sie eine Map Collection und fügen der Sammlung DITA-Maps hinzu:

1. Klicken Sie auf der Assets-Benutzeroberfläche auf **Sammlungen zuordnen**.

   Wenn der Link Sammlungen zuordnen nicht verfügbar ist, wählen Sie die **Navigation** in der linken Leiste und klicken Sie dann auf **Sammlungen zuordnen**.

   ![](images/access-map-collection-left-rail.png)

1. Geben Sie einen Titel für Ihre Zuordnungssammlung ein.
1. Klicken Sie auf **Erstellen**.

   Bei der Erstellung der Zuordnungssammlung wird eine Erfolgsmeldung angezeigt.

1. Klicken **Schließen** in der Erfolgsmeldung angezeigt.

   Die neu erstellte Zuordnungsdatei wird auf der Seite Sammlungen zuordnen angezeigt.

1. Klicken Sie auf das graue Feld in der Kachel der Sammlung, die Sie bearbeiten möchten.
1. Klicken **Bearbeiten** und klicken Sie anschließend auf **Zuordnen hinzufügen**.
1. Suchen und fügen Sie die DITA-Maps hinzu, die Sie der Map-Sammlung hinzufügen möchten.

   Standardmäßig werden alle Vorgaben und Gebietsschemata, die mit der Zuordnung verknüpft sind, automatisch hinzugefügt.

1. Wählen Sie die gewünschte Ausgabe aus, indem Sie die gleitende Schaltfläche ein- oder ausschalten.
1. Klicken Sie auf **Fertig**.

   Die DITA-Zuordnungsdateien werden Ihrer Zuordnungssammlung hinzugefügt.


![](images/maps_presets_62_63.png)

Die folgenden Filteroptionen und Zuordnungsdetails werden auf der Sammlungsseite angezeigt:

- **Filter:** Die aktuelle Leiste zeigt die folgenden Filter an:
   - **Geändert**: Sie können &quot;Ja&quot;oder &quot;Nein&quot;auswählen. Wenn Sie &quot;Ja&quot;auswählen, werden nur die modifizierten DITA-Maps in der Tabelle Maps und Vorgaben angezeigt.
   - **Vorgabe**: Wählen Sie eine Vorgabe aus, nach der Sie die Zuordnungsdateien herausfiltern möchten. Wenn Sie beispielsweise *AEM Site* voreingestellt ist, werden nur die Karten angezeigt, die die *AEM Site* Ausgabevorgabe, die für sie konfiguriert ist.
   - **Sprache**: Sie können einen beliebigen Sprachcode auswählen und nur die ausgewählte Sprache in der Tabelle Karten und Vorgaben anzeigen.
- **Karten und Vorgaben** table: Die Tabelle &quot;Karten und Vorgaben&quot;enthält Informationen in den folgenden Spalten:
   - **Zuordnung**: Zeigt den Titel der DITA-Map-Datei an.
   - **Sprache**: Zeigt die Sprache der DITA-Zuordnung an.
   - **Vorgabe**: Zeigt den Typ der in der Zuordnungsdatei konfigurierten Ausgabevorgabe an.
   - **Geändert**: Gibt an, ob die DITA-Zuordnung nach der letzten Veröffentlichung aktualisiert wird. Anhand dieser Informationen können Sie entscheiden, ob Sie die Ausgabe für diese DITA-Zuordnung erneut veröffentlichen möchten oder nicht.
   - **Zuletzt generiert**: Zeigt das Datum und die Uhrzeit der letzten generierten Ausgabe an.

## Konfigurieren und Generieren der Ausgabe mithilfe einer Map Collection

Um die Ausgabe mithilfe einer Map Collection zu konfigurieren und zu generieren, führen Sie die folgenden Schritte aus:

1. Öffnen Sie die Kartensammlung.
1. \(Optional\) Führen Sie je nach Anforderung einen der folgenden Schritte aus:
   - Wenden Sie Filter aus der linken Leiste an, um die geänderten Zuordnungen, Ausgabevorgaben oder Sprachen zu filtern.
   - Klicken Sie bei Bedarf auf **Bearbeiten** und ändern Sie die gewünschte Ausgabe, indem Sie die gleitende Schaltfläche ein- oder ausschalten.
1. Führen Sie einen der folgenden Schritte aus:

   - Um die Ausgabe der ausgewählten Karten zu generieren, wählen Sie die Zuordnungsdateien aus und klicken Sie auf **Ausgewählte generieren**.
   - Um die Ausgabe aller DITA-Maps mit den konfigurierten Vorgaben zu generieren, klicken Sie auf **Alle generieren**.

   >[!IMPORTANT]
   >
   > Wenn sich ein Ausgabeerstellungsprozess für eine Vorgabe oder DITA-Zuordnung entweder in der Warteschlange befindet oder in Bearbeitung ist, können Sie keine weitere Ausgabegenerierungsaufgabe für dieselbe Vorgabe oder Zuordnung starten.


## Löschen einer Map-Sammlung oder einer DITA-Zuordnung aus der Map Collection

- Um eine Zuordnungssammlung zu löschen, wählen Sie eine Sammlung auf der Seite &quot;Zuordnungssammlung&quot;aus und klicken Sie auf **Löschen**.
- Um eine DITA-Map aus einer Map-Sammlung zu löschen, öffnen Sie die Map-Sammlung im Bearbeitungsmodus, wählen Sie die DITA-Map-Datei aus und klicken Sie auf **Aus Sammlung löschen**.

   Dadurch werden auch alle mit der DITA-Map verknüpften Vorgaben oder Gebietsschemata aus der Map-Sammlung entfernt.


## Abbrechen einer Ausgabenerstellungsaufgabe aus einer Map Collection

Ähnlich wie beim Abbrechen einer Ausgabegenerierungsaufgabe über die [DITA-Zuordnungskonsole](generate-output-for-a-dita-map.md#id2061H100T5Z) oder [Dashboard veröffentlichen](generate-output-publish-dashboard.md#)können Sie eine Ausgabegenerierungsaufgabe über eine Map Collection abbrechen. Rufen Sie die Registerkarte &quot;Outputs&quot;einer Map Collection auf, wechseln Sie zur Veröffentlichungsaufgabe, die Sie abbrechen möchten, und klicken Sie auf **Vorgang abbrechen** zum Abbrechen der Veröffentlichungsaufgabe.

![](images/cancel-publish-task-map-collection.png)

**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)

