---
title: Schlüssel
description: Mit Schlüsseln können Sie bei der Arbeit mit DITA in AEM Handbüchern Variableninformationen einschließen.
exl-id: cb64e094-fe6d-4a5e-8f0e-25ae58aaa2c6
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Schlüssel

Verschiedene Materialgruppen können ähnliche Informationen enthalten, die an ausgewählten Stellen angepasst werden müssen. Schlüssel ermöglichen es Ihnen, bei der Arbeit mit DITA Variableninformationen in einzuschließen.

Beispieldateien, die Sie für diese Lektion verwenden können, finden Sie in der Datei . [keys.zip](assets/keys.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342756)

## Schlüssel aktivieren

1. Laden Sie den Satz der bereitgestellten Beispieldateien hoch.

   a. Laden Sie die ZIP-Datei.

   b. Aktualisieren Sie die AEM.

   c. Wählen Sie die zu extrahierende Datei aus.

   ![Zip auswählen](images/lesson-9/select-zip.png)

   d. Klicken [!UICONTROL **Archiv extrahieren**] in der oberen Symbolleiste.

   ![Symbolleiste](images/lesson-9/extract-archive.png)

   e. Wählen Sie im Dialogfeld den spezifischen Speicherort für zu extrahierende Dateien aus, z. B. den Ordner Schlüssel .

   f. Klicken [!UICONTROL **Nächste**].

   g. Konflikte überspringen, da sie nicht für Inhalte vorhanden sind, die noch nie hochgeladen wurden.

   h. Auswählen [!UICONTROL **Extract**] oben rechts auf dem Bildschirm.

2. Wenn die Extraktion abgeschlossen ist, klicken Sie auf [!UICONTROL **Navigieren Sie zum Zielordner**].

   ![Bestätigung](images/lesson-9/go-to-target.png)

## Schlüssel zu referenzierten Werten auflösen

Um Schlüssel richtig zu verwenden, müssen Benutzereinstellungen auf eine bestimmte Zuordnung als Stammzuordnung verweisen. Innerhalb dieser Zuordnung befindet sich eine Sammlung von Schlüsseln, die in einer Topicgroup gruppiert sind. Wenn Sie die Zuordnung und die Themen öffnen, werden die Schlüssel zu den Werten aufgelöst, auf die diese Zuordnung verweist.

1. Geben Sie eine Stammzuordnung an.

   a. Öffnen Sie im Bildschirm Schlüssel eine Karte.

   b. Benutzereinstellungen konfigurieren.

   c. Klicken Sie auf die [!UICONTROL **Benutzereinstellungen**] in der oberen Symbolleiste.

   ![Obere Symbolleiste](images/lesson-9/author-view.png)

   d. Klicken Sie auf das Schlüsselsymbol, um eine **Stammkarte** wird verwendet, um Schlüssel aufzulösen.

   e. Aktivieren Sie die Kontrollkästchen für die gewünschten Assets.

   ![Asset-Dropdown](images/lesson-9/select-assets.png)

   f. Klicken [!UICONTROL **Auswählen**].

   g. **Speichern** die Benutzereinstellungen.

2. Navigieren Sie zum **Kartenansicht**.

3. Öffnen Sie die angegebene Karte.

Die Schlüssel werden aufgelöst.

## Manuelles Hinzufügen eines neuen Keydefs

1. Öffnen Sie eine Karte mit einer angegebenen Stammzuordnung.

2. Wählen Sie einen Schlüssel aus.

   ![Dropdown-Liste für Schlüssel](images/lesson-9/hybrid-key.png)

3. Fügen Sie ein neues Keydef ein.

   a. Klicken Sie an einer gültigen Stelle in der Karte auf .

   b. Wählen Sie die **keydef** in der oberen Symbolleiste.

   ![Keydef-Symbolleiste](images/lesson-9/key-icon.png)

   c. Geben Sie im Dialogfeld &quot;Keydef einfügen&quot;einen eindeutigen Wert für Schlüssel ein, der für die von Ihnen erstellte Definition sinnvoll ist.

   d. Klicken [!UICONTROL **Einfügen**].

4. Fügen Sie topicmeta innerhalb der keydef hinzu.

   a. Klicken Sie auf [!UICONTROL **Element einfügen**] in der oberen Symbolleiste.

   ![Keydef-Symbolleiste](images/lesson-9/add-icon.png)

   b. Suchen Sie im Dialogfeld Element einfügen nach &quot;topicmeta&quot;.

5. Fügen Sie Suchbegriffe innerhalb des topicmeta hinzu.

   a. Klicken Sie auf [!UICONTROL **Element einfügen**] in der oberen Symbolleiste.

   ![Keydef-Symbolleiste](images/lesson-9/add-icon.png)

   b. Suchen Sie im Dialogfeld Element einfügen nach &quot;Keywords&quot;.

6. Fügen Sie einen Suchbegriff in der topicmeta hinzu.

   a. Klicken Sie auf [!UICONTROL **Element einfügen**] in der oberen Symbolleiste.

   ![Keydef-Symbolleiste](images/lesson-9/add-icon.png)

   b. Im **Element einfügen** Dialog, suchen und wählen Sie &quot;Keyword&quot;

7. Geben Sie den Wert für den keydef in den Suchbegriff ein.

In der Karte sollte Ihr Keydef jetzt etwa wie folgt aussehen:

![Keydef beendet](images/lesson-9/keydef.png)

## Konfigurieren eines Keydefs als Snippet

Snippets sind kleine Inhaltsfragmente, die über verschiedene Themen in Ihrem Dokumentationsprojekt hinweg wiederverwendet werden können. Anstatt jede Keydef manuell zu generieren, können Sie eine einzelne Keydef als Snippet konfigurieren.

1. Wählen Sie ein keydef-Element in der Zuordnung aus.

2. Klicken Sie im Kontextmenü auf [!UICONTROL **Snippet erstellen**].

3. Fügen Sie im Dialogfeld Neues Snippet einen Titel und eine Beschreibung hinzu.
Sie können auch vorhandene Schlüssel- oder Suchbegriffdefinitionen aus dem Inhalt entfernen.

4. Klicken Sie auf [!UICONTROL **Erstellen**].

5. Wählen Sie im linken Bereich die Option **Snippets**.

6. Ziehen Sie das soeben erstellte Snippet aus dem Bedienfeld &quot;Snippets&quot;in die Karte.

7. Aktualisieren Sie die keydef nach Bedarf mithilfe der Inhaltseigenschaften.
Nach dem Speichern und Aktualisieren ist dieser Satz von Schlüssel für jeden Benutzer verfügbar, der eine Zuordnung definiert hat, die dieselbe Stammzuordnung enthält.
