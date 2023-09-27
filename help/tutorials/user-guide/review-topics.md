---
title: Prüfungsthemen
description: Erfahren Sie, wie Sie Themen überprüfen und die Funktionen als Prüfer, Dokumentansicht, Themenansicht, kontextbezogene Symbolleiste, Vorschaumodus, Hinzufügen von Anlagen zu Kommentaren und Bedingungsbedienfeld in AEM Handbüchern verwenden.
exl-id: ca94ec2e-cd45-418d-9b35-73d587ba51ec
source-git-commit: 8504a0a52d381044bf1f0d6e7de3585ebecf3a7b
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 0%

---

# Prüfungsthemen {#id2056B0W0FBI}

Wenn Sie Überprüfer sind, erhalten Sie eine E-Mail mit einer Überprüfungsanfrage mit dem Link zu den Prüfungsthemen. Durch Klicken auf den Link gelangen Sie zur Überprüfungsseite, auf der Sie Ihr Feedback zu den freigegebenen Themen hinzufügen können.

Führen Sie die folgenden Schritte aus, um ein Thema zu überprüfen:

1. Klicken Sie auf den direkten Link in der E-Mail mit der Überprüfungsanforderung.

   Der Themen- oder Zuordnungslink wird in einem Browser geöffnet.

   >[!NOTE]
   >
   > Sie können auch über Ihren Benachrichtigungsbereich im Posteingang in der AEM-Benutzeroberfläche auf den Link zur Themenüberprüfung zugreifen.

1. Je nachdem, wie die Themenüberprüfung initiiert wird, können Sie einen der folgenden beiden Bildschirme sehen:

   >[!NOTE]
   >
   > Die Benutzeroberfläche kann sich unterscheiden, wenn Sie die Überprüfung in erstellt haben:
   >
   > - AEM Handbücher as a Cloud Service Version November 2022 oder früher
   > - AEM Guides Version 4.1 oder früher



   Der folgende Bildschirm wird angezeigt, wenn eine DITA-Zuordnung zum Initiieren des Überprüfungs-Workflows verwendet wird:

   ![](images/multiple-topics-review.png){width="800" align="left"}

   Auf diesem Bildschirm stehen die folgenden Optionen zur Verfügung:

   - **A**: Der Name der Prüfungsaufgabe.
   - **B**: Klicken Sie auf das Symbol &quot;Themenansicht&quot;, um den Themenbereich ein- oder auszublenden.

   - **C**: Sie können nach dem erforderlichen Thema suchen, indem Sie einen Teil des Textes des Titels oder Dateipfads in die Suchleiste eingeben.

     Auswählen  ![](images/view-options.svg) in der Nähe der Suchleiste, um alle Themen oder Themen mit Kommentaren anzuzeigen. Standardmäßig können Sie alle in der Prüfungsaufgabe vorhandenen Themen anzeigen.


   - **D**: Die Zahlen, die durch ***F*** können gefiltert werden, indem Sie die gewünschte Filteroption von hier aus auswählen. Sie können Kommentare nach Typ, Status, Überprüfer oder Version filtern. Wenn Sie z. B. sehen möchten, wie viele Durchstreichen-Kommentare in jedem der unter &quot;Überprüfen&quot;-Themen abgegeben wurden, klicken Sie auf das Filtersymbol und wählen Sie dann **Überprüfungstyp** \> **Löschen**.

     >[!NOTE]
     >
     > Beim Anwenden der Filter werden nur die Kommentare angezeigt, die mit den ausgewählten Filtern übereinstimmen. Die Anzahl der gefilterten Kommentare wird links im Themenbereich angezeigt.

   - **E**: Ein Thema, das dem aktuellen Überprüfer zur Überprüfung zugewiesen ist, wird schwarz angezeigt und kann angeklickt werden. Wenn der Validierer auf einen Themenlink klickt, wird das Thema an den Anfang des Bildschirms gebracht.
   - **F**: Ein Thema, das nicht zur Überprüfung verfügbar ist, ist ausgegraut. Das Thema wird im schreibgeschützten Modus angezeigt und Sie dürfen zu solchen Themen keine Überprüfungskommentare hinzufügen.

   - **G**: Anzahl der Kommentare zu einem Thema. Diese Zahl ändert sich je nach angewendetem Filter.

   Alle Themen in der Karte werden als ein einziges zusammengesetztes Dokument angezeigt. Die Themen, die der Validierer überprüfen darf, werden normal angezeigt. Die Themen, die der Review nicht überprüfen darf, werden nicht angezeigt.

   ![](images/review-read-only.png){width="800" align="left"}

   Im obigen Screenshot wird das Thema &quot;Allgemeine Beschreibung&quot;für die Überprüfung des aktuellen Validierers freigegeben, was normal angezeigt wird. Das nächste Thema, Verlauf des Fluginhalts, wird jedoch nicht zur Überprüfung freigegeben und im schreibgeschützten Modus angezeigt. Das Thema, das derzeit im Fokus ist, wird auch im Inhaltsverzeichnis hervorgehoben.

   Der folgende Bildschirm wird angezeigt, wenn ein Thema oder mehrere Themen ausgewählt und zur Überprüfung freigegeben werden:

   ![](images/review-composite-view.png){width="800" align="left"}

   >[!NOTE]
   >
   > Bei mehreren Themen werden sie in der Dokumentansicht als ein zusammengesetztes Dokument angezeigt. Im obigen Screenshot werden zwei verschiedene Themen hervorgehoben, die nacheinander in einer Ansicht dargestellt werden.

