---
title: Hinzufügen und Verwalten von Zitaten in Ihrem Inhalt
description: Erfahren Sie, wie Sie Referenzen implementieren können, indem Sie Zitate zu Ihrem Inhalt hinzufügen und darauf anwenden.
source-git-commit: 85eb0228908134080f3f1e2644f3f7c37b8d7497
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 1%

---


# Hinzufügen und Verwalten von Zitaten in Ihrem Inhalt

Zitate sind Verweise auf die Informationsquelle, die zu Ihrem Inhalt hinzugefügt wird. Mithilfe von Zitaten können Sie den Autoren die Quellinformationen zuschreiben und Lesern dabei helfen, die Quellinformationen zu verfolgen. Durch das Hinzufügen von Zitaten wird der Inhalt zuverlässiger und es wird Plagiat verhindert. Sie ermöglichen es Ihnen auch, gut recherchierte Inhalte anzuzeigen.

In AEM Handbüchern können Sie Zitate hinzufügen und importieren und auf Ihren Inhalt anwenden. Sie können diese Zitate aus jeder Quelle von Büchern, Websites und Zeitschriften hinzufügen.


AEM Guides helfen Ihnen beim Bearbeiten, Anzeigen einer Vorschau und Sortieren Ihrer Zitate. Nachdem Sie Ihre Zitate in den Inhalt eingefügt haben, können Sie die Ausgabe mithilfe der nativen PDF generieren. Sie können auch die Bibliografie- oder Referenzseite in der Ausgabe Native PDF hinzufügen.

AEM Guides unterstützt mehrere Arten von Zitaten, wie z. B. Modern Language Association (MLA), American Psychological Association (APA), Chicago, Institute for Electrical and Electronics Engineers (IEEE) und American Heart Association (AHA). Es wird empfohlen, sie klar und konsistent zu verwenden.


>[!NOTE]
>
>Derzeit unterstützt AEM Guides nur natives PDF für Zitate.


## Zitate hinzufügen

Gehen Sie wie folgt vor, um Zitate hinzuzufügen:

1. Wählen Sie die **Zitate** ![Zitatensymbol](images/citations-icon.svg) im linken Bereich.
Die **Zitate** -Bedienfeld geöffnet.

   ![](images/citation-panel.png){width="300" align="left"}

1. Im **Zitate** Bereich, wählen Sie ![Symbol &quot;Hinzufügen&quot;](images/Add_icon.svg). Im Dropdown-Menü haben Sie die Möglichkeit, einen neuen Zitat hinzuzufügen oder einen Zitat zu importieren.

1. Auswählen **Neue Bezeichnung** um eine neue Zitate hinzuzufügen.
Die **Erwähnung hinzufügen** wird geöffnet.

   ![Teilnahmebereich im Web-Editor](images/citation-add.png) {width="300" align="left"}


