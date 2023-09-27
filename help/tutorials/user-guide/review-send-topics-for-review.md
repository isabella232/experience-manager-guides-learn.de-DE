---
title: Senden von Themen zur Überprüfung
description: Erfahren Sie in AEM Handbüchern, wie Sie eine Prüfungsaufgabe erstellen und Themen zur Überprüfung senden. Senden Sie mindestens ein Thema in einer DITA-Map zur Überprüfung.
exl-id: 7a9b36ad-44d4-4952-9906-d95feb95d0c6
source-git-commit: 8504a0a52d381044bf1f0d6e7de3585ebecf3a7b
workflow-type: tm+mt
source-wordcount: '2752'
ht-degree: 0%

---

# Senden von Themen zur Überprüfung {#id199RD0S035Z}

Der Prüfungs-Workflow erstellt eine Umgebung mit mehreren Validierern, in der der Initiator eine Liste von Themen für die Überprüfung angibt, mehrere Validierer hinzufügt und eine Zeitleiste für die Prüfungsaufgabe zuweist. AEM Handbücher ermöglichen es Benutzern, die zu den Gruppen Autoren und Herausgeber gehören, eine Überprüfung zu initiieren.

Da der Prüfungs-Workflow projektspezifisch ist, muss der Initiator der Überprüfung Teil des Projektteams sein oder über die Berechtigung zum Erstellen eines Projekts verfügen. Zum Zeitpunkt der Erstellung eines Projekts definieren Sie die Teammitglieder für das Projekt und weisen ihnen verschiedene Rollen oder Gruppen zu. Weitere Informationen zu Projekten finden Sie unter [Erstellen eines DITA-Projekts](authoring-create-dita-project.md#).

Sie können eine Prüfungsaufgabe aus folgenden Quellen erstellen:

- **Web-Editor**: Ermöglicht das Senden eines einzelnen Themas oder einer DITA-Map zur Überprüfung. Beachten Sie, dass der Workflow zum Erstellen einer Prüfungsaufgabe im Web-Editor und in der Assets-Benutzeroberfläche üblich ist. Nur die Methode zum Starten des Überprüfungs-Workflows unterscheidet sich. Informationen zum Starten des Prüfungs-Workflows über den Web-Editor finden Sie in der [Prüfungsaufgabe erstellen](web-editor-features.md#id215OCJ00JXA) im Web-Editor.

- **Assets-Benutzeroberfläche**: Ermöglicht das Senden eines oder mehrerer Themen und einer DITA-Map zur Überprüfung. Die Freigabe von Dokumenten zur Überprüfung über den Workflow der Assets-Benutzeroberfläche wird in diesem Thema behandelt.


In der Assets-Benutzeroberfläche gibt es zwei Möglichkeiten, wie ein Autor/Herausgeber eine Prüfungsaufgabe erstellen kann:

- Senden eines oder mehrerer Themen zur Überprüfung
- Senden mehrerer Themen aus einer DITA-Map zur Überprüfung

## Senden eines oder mehrerer Themen zur Überprüfung {#id1721E600FY4}

>[!IMPORTANT]
>
> Bevor Sie eine Prüfungsaufgabe erstellen, stellen Sie sicher, dass Sie ein Projekt erstellt und diesem Projekt Überprüfer hinzugefügt haben.

Um eine Prüfungsaufgabe zu erstellen und Themen zur Überprüfung zu senden, führen Sie die folgenden Schritte aus:

>[!NOTE]
>
> Sie können eine Prüfungsaufgabe nur erstellen, wenn Sie Autor oder Herausgeber eines DITA-Projekts sind.

1. Navigieren Sie in der Assets-Benutzeroberfläche zum gewünschten Ordner.

1. Klicken Sie in der Schnellaktion auf das Symbol Auswählen und wählen Sie die Themen aus, die Sie zur Überprüfung senden möchten.

   ![](images/select-asset-62.png){width="300" align="left"}

1. Klicken Sie in der Symbolleiste auf **Prüfungsaufgabe erstellen**. Die Seite zur Erstellung von Prüfungsaufgaben wird angezeigt.

   >[!NOTE]
   >
   > Sie können eine Prüfungsaufgabe nur für die Themen erstellen, die überarbeitet wurden. Wenn das ausgewählte Thema keine Revision aufweist, wird eine Eingabeaufforderung angezeigt.

   ![](images/create-review-task-023.png){width="650" align="left"}

1. Geben Sie einen **Titel** für die Aufgabe und wählen Sie eine DITA aus. **Projekt** aus der Dropdown-Liste.

1. Im **Zuweisen zu** Dropdown-Feld die Validierer auswählen, an die Sie die Themen zur Überprüfung senden möchten.

   Sie können eine Prüfungsaufgabe einzelnen Benutzern des Projekts oder Benutzergruppen zuweisen. Beachten Sie, dass Sie einzelnen Benutzern nur dann eine Prüfungsaufgabe zuweisen können, wenn Sie Teil der Administratorgruppe des Projekts sind. Andernfalls werden nur die Benutzergruppen im Feld Zuweisen zu angezeigt.

   >[!NOTE]
   >
   > Überprüfungs-Workflow ist projektspezifisch. Wenn Sie Projekte erstellen, fügen Sie die Teammitglieder zum Projekt hinzu und weisen sie Gruppen zu. Wenn Sie also das Projekt hier auswählen, können Sie die Mitglieder auswählen, die Teil dieses Projekts sind. Weitere Informationen zu Projekten finden Sie unter [Erstellen eines DITA-Projekts](authoring-create-dita-project.md#).

1. Geben Sie einen **Beschreibung** für die Aufgabe.

   Diese Beschreibung wird als Hauptteil der Benachrichtigungs-E-Mail verwendet, die an die validierungsverantwortlichen Benutzer gesendet wird.

1. Wählen Sie die **Fälligkeitsdatum** und Zeit, um die Frist für die Überprüfung festzulegen.

   >[!NOTE]
   >
   > Nach Ablauf der Frist wird dem Initiator eine E-Mail gesendet, in der er darüber informiert wird, dass die Überprüfungsaufgabe abgeschlossen wurde. Der Initiator kann den Termin für die Überprüfungsaufgabe von der [Dashboard überprüfen](review-manage-tasks-review-dashboard.md#).

1. Wählen Sie die Stammzuordnung aus der **Rootmap-Pfad**. Diese Rootmap wird verwendet, um alle wichtigen Verweise und Glossarbegriffe aufzulösen, die im Reviewinhalt verwendet werden. Wenn Sie die Rootmap nicht auswählen, werden die mit dem DITA-Thema verknüpften Schlüsselreferenzen oder Glossarbegriffe nicht aufgelöst, bevor das Thema zur Überprüfung gesendet wird.

   Wenn Sie die Überprüfung für eine DITA-Zuordnung erstellen, wird standardmäßig **Rootmap-Pfad** auf den Pfad dieser Karte festgelegt ist. Wenn Sie die Überprüfung für ein einzelnes oder mehrere Themen erstellen, wird standardmäßig die **Rootmap-Pfad** auf die in den Benutzereinstellungen definierte Zuordnung eingestellt ist.

   >[!NOTE]
   >
   > Die ausgewählte Stammzuordnung hat die höchste Priorität, um Schlüsselverweise aufzulösen. Weitere Informationen finden Sie unter [Schlüsselverweise auflösen](map-editor-other-features.md#id176GD01H05Z).

1. Da Sie verschiedene Validierer verschiedenen Themen zuweisen können, **Zuweisung zum Überprüfen von Themen zulassen** steuert, ob Überprüfer alle Themen in einer Prüfungsaufgabe oder nur die Themen überprüfen können, die ihnen zugewiesen sind.

   Wenn Sie allen Validierungsverantwortlichen erlauben möchten, ein Thema in der Prüfungsaufgabe zu überprüfen, wählen Sie **Zuweisung zum Überprüfen von Themen zulassen**.

   Wenn Sie diese Option nicht auswählen, werden die Überprüfer im **Zuweisen zu** kann nur die Themen überprüfen, die ihnen zugewiesen sind.

1. Klicken Sie auf **Weiter**.

   Die Inhaltsseite wird angezeigt.

   ![](images/content_page_review.png){width="800" align="left"}

1. Wählen Sie auf der Seite Inhalt eine Version des Themas aus, das Sie zur Überprüfung freigeben möchten.

   Sie können eine der folgenden Methoden verwenden, um eine Version auszuwählen:

   - *\(Standard\)* Wählen Sie die Option **Neueste Version** , um die letzte gespeicherte Revision der Themen auszuwählen.
   - Wählen Sie die **Version auf** und geben Sie das Datum und die Uhrzeit an, zu denen eine Version am angegebenen Datum und zur angegebenen Uhrzeit ausgewählt werden soll. Wenn am angegebenen Datum keine Themenversion verfügbar ist, wird eine Version unmittelbar nach dem angegebenen Datum und der angegebenen Uhrzeit ausgewählt.
   - Wählen Sie die **Titel auswählen** und wählen Sie einen Titel aus der Dropdown-Liste aus.
1. Nachdem Sie Ihre Auswahl für eine Version getroffen haben, klicken Sie auf **Anwenden**.

   Die auf der ausgewählten Option basierende Version wird für die Themen ausgewählt.

   >[!NOTE]
   >
   > Sie können die gewünschte Version auch manuell aus dem **Version** Dropdown-Liste der einzelnen Themen.

1. Klicken Sie auf **Weiter**.

   Die Seite &quot;Überprüfer&quot;wird angezeigt, auf der Sie Überprüfer hinzufügen oder entfernen können. Standardmäßig werden die im Feld Zuweisen zu hinzugefügten Validierungsverantwortlichen automatisch zu jedem Thema hinzugefügt, das für die Überprüfung ausgewählt wurde.

   ![](images/add-reviewers-topics.png){width="650" align="left"}

1. Auf der Seite &quot;Überprüfer&quot;können Sie Überprüfer hinzufügen oder entfernen. Die folgenden Vorgänge sind auf der Seite &quot;Validierungsverantwortliche&quot;verfügbar:

   - **Alle auswählen**: Auswahl aller Themen in der Themenliste. Nach Auswahl aller Themen können Sie einfach einen Batch-Vorgang ausführen.
   - **Auswahl löschen**: Hebt die Auswahl der in der Themenliste ausgewählten Themen auf.

     >[!NOTE]
     >
     > Sie können ein Thema auch einzeln auswählen oder deaktivieren, indem Sie auf das Kontrollkästchen neben dem Thema klicken.

   - **Hinzufügen**: Zeigt das Dialogfeld &quot;Überprüfer hinzufügen&quot;an. Sie können den Namen eines Validierers oder einer Benutzerrolle \(oder Gruppe\) eingeben, den Sie als Validierer zu den ausgewählten Themen hinzufügen möchten.
   - **Entfernen**: Zeigt das Dialogfeld &quot;Reviewer entfernen&quot;an. Sie können den Namen eines Validierers oder einer Benutzerrolle \(oder Gruppe\) eingeben, den Sie als Validierer aus den ausgewählten Themen entfernen möchten.

     >[!NOTE]
     >
     > Sie können eine Überprüfung auch aus einem Thema entfernen, indem Sie im Feld des Überprüfers auf das Kreuzzeichen klicken.

   - **Neu zuweisen**: Zeigt das Dialogfeld Reviewer erneut zuweisen an. Sie können den Namen eines Validierers oder einer Benutzerrolle eingeben \(oder Gruppe\), dem Sie die Prüfungsaufgabe zuweisen möchten. Dadurch werden alle vorhandenen Prüfer aus den ausgewählten Themen entfernt und die neu ausgewählten Prüfer diesen Themen zugewiesen.
   - **Export**: Ermöglicht den Export der Details der Prüfungsaufgabe in eine CSV-Datei. Die Datei enthält Details wie den Pfad und Titel des Themas, den Namen des Prüfers und die Version der Themen, die zur Überprüfung gesendet werden.
   - **Validierungsverantwortliche bearbeiten**: Klicken Sie auf das ![](images/edit_pencil_icon.svg)-Symbol in der Themenliste wird das Dialogfeld &quot;Überprüfer bearbeiten&quot;angezeigt. Sie können Überprüfer für das ausgewählte Thema in diesem Dialogfeld hinzufügen oder entfernen.
1. Klicks **Erstellen** , um die Prüfungsaufgabe zu erstellen.

   Wenn die Prüfungsaufgabe erfolgreich erstellt wurde, wird eine Bestätigungsmeldung angezeigt. Die [Dokumentstatus](web-editor-document-states.md#) für die Themen, die zur Überprüfung gesendet werden, auf &quot;In Review&quot;eingestellt ist.

   >[!NOTE]
   >
   > Sie können auch oben rechts im Bildschirm auf Benachrichtigungsglocke klicken und bestätigen, dass die Überprüfungsaufgabe erfolgreich erstellt wurde. Im Bereich Benachrichtigungen finden Sie jeweils eine Benachrichtigung für die validierungsverantwortlichen Benutzer, die Teil der Prüfungsaufgabe waren, und eine Benachrichtigung für den Initiator der Überprüfung.


Allen Validierungsverantwortlichen wird eine E-Mail gesendet, in der sie darauf hingewiesen werden, dass ihnen ein Thema oder mehrere Themen zur Überprüfung zugewiesen wurden. Die E-Mail enthält einen direkten Link, auf den sie klicken und in einem Browserfenster auf das Thema zugreifen können.

Wenn mehrere Themen zugewiesen werden, können die validierungsverantwortlichen Benutzer sie in einer Dropdown-Liste mit Themen im Webbrowser anzeigen und auswählen.

## Senden mehrerer Themen zur Überprüfung über eine DITA-Zuordnung

Eine DITA-Karte ist eine logische Organisation von Themen in einem Buch. Wenn Sie ein einzelnes Thema zur Überprüfung senden, erhält der Validierer keine Informationen über den Speicherort dieses Themas im Buch. Wenn ein Prüfer über Informationen zum genauen Speicherort des zu überprüfenden Themas verfügt, erhält der Prüfer einen besseren Kontext für das zu überprüfende Thema.

Mit AEM Guides können Sie ein oder mehrere Themen in einer DITA-Map zur Überprüfung gleichzeitig senden. Der Validierer sieht die vollständige Zuordnungsdatei zusammen mit Themen, die zur Überprüfung freigegeben wurden. Dies erleichtert es dem Validierer, einen Kontext des Themas in der Landkarte oder Buchdatei zu erhalten.

Sie können dieselbe DITA-Zuordnung in für die Überprüfung in mehreren Prüfungsaufgaben freigeben. Wenn es beispielsweise in einer DITA-Zuordnung die Themen A, B, C, D und E gibt. In einer Prüfungsaufgabe können Sie A, B und C zur Überprüfung freigeben, während Sie in einer anderen Prüfungsaufgabe die Themen C, D und E zur Überprüfung senden können. Der Überprüfungsprozess ermöglicht die Freigabe derselben Themen- und Zuordnungsdatei in mehreren Prüfungsaufgaben. Beim gemeinsamen Thema in mehreren Prüfungsaufgaben überschreiben die in einer Prüfungsaufgabe gegebenen Kommentare nicht die Kommentare in den anderen Prüfungsaufgaben oder führen sie mit ihnen zusammen.

>[!IMPORTANT]
>
> Wenn ein Thema einer Map-Datei in mehreren Prüfungsaufgaben freigegeben wurde, zeigt ihr Status In Review an, bis alle Prüfungsaufgaben abgeschlossen sind.

Um ein oder mehrere Themen zusammen mit der Map-Datei zur Überprüfung zu senden, führen Sie die folgenden Schritte aus:

>[!IMPORTANT]
>
> Nachdem Sie einen Review über eine Map-Datei initiiert haben, dürfen Sie die Struktur der Map-Datei nicht ändern, indem Sie neue Themen hinzufügen oder vorhandene Themen entfernen.

1. Navigieren Sie in der Assets-Benutzeroberfläche zum gewünschten Ordner.

   >[!NOTE]
   >
   > Stellen Sie sicher, dass die Ansicht der Konsole entweder auf Karten- oder Listenansicht eingestellt ist.

1. Wählen Sie die Karte aus, von der Sie die Themen zur Überprüfung senden möchten.

1. Klicken Sie in der Symbolleiste auf **Prüfungsaufgabe erstellen**. Die Seite zur Erstellung von Prüfungsaufgaben wird angezeigt.

1. Geben Sie einen **Titel** für die Aufgabe und wählen Sie eine DITA aus. **Projekt** aus der Dropdown-Liste.

   >[!NOTE]
   >
   > Sie können eine Prüfungsaufgabe nur für die Themen erstellen, die überarbeitet wurden. Wenn Ihre Zuordnung Themen enthält, die keine Revision haben, wird Ihnen eine Eingabeaufforderung mit einer Liste dieser Dateien angezeigt. Dateien ohne Revision sind von der Prüfungsaufgabe ausgeschlossen.

1. Im **Zuweisen zu** Dropdown-Feld die Validierer auswählen, an die Sie die Themen zur Überprüfung senden möchten.

   Sie können eine Prüfungsaufgabe einzelnen Benutzern des Projekts oder Benutzergruppen zuweisen. Beachten Sie, dass Sie einzelnen Benutzern nur dann eine Prüfungsaufgabe zuweisen können, wenn Sie Teil der Administratorgruppe des Projekts sind. Andernfalls werden nur die Benutzergruppen im Feld Zuweisen zu angezeigt.

   >[!NOTE]
   >
   > Überprüfungs-Workflow ist projektspezifisch. Wenn Sie Projekte erstellen, fügen Sie die Teammitglieder zum Projekt hinzu und weisen sie Gruppen zu. Wenn Sie also das Projekt hier auswählen, können Sie die Mitglieder auswählen, die Teil dieses Projekts sind. Weitere Informationen zu Projekten finden Sie unter [Erstellen eines DITA-Projekts](authoring-create-dita-project.md#).

1. Geben Sie einen **Beschreibung** für die Aufgabe.

   Diese Beschreibung wird als Hauptteil der Benachrichtigungs-E-Mail verwendet, die an die validierungsverantwortlichen Benutzer gesendet wird.

1. Wählen Sie die **Fälligkeitsdatum** und Zeit, um die Frist für die Überprüfung festzulegen.

   >[!NOTE]
   >
   > Nach Ablauf der Frist wird dem Initiator eine E-Mail gesendet, in der er darüber informiert wird, dass die Überprüfungsaufgabe abgeschlossen wurde. Der Initiator kann den Termin für die Überprüfungsaufgabe von der [Dashboard überprüfen](review-manage-tasks-review-dashboard.md#).

1. Da Sie verschiedene Validierer verschiedenen Themen zuweisen können, **Zuweisung zum Überprüfen von Themen zulassen** steuert, ob Überprüfer alle Themen in einer Prüfungsaufgabe oder nur die Themen überprüfen können, die ihnen zugewiesen sind.

   Wenn Sie allen Validierungsverantwortlichen erlauben möchten, ein Thema in der Prüfungsaufgabe zu überprüfen, wählen Sie **Zuweisung zum Überprüfen von Themen zulassen**.

   Wenn Sie diese Option nicht auswählen, werden die Überprüfer im **Zuweisen zu** kann nur die Themen überprüfen, die ihnen zugewiesen sind.

1. Klicken Sie auf **Weiter**.

   Die Inhaltsseite wird mit allen Themen angezeigt, auf die in der Zuordnungsdatei verwiesen wird. Wenn Ihre DITA-Map verschachtelte Karten enthält, werden hier auch Themen aus den verschachtelten Maps aufgelistet.

   ![](images/content-page-map-review.png){width="800" align="left"}

1. Wählen Sie auf der Seite Inhalt eine Version des Themas aus, das Sie zur Überprüfung freigeben möchten.

   Sie können eine der folgenden Methoden verwenden, um eine Version auszuwählen:

   - *\(Standard\)* Wählen Sie die Option **Neueste Version** , um die letzte gespeicherte Revision der Themen auszuwählen.
   - Wählen Sie die **Version auf** und geben Sie das Datum und die Uhrzeit zur Auswahl einer Version gemäß Datum und Uhrzeit an. Wenn am angegebenen Datum keine Themenversion verfügbar ist, wird eine Version unmittelbar nach dem angegebenen Datum und der angegebenen Uhrzeit ausgewählt.
   - Wählen Sie die **Titel auswählen** und wählen Sie einen Titel aus der Dropdown-Liste aus. Alle Themen, die die ausgewählte Bezeichnung enthalten, werden im **Version** Dropdown-Liste.
   - Wählen Sie die **Auswählen einer Grundlinie** und wählen Sie eine Grundlinie aus der Dropdownliste aus. Alle Themenversionen, die Teil der ausgewählten Grundlinie sind, werden im **Version** Dropdown-Liste.
1. Nachdem Sie Ihre Auswahl für eine Version getroffen haben, klicken Sie auf **Anwenden**.

   Die auf der ausgewählten Option basierende Version wird für die Themen ausgewählt.

   >[!NOTE]
   >
   > Sie können die gewünschte Version auch manuell aus dem **Version** Dropdown-Liste der einzelnen Themen.

1. Klicken Sie auf **Weiter**.

   Die Seite &quot;Überprüfer&quot;wird angezeigt, auf der Sie Überprüfer hinzufügen oder entfernen können. Standardmäßig werden die im Feld Zuweisen zu hinzugefügten Validierungsverantwortlichen automatisch zu jedem Thema hinzugefügt, das für die Überprüfung ausgewählt wurde.

1. Auf der Seite &quot;Überprüfer&quot;können Sie Überprüfer hinzufügen oder entfernen. Die folgenden Vorgänge sind auf der Seite &quot;Validierungsverantwortliche&quot;verfügbar:

   - **Alle auswählen**: Auswahl aller Themen in der Themenliste. Nach Auswahl aller Themen können Sie einfach einen Batch-Vorgang ausführen.
   - **Auswahl löschen**: Hebt die Auswahl der in der Themenliste ausgewählten Themen auf.

     >[!NOTE]
     >
     > Sie können ein Thema auch einzeln auswählen oder deaktivieren, indem Sie auf das Kontrollkästchen neben dem Thema klicken.

   - **Hinzufügen**: Zeigt das Dialogfeld &quot;Überprüfer hinzufügen&quot;an. Sie können den Namen eines Validierers oder einer Benutzerrolle \(oder Gruppe\) eingeben, den Sie als Validierer zu den ausgewählten Themen hinzufügen möchten.
   - **Entfernen**: Zeigt das Dialogfeld &quot;Reviewer entfernen&quot;an. Sie können den Namen eines Validierers oder einer Benutzerrolle \(oder Gruppe\) eingeben, den Sie als Validierer aus den ausgewählten Themen entfernen möchten.
   - **Neu zuweisen**: Zeigt das Dialogfeld Reviewer erneut zuweisen an. Sie können den Namen eines Validierers oder einer Benutzerrolle eingeben \(oder Gruppe\), dem Sie die Prüfungsaufgabe zuweisen möchten. Dadurch werden alle vorhandenen Prüfer aus den ausgewählten Themen entfernt und die neu ausgewählten Prüfer diesen Themen zugewiesen.
   - **Export**: Ermöglicht den Export der Details der Prüfungsaufgabe in eine CSV-Datei. Die Datei enthält Details wie den Pfad und Titel des Themas, den Namen des Prüfers und die Version der Themen, die zur Überprüfung gesendet werden.
   - **Validierungsverantwortliche bearbeiten**: Klicken Sie auf das ![](images/edit_pencil_icon.svg)-Symbol in der Themenliste wird das Dialogfeld &quot;Überprüfer bearbeiten&quot;angezeigt. Sie können Überprüfer für das ausgewählte Thema in diesem Dialogfeld hinzufügen oder entfernen.
   >[!IMPORTANT]
   >
   > Sie müssen mindestens einen Validierer zuweisen, um die Prüfungsaufgabe zu erstellen.

1. Klicks **Erstellen** , um die Prüfungsaufgabe zu erstellen.

   Wenn die Prüfungsaufgabe erfolgreich erstellt wurde, wird eine Bestätigungsmeldung angezeigt. Die [Dokumentstatus](web-editor-document-states.md#) für die Themen, die zur Überprüfung gesendet werden, auf &quot;In Review&quot;eingestellt ist.

   >[!NOTE]
   >
   > Sie können auch oben rechts in der Benutzeroberfläche auf das Bedienfeld Benachrichtigungen klicken und bestätigen, dass die Aufgabe erfolgreich erstellt wurde. Im Fenster Benachrichtigungen finden Sie jeweils eine Benachrichtigung für die Überprüfungen, die Teil der Prüfungsaufgabe waren, und eine Benachrichtigung für den Initiator der Überprüfung.

   >[!IMPORTANT]
   >
   > Nachdem Sie eine Überprüfung initiiert haben, dürfen Sie die DITA-Zuordnung oder Themen nicht an einen anderen Ort verschieben oder löschen. Dies führt zu einer Unterbrechung des Überprüfungsprozesses.


Allen Validierungsverantwortlichen wird eine E-Mail gesendet, in der sie darauf hingewiesen werden, dass ihnen Themen zur Überprüfung zugewiesen wurden. Die E-Mail enthält einen direkten Link, auf den sie klicken und in einem Browserfenster auf das Thema zugreifen können. Die Themen werden zusammen mit der DITA-Zuordnung im Überprüfungsmodus geöffnet.

**Übergeordnetes Thema:**[ Themen oder Zuordnungen überprüfen](review.md)