1. Öffnen Sie das Fenster Kommentare , indem Sie auf die **Kommentare** rechts oben in der Symbolleiste.

   Geben Sie Überprüfungskommentare ein, indem Sie in der Symbolleiste einen geeigneten Kommentartyp auswählen und die Eingabetaste drücken, um Ihren Kommentar einzureichen.

   >[!NOTE]
   >
   > Im Bereich &quot;Kommentare&quot;werden nur die Kommentare zu den aktuellen Themen angezeigt. Wenn Sie den Fokus auf ein anderes Thema verschieben, werden die Kommentare zum anderen Thema angezeigt.

1. Klicks **Schließen** nach Abschluss der Überprüfung des Themas. Beim Klicken auf **Schließen** auf, werden Sie zu der Seite weitergeleitet, von der Sie auf das Prüfungsthema zugegriffen haben.

## Zusätzliche Funktionen auf dem Prüfungsbildschirm

**Dokumentansicht und Themenansicht** - Wenn mehrere Themen zur Überprüfung freigegeben werden, wird den Validierern standardmäßig eine zusammengesetzte Dokumentansicht der Themen angezeigt. Bei einer DITA-Map-Überprüfung werden alle Themen in der Karte in Form eines einzigen Dokuments präsentiert, das einer Buchansicht ähnelt. Wenn Sie möchten, können Sie auch auf ein bestimmtes Thema klicken und nur dieses Thema wird dann auf dem Prüfungsbildschirm angezeigt.

Wenn Sie ein einzelnes Thema anzeigen, erhalten Sie eine zusätzliche Option, um zur Dokumentansicht zurückzukehren. Im folgenden Screenshot wird ein bestimmtes Thema aus einer Map-Datei zur Überprüfung geöffnet. Die hervorgehobene Option — **Dokumentansicht anzeigen** ermöglicht dem Benutzer, zur Dokumentansicht der Zuordnungsdatei zurückzukehren.

![](images/switch-document-view.png){width="800" align="left"}

**Arbeiten mit verschiedenen Arten von Kommentar-Tools** - Sie können Inline-Kommentare hinzufügen, indem Sie Text markieren, Text durchstreichen, Text einfügen oder eine Kommentar-Anmerkung hinzufügen. Die verschiedenen in der Symbolleiste &quot;Kommentare&quot;verfügbaren Tools für die Kommentarbearbeitung werden nachfolgend beschrieben:

![](images/comments-toolbar.png){width="350" align="left"}

- **Hervorheben** \(![](images/review-highlight-icon.svg)\): Um einen Hervorhebungskommentar hinzuzufügen, wählen Sie den Text aus und klicken Sie auf das Symbol Hervorheben . Oder klicken Sie auf das Symbol Hervorheben und wählen Sie den gewünschten Text aus:

  ![](images/highlight-comment.png){width="650" align="left"}

  Im Fenster Kommentare wird ein Popup angezeigt, in dem Sie Ihren Kommentar für den hervorgehobenen Inhalt hinzufügen können.

- **Durchstreichen** \(![](images/review-text-strike-through-icon.svg)\): Wenn Sie das Entfernen von Inhalten vorschlagen möchten, wählen Sie den Inhalt aus und klicken Sie auf das Symbol Durchstreichen . Wählen Sie alternativ den gewünschten Text aus und klicken Sie auf die Entf-Taste:

  Im Fenster Kommentare wird ein Popup angezeigt, in dem Sie Ihren Kommentar für den gelöschten Inhalt hinzufügen können.