1. Füllen Sie die Felder im **Erwähnung hinzufügen** Dialogfeld.

   >[!NOTE]
   >
   >Sie können auch die ISBN-, DOI- oder PubMed-ID hinzufügen. AEM Guides füllen die anderen Felder automatisch aus.

   | Buch | Website | Journal |
   | --- | ---|---|
   | **Quelle** <br> Wählen Sie aus der Dropdown-Liste die Quelle des Zitats als Buch aus. | **Quelle**<br> Wählen Sie aus der Dropdown-Liste die Quelle des Zitats als Website aus. | **Quelle** <br> Wählen Sie aus der Dropdown-Liste die Quelle des Zitats als Journal aus. |
   | **Suchen nach** <br> Auswählen **ISBN** oder **DOI** aus der Dropdown-Liste, um nach der digitalen ID zu suchen, die mit der Erwähnung verknüpft ist.  <br> DOI: Digital Object Identifier <br> ISBN: Unique Numeric Book Identifier | **Suchen nach** <br> Auswählen **DOI** aus der Dropdown-Liste, um nach der digitalen ID zu suchen, die mit der Erwähnung verknüpft ist. | **Suchen nach** <br> Auswählen **DOI** oder PubMed-ID aus der Dropdown-Liste aus, um nach der digitalen ID zu suchen, die mit der Erwähnung verknüpft ist. <br>  <br> |
   | **Autor** <br> Fügen Sie den Vor- und Nachnamen des Autors der Zitat hinzu. Auswählen ![](images/Add_icon.svg) um weitere Namen hinzuzufügen. | **Autor** <br> Fügen Sie den Vor- und Nachnamen des Autors der Zitat hinzu. Auswählen ![](images/Add_icon.svg)  um weitere Namen hinzuzufügen. | **Autor** <br> Fügen Sie den Vor- und Nachnamen des Autors der Zitat hinzu. Auswählen ![](images/Add_icon.svg)um weitere Namen hinzuzufügen. |
   | **Titel** <br> Fügen Sie den Titel des Buches hinzu. | **Titel** <br> Fügen Sie den Titel der Webseite hinzu. | **Titel** <br> Fügen Sie den Titel des Artikels hinzu. |
   | **Bearbeiter** <br> Fügen Sie den Herausgeber des Buches hinzu. | **Website-Name** <br> Fügen Sie den Namen der Website hinzu. | **Journaltitel** <br> Fügen Sie den Titel des Werkes hinzu, in dem der Artikel gefunden wird. |
   | **Edition** <br> Fügen Sie die Ausgabe des Buches hinzu. | **URL** <br> Fügen Sie den Weblink der Website hinzu, um den Inhalt zu durchsuchen. | **Jahr** <br> Fügen Sie das Jahr hinzu, in dem der Artikel veröffentlicht wird. |
   | **Ort** <br> Fügen Sie die Stadt der Veröffentlichung hinzu. | **Aufrufdatum**<br> Fügen Sie das Datum hinzu, an dem auf den Inhalt der Website zugegriffen wird. | **Lautstärke** <br> Fügen Sie das Volumen der Arbeit in der Reihe hinzu. |
   | **Herausgeber** <br> Fügen Sie den Namen des Herausgebers des Buches hinzu. | **Veröffentlichungsdatum** <br> Fügen Sie das Datum hinzu, an dem der Inhalt der Website veröffentlicht wird. | **Zahl** <br> Fügen Sie die Anzahl der Lautstärke innerhalb der Serie hinzu. |
   | **Jahr** <br> Fügen Sie das Jahr hinzu, in dem das Buch veröffentlicht wird. | **Aktualisiertes Datum** <br> Fügen Sie das Datum hinzu, an dem der Inhalt der Website aktualisiert wird. | **Seiten** <br> Fügen Sie die Seitenzahl oder den Seitenbereich hinzu, in dem der Artikel gefunden wird. |
   | **Version** <br> Fügen Sie die Version des Buches hinzu. | **Eindeutige ID** <br> Fügen Sie eine eindeutige ID für die Erwähnung hinzu. Eine eindeutige ID ist eine eindeutige Kennung für diese Erwähnung. | **URL** <br>Fügen Sie den Web-Link zum Protokoll hinzu. |
   | **Serie** <br>Fügen Sie die Reihe des Buches hinzu. |  | **Eindeutige ID** <br> Fügen Sie eine eindeutige ID für die Erwähnung hinzu. Eine eindeutige ID ist eine eindeutige Kennung für diese Erwähnung. |
   | **URL**  <br>  Fügen Sie den Web-Link zum Buch hinzu. |
   | **Eindeutige ID** <br> Fügen Sie eine eindeutige ID für die Erwähnung hinzu. Eine eindeutige ID ist eine eindeutige Kennung für diese Erwähnung. |





1. Klicken Sie auf **Fertig**.

   Dem Feld &quot;Zitat&quot;wird ein neuer Zitat hinzugefügt.

