---
sidebar_position: 8
source-git-commit: d99be38f5d69a7472909511faad230bea9bc435b
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---


# Beispiele

In diesem Paket haben wir auch einige Beispiele für Anpassungen bereitgestellt (verfügbar unter `guides_extension/src`) . Unten finden Sie eine kurze Beschreibung für jeden von ihnen.

1. [Kontextmenü](./../../src/file_options.ts)
In diesem Beispiel haben wir die `file_options` Kontextmenü, um die `Delete` und `Edit` und ersetzen Sie die `Duplicate` mit einer `Download` -Option.

2. [Linke Leiste](../../src/left_panel_container.ts)
In diesem Beispiel haben wir die `left tab panel` um einen anderen`tab` mit dem Titel &quot;TESTERWEITERUNG&quot;und einer entsprechenden `tab panel` mit einer Bezeichnung: `Test Tab Panel`

3. [Rechter Bereich](../../src/right_panel_container.ts)
In diesem Beispiel haben wir die `right tab panel` um einen anderen `tab` mit dem Titel &quot;TESTERWEITERUNG&quot;und einer entsprechenden `tab panel` mit einer Bezeichnung: `New Tab Panel`

4. [Repository-Bereich](../../src/repository_panel.ts)

5. [Symbolleiste](../../src/toolbar.ts)
In diesem Beispiel haben wir die `Insert Element`, `Insert Paragraph`, `Insert Numbered List`, `Insert Bulleted List` Schaltflächen mit nur einer `More Insert Options` -Schaltfläche mit all diesen Elementen.

[Anwendungsbeispiele überprüfen]

1. [Anmerkungssymbolleiste](../../src/review_app_examples/annotation_extension.ts)
In diesem Beispiel haben wir der Anmerkungs-Toolbox eine weitere Schaltfläche hinzugefügt, mit der das aktuelle Prüfungsthema in AEM geöffnet wird.

2. [Überprüfungskommentar](../../src/review_app_examples/review_comment.ts)
In diesem Beispiel haben wir den Benutzernamen durch Benutzerinformationen ersetzt (bestehend aus dem vollständigen Namen und dem Titel des Kommentars), eine eindeutige Kommentar-ID, ein mailTo-Symbol hinzugefügt und Eingabefelder hinzugefügt, mit denen der Schweregrad und die Begründung von Kommentaren erwähnt werden.
Wir haben auch eine `accept with modification` auf Kommentare auf der XMLEditor-Seite, die ein Dialogfeld öffnet.

3. [Kommentar-Antwort](../../src/review_app_examples/comment_reply.ts)
In diesem Beispiel haben wir den Benutzernamen durch Benutzerinformationen ersetzt (bestehend aus dem vollständigen Namen und dem Titel des Kommentars) und ein mailTo -Symbol in der Kommentarkopfzeile hinzugefügt.

4. [Inline-Prüfungsbereich](../../src/review_app_examples/inline_review_panel.ts)
In dieser Datei berechnen und weisen wir die eindeutige Kommentar-ID zu, die im Abschnitt `Review Comment` und `Comment Reply` Beispiele.
   - Die `setCommentId` -Methode legt die eindeutige Kommentar-ID für jeden Kommentar fest, je nach Anzahl der Kommentare.

   - Die `setUserInfo` legt den Wert von userInfo fest, wobei für jeden Kommentar der vollständige Name und der Titel verwendet werden.

   - Die `onNewCommentEvent` stellt sicher, dass `setUserInfo` -Methode für jeden neuen Kommentar oder jede neue Antwort aufgerufen.

   - Die `updatedProcessComments` -Funktion für jedes neue Kommentar-Ereignis ausgeführt und stellt sicher, dass `setCommentId` wird aufgerufen, wenn wir ein neues Kommentar-Ereignis erhalten.

5. [Themenüberprüfungsbereich](../../src/review_app_examples/topic_reviews.ts): Diese Datei erweitert [Inline-Prüfungsbereich](../../src/review_app_examples/inline_review_panel.ts) sodass hinzugefügte Anpassungen auch auf der Seite &quot;Review App&quot;funktionieren.

6. [Annehmen mit Dialogfeld &quot;Änderung&quot;](../../src/review_app_examples/accept_with_modification_dialog.ts)
Dies ist ein Beispiel für das Hinzufügen eines neuen Widgets zur App. Hier haben wir ein neues Dialogfeld erstellt, das zwei Eingabetextfelder enthält: `Revised Text` und `Adjudicator Comment Rationale`

![Dialogfeld &quot;Annehmen mit Änderung&quot;](./imgs/accept_with_modification_dialogue.png)

Hier finden Sie das Überprüfungsbedienfeld vor und nach der Anpassung:

![Überprüfungsgruppe;](./imgs/review_panel.png)
![Dialogfeld &quot;Annehmen mit Änderung&quot;](./imgs/customised_review_panel.png)