- **Text einfügen** \(![](images/review-insert-text-icon.svg)\): Wenn Sie Text einfügen möchten, klicken Sie auf das Symbol Text einfügen und platzieren Sie den Cursor an die Stelle, an der Sie den Text einfügen möchten, und geben Sie ihn in die Informationen ein. Oder platzieren Sie den Cursor an die Stelle, an der Sie Text einfügen und mit der Eingabe beginnen möchten. Die hinzugefügten Informationen werden in grüner Schriftart angezeigt:

- **Kommentar hinzufügen**\(![](images/review-comment-icon.svg)\): Wenn Sie einen Kommentartyp mit Kurznotiz hinzufügen möchten, klicken Sie auf das Symbol Kommentar hinzufügen und geben Sie den Kommentar in das Popup ein.


**Kontextuelle Symbolleiste**

Mit der dedizierten Symbolleiste können Sie Text auch schnell hervorheben oder durchsuchen. Führen Sie die folgenden Schritte aus, um Kommentare über die dedizierte Symbolleiste zu erstellen:

1. Wählen Sie den Text aus, den Sie markieren oder durchstreichen möchten. Die dedizierte Symbolleiste wird angezeigt.

   ![](images/review-quick-launch-toolbar.png){width="550" align="left"}

1. Klicken Sie auf **Hervorheben** oder **Durchstreichen** Symbol.
1. Sie können Kommentare zum Hervorheben oder Durchstreichen im Kommentarbereich hinzufügen.

**Überprüfen mithilfe des Bedienfelds &quot;Kommentare&quot;** - Im Bereich &quot;Kommentare&quot;wird eine Liste mit Kommentaren zum aktuellen Thema angezeigt. In diesem Bedienfeld werden auch Kommentare von anderen Validierern aufgelistet, wenn das Thema an mehrere Validierungsverantwortliche gesendet wird. Jeder Kommentar im Kommentarbereich ist mit dem entsprechenden Text im aktuellen Thema verknüpft. Sie können damit den kommentierten Text identifizieren. Jeder Kommentar zeigt den Namen des Validierers an, der den Kommentar hinzugefügt hat, sowie den Zeitstempel.

Die Kommentare werden in der Reihenfolge des kommentierten Texts im Dokument angezeigt. Zum Beispiel gibt es einen Hervorhebungskommentar zum ersten Satz und einen Einfügetext-Kommentar zum zweiten Satz im ersten Absatz. Dann wird der Hervorhebungstext-Kommentar vor dem eingefügten Textkommentar angezeigt.

Die Aufgaben, die Sie mit dem Bereich &quot;Kommentare&quot;ausführen können, werden unten beschrieben:

- Wenn Sie auf einen Kommentar klicken, wird der Speicherort des entsprechenden Kommentars im Dokument hervorgehoben und angezeigt.
- Sie können Antworten zu Kommentaren hinzufügen.
- Sie können Ihren eigenen Kommentar bearbeiten, indem Sie auf den Kommentar-Text im Fenster &quot;Kommentare&quot;klicken und dann **Bearbeiten** über das Menü &quot;Optionen&quot;.
- Sie können Ihre eigenen Kommentare löschen, indem Sie auf den Kommentar im Fenster &quot;Kommentare&quot;klicken und dann die **Löschen** im Menü &quot;Optionen&quot;.

  ![](images/review-comment-options-menu.png){width="300" align="left"}

  >[!NOTE]
  >
  > Das Menü Optionen wird nur angezeigt, wenn Sie den Mauszeiger über Ihre eigenen Kommentare bewegen. Sie wird von anderen Validierern nicht für die Kommentare angezeigt.

- Alle teilnehmenden Benutzer können auf Kommentare anderer Benutzer antworten. Klicken Sie in einem Kommentar auf **Antwort** und drücken Sie die Eingabetaste , um eine Antwort zu senden.

**Vorschaumodus**

- Wenn Sie ein Thema im Vorschaumodus öffnen, wird gezeigt, wie ein Thema angezeigt wird, wenn es von einem Autor nach Anwendung aller Änderungen angezeigt wird. So wird beispielsweise der gesamte eingefügte Text als normaler Text angezeigt und der gesamte Text, der durch &quot;\(gelöscht\)&quot;abgeschnitten wurde, wird aus dem Inhalt entfernt.

- Der folgende Screenshot zeigt den Inhalt in *Überprüfen* mode:

![](images/review-author-mode.png){width="550" align="left"}

Der folgende Screenshot zeigt den Inhalt in *Vorschau* mode:

![](images/review-preview-mode.png){width="550" align="left"}