>[!NOTE]
>
> Das Hinzufügen einer eindeutigen ID für das Feld &quot;citation&quot;ist obligatorisch.  Sie können die eindeutige ID nicht mehr ändern, nachdem die Referenz hinzugefügt wurde.

## Einfuhrauflistungen

Gehen Sie wie folgt vor, um Zitate zu importieren:

1. Wählen Sie im linken Bereich die Option **Zitate** ![Zitatensymbol](images/citations-icon.svg).

   Die **Zitate** -Bedienfeld geöffnet.

1. Im **Zitate** Bereich, wählen Sie ![Symbol &quot;Hinzufügen&quot;](images/Add_icon.svg)und wählen Sie **Import** aus dem Dropdown-Menü aus.
1. Durchsuchen Sie eine .bib-Datei von Ihrem System und importieren Sie sie .

   >[!TIP]
   >
   > Eine .bib-Dateinamenerweiterung ist eine BibTeX Bibliografische Datenbankdatei. Es handelt sich dabei um eine speziell formatierte Textdatei, die Verweise auf eine bestimmte Informationsquelle auflistet.

   Nachdem die Datei erfolgreich importiert wurde, können Sie die Verweise im Fenster &quot;Zitate&quot;anzeigen.

   >[!NOTE]
   > <ol><li> AEM Guides importiert nur die Zitate, die einzigartig sind und noch nicht vorhanden sind.
    &gt; <li> AEM Guides können Zitate aus einem Buch, einer Zeitschrift oder einer Website importieren. Derzeit werden Zitate aus anderen Quellen nicht unterstützt.

## Zitate verwalten

Die Zitate werden in der linken Leiste alphabetisch sortiert. Suchen Sie nach den Zitaten entsprechend den Quellen, die für Ihr Thema verwendet werden sollen.

### Filter

Wählen Sie die **Filter** ![](images/filter-search-icon.svg) neben der Suchleiste und wählen Sie die Quelloptionen aus der Dropdown-Liste aus, um die Zitate-Liste zu filtern. Sie ermöglicht sowohl eine als auch mehrere Auswahlen.

* **Alle Quellen**: Es wird eine vollständige Liste der Zitate einschließlich aller Quellen angezeigt.

* **Buch**: Zeigt die Liste der aus Büchern stammenden Zitate an.

* **Webseite**: Zeigt die Liste der von Websites stammenden Zitate an.

* **Protokoll**: Zeigt die Liste der Zitate aus Zeitschriften an.

### Suchen

Durchsuchen Sie die Zitate nach Ihrem Inhalt.

1. Wählen Sie im linken Bereich die Option &quot;Zitate&quot;.
Die **Zitate** -Bedienfeld geöffnet.

1. Verwenden Sie die Suchleiste, um in einer langen Liste nach der entsprechenden Erwähnung zu suchen.

### Bearbeitungsstil ändern {#change-citation-style}

Ihr Systemadministrator kann den Stil von Zitaten aus dem **Zitate**  Dropdown im **Allgemeine Einstellungen** im **Editor-Einstellungen**.
Diese Stile bestimmen, wie Zitate im Vorschaufenster oder in der nativen PDF-Ausgabe angezeigt werden.

Die folgenden Optionen sind im Dropdown-Menü verfügbar:

| MLA | APA | Chicago | IEEE | AHA |
|---|---|---|---|---|
| Modern Language Association Style <br> | American Psychology Association Style | Chicago Manual of Style | Institut für Elektrotechnik und Elektroniktechnik | American Heart Association Style |
| Beispiel:<br> Crawford, Claire, et al. *Emotionaler Inhalt dunkler Erinnerungen*.Edited by Memory, vol 16, 2010, Amsterdam. | Beispiel: <br> Crawford, C., J., &amp; , C. (2010). *Emotionaler Inhalt dunkler Erinnerungen* (505-16 ed.). 10.1080/ 09658210902067289 | Beispiel: <br> Crawford, Claire, et al. *Emotionaler Inhalt dunkler Erinnerungen*. 505-16, 2010. | Beispiel: <br> C. Crawford, J. und C. , *Emotionaler Inhalt dunkler Erinnerungen*. Amsterdam, 2010. | Beispiel: <br> C. Crawford, J. und C. , *Emotionaler Inhalt dunkler Erinnerungen*. Amsterdam, 2010. |


