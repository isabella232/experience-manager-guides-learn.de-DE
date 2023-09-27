---
title: Massen-Tagging von DITA-Inhalten
description: Verwenden Sie das Massen-Tagging von Inhalten in AEM Handbüchern, um die Entdeckung von DITA-Inhalten zu verbessern. Erfahren Sie, wie Sie Massen-Tags auf einzelne Themen oder mehrere Themen anwenden, entfernen, anzeigen oder ausblenden.
exl-id: 0e855575-e62f-4dc7-869c-7fd3ec61ffdb
source-git-commit: 8504a0a52d381044bf1f0d6e7de3585ebecf3a7b
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Massen-Tagging von DITA-Inhalten {#id179SG0TN05Z}

Mit Tags können Sie Inhalte innerhalb Ihres Inhalts-Repositorys und auch in der veröffentlichten Ausgabe gruppieren oder klassifizieren. Wenn Sie Tags auf Ihren Inhalt angewendet haben, können Sie verwandte Themen in einer DITA-Map finden, die Ihnen beim Authoring von Inhalten helfen kann. Mit der veröffentlichten Ausgabe können Endbenutzer den richtigen Inhalt schneller finden, wenn geeignete Tags vorhanden sind.

Mit AEM Guides können Sie DITA-Inhalte mit wenigen Klicks taggen. Sie können die Massen-Tagging-Funktion verwenden, um mehrere Tags auf mehrere Themen, eine DITA-Zuordnung oder auf eine Unterzuordnung anzuwenden. Sie können auch Tags auf ein einzelnes Thema anwenden. Tagging ist die native Funktion in AEM. Weitere Informationen zum Erstellen und Verwalten von Tags finden Sie in der [Verwalten von Tags](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) in AEM Dokumentation.

Standardmäßig gewähren AEM Guides keinen Lesezugriff für Benutzer im Ordner, in dem alle Tags im AEM-Repository gespeichert sind. Um im AEM-Repository definierte Tags zu verwenden, müssen Sie Ihren Systemadministrator bitten, Zugriff auf den Ordner zu gewähren, in dem die Tags gespeichert sind.

## Anwenden von Bulk-Tags

Verwenden Sie die Massen-Tagging-Funktion, um mehrere Tags gleichzeitig anzuwenden. Führen Sie die folgenden Schritte aus, um Tags auf Ihre Themen in einer DITA-Zuordnung anzuwenden:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnungsdatei und klicken Sie darauf.

   Die DITA-Zuordnungskonsole wird mit der Liste der zum Generieren der Ausgabe verfügbaren Ausgabevorgaben angezeigt.

1. Klicks **Themen**.

   Eine Liste der in der DITA-Map verfügbaren Themen wird angezeigt. Die UUIDs der Themen werden unter dem Thementitel angezeigt.

1. Wählen Sie die Themen oder Unterkarten aus, auf die Sie Tags anwenden möchten.

   ![](images/apply-tags-uuid.png){width="650" align="left"}


   >[!NOTE]
   >
   > Der obige Screenshot zeigt eine ausgewählte und erweiterte Unterkarte. Bei Auswahl der Unterzuordnung werden auch alle Themen unter der Unterzuordnung ausgewählt.

1. Klicks **Anwenden von Tags**.

   Das Dialogfeld Tags auswählen wird angezeigt.

1. Wählen Sie ein oder mehrere Tags aus, die Sie auf die ausgewählten Themen anwenden möchten.

1. Bestätigen Sie Ihre Auswahl.

   Die ausgewählten Tags werden auf die Themen angewendet und neben dem Thementitel angezeigt.

   >[!NOTE]
   >
   > Wenn Sie nach dem Hinzufügen von Tags zu Ihren Themen ein Thema verschieben oder löschen, werden die Tags für diese Themen ebenfalls entfernt. Dieses Thema bleibt jedoch auf der Karte, bis Sie es entfernen.


## Anwenden von Tags auf ein einzelnes Thema

Führen Sie die folgenden Schritte aus, um Tags auf ein einzelnes Thema anzuwenden:

1. Navigieren Sie in der Assets-Benutzeroberfläche zu der Themendatei, auf die Sie Tags anwenden möchten, und wählen Sie sie aus.

1. Klicken Sie in der Symbolleiste auf **Eigenschaften**.

   Die Eigenschaftenseite des Themas wird angezeigt.

1. Klicken Sie auf der Registerkarte Allgemein auf das Symbol Durchsuchen neben dem **Tags** -Feld.

1. Wählen Sie ein oder mehrere Tags aus, die Sie auf das ausgewählte Thema anwenden möchten.

1. Bestätigen Sie Ihre Auswahl.

1. Klicks **Anwenden von Tags**.

   Die ausgewählten Tags werden auf das Thema angewendet und im Feld Tags angezeigt.

1. Klicken Sie auf **Speichern und schließen**.


## Entfernen von Tags

Je nach Ihren geschäftlichen Anforderungen können Sie die Tagging-Informationen für jedes DITA-Thema ändern. Sie können einfach alle Tags gleichzeitig entfernen oder nur die Tags entfernen, die für das Thema nicht gültig sind.

Führen Sie die folgenden Schritte aus, um alle Tags aus einem oder mehreren Themen zu entfernen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnungsdatei und klicken Sie darauf.

   Die DITA-Zuordnungskonsole wird mit der Liste der zum Generieren der Ausgabe verfügbaren Ausgabevorgaben angezeigt.

1. Klicks **Themen**.

   Eine Liste der in der DITA-Map verfügbaren Themen wird angezeigt.

1. Wählen Sie die Themen aus, aus denen Sie Tags entfernen möchten.

1. Klicks **Entfernen von Tags**.

   >[!NOTE]
   >
   > Wenn das Symbol Tags löschen nicht angezeigt wird, stellen Sie sicher, dass Sie die Funktion Tags ausblenden nicht aktiviert haben.

1. Klicken Sie im Dialogfeld Löschen bestätigen auf **OK** , um Tags aus den ausgewählten Themen zu entfernen.


## Anzeigen oder Ausblenden von Tags

Wenn Sie eine lange Liste von Tags auf Ihre Themen angewendet haben, ist die Navigation möglicherweise etwas schwerfällig. Sie können Tags in der Ansicht der DITA-Map-Konsole einfach ausblenden, indem Sie auf das Symbol Tags ausblenden klicken. Wenn die Tags nicht sichtbar sind, werden durch Klicken auf &quot;Tags anzeigen&quot;alle Tags angezeigt.

**Übergeordnetes Thema:**[ Verwalten von Metadaten](manage-metadata.md)