**Hinzufügen von Anlagen zu Kommentaren** - Wenn Sie Ihren Kommentar durch zusätzliche Informationen ergänzen möchten, die in einer anderen Datei verfügbar sind, können Sie dies tun, indem Sie ihn mit Ihrem Kommentar hinzufügen. Als Validierer können Sie einfach eine oder mehrere Dateien aus Ihrem lokalen System zu Ihrem Kommentar hinzufügen. Eine Datei kann allen unterstützten Formen von Kommentaren hinzugefügt werden: Hervorheben, Durchstreichen, Text einfügen oder ein Kommentar.

Wenn Sie einen Kommentar einfügen, wird das Kommentar-Popup angezeigt. Nachdem Sie im Popup zusätzliche Kommentare oder Informationen bereitgestellt haben, senden Sie sie durch Drücken der Eingabetaste. Nachdem der Kommentar hinzugefügt wurde, erhalten Sie die Möglichkeit, diesem Kommentar eine Anlage hinzuzufügen.

![](images/comment-pop-up-panel.png){width="800" align="left"}

Im obigen Screenshot enthält das Dokument das Popup-Fenster des Hervorhebungskommentars und der Kommentar wird auch im Fenster &quot;Kommentare&quot;hinzugefügt. Symbol für Dateianlagen ![](images/file-attach-review.svg)ist zusammen mit dem Kommentar an beiden Orten verfügbar.

Führen Sie die folgenden Schritte aus, um Ihrem Kommentar Anlagen hinzuzufügen:

1. Klicken Sie auf *Anhang hinzufügen* icon ![](images/file-attach-review.svg) auf den Kommentar, mit dem Sie einen Anhang hinzufügen möchten.

   Das Dialogfeld &quot;Datei öffnen&quot;wird angezeigt.

1. Wählen Sie eine oder mehrere Dateien aus, die Sie anhängen möchten.

   Die ausgewählten Dateien werden zusammen mit dem Kommentar im Bereich &quot;Kommentare&quot;angezeigt.

   Im Bereich &quot;Kommentare&quot;können Sie den Dateinamen und die zugehörige Größe sehen. Sie können auch eine Datei entfernen, indem Sie auf das Löschsymbol klicken ![](images/Delete_icon.svg) mit dem Dateinamen verknüpft ist.

1. Klicken Sie auf **Senden**.

   Die Anlagen werden hochgeladen und zum Kommentar hinzugefügt.


**Weitere Hinweise zum Arbeiten mit Anlagen:**

- Standardmäßig werden nur zwei Dateien mit einem Kommentar angezeigt. Wenn es weitere Dateien gibt, dann **Anlage anzeigen** auf der rechten Seite die Anzahl aller Anlagen \(die mehr als zwei\ sind), die mit dem Kommentar verknüpft sind. Sie können auf die Zahl klicken, um alle Anlagen anzuzeigen. Wenn Sie beispielsweise vier Anlagen mit einem Kommentar haben, sehen Sie +2 auf der Schaltfläche.

![](images/review-view-attachment.png){width="550" align="left"}

- Wenn Sie den Mauszeiger über einen Anhang bewegen, haben Sie die Möglichkeit, den Anhang herunterzuladen oder zu entfernen. Das Entfernen des Anhangs ist nur verfügbar, wenn der aktuelle Überprüfer diesen Kommentar hinzugefügt hat, wie im folgenden Screenshot gezeigt:

![](images/current-user-comment-options.png){width="550" align="left"}

Die anderen Validierer oder Autoren erhalten nur die Option zum Herunterladen von Anlagen.

![](images/other-reviewer-download.png){width="550" align="left"}

- Sie können alle Anlagen, die mit einem Kommentar verknüpft sind, aus der **Anlagen anzeigen** angezeigt. Wählen Sie die Anlagen aus und klicken Sie auf die **Herunterladen** auf der Kommentarebene.

- Sie können die Anlagen, die mit einem Kommentar verknüpft sind, auch aus dem **Anlagen anzeigen** angezeigt. Wählen Sie die Anlagen aus und klicken Sie auf die **Löschen** Symbol.

![](images/attach-files-comments-panel.png){width="550" align="left"}


**Bedingungsbedienfeld** - Wenn Ihr Thema bedingte Inhalte enthält, wird Ihnen die **Bedingungen** \(![](images/conditions-icon.svg)\) rechts. Klicken auf **Bedingungen** -Symbol öffnet das Bedienfeld Bedingungen , in dem Sie den Inhalt gemäß den verfügbaren Bedingungen im Thema hervorheben können.

: Standardmäßig **Alle Bedingungen hervorheben** aktiviert ist, werden alle Bedingungen ausgewählt, der gesamte Inhalt angezeigt und der konditionierte Inhalt wird sowohl im Vorschau- als auch im Vorschaumodus hervorgehoben dargestellt.