## Bearbeiten von Zitaten

Gehen Sie wie folgt vor, um die Zitate zu bearbeiten:

1. Bewegen Sie den Mauszeiger über den Namen der Zitation aus der Liste. Auswählen  ![](images/options.svg) die **Optionen** Symbol.

1. Wählen Sie **Bearbeiten** aus.

Die **Zitat bearbeiten** wird geöffnet.

1. Nehmen Sie die erforderlichen Änderungen vor. Klicken Sie auf **Fertig**.
Die ausgewählte Zitat wird bearbeitet.

>[!NOTE]
>
>Sie können die eindeutige ID nicht mehr ändern, nachdem die Referenz hinzugefügt wurde.

## Vorschau einer Zitation anzeigen

Gehen Sie wie folgt vor, um eine Zitate in der Vorschau anzuzeigen:

Bewegen Sie den Mauszeiger über den Namen der Zitation aus der Liste. Auswählen     ![](images/options.svg) **Optionen** Symbol.

1. Wählen Sie **Vorschau**.
Sie können den Inhalt und das Format der Zitate im Vorschaufenster in der Vorschau anzeigen.

   >[!NOTE]
   >
   >Die Vorschau basiert auf dem Zitat-Stil, den Ihr Administrator in der Variablen **Editor-Einstellungen**.

1. Klicken Sie auf eine beliebige Stelle auf dem Bildschirm, um das Vorschaufenster zu schließen.

   ![](images/citation-preview.png){width="550" align="left"}

>[!NOTE]
>
> Sie können auch eine Vorschau einer in ein Thema eingefügten Zitation über die Assets-Benutzeroberfläche oder die Registerkarte Vorschau des Web-Editors anzeigen.

## Zitate einfügen

Führen Sie die folgenden Schritte aus, um Zitate in ein Thema einzufügen:
1. Wählen Sie das Thema im Repository-Bedienfeld aus und doppelklicken Sie dann auf , um es im Bearbeitungsfenster zu öffnen.
1. Setzen Sie den Cursor an die Stelle des Themas, an der Sie die Referenz hinzufügen möchten.



Sie können Zitate zum Thema über die Hauptsymbolleiste oder das linke Bedienfeld einfügen.

### In der Symbolleiste

1. Wählen Sie die **Zitate** ![Zitatensymbol ](images/citations-icon.svg) in der Hauptsymbolleiste.
1. Im **Zitate** wählen Sie den Titel aus. Sie können auch mehrere Zitate auswählen.
   ![Anführungsdialogfeld](images/citation-dialog-main-toolbar.png){width="300" align="left"}
1. Sie können Zitate filtern, indem Sie die ersten Buchstaben im Suchbereich der **Zitat** Dialogfeld.

1. Klicken Sie auf **Fertig**.
Die ausgewählte Erwähnung wird an der Cursorposition in Ihrem Thema hinzugefügt.


### Im linken Bereich

>[!NOTE]
> 
>So zeigen Sie die **Zitate** im linken Bereich angezeigt, muss Ihr Systemadministrator die **Zitate** in der **Bedienfelder** Registerkarte in **Editor-Einstellungen**.

1. Auswählen **Zitate** ![Zitatensymbol ](images/citations-icon.svg) im linken Bereich.
1. Ziehen Sie die Zitate aus der **Zitate** und legen Sie es an der entsprechenden Stelle im Thema ab.

   Sie können auch **Einfügen** von  ![](images/options.svg) **Optionen** , um eine Zitate einzufügen.

   ![Zitate einfügen](images/citation-panel-insert.png)
