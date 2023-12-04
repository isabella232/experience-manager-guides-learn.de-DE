---
title: Symbolleiste anpassen
description: Erfahren Sie, wie Sie die Symbolleiste anpassen
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Symbolleiste anpassen {#id172FB00L0V6}

Standardmäßig werden im Web Editor die gängigsten redaktionellen Funktionen bereitgestellt, die für jeden DITA-Editor erforderlich sind. Funktionen wie das Einfügen von Elementen des Typs Liste \(nummeriert oder mit Aufzählungszeichen\), Querverweis, Inhaltsverweis, Tabelle, Absatz und Zeichenformatierung sind im Editor verfügbar. Zusätzlich zu diesen grundlegenden Elementen können Sie den Web-Editor anpassen, um Elemente einzufügen, die in Ihrer Authoring-Umgebung verwendet werden.

Es gibt zwei Möglichkeiten, die Symbolleiste des Web-Editors anzupassen:

- Hinzufügen neuer Funktionen zur Symbolleiste

- Entfernen vorhandener Funktionen aus der Symbolleiste


## Hinzufügen einer Funktion in der Symbolleiste

Das Hinzufügen einer Funktion zum Web-Editor umfasst zwei Hauptaufgaben - das Hinzufügen eines Symbols für die Funktion im *ui\_config.json* und das Hinzufügen der Hintergrundfunktion in JavaScript.

Führen Sie die folgenden Schritte aus, um der Symbolleiste des Web-Editors eine Funktion hinzuzufügen:

1. Um die Benutzeroberflächenkonfigurationsdatei herunterzuladen, melden Sie sich als Administrator bei Adobe Experience Manager an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die Schaltfläche **Ordnerprofile**.
1. Klicken Sie auf **Globales Profil** Kachel.
1. Wählen Sie die **Konfiguration des XML-Editors** Registerkarte und klicken Sie auf **Bearbeiten** Symbol oben
1. Klicken Sie auf **Herunterladen** -Symbol, um die Datei ui\_config.json auf Ihr lokales System herunterzuladen. Anschließend können Sie Änderungen an der Datei vornehmen und diese dann hochladen.
1. Im `ui_config.json` -Datei, fügen Sie die Definition der neuen Funktion im Abschnitt &quot;Symbolleisten&quot;hinzu. Speichern Sie die Datei und laden Sie sie hoch.

   In der Regel können Sie eine neue Schaltflächengruppe für Symbolleisten erstellen und eine oder mehrere Schaltflächen der Symbolleiste hinzufügen. Sie können auch eine neue Symbolleistenschaltfläche innerhalb einer vorhandenen Symbolleistengruppe hinzufügen. Die folgenden Details sind erforderlich, um eine neue Symbolleistengruppe zu erstellen:

   **type**: Geben Sie `blockGroup` als `type` -Wert. Dieser Wert gibt an, dass Sie eine Blockgruppe erstellen, die eine oder mehrere Symbolleistengruppen enthalten würde.

   **extraklasse**: Name der Klasse(n), getrennt durch Leerzeichen.

   **items**: Geben Sie die Definition aller Gruppen in der Symbolleiste an. Jede Gruppe kann ein oder mehrere Symbolleistensymbole enthalten. Um Symbole in einer Symbolleistengruppe zu definieren, müssen Sie die `type` -Attribut innerhalb der `items`und setzen Sie den Wert auf `buttonGroup`. Geben Sie einen oder mehrere Klassennamen in der `extraclass` -Eigenschaft. Geben Sie den Namen der Funktion im `label` -Eigenschaft. Das folgende Snippet aus dem `ui_config.json` -Datei zeigt die Definition des Hauptbausteins der Symbolleiste, gefolgt von der `buttonGroup` Definition:

       &quot;
       &quot;toolbar&quot;: {
       &quot;type&quot;: &quot;blockGroup&quot;,
       &quot;extraclass&quot;:
       &quot;Symbolleistenvorgänge&quot;,
       &quot;items&quot;: [
       {
       &quot;type&quot;: &quot;buttonGroup&quot;,
       &quot;extraclass&quot;: &quot;left-control&quot;,
       &quot;label&quot;: &quot;Linke Steuerelemente&quot;,
       &quot;items&quot;: [
       &quot;
   
   Innerhalb der `items` -Sammlung müssen Sie die Definition für ein oder mehrere Symbolleistensymbole angeben.

   Sie müssen die folgenden Eigenschaften definieren, um ein Symbolleistensymbol hinzuzufügen:

   **type**: Geben Sie `button` als `type` -Wert. Dieser Wert gibt an, dass Sie eine Symbolleistenschaltfläche hinzufügen.

   **icon**: Geben Sie den Namen des Coral-Symbols an, das Sie in der Symbolleiste verwenden möchten.

   **Variante**: Geben Sie `quiet` als `variant` -Wert.

   **title**: Geben Sie die QuickInfo für das Symbol an.

   **on-click**: Geben Sie den für die Funktion definierten Befehlsnamen in der JavaScript-Datei an. Wenn für Ihren Befehl Eingabeparameter erforderlich sind, geben Sie den Befehlsnamen wie folgt an:

       &quot;Javascript
       &quot;on-click&quot;: {&quot;name&quot;: &quot;AUTHOR_INSERT_ELEMENT&quot;, &quot;args&quot;: &quot;simplable&quot;}
       &quot;
   
   **ein- oder ausblenden**: Wenn Sie die `show` -Eigenschaft und geben Sie dann die Modi an, in denen das Symbol angezeigt wird. Mögliche Werte sind - `@isAuthorMode`, `@isSourceMode`, `@isPreviewMode`, `true` \(in allen Modi anzeigen\) oder `false` \(In allen Modi ausblenden\).

   anstelle von `show`, können Sie auch die `hide` -Eigenschaft. Die möglichen Werte sind identisch mit in `show` -Eigenschaft mit dem einzigen Unterschied, dass das Symbol für den angegebenen Modus nicht angezeigt wird.

   Das folgende Beispiel zeigt AEM Versionsnummer des Guides, wenn der Benutzer in der Symbolleiste auf das Symbol Version anzeigen klickt.

   Fügen Sie einer JavaScript-Datei den folgenden Code hinzu:

   ```Javascript
   $(document).ready(setTimeout(function() {
                           fmxml.commandHandler.subscribe({
                           key: 'user.alert',
                           next: function() {
                           alert("AEM Guides version x.x")
                           }
                           })
                           }, 1000))
   ```

   Fügen Sie die Funktion im *ui\_config.json* Datei als:

   ```Javascript
   "type": "button",
   "icon": "alert","variant": "quiet","title": "About AEM Guides","show": "true","on-click": "user.alert"
   ```

1. Erstellen Sie eine *clientlib* und fügen Sie Ihr JavaScript in diesen Ordner ein.

1. Aktualisieren Sie die categories-Eigenschaft des *clientlib* Ordner, indem ihm der Wert von *apps.format.xml\_editor.page\_overrides*.

1. Speichern Sie die *ui\_config.json* und laden Sie den Web Editor neu.


## Entfernen einer Funktion aus der Symbolleiste

Manchmal möchten Sie nicht alle derzeit im Web-Editor verfügbaren Funktionen bereitstellen. In diesem Fall können Sie die unerwünschte Funktion aus der Symbolleiste des Web-Editors entfernen.

Führen Sie die folgenden Schritte aus, um unerwünschte Funktionen aus der Symbolleiste zu entfernen:

1. Um die Benutzeroberflächenkonfigurationsdatei herunterzuladen, melden Sie sich als Administrator bei Adobe Experience Manager an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die Schaltfläche **Ordnerprofile**.
1. Klicken Sie auf **Globales Profil** Kachel.
1. Wählen Sie die **Konfiguration des XML-Editors** Registerkarte und klicken Sie auf **Bearbeiten** Symbol oben
1. Klicken Sie auf **Herunterladen** -Symbol, um die Datei ui\_config.json auf Ihr lokales System herunterzuladen. Anschließend können Sie Änderungen an der Datei vornehmen und diese dann hochladen.

   Die `ui_config.json` -Datei umfasst drei Abschnitte:

   1. **Symbolleisten**: Dieser Abschnitt enthält die Definition aller in der Symbolleiste des Editors verfügbaren Funktionen wie &quot;Nummerierte Liste einfügen/entfernen&quot;, &quot;\(Datei\) schließen&quot;, &quot;Speichern&quot;, &quot;Kommentare&quot;und mehr.

   1. **Kurzbefehle**: Dieser Abschnitt enthält die Definition von Tastaturbefehlen, die einer bestimmten Funktion im Editor zugewiesen sind.

   1. **templates**: Dieser Abschnitt enthält die vordefinierte Struktur von DITA-Elementen, die Sie in Ihrem Dokument verwenden können. Standardmäßig enthält der Abschnitt &quot;Vorlagen&quot;Vorlagendefinitionen für Absätze, einfache Tabellen, Tabellen und Textelemente. Sie können eine Vorlagendefinition für jedes Element erstellen, indem Sie eine gültige XML-Struktur für das gewünschte Element hinzufügen. Wenn Sie beispielsweise eine `p` Element mit jeder neuen `li` -Element in eine Liste ein, können Sie am Ende des Vorlagenabschnitts folgenden Code hinzufügen, um dies zu erreichen:

   ```css
   "li": "<li><p></p></li>"
   ```

1. Entfernen Sie im Abschnitt &quot;Symbolleisten&quot;den Eintrag der Funktion, die Sie Ihren Benutzern nicht zur Verfügung stellen möchten.

1. Speichern Sie die *ui\_config.json* und laden Sie den Web Editor neu.


**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