: Sie können **Alle Bedingungen hervorheben** und sehen Sie alle im Thema vorhandenen Inhalte als normalen Text ohne Highlights.

![](images/review-conditions-panel.png){width="350" align="left"}

Sie können eine bestimmte Bedingung ein- oder ausblenden.

- Wenn Sie eine Bedingung ausblenden, wird der Inhalt mit dieser Bedingung im Überprüfungsmodus nicht hervorgehoben.
- Wenn Sie eine Bedingung anzeigen, wird der konditionierte Inhalt im Überprüfungsmodus hervorgehoben. Im folgenden Screenshot verwendet nur der Inhalt zwei Bedingungen: `win` und `mac` hervorgehoben ist.


![](images/review-condition-normal-mode.png){width="650" align="left"}

Im Vorschaumodus werden der nicht konditionalisierte Inhalt und der konditionalisierte Inhalt, der die beiden angezeigten Bedingungen verwendet - `win` und `mac` angezeigt. Der verbleibende bedingte Inhalt, für den die Bedingungen ausgeblendet sind, wird nicht angezeigt.

**Echtzeitüberprüfung** - Das Fenster Kommentare wird in Echtzeit mit Kommentaren und dem Feedback oder der Aktion aktualisiert, die der Autor zu den Kommentaren durchgeführt hat.

- Mehrere Überprüfer können Kommentare hinterlassen oder auf Kommentare gleichzeitig zum selben Dokument antworten. Sie können ermitteln, wer das Dokument derzeit überprüft, indem Sie den Mauszeiger über das Benutzersymbol in der oberen rechten Ecke des Bildschirms bewegen.

- Wenn ein Thema Teil mehrerer Prüfungsaufgaben ist, werden die in einer Aufgabe vorgenommenen Kommentare in der anderen Aufgabe nicht angezeigt.

- Klicken Sie auf das Symbol Veralteter Kommentar \(![](images/outdated-comment-icon.svg)\) zeigt die Unterschiede zwischen der neuesten und der kommentierten Version des Dokuments an. Die Versionsnummern \(der verglichenen Versionen\) werden oben in den Dokumenten angezeigt.

  ![](images/comments-page-review-mode.png){width="800" align="left"}

  >[!NOTE]
  >
  > Wenn Sie den Mauszeiger über das Symbol Veralteter Kommentar bewegen, wird die Versionsnummer des Themas angezeigt, zu dem der Kommentar hinzugefügt wurde. Wenn beispielsweise ein Kommentar zu Version 1.0 abgegeben wurde, wird derselbe Kommentar angezeigt.

- Wenn Sie auf einen veralteten Kommentar klicken, wird die Version dieses Kommentars im linken Bereich geöffnet. Die vorherige Version wird im linken Bereich angezeigt und die aktuelle Version wird im rechten Bereich angezeigt. Alle Kommentare zur veralteten Version werden links importiert. Sie können die vorherige Version mit der aktuellen Version vergleichen.

**Kommentare filtern** - Sie können Kommentare in einem Dokument filtern, um bestimmte Kommentare nach Bedarf anzuzeigen. Um Kommentare zu filtern, klicken Sie auf die **Filter** icon \(![](images/filter-search-icon.svg)\), das im Menü rechts neben dem Textfeld &quot;Suchkommentare&quot;im Bereich &quot;Kommentare&quot;angezeigt wird.

Wählen Sie eine oder mehrere der folgenden Filteroptionen aus dem **Filtertyp** Dialogfeld und klicken Sie auf **Anwenden**.

- **Überprüfungstyp** - Filtern Sie nach dem Kommentartyp - Hervorheben, Löschen, Einfügen oder Kommentar.
- **Prüfungsstatus** - Filtern Sie nach dem Status des Kommentars wie &quot;Akzeptiert&quot;, &quot;Abgelehnt&quot;oder &quot;Keine&quot;.
- **Überprüfer** - Filtern Sie nach dem Namen des Validierers.

- **Versionen** - Filtern Sie nach den Kommentaren, die zu einer bestimmten Version des Themas eingegangen sind.

  Bei Verwendung der Filter werden die Kommentare im rechten Bereich entsprechend der Auswahl gefiltert und die Anzahl der Kommentare im linken Bereich entsprechend aktualisiert.


Um den Filter zu entfernen und alle Kommentare anzuzeigen, deaktivieren Sie alle Filter aus dem **Filtertyp** Dialogfeld und klicken Sie auf **Anwenden**.

**Übergeordnetes Thema:**[ Themen oder Zuordnungen überprüfen](review.md)