1. Um mehrere Zitate auszuwählen, klicken Sie mit der rechten Maustaste auf eine Zitation im Thema und wählen Sie **Änderungsbeschriftung** aus dem Kontextmenü.
1. Wählen Sie die einzufügenden Zitate aus der **Zitat** angezeigt.
1. Auswählen **Fertig** , um sie zum Thema hinzuzufügen.

Nachdem Sie die Zitate in das Thema eingefügt haben, können Sie sie im Web-Editor in der Vorschau anzeigen. Sie können auch Inhalte mit Zitaten mithilfe des nativen PDF veröffentlichen.



## Zitat löschen

Sie können Zitate aus dem Bereich &quot;Zitate&quot;oder aus einem Thema löschen, das Sie eingefügt haben.

### Zitate aus dem Bereich &quot;Zitate&quot;löschen

Gehen Sie wie folgt vor, um eine Zitate aus dem Bereich &quot;Zitate&quot;zu löschen:

1. Bewegen Sie den Mauszeiger über den Namen der Zitation aus der Liste.
1. Wählen Sie die ![](images/options.svg) **Optionen** Symbol.
1. Wählen Sie die   **Löschen** ![](images/Delete_icon.svg).
Das Bestätigungsdialogfeld wird geöffnet.
1. Auswählen **Ja**.
Die ausgewählte Zitation wird aus dem Zitate-Panel gestrichen.



### Zitate aus einem Thema löschen

Gehen Sie wie folgt vor, um eine bereits im Thema verwendete Zitation zu löschen:

Platzieren Sie im Thema den Cursor am Ende des Zitats.

1. Klicken Sie mit der rechten Maustaste auf eine Erwähnung des Themas und wählen Sie **Änderungsbeschriftung** aus dem Kontextmenü. Das Dialogfeld Zitat wird geöffnet.
   ![Kontextmenü einer Erwähnung](./images/modify-citation.png)

1. Sie können die Zitate auswählen, die Sie in das Dokument einfügen möchten.

   >[!NOTE]
   >
   >Die bereits im Thema verwendeten Zitate werden durch die im Dialogfeld ausgewählten Aktionen ersetzt.


1. Klicken Sie auf **Fertig**.

## Generieren der Ausgabe von Inhalten mit Zitaten

Nachdem Sie Zitate in das Thema eingefügt haben, können Sie Inhalte mit Zitaten mithilfe von Native PDF veröffentlichen.

In der nativen PDF-Ausgabe erscheinen die Zitate in dem Inhalt, in den Sie sie eingefügt haben. Sie können auch eine Bibliografie-Seite erstellen. Wenn Sie auf eine beliebige Erwähnung klicken, werden Sie zur bibliography-Seite weitergeleitet.

Erstellen Sie eine **Zitate** Seitenlayout in den PDF-Vorlagen und fügen Sie sie in Ihr Dokument ein. Alle im Buch verwendeten Zitate werden auf einer Seite aufgelistet, die in der PDF-Ausgabe erscheint. Weitere Informationen zum Erstellen eines Seitenlayouts finden Sie unter [Seitenlayout erstellen](../native-pdf/components-pdf-template.md#create-page-layout).


Um die Ansicht und das Erscheinungsbild der Zitationsseite zu ändern, zeigen Sie [PDF-Vorlagen anpassen](../native-pdf/pdf-template.md).



### Anwenden des Inhaltsstils auf eine Erwähnung

Wenden Sie Formatierungen auf die Zitate an, wenn sie zum Thema hinzugefügt werden.

1. Auswählen **Stylesheets** im **Vorlagen** -Bedienfeld einer nativen PDF-Ausgabevorgabe.   Er öffnet die **STILE** -Bereich, der alle Stiloptionen enthält.

1. Suchen Sie im Suchbereich nach `<cite>`.

Weitere Informationen zu Stilen finden Sie unter [Arbeiten mit allgemeinen Inhaltsstilen](../native-pdf/stylesheet.md).