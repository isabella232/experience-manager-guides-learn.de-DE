---
title: Veröffentlichung mit Bedingungen
description: Veröffentlichen mit Bedingungen in Adobe Experience Manager-Handbüchern
exl-id: ea94824a-884b-447f-9562-e6c629b8133b
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 4%

---

# Veröffentlichung mit Bedingungen

Durch die bedingte Veröffentlichung kann eine Inhaltsquelle für eine oder mehrere Zielgruppen, Produkte oder Plattformen geschrieben werden. Diese Informationen können dann dynamisch veröffentlicht werden und nur speziell erforderliche Inhalte, die in der Ausgabe enthalten sind.

>[!VIDEO](https://video.tv.adobe.com/v/339041?quality=12&learn=on)

## Vorbereitung der Übung

Hier können Sie Beispieldateien für die Übung herunterladen.

[Übung-Download](assets/exercises/publishing-with-conditions.zip)

## Markieren von Inhalten mit bedingten Attributen

1. Öffnen Sie das zu ändernde Thema.

1. Geben Sie den Text ein, der an Bedingungen geknüpft werden soll. Beispielsweise einen oder mehrere Absätze, eine gesamte Tabelle, eine Abbildung oder andere Inhalte.

   ![Presenting-Information](images/presenting-info.png)

1. Wählen Sie den spezifischen Inhalt aus, dem ein bedingtes Attribut zugewiesen werden soll. Beispielsweise einen einzelnen Absatz innerhalb der Quelle.

   ![Template-Choice](images/template-choice.png)

1. Stellen Sie in der rechten Leiste sicher, dass die Eigenschaften angezeigt werden.

1. Fügen Sie ein Attribut für Zielgruppe, Produkt oder Plattform hinzu.

1. Weisen Sie dem Attribut einen Wert zu. Die Inhaltsanzeige wurde aktualisiert, um bedingte Markierungen anzuzeigen.

   ![Vorlage festlegen](images/specify-template.png)

## Vorschau bedingter Inhalte

1. Klicken Sie auf **Vorschau**. 

1. under **Filter**, wählen Sie die ein- oder auszublendenden Bedingungen aus oder heben Sie die Auswahl auf.

1. Auswählen oder Aufheben der Auswahl **Text für Bedingungen hervorheben**.

   ![Vorschau-Conditional-Content](images/preview-conditional-content.png)

## Bedingungsvorgabe erstellen

Eine Bedingungsvorgabe ist eine Sammlung von Eigenschaften, die definieren, was während der Generierung der Ausgabe ein- oder ausgeschlossen bzw. anderweitig markiert werden soll.

1. Wählen Sie im Map Dashboard die **Bedingungsvorgaben** Registerkarte.

1. Klicken Sie auf **Erstellen**.

1. Auswählen **Hinzufügen** (oder **Alle hinzufügen**).

1. Benennen Sie die Bedingung.

1. Wählen Sie eine Kombination aus Attribut, Titel und Aktion aus.

   ![Create-Condition-Preset](images/create-condition-preset.png)

1. Wiederholen Sie dies nach Bedarf.

1. Klicken Sie auf **Speichern**.

## Bedingte Ausgabe generieren

Sobald Bedingungen auf Inhalte angewendet wurden, können sie als Ausgabe generiert werden. Dies kann entweder eine Bedingungsvorgabe oder eine DITAval-Datei verwenden.

## Bedingte Ausgabe mithilfe einer Bedingungsvoreinstellung generieren

1. Wählen Sie die **Ausgabevorgaben** Registerkarte.

1. Wählen Sie eine Ausgabevorgabe aus.

1. Klicken Sie auf **Bearbeiten**.

1. under **Anwenden einer Bedingung mithilfe von** Wählen Sie eine Bedingungsvorgabe aus.

   ![Generate-Conditional-Output](images/generate-conditional-output.png)

1. Klicken Sie auf **Fertig**.

1. Generieren Sie die Ausgabevorgabe und überprüfen Sie den Inhalt.

## Generieren einer bedingten Ausgabe mit einer DITAval-Datei

Die DITAval-Datei kann verwendet werden, um bedingte Inhalte zu veröffentlichen. Dazu muss eine Datei erstellt oder hochgeladen und dann bei der Veröffentlichung referenziert werden.

1. Wählen Sie die **Ausgabevorgaben** Registerkarte.

1. Wählen Sie eine Ausgabevorgabe aus.

1. Klicken Sie auf **Bearbeiten**.

1. Wählen Sie unter &quot;Bedingungen anwenden mit&quot;eine DITAval-Datei aus.

   ![generate-using-DITAval](images/generate-using-ditaval.png)

1. Klicken Sie auf **Fertig**.

1. Generieren Sie die Ausgabevorgabe und überprüfen Sie den Inhalt.
