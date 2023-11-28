---
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---
# Anpassen der Überprüfungs-App

Um die Anpassung der Review-App zu erleichtern, haben wir einige der unten aufgeführten und erläuterten Erweiterungspunkte bereitgestellt:

## Review-Comment

- id: `review_comment`
- Hook: `this.updateExtraProps`:

Wie besprochen [here](../../aem_guides_framework/basic_customisation.md), werden alle neuen Attribute, die bei der Anpassung hinzugefügt werden, unter `this.model.extraProps`. Die -Methode `updateExtraProps` ermöglicht es Ihnen, einem Überprüfungskommentar Attribute hinzuzufügen und dabei auch die Aktualisierung und Speicherung des hinzugefügten Attributs auf dem Server zu verarbeiten.

### Nutzungsbeispiel

Angenommen, Sie möchten Felder hinzufügen `commentRationale` und `severity` zu Ihren Kommentaren.
Aktualisieren wir die `commentRationale` zu &quot;Dies ist ein wichtiger Satz.&quot; und `severity` auf &quot;CRITICAL&quot;.
Dies kann mithilfe der folgenden Syntax erfolgen:

```typescript
 this.updateExtraProps(
        {'commentRationale': 'This is an important sentence.',
        'severity': 'CRITICAL'}
      )
```

Das obige Codefragment verarbeitet die Aktualisierung und Speicherung der Werte. Die gespeicherten Werte können über die Benutzeroberfläche gerendert werden, indem die Ansicht definiert wird.

```JSON
{
    "component" : "label",
    "label": "@extraProps.commentRationale"
}
```

## Bedienfeld für Inline-Überprüfung

- id: `inline_review_panel`

1. Hook: `onNewCommentEvent`
Der Haken `onNewCommentEvent` ermöglicht es Ihnen, ein Ereignis auszulösen oder eine Methode für ein neues Kommentar- oder Antwortereignis aufzurufen.
Die im `onNewCommentEvent` include:
   - events: das Kommentar-/Antwortereignis, das gesendet wurde.
   - newComment: boolean Wenn das gesendete Ereignis ein neues Kommentar-Ereignis war, d. h. `highlight`, `insertion`, `deletion`, `sticky note comment`
   - newReply: boolescher Wert, wenn das gesendete Ereignis ein neues Antwortereignis war.

2. Hook: `sendExtraProps`

Dieser Erweiterungspunkt ist nützlich, wenn Sie eine `event` und senden `extraProps` aus dem Inline-Überprüfungsfenster. Wir erklären Ihnen die Verwendung dieser beiden Haken unten.

### Beispiel für Inline-Prüfungsbereich

Angenommen, wir möchten eine extraProp senden, `userInfo`, jedes Mal, wenn ein neuer Kommentar oder eine neue Antwort gesendet wird. Nun erfolgt dies über das Inline-Überprüfungsfenster, aber wir haben nicht den Verweis auf die commentId des neu generierten Kommentars, daher können wir zu diesem Zweck den folgenden Code schreiben.

```typescript
    onNewCommentEvent(args){
      const events = _.get(args, "events")
      const currTopicIndex = tcx.model.getValue(tcx.model.KEYS.REVIEW_CURR_TOPIC) || this.model.currTopicIndex || "0"
      const event = _.get(_.get(events, currTopicIndex), '0')
      const newComment = _.get(args, 'newComment')
      const newReply = _.get(args, 'newReply')
      if ((newComment || newReply) && event) {
        this.next('setUserInfo', event)
      }
    },
```

Im obigen Codeausschnitt überprüfen wir, ob das gesendete Ereignis ein neuer Kommentar oder eine neue Antwort war. Im Falle eines neuen Kommentars oder einer neuen Antwort rufen wir die Methode auf `setUserInfo`

```typescript
    setUserInfo(event) {
      this.loader?.getUserInfo(event.user).subscribe(userData => {
        const extraProps = {
          "userFirstName": userData?.givenName || '',
          "userLastName": userData?.familyName || '',
          "userTitle": userData?.title || '',
          "userJobTitle": userData?.jobTitle || '',
          'userEmail': userData?.email || '',
        }
        const data = {... event, extraProps}
        this.sendExtraProps(
          data
        )
      })
    },
```

In der obigen Methode erweitern wir das Ereignis, um extraProps zu senden, die den Vornamen, die E-Mail-Adresse, den Titel usw. des Benutzers enthalten. Wenn Sie das Ereignis auf diese Weise erweitern, wird sichergestellt, dass die extraProps mit der richtigen commentId gesendet werden, sodass sie an den richtigen Kommentar angehängt werden.

Der Haken `updateExtraProps` ruft grundsätzlich den Hook auf `sendExtraProps`, also wann zu verwenden, was?

Wir verwenden `updateExtraProps` im `review_comment` Verantwortlicher, der bereits über die `id` und deshalb müssen Sie nur die `extraProps.`

Die `inline_review_panel` hat jedoch keinen Zugriff auf die ID des Kommentars. Daher müssen Sie jedes Mal, wenn Sie ein Ereignis aus dem Inline-Überprüfungsfenster senden, die `sendExtraProps` wird praktisch sein.
