---
title: Einfache Workflows zur Inhaltserstellung
description: Erstellen von Inhalten in AEM Handbüchern
exl-id: e4b8e512-0688-44f7-b981-78af33b57b08
source-git-commit: 92c269c4a5f73317345bbd0ab247951656426ff4
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---

# Workflows zur einfachen Inhaltserstellung

Der AEM Guides-Editor verfügt über mehrere Tastaturbefehle, die den Arbeitsablauf für die Inhaltserstellung vereinfachen. Mit diesen Tastaturbefehlen können Benutzer schnell Bilder hinzufügen und ändern, mit mehreren Themen gleichzeitig arbeiten, Fehler korrigieren, Themenversionen herunterladen und mit PDF und Beschriftungen arbeiten.

>[!VIDEO](https://video.tv.adobe.com/v/342770)

## Hinzufügen eines Bilds

Bilder können direkt von einem lokalen Laufwerk aus hinzugefügt werden.

1. Ziehen Sie das Bild direkt in das Thema. Die **Hochladen von Assets** angezeigt.

   ![Dialogfeld &quot;Assets hochladen&quot;](images/lesson-15/upload-assets-dialog.png)

2. Ändern Sie den Ordnerpfad zum gewünschten Bildspeicherort.

3. Ändern Sie den Namen des Bildes in einen für seinen Zweck repräsentativen Namen.

4. Klicken Sie auf [!UICONTROL **Hochladen**].

## Bild ändern

1. Ändern Sie die Größe eines Bildes durch Ziehen und Ablegen einer Ecke.

2. Verschieben Sie ein Bild durch Ziehen und Ablegen an eine andere Position innerhalb des Themas.

3. Verwendung **Inhaltseigenschaften** auf der rechten Seite, um die

   - scale

   - position

   - Ausrichtung oder

   - andere Attribute.

   ![Inhaltseigenschaften](images/lesson-15/content-properties.png)

## Arbeiten mit mehreren Themen

Die Aufspaltungsansicht ist beim Vergleichen von Themen, beim Kopieren und Einfügen zwischen Themen oder beim Ziehen und Ablegen von Inhalten von einem Thema zum anderen hilfreich.

1. Öffnen Sie zwei oder mehr verwandte Themen.

2. Klicken Sie auf die Registerkarte Titel einer Datei, um das Kontextmenü zu öffnen.

3. Auswählen [!UICONTROL **Aufspaltung**].

4. Auswählen **Right**.

   ![Aufspaltungsansicht](images/lesson-15/split-view.png)

## Korrigieren typografischer Fehler

1. Suchen Sie das Wort oder die Wortgruppe, das/die den Fehler enthält.

2. Drücken und halten [!UICONTROL **Strg**].

3. Klicken Sie auf die sekundäre Maustaste auf den Fehler.

4. Wählen Sie die richtige Schreibweise aus.

Der Fehler wurde im Thementext korrigiert.

## Thema-PDF herunterladen

Benutzer können eine PDF des aktuellen Themas herunterladen, um sie zu markieren oder für andere freizugeben.

1. Klicken [!UICONTROL **Vorschau**] oben rechts auf dem Bildschirm.

2. Klicken Sie auf [!UICONTROL **PDF-Symbol**] über das Thema. Ein Dialogfeld wird angezeigt.

   ![PDF-Export](images/lesson-15/pdf-export.png)

3. Füllen Sie die Informationen für **Name der Umwandlung** oder **DITA-OT-Befehlszeilenargumente** falls erforderlich. Beachten Sie, dass eine PDF immer noch generiert wird, wenn alle Felder leer gelassen werden.

4. Klicken Sie auf [!UICONTROL **Herunterladen**]. Die PDF generiert.

5. Verwenden Sie verfügbare Symbole, um das PDF-Thema zu konfigurieren, herunterzuladen oder freizugeben.

## Suchen Sie ein Thema im Repository oder in der Zuordnung

1. Öffnen Sie das Thema.

2. Klicken Sie auf die sekundäre Maustaste auf der Registerkarte Titel .

3. Auswählen **Suchen in**.

4. Wählen Sie entweder **Repository** oder **Zuordnung** , um zur gewünschten Themenposition zu springen.

## Thema verändern

1. Nehmen Sie eine Änderung an einem Thema vor.

2. Speichern Sie das Thema.

3. Klicken Sie auf **Repository** Symbol oben links im Menü.

   ![Repository-Symbol](images/lesson-15/repository-icon.png)

4. Fügen Sie im Dialogfeld **Kommentare für neue Version**.

   ![Dialogfeld &quot;Neue Version&quot;](images/lesson-15/version-dialog.png)

5. Klicken Sie auf [!UICONTROL **Speichern**].

Die Versionsnummer wird aktualisiert.

## Versionshinweise laden

Es kann schwierig sein, den Status eines Themas nur anhand der Versionsnummer zu verfolgen. Beschriftungen erleichtern die Identifizierung des genauen Zustands eines Themas, das mehrfach überarbeitet wurde.

1. Wählen Sie eine **Ordnerprofil**.

2. Konfigurieren Sie im Ordnerprofil den XML-Editor.

   a. Wählen Sie links oben im Bildschirm Bearbeiten aus.

   b. Fügen Sie unter &quot;Beschriftungen der XML-Inhaltsversion&quot;entweder ein neues Thema hinzu oder verwenden Sie ein vorhandenes.

   ![Beschriftungen für Inhaltsversionen](images/lesson-15/version-labels.png)

3. Wählen Sie [!UICONTROL **Hochladen**].

4. Wählen Sie eine Datei wie ReviewLabels.json oder eine ähnliche. Weitere Informationen zum Erstellen einer solchen Datei finden Sie in einem anderen Video.

5. Klicken [!UICONTROL **Öffnen**].

6. Klicken [!UICONTROL **Speichern**] oben links im Bildschirm Ordnerprofil .

7. Klicken [!UICONTROL **Schließen**] oben rechts.

Versionsbeschriftungen werden jetzt geladen.

## Zuweisen von Versionsbeschriftungen

1. Versionsbeschriftungen laden.

2. Klicken Sie auf [!UICONTROL **Benutzereinstellungen**] Symbol oben links im aktuellen Thema.

   ![Ordnerprofil](images/lesson-15/folder-profile-icon.png)

3. Wählen Sie dasselbe Ordnerprofil aus, in das bereits Versionsbezeichnungen geladen wurden.

4. Stellen Sie im Dialogfeld Benutzereinstellungen sicher, dass der Basispfad auf dieselben Informationen verweist, auf die das Ordnerprofil angewendet wurde.

   ![Benutzereinstellungen](images/lesson-15/user-preferences.png)

5. Klicken Sie auf [!UICONTROL **Speichern**].

6. Veröffentlichen Sie das Thema.

7. Fügen Sie einen Kommentar hinzu und wählen Sie eine Versionsbezeichnung aus der Dropdown-Liste aus.

   ![Dialogfeld &quot;Neue Versionsbezeichnung&quot;](images/lesson-15/labels-dialog.png)

8. Klicken Sie auf [!UICONTROL **Speichern**].

Die Versionsnummer wird aktualisiert.

## Versionsverlauf und Titel anzeigen

1. Suchen Sie im linken Bereich den aktuellen Thementitel.

2. Klicken Sie auf den Titel, um das Kontextmenü zu öffnen.

3. Auswählen [!UICONTROL **Anzeigen in der Assets-Benutzeroberfläche**].

   ![Assets-Benutzeroberfläche](images/lesson-15/view-assets-ui.png)

   - Der Versionsverlauf mit Bezeichnungen wird auf der linken Seite angezeigt.

   ![Versionsverlauf](images/lesson-15/version-history.png)

4. Klicken Sie auf eine Version, um auf Optionen wie **Auf diese Version zurücksetzen** und **Vorschau der Version**.

## Neue Vorlage erstellen

Es gibt Vorlagen für Themen und Maps. Administratoren können auf Vorlagen im linken Bereich zugreifen.

1. Klicken [!UICONTROL **Vorlagen**] im linken Bereich.

2. Wählen Sie entweder Karte oder Thema aus, um das zugehörige Kontextmenü zu öffnen.

3. Klicken Sie auf , um die neue Vorlage hinzuzufügen.

   ![Neue Themenvorlage](images/lesson-15/version-history.png)

4. Füllen Sie die Felder im daraufhin angezeigten Dialogfeld aus.

Die Shell-Vorlage wird angezeigt, die Beispielinhalt und eine Beispielstruktur enthält.
