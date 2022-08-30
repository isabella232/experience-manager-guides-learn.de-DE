---
title: Native PDF-Veröffentlichungsfunktion | Erstellen eines Seitenlayouts
description: Erfahren Sie, wie Sie Ihr Seitenlayout für die Präsentation von Informationen in verschiedenen Bereichen Ihrer PDF-Ausgabe entwerfen.
hide: true
hidefromtoc: true
exl-id: b4d3bdc4-0d01-46eb-b182-540380220485
source-git-commit: f8af7d7180b3d70d17e1410885017212dec721ef
workflow-type: tm+mt
source-wordcount: '4688'
ht-degree: 0%

---


# Erstellen eines Seitenlayouts

Bei der Erstellung eines PDF-Dokuments würden Sie verschiedene Bereiche für die Darstellung verschiedener Informationstypen haben. Beispielsweise würde ein PDF-Dokument von einer Vorder- oder Titelseite aus beginnen, die das Logo, den Buchtitel oder die Versionsinformationen Ihres Unternehmens enthält. Dann gibt es Kapitel, Anhänge oder Glossarseiten. Jeder Bereich in einem PDF-Dokument sieht anders aus, was durch Erstellen und Anpassen des Seitenlayouts erreicht wird.

Beim Entwerfen des Seitenlayouts können Sie die verschiedenen Elemente einer Seite definieren. Sie können beispielsweise die Seitengröße, die Ränder, Kopf- und Fußzeilen, die Ausrichtung und andere Seitenspezifikationen auf einer Seite definieren. Mit der nativen PDF-Veröffentlichungsfunktion können Sie Ihre Seite gemäß dem [Seitenmedienstandards](https://www.w3.org/TR/css-page-3/). Die meisten Einstellungen, die unter den Standards für Seitenmedien behandelt werden, können einfach über die Benutzeroberfläche der nativen PDF-Veröffentlichungsfunktion angepasst werden. Für weitere Formatierungen auf erweiterter Ebene können Sie die Quellansicht verwenden, um Ihren eigenen CSS-Code zu schreiben.

Nachdem Sie die Seitenlayouts entworfen haben, müssen Sie diese Layouts mit den entsprechenden Abschnitten in den PDF-Seitenlayouteinstellungen verknüpfen. Siehe _Seitenlayouts erstellen und anpassen_ -Abschnitt für Details zum Erstellen und Öffnen eines Seitenlayouts für die Anpassung.

## Typen von Seitenlayouts

Ein PDF-Dokument enthält in der Regel die folgenden Abschnitte:

* Titelseite
* Inhaltsverzeichnis
* Aufstockung der Zahlen
* Tabellensteigerung
* Kapitel- oder Themenseiten
* Glossar
* Index
* Zurück-Seite

Diese Abschnitte benötigen ein entsprechendes Seitenlayout, um die Informationen in einem bestimmten Format darzustellen. Darüber hinaus können Sie auch eine leere Seite haben, die als Füller verwendet wird, um ein neues Kapitel von einer ungeraden oder geraden Seite aus zu beginnen. In diesem Fall können Sie entweder das standardmäßige Seitenlayout verwenden oder ein Seitenlayout für eine leere Seite erstellen. Siehe _Neues Seitenlayout erstellen_ für weitere Details.

Die Einstellungen für Seitenlayouts unter **Vorlage > Einstellungen** können Sie festlegen, welches Seitenlayout für verschiedene Bereiche Ihrer PDF verwendet werden soll. Jedes Seitenlayout kann außerdem verschiedene Varianten für die erste, rechte oder linke Seite aufweisen.

### Erstellen der Layout-Varianten für die erste, rechte oder linke Seite

Verschiedene Seitenlayouts in Ihrer PDF-Vorlage können weiter angepasst werden, indem unterschiedliche Layoutvarianten für die erste, rechte oder linke Seite verwendet werden. Sie können diese Seiten mit dem Seitenlayout-Designer unterschiedlich entwerfen.

>[!NOTE]
>
>Wenn Sie ein einseitiges Seitenlayout für einen Abschnitt in Ihrem Buch haben möchten, müssen Sie keine Layouts für die erste, rechte oder linke Seite erstellen.

Beachten Sie beim Erstellen der Seitenlayouts die folgenden Punkte:

>[!NOTE]
>
>In den folgenden Punkten wird das Kapitel-Seitenlayout als Beispiel verwendet. Diese Punkte gelten jedoch auch für andere Seitenlayouts.

* Wenn Sie ein einzelnes Seiten-Layout für alle Seiten in einem Kapitel verwenden möchten, erstellen Sie nur ein einzelnes Kapitelseitenlayout ohne Variante.

* Wenn Sie ein anderes Erscheinungsbild für die erste Seite für Kapitel in Ihrem Buch haben möchten, müssen Sie eine Layoutvariante für die erste Seite für Ihre Kapitel erstellen.

* Wenn Sie für jede linke und rechte Seite Ihres Buches ein anderes Erscheinungsbild wünschen, müssen Sie die Varianten Links und Rechts für Ihr Kapitel-Seitenlayout erstellen.

* Wenn Ihre Kapitel von einer ungeraden oder geraden Seite beginnen sollen, können Sie ein Seitenlayout für die leere Seite erstellen. Mit diesem Seitenlayout wird die Lücke zwischen zwei Kapiteln gefüllt, um sicherzustellen, dass das Kapitel von der gewünschten ungeraden oder geraden Seite beginnt.

   >[!NOTE]
   >
   >Wenn Sie kein eigenes leeres Seitenlayout erstellen, wird das standardmäßige Seitenlayout verwendet. Informationen zum Erstellen eines Seitenlayouts finden Sie unter _Neues Seitenlayout erstellen_.

Das folgende Beispiel führt Sie durch den Prozess der Erstellung von Varianten eines Seitenlayouts:

1. Erstellen Sie ein &quot;Kapitel&quot;-Seitenlayout anhand der unter &quot;Neues Seitenlayout erstellen&quot;beschriebenen Schritte.

   Unter Seitenlayouts wird ein leeres Seiten-Layout für Kapitel erstellt und hinzugefügt.

   Wenn Sie ein Seitenlayout erstellen, wird es standardmäßig auch zur Bearbeitung geöffnet. Im folgenden Screenshot wird ein leeres (standardmäßiges) Seitenlayout angezeigt:

   <img src="./assets/default-blank-page-layout.png" width="300">

   Der Kopf-, Fußzeilen- und Inhaltsbereich in einer Vorlage wird standardmäßig erstellt. Sie können diese Bereiche mithilfe der Seiteneigenschaften, Inhaltseigenschaften und verschiedener Tools (wie Einfügen von Bildern, Feldern usw.) in der Benutzeroberfläche einfach anpassen.

   >[!NOTE]
   >
   >Für eine erweiterte Konfiguration können Sie die Quellansicht verwenden und Ihren benutzerdefinierten HTML- und CSS-Code hinzufügen.

1. Bewegen Sie den Mauszeiger über den **Kapitel** und klicken Sie auf **Optionen** , um das Kontextmenü anzuzeigen.

1. Klicken oder bewegen Sie den Mauszeiger über **Layout-Variante hinzufügen** und wählen Sie das gewünschte Seitenlayout (Erste, Links oder Rechts), das Sie erstellen möchten.

Das Layout der ausgewählten Seite wird mithilfe einer Kopie des grundlegenden Kapitellayouts erstellt. Wenn Sie also Änderungen am standardmäßigen Seiten-Layout für Kapitel vorgenommen haben, werden dieselben Änderungen zum Zeitpunkt der Erstellung des Seitenlayouts im varianten Seitenlayout repliziert.

## Arbeiten mit den Seiteneigenschaften eines Seitenlayouts

Beim Entwerfen eines Seitenlayouts ist es wichtig, die verschiedenen Seiteneigenschaften zu steuern. Die Funktion Natives PDF-Publishing enthält alle wichtigen Seiteneigenschaften im Bereich Seiteneigenschaften . Der Bereich Seiteneigenschaften bietet Zugriff auf verschiedene Eigenschaften in den folgenden Abschnitten:

>[!NOTE]
>
>Das Bedienfeld Seiteneigenschaften enthält die Eigenschaften und folgt den Regeln, die unter dem [Seitenmedienstandards](https://www.w3.org/TR/css-page-3/).

* **Seitengröße** : Geben Sie die Seitengröße für das Seitenlayout an. In der Dropdownliste Seitengröße können Sie aus über 15 Seitengrößen wählen. Sie können auch ein Seitenlayout mit einer benutzerdefinierten Seitengröße erstellen, siehe **Seitengröße festlegen** für weitere Details.

* **Ausrichtung** : Geben Sie die Seitenausrichtung für das Seitenlayout an. Sie können zwischen den Ausrichtungen Hochformat oder Querformat wählen. Beachten Sie, dass Sie in einem Seitenlayout unterschiedliche Ausrichtungen auf verschiedene Seitenvarianten anwenden können. Wenn Ihr Inhalt beispielsweise eine breite Tabelle oder ein großes Bild enthält, können Sie ein Querformatlayout erstellen und dieses Layout auf die breitere Tabelle oder das Bild anwenden.

* **Rotation anzeigen** : Geben Sie die Seite oder Richtung an, in der die ursprüngliche obere Seite nach der Drehung dargestellt wird. Sie können zwischen dem Uhrzeigersinn 90, dem Uhrzeigersinn 90 oder dem Uhrzeigersinn 180 Grad wählen. Dies ist sehr nützlich in einer Situation, in der Sie eine Kombination aus Hochformat- und Querformat-Layouts in Ihrer Ausgabe verwenden möchten. Sie können beispielsweise das Hochformat als generisches Seitenlayout verwenden und ein Querformat-Seitenlayout für die Darstellung von Tabellen mit großen Flächen festlegen. In diesem Fall können Sie festlegen, dass der Tabelleninhalt im Uhrzeigersinn 90 Grad angezeigt wird. Dadurch wird die Seite im Querformat ausgerichtet und der Inhalt wird um 90 Grad gedreht, um die Kontinuität im Blick zu wahren. Wir werden sehen, wie dies erreicht wird, als Beispiel weiter unten in diesem Abschnitt.

* **Nummerierung neu starten von** : Geben Sie die Seitenzahl an, von der aus die Nummerierung für dieses Seitenlayout beginnen soll. Sie können beispielsweise die Seitennummer so festlegen, dass sie für jedes Kapitel neu gestartet wird. In diesem Fall müssen Sie die Eigenschaft Nummerierung von neu starten auf 1 der Layoutvariante Erste Seite des Kapitelseitenlayouts festlegen.

* **Layout** : Geben Sie die Seitenränder zusammen mit dem Abstand für die oberen, unteren, linken und rechten Seiten an. In der folgenden Abbildung wird erläutert, wie Ränder, Abstand und Rahmen um den Inhalt gerendert werden. Beachten Sie, dass der Rand oben und unten auf einer Seite die Kopf- und Fußzeile enthält.

   <img src="./assets/margins-padding-illustration.png" width="300">

* **Hintergrund** : Fügen Sie ein Bild oder eine Farbe als Hintergrund Ihres Seitenlayouts hinzu. Für ein Bild können Sie die Höhe und Breite des Bildes sowie die Wiederholungs- und Positionseigenschaften angeben.

* **Fußnote** : Geben Sie die Eigenschaften an, mit denen Fußnoten in der Ausgabe angezeigt werden sollen. Sie können die Eigenschaften für Ränder und Abstand sowie einen Randstil festlegen.

### Seitengröße festlegen

Das allererste, was Sie in einem Seitenlayout definieren müssen, ist die Seitengröße. In den Seiteneigenschaften gibt es mehr als 15 Seitengrößen, die Sie für ein Seitenlayout auswählen können. Sie können auch eine benutzerdefinierte Seitengröße erstellen, indem Sie die folgenden Schritte ausführen:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie im rechten Bereich auf **Seiteneigenschaften**.
1. Im **Seitengröße** Dropdown-Liste auswählen **Benutzerdefiniert**.

   Die Felder Seitenbreite und Seitenhöhe werden angezeigt.

1. Geben Sie die gewünschten Seitendimensionen in die **Seitenbreite** und **Seitenhöhe** -Felder.

   >[!NOTE]
   >
   >Einige der am häufigsten verwendeten Einheiten sind px (Pixel), pt (Punkte), rem, em, % (Prozent) und in (Zoll).

### Seitenausrichtung und Anzeigenrotation verwenden

Sehen wir uns ein Beispiel an, in dem eine Kombination aus Seitenausrichtung im Hoch- und Querformat und Seitenumdrehungseigenschaften verwendet wird. In diesem Beispiel wird eine PDF mit standardmäßiger Hochformatausrichtung erstellt, eine Tabelle wird jedoch im Querformat mit Inhalten in der 90-Grad-Ansicht im Uhrzeigersinn gerendert. Die endgültige Ausgabe sieht in etwa wie folgt aus:

<img src="./assets/portrait-landscape-page-layouts.png" width="400">

In der obigen Ausgabe werden die Kontaktlisten-Informationen im Querformat angezeigt, wobei der Inhalt ebenfalls um 90 Grad gedreht wird. Der restliche Inhalt wird im normalen Hochformat angezeigt.

Um diese Art von Ausgabe zu erzielen, müssen wir die folgenden Hauptaufgaben durchführen:

1. Erstellen Sie ein Seitenlayout mit der Ausrichtung &quot;Querformat&quot;.

1. Ändern Sie die **Rotation anzeigen** -Eigenschaft zum Rendern von Inhalten in 90°.

1. Erstellen Sie einen benutzerdefinierten Stil, um das neue Seitenlayout zu verwenden.

1. Fügen Sie den Stil in der Definition der Ausgabeklasse der Tabelle hinzu, die wir im Querformat-Seitenlayout rendern möchten.

Führen Sie die folgenden Schritte aus, um die oben genannten Aufgaben zu erledigen:

1. Erstellen Sie ein Seitenlayout mit der Ausrichtung &quot;Querformat&quot;.
   1. Erstellen Sie ein &quot;Querformat&quot;-Seitenlayout anhand der unter &quot;Neues Seitenlayout erstellen&quot;beschriebenen Schritte.

   1. Klicken Sie im rechten Bereich auf **Seiteneigenschaften**.

      <img src="./assets/page-properties-panel.png" width="300">
   1. Ändern Sie die **Ausrichtung** nach **Querformat**.

1. Ändern Sie die Eigenschaft &quot;View Rotation&quot;, um Inhalte im Uhrzeigersinn um 90° zu rendern.

   1. Auswählen **Im Uhrzeigersinn 90°** aus der Dropdown-Liste Drehung anzeigen .

   <img src="./assets/view-rotation-page-props.png" width="300">

   1. Klicken **Alle speichern** , um die aktualisierten Seitenlayouteigenschaften zu speichern.

1. Erstellen Sie einen benutzerdefinierten Stil, um das neue Seitenlayout zu verwenden.
   1. Erweitern Sie die linke Seitenleiste und doppelklicken Sie auf die Vorlage, in der Sie den Stil erstellen möchten.

   1. Erweitern Sie den Abschnitt Stylesheets .

   1. Bewegen Sie den Mauszeiger über das Layout-Stylesheet und klicken Sie auf (_Optionen_ ) ... und wählen Sie &quot;Bearbeiten&quot;.

      Das Stylesheet Layout wird zur Bearbeitung geöffnet.

   1. Rechtsklick **Weitere Stile** und wählen Sie **Neuer Stil**.
      <img src="./assets/stylesheet-other-new-style.png" width="300">

   1. Geben Sie im Popup Stil hinzufügen **Querformat** im **classname**.
      <img src="./assets/stylesheet-new-landscape-style.png" width="400">

   1. Klicken Sie auf **Fertig**.

      Ein neuer Stil mit dem Namen `.landscape-style` wird erstellt und am Ende der Liste Andere Stile hinzugefügt.

   1. Doppelklicken Sie auf die `.landscape-style` -Stil, um ihn zur Bearbeitung zu öffnen.

   1. Erweitern Sie die **Paginierung** -Eigenschaft.

   1. Eingabe `Landscape` im **Seitenlayout** -Eigenschaft.

      <img src="./assets/new-style-with-landscape-layout.png" width="500">

   1. Klicken **Alle speichern** , um die aktualisierten Stileigenschaften zu speichern.

1. Fügen Sie den Stil im `outputclass` Definition der Tabelle, die im Querformat-Seitenlayout dargestellt werden soll.
   1. Öffnen Sie in einem DITA-Dateieditor die Datei, auf die Sie das neue Seitenlayout anwenden möchten.

   1. Suchen Sie die `<table>` -Element, das im Querformat gerendert werden soll.

   1. Klicken Sie im Breadcrumb auf das Tabellenelement, um die Tabelle auszuwählen.

      <img src="./assets/new-style-table-element.png" width="400">

   1. Klicken Sie im rechten Bereich auf und öffnen Sie den Bereich Inhaltseigenschaften .

   1. Fügen Sie im Bereich &quot;Inhaltseigenschaften&quot;eine neue **outputClass** Eigenschaft mit **Querformat** als Eigenschaftswert.

      <img src="./assets/new-style-table-outputclass.png" width="300">

1. Klicken **Alle speichern** , um die aktualisierte Datei zu speichern.
1. Generieren Sie die PDF-Ausgabe.

Der Tabelleninhalt wird am Anfang des PDF im Querformat gerendert.

### Hintergrundbild hinzufügen

Je nach Ihren Anforderungen können Sie ein Hintergrundbild hinzufügen, das auf jeder ersten Seite einer Kapitelausgabe (PDF) angezeigt wird. Mit den Hintergrundeigenschaften unter &quot;Seiteneigenschaften&quot;können Sie einfach ein Hintergrundbild hinzufügen. Sie können dieses Bild auf einer Seite replizieren und das Bild an einer beliebigen Stelle im oberen, unteren oder mittleren Bereich der Seite positionieren.

Um beispielsweise ein Hintergrundbild in den mittleren Teil Ihres Inhaltsbereichs einzufügen, führen Sie die folgenden Schritte aus:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie auf eine beliebige Stelle im Inhaltsbereich.

1. Klicken Sie im rechten Bereich auf **Seiteneigenschaften**.

1. Erweitern Sie die **Hintergrund** Abschnitt.

1. Klicken Sie auf die Schaltfläche &quot;Durchsuchen&quot;im **Bildpfad** Ortsfeld.

1. Suchen Sie nach dem Bild, das Sie als Hintergrundbild verwenden möchten, und wählen Sie es aus.

   Das Bild wird eingefügt und repliziert, um die gesamte Seite abzudecken.

1. Ändern Sie die Bildgröße, indem Sie die Höhe- und Breiteneigenschaften anpassen.

   >[!NOTE]
   >
   >Sie können eine der Eigenschaften für Höhe oder Breite eingeben, da das Bild automatisch skaliert wird, um das Seitenverhältnis beizubehalten.

1. Legen Sie die anderen Eigenschaften fest, um die gewünschte Darstellung des Hintergrundbilds anzupassen.

   * **Wiederholung im Hintergrund** : Geben Sie an, ob der Hintergrund wiederholt werden soll oder nicht.

   * **Hintergrundposition** : Legen Sie eine Position für das Hintergrundbild auf Ihrer Seite fest.

Der folgende Screenshot zeigt das Hintergrundbild mit der Eigenschaft &quot;Background Repeat&quot;auf _no-repeat_ und Eigenschaft &quot;Background Position&quot;auf _Zentrum_.

<img src="./assets/background-image.png" width="500">

## Arbeiten mit Seitenkopf- und -fußzeile

Wenn Sie Informationen in eine Kopf- oder Fußzeile eines Seitenlayouts aufnehmen, werden diese Informationen auf allen Seiten mit diesem Seitenlayout wiederholt. In der Regel wird der Kopfzeilenbereich für den Kapitel- oder Thementitel und der Fußzeilenbereich für die Anzeige der Seitenzahlen verwendet.

Wenn Sie ein neues Seitenlayout erstellen, wird der Kopf- und Fußzeilenbereich standardmäßig erstellt. Sie können viele Anpassungen im Kopf- und Fußzeilenbereich eines Seitenlayouts vornehmen. Sie können beispielsweise ein Bild (wie ein Logo), Variablen (mit dynamischen Informationen) oder statischen Inhalt einfügen.

### Ändern der Kopf- und Fußzeilenränder und -zeilen

Standardmäßig sind die Ränder für Kopf- und Fußzeilen auf 1 Zoll eingestellt. Sie können diesen Standardwert ändern, indem Sie im Bereich Seiteneigenschaften die Einstellung Rand ändern. Führen Sie die folgenden Schritte aus, um die Kopf- und Fußzeilengröße zu ändern:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie im rechten Bereich auf **Seiteneigenschaften**.
1. Erweitern Sie die **Layout** Abschnitt.
1. Klicken Sie auf das Sperrsymbol neben dem **Marge** -Eigenschaft.
1. Um die Größe der Kopfzeile zu ändern, geben Sie den gewünschten Wert in das Feld Oberer Rand ein.

   >[!NOTE]
   >
   >Einige der am häufigsten verwendeten Einheiten sind px (Pixel), pt (Punkte), rem, em, % (Prozent) und in (Zoll).

1. Um die Fußzeilengröße zu ändern, geben Sie den gewünschten Wert in das Feld &quot;Unterer Rand&quot;ein.

Sie können den Kopf- und Fußzeilenbereich so gestalten, dass er mehrere Zeilen enthält. Fügen Sie dazu einen \ hinzu&lt;p> -Tag mit der Einfüge-HTML Elemente (<img src="./assets/insert-html-element-2.svg" width="25">) im Kopf- oder Fußzeilenbereich.

| _Entwicklerecke_: <img src="./assets/developer-corner-icon.svg" width="25"> |
|---|

Wenn Sie direkt mit dem CSS- und HTML-Code arbeiten möchten, können Sie die Randwerte ändern, wie im folgenden Codefragment gezeigt:

```css
…

<meta name="page-style" content="size:A4 portrait;margin-top:3cm;margin-right:30pt;margin-bottom:1in;margin-left:90px;" />

…
```

>[!NOTE]
>
>Im obigen Beispiel werden verschiedene Einheiten verwendet, um die Randwerte anzugeben.

### Kopf- und Fußzeile entfernen

Die Überlagerung für Kopf- und Fußzeile befindet sich am oberen und unteren Rand. Technisch gesehen bedeutet dies, dass Sie, wenn Sie eine Kopf- und Fußzeile in Ihrem Seitenlayout haben möchten, den erforderlichen Platz am oberen und unteren Rand beibehalten müssen.

Wenn Sie nicht möchten, dass ein Seitenlayout über eine Kopf- und Fußzeile verfügt, gibt es zwei Möglichkeiten, dies zu erreichen:

* Wenn Sie die oberen und unteren Ränder beibehalten möchten, lassen Sie den Kopf- und Fußzeilenbereich leer.
* Wenn Sie die oberen und unteren Ränder nicht beibehalten möchten (z. B. die Vorder- und Rückseite einer Zeitschrift), können Sie die Ränder entfernen, indem Sie die Eigenschaften für die oberen und unteren Ränder auf 0 setzen. Dadurch bleibt kein Platz für die Kopf- und Fußzeile.

### Hinzufügen eines Bildes oder eines Logos in der Kopfzeile

Je nach Ihren Anforderungen können Sie ein Bild hinzufügen, das im Kopfzeilenbereich (oder einem anderen Teil) des Seitenlayouts angezeigt wird. Es gibt zwei Möglichkeiten, ein Bild in Ihrem Seitenlayout hinzuzufügen:

* Verwenden Sie ein Bild aus den Vorlagenressourcen.
* Verwenden Sie den \&lt;add image=&quot;&quot;> im Seitenlayout-Editor.

>[!NOTE]
>
>Es wird empfohlen, den Ordner Ressourcen zu verwenden, um alle Vorlagen-Assets wie Bilder oder Schriftarten zu verwalten.

Gehen Sie wie folgt vor, um ein Bild wie das Logo Ihres Unternehmens in den Kopfzeilenbereich einzufügen:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

>[!NOTE]
>
>Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie auf die Kopfzeile bearbeiten (<img src="./assets/header-icon.svg" width="25">), um den Cursor in den Kopfzeilenbereich zu bringen.

   Oder klicken Sie in den Kopfzeilenbereich.

1. Um ein Bild hinzuzufügen, wählen Sie eine der folgenden Methoden:
1. Klicken Sie auf **Bild einfügen** (<img src="./assets/insert-image-icon.svg" width="25">) in der Symbolleiste; im **Pfad auswählen** Popup, navigieren Sie zur Bildposition und klicken Sie auf **Auswählen** , um sie in den Kopfzeilenbereich einzufügen.
1. Ziehen Sie ein Bild aus dem Ordner Ressourcen in den Kopfzeilenbereich.

Der folgende Screenshot zeigt ein Beispielbild, das im Kopfzeilenbereich hinzugefügt wurde.

<img src="./assets/image-in-header-area.png" width="500">

Nachdem ein Bild eingefügt wurde, können Sie seine Attribute ändern, um ihm das gewünschte Aussehen zu verleihen. Die einfachste Möglichkeit, die Darstellung eines Bildes oder eines anderen Elements im Seitenlayout zu ändern, besteht darin, den Bereich Inhaltseigenschaften zu verwenden. Siehe _Arbeiten mit dem Bereich &quot;Inhaltseigenschaften&quot;_ für die verschiedenen Eigenschaften, die über die Benutzeroberfläche zur Anpassung verfügbar sind.

### Felder und Metadaten hinzufügen

Felder sind sehr nützlich, wenn Sie vordefinierte Informationen einfügen möchten. Sie können beispielsweise ein Feld für den Kapiteltitel in den Kopfzeilenbereich Ihres Kapitels einfügen, das bei seiner Veröffentlichung durch den Titel des Kapitels ersetzt wird.

Es gibt die folgenden Kategorien für Felder, die Sie in Ihr Seitenlayout einfügen können:

* Datum
* Zeit
* Thementitel
* Projekttitel
* Page Number
* Gesamtseite
* Kapiteltitel
* Kapitelnummer
* Metadaten

Jede dieser Feldkategorien enthält verschiedene Varianten, in die die Feldinformationen eingefügt werden können. Ein Datumsfeld kann beispielsweise unterschiedliche Varianten aufweisen, z. B. `YYYY-MM-DD`, `MM/DD/YY`, `MM/DD/YYYY` und so weiter. Auf ähnliche Weise kann die Seitenzahl Variationen in Form von roman-, decimal- oder sogar gebietsschemaspezifischen Formaten wie _Arabisch_, _Devanagari_, _Hebräisch_ und mehr.

Zusätzlich zu den vordefinierten Feldern können Sie auch Metadateninformationen als Variablen oder Felder in Ihrem Seitenlayout hinzufügen. Diese Metadaten werden in Ihrem Quell-DITA-Map-Inhalt gespeichert und können einfach in Ihr Seitenlayout eingefügt werden. Weitere Informationen finden Sie unter _Arbeiten mit Feldern und Metadaten_.

Im folgenden Beispiel werden wir eine Seitenzahl und einen Kapiteltitel in den Fußzeilenbereich eines Seitenlayouts einfügen.

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie auf **Fußzeile bearbeiten** (![](./assets/footer-icon.svg)), um den Cursor in den Fußzeilenbereich zu bringen.

   Oder klicken Sie in den Fußzeilenbereich.

1. Fügen Sie ein Absatzelement ein, indem Sie auf **HTML-Elemente einfügen** (<img src="./assets/insert-html-element-2.svg" width="25">) und wählen Sie Absatz aus der Liste der Elemente aus.

1. Klicken Sie auf **Felder einfügen** (![](./assets/insert-fields-icon.svg)).

   Das Popup Felder wird angezeigt.

1. Wählen Sie die **Seitenzahl** in der Liste &quot;Feld&quot;die **default(1)** Seitennummernformat aus der Liste &quot;Format&quot;und klicken Sie auf **Einfügen**.

   <img src="./assets/insert-page-number-field.svg" width="400">

   >[!NOTE]
   >
   >Sie können auch das Format aller Felder mit Ausnahme des Standardformats bearbeiten. Klicken Sie dazu auf das Symbol Bearbeiten neben dem Format, das Sie bearbeiten möchten, nehmen Sie Änderungen vor und klicken Sie auf OK. Weitere Informationen finden Sie unter _Arbeiten mit Feldern und Metadaten_.

   Das standardmäßige Feld für die Seitenzahl wird in den Fußzeilenbereich des Seitenlayouts eingefügt.

   <img src="./assets/page-number-field-in-footer.png" width="400">

   Im oberen Breadcrumb werden die Elemente aufgelistet, in denen die Informationen gespeichert werden.

1. Geben Sie nach dem Feld &quot;Seitenzahl&quot;eine leere Stelle ein und klicken Sie auf die Schaltfläche **Felder einfügen** Symbol.

1. Wählen Sie die **Kapiteltitel** in der Liste &quot;Feld&quot;die **Kapiteltitel** in der Liste &quot;Format&quot;auf &quot;Format&quot;klicken und **Einfügen**.

   Die _Kapiteltitel_ -Feld, das zum Zeitpunkt der Veröffentlichung mit dem Titel des Kapitels gefüllt wird, wird in den Fußzeilenbereich eingefügt. Derzeit sind die Felder für die Seitenzahl und den Kapiteltitel durch ein Leerzeichen getrennt.

   <img src="./assets/page-number-topic-title-near-footer.png" width="400">

1. Um den Kapiteltitel rechtsbündig auszurichten, führen Sie die folgenden Schritte aus:

   1. Klicken Sie auf das Element Feld im Breadcrumb, um das Feld Kapiteltitel auszuwählen.

   1. Klicken Sie im rechten Bereich auf die **Inhaltseigenschaften** (<img src="./assets/content-properties-icon.png" width="25">) icon.

   1. Erweitern Sie die **Layout** Eigenschaftenabschnitt und legen Sie die **Float** Eigenschaftswert auf **right**.
      <img src="./assets/float-prop-html-content.png" width="400">

      Das Feld Kapiteltitel ist rechts neben der Fußzeile der Seite ausgerichtet.
      <img src="./assets/topic-title-moved-right-footer.png" width="500">


| _Entwicklerecke_: <img src="./assets/developer-corner-icon.svg" width="25"> |
|---|

Wenn Sie direkt mit dem CSS- und HTML-Code arbeiten möchten, können Sie dies auch erreichen, indem Sie zur Quellansicht des Seitenlayouts navigieren und Änderungen am Code vornehmen. Das folgende Codefragment zeigt dieselbe Fußzeileneinstellung, die über den Code vorgenommen wurde:

```css
…
<p>

<span data-field="page-number" data-format="default">1</span>

<span data-field="chapter-title" data-format="default" style="float: right">Chapter Title</span>

</p>
…
```

## Arbeiten mit dem Inhaltsbereich

Der Inhaltsbereich ist gemessen am Inhaltsbereich der größte Bereich. Der Inhaltsbereich wird mit dem Inhalt Ihres Themas gefüllt. In einigen Sonderfällen können Sie Bausteininhalte im Inhaltsbereich hinzufügen. Dieser Inhalt wird an der angegebenen Stelle in Ihrem Seitenlayout veröffentlicht. Beispielsweise kann die Überschrift in Ihrem Inhaltsverzeichnis, Glossar und Index als Textbausteininhalt hinzugefügt werden, der &quot;unverändert&quot;in der endgültigen Ausgabe veröffentlicht wird. Ein weiteres Beispiel ist das Kapitel-TOC, das normalerweise auf der ersten Seite eines jeden Kapitels hinzugefügt wird.

Eine der am häufigsten verwendeten Anpassungen im Inhaltsbereich ist das mehrspaltige Layout. Mit dem leistungsstarken Seitenlayout-Designer können Sie bestimmte Seiten anpassen, die in mehreren Spalten gerendert werden sollen, während der Inhalt auf anderen Seiten in einer Spalte beibehalten wird.

In den folgenden Abschnitten werden wir verschiedene Szenarien behandeln, um den Inhaltsbereich anzupassen.

### Kapitel-Inhaltsverzeichnis hinzufügen

Ein Kapitelinhaltsverzeichnis dient den Lesern als Kurzanleitung, um zu erfahren, was im Kapitel enthalten ist. Normalerweise wird ein Kapitel-Inhaltsverzeichnis ganz am Anfang eines Kapitels hinzugefügt. Wenn Sie also ein Kapitel-Inhaltsverzeichnis verwenden möchten, können Sie es im Inhaltsbereich des Hauptseitenlayouts des Kapitels oder der ersten Seitenlayoutvariante eines Kapitels hinzufügen.

Im folgenden Beispiel wird ein Kapitel-TOC in das erste Seitenlayout eines Kapitels eingefügt:

>[!NOTE]
>
>Für dieses Verfahren wird davon ausgegangen, dass Sie die erste Seitenvariante für ein Kapitelseitenlayout erstellt haben. Anweisungen zum Erstellen einer Seitenvariante finden Sie unter _Erstellen der Layout-Varianten für die erste, rechte oder linke Seite_.

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Platzieren Sie den Cursor im Inhaltsbereich des Seitenlayouts.

1. Klicken Sie auf das Kapitel-Inhaltsverzeichnis (<img src="./assets/chapter-toc-icon.svg">).

   Das standardmäßige Kapitel-Inhaltsverzeichnis wird in den Inhaltsbereich eingefügt.

   <img src="./assets/chapter-toc-default.png" width="400">

   >[!NOTE]
   >
   >Das standardmäßige Kapitel-Inhaltsverzeichnis enthält die Überschriften 1 bis 4. Hier ist Überschrift 1 der Titel des Kapitels selbst. Daher möchten Sie möglicherweise nicht, dass der Kapiteltitel erneut im Inhaltsverzeichnis enthalten ist, oder Sie möchten die Ebene der Überschriften, die Sie im Inhaltsverzeichnis anzeigen möchten, erhöhen. Sie können das Inhaltsverzeichnis anpassen, indem Sie die Eigenschaften ändern.

1. Öffnen Sie das Bedienfeld Inhaltseigenschaften , um die Überschriftenebenen des Inhaltsverzeichnisses anzupassen.

   Wenn Sie beispielsweise mit Überschrift 2 beginnen möchten, ändern Sie die erste Dropdown-Liste so, dass sie von 2 beginnt.

   <img src="./assets/customize-chapter-toc.png" width="400">

   Wenn Sie Überschriften bis Ebene 5 haben möchten, ändern Sie die zweite Dropdown-Liste in 5. Das aktualisierte Inhaltsverzeichnis sieht wie folgt aus:

   <img src="./assets/chapter-toc-updated.png" width="400">

   >[!NOTE]
   >
   >Die endgültige veröffentlichte PDF zeigt nur die TOC-Einträge basierend auf dem Inhalt in Ihren Kapiteln an. Wenn ein Kapitel keine Überschriften der Stufe 5 enthält, wird es nicht in der endgültigen Ausgabe angezeigt.

Das Erscheinungsbild des Standard-Inhaltsverzeichnisses kann mithilfe der Stylesheets angepasst werden. Der Stil beginnt mit `chaptoc-level-#` (like `chaptoc-level-1`, `chaptoc-level-2`usw.) verwendet werden, um die Stile für das Kapitel-Inhaltsverzeichnis anzupassen. Weitere Informationen zu den im Inhaltsverzeichnis verwendeten Stylesheet-Elementen und deren Anpassung finden Sie unter _Anpassen des standardmäßigen Kapitel-TOC_.

>[!IMPORTANT]
>
>Wenn Sie derzeit Stilaktualisierungen in einem Stylesheet vornehmen, wird dies möglicherweise nicht in der Inhaltsvorschau angezeigt. Die Ausgabe wird jedoch mit den aktualisierten Stilen gerendert.

### Arbeiten mit mehrspaltigem Seitenlayout

Mehrspaltige Seitenlayouts kommen häufig bei der Veröffentlichung von Zeitschriften oder Indizes in einem Buch vor. Mit der nativen PDF-Veröffentlichungsfunktion können Sie Ihr Dokument einfach in mehrere Spalten aufteilen. Bei unterschiedlichen Seitenlayouts können Sie festlegen, dass nur ein bestimmter Abschnitt in mehrere Spalten unterteilt bleibt, während Sie die anderen Abschnitte in einem einzigen Spalten- (oder normalen) Layout beibehalten.

So erstellen Sie ein Seitenlayout mit mehreren Spalten:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Da das mehrspaltige Layout auf den Inhalt angewendet wird, mit Ausnahme des Kopf- und Fußzeilenbereichs, müssen Sie das Inhaltselement im Breadcrumb auswählen.

   Nachdem Sie die Inhalts-Breadcrumb ausgewählt haben, werden im Bereich &quot;Inhaltseigenschaften&quot;die Eigenschaften für &quot;Mehrere Spalten&quot;angezeigt.

   <img src="./assets/multiple-columns-properties.png" width="400">

1. Verwenden Sie die Eigenschaften für mehrere Spalten, um das mehrspaltige Seitenlayout anzupassen:

   * **Spaltenanzahl:** Geben Sie die Anzahl der Spalten an, durch die die Seite geteilt werden soll. Verwenden Sie die Pfeilsymbole nach oben und unten oder geben Sie eine Zahl ein, um die Anzahl der Spalten festzulegen.

   * **Spaltenbreite:** Geben Sie die Breite einer Spalte in einem mehrspaltigen Layout an. Standardmäßig wird die Größe in Pixel (px) festgelegt. Sie können sie auch in pt, rem, em, % oder in Einheiten angeben.

      >[!NOTE]
      >
      >Wenn Sie keine Größe angeben, werden die Spalten gleichmäßig aufgeteilt, sodass sie zur angegebenen Seite passen. In den meisten Fällen müssen Sie diesen Wert nicht angeben.

   * **Spalten-Gap** : Geben Sie den Abstand zwischen einzelnen Spalten an.

   * **Spaltenbereich** : Wenn Sie möchten, dass ein Element im Seitenlayout über mehrere Spalten erstreckt, müssen Sie diese Eigenschaft verwenden. Dies wird erreicht, indem der Stil des gewünschten Elements mithilfe der Stylesheets geändert wird. Weitere Informationen finden Sie unter _Abschnitt zur Stilanpassung_.

   Wenn im Seitenlayout ein bestimmter Text auf der ersten Seite aller Kapitelseitenlayouts angezeigt werden soll, können Sie ihn der ersten Seitenvariante des Kapitelseitenlayouts hinzufügen.

   Wie im folgenden Beispiel gezeigt, ist die Eigenschaft Spalte spalten für den Überschriftentext auf &quot;all&quot;festgelegt. Dadurch wird sichergestellt, dass sich die Überschrift, auch wenn das Dokument mehrspaltig ist, über mehrere Spalten erstreckt.

   <img src="./assets/element-span-across-columns.png" width="400">

   >[!IMPORTANT]
   >
   >Sie können die Eigenschaft &quot;Span Column&quot;mithilfe des Attributs &quot;outputClass&quot;auf jedes DITA-Element anwenden.

   * **Spaltenfüllung** : Geben Sie an, wie Spalten mit Inhalt gefüllt werden sollen. Standardmäßig ist dies auf Balance gesetzt, wodurch jede Spalte mit gleicher Inhaltsmenge gefüllt wird.

   * **Spaltenregel** : Wenn Sie eine Zeile zwischen Spalten haben möchten, verwenden Sie diese Eigenschaft, um die Zeilen- oder Regelstile zu definieren. Geben Sie die Werte für Stil, Farbe und Breite des Lineals an, um eine Linie zwischen den Spalten hinzuzufügen.


## Arbeiten mit dem Bereich &quot;Inhaltseigenschaften&quot;

Im Bereich &quot;Inhaltseigenschaften&quot;können Sie das Erscheinungsbild der Elemente auf Ihrer Seite einfach aktualisieren. Die Eigenschaften im Bereich Inhaltseigenschaften sind in die folgenden Abschnitte unterteilt:

* **Schriftart** : Enthält textbezogene Eigenschaften. Sie können Schriftfamilie, Gewichtung, Größe, Textdekoration (als Unterstrichen, Überstrichen, Zeilenumbruch), Textstil (als Fett, kursiv usw.), Textausrichtung (als links, rechts, zentriert oder ausgerichtet) festlegen, Leerzeichen (als vordefiniertes Format, kein Umbruch, Zeilenhöhe, Zeichenabstand und Textinzug) verarbeiten.

* **Rahmen** : Enthält Eigenschaften zum Hinzufügen und Formatieren eines Rands zu einem Element im Seitenlayout. Sie können für einen gekrümmten Rand &quot;Rahmenseitenstil&quot;(wie alle, oben, unten, rechts oder links), &quot;Rahmenstil&quot;(als &quot;Durchgehend&quot;, &quot;Gestrichelt&quot;, &quot;Punktlinien&quot;oder mehr), &quot;Rahmenfarbe&quot;, &quot;Breite&quot;und &quot;Radius&quot;festlegen. Im folgenden Beispiel wurde im Kopfzeilenbereich der Seite ein gekrümmter Rand hinzugefügt.

   <img src="./assets/border-properties.png" width="500">

* **Layout** : Enthält Eigenschaften zum Konfigurieren des Layouts eines Elements im Seitenlayout. Sie können Höhe, Breite, Spannen und Abstand (für oben, unten, links oder rechts), Horizontale oder vertikale Ausrichtung, Gleitkommazahl (als links, rechts oder nicht), Löschen (als links, rechts, beides oder ohne), Elementposition (als absolut, fest, relativ oder mehr), Anzeige (als Block, Inhalt, Korrektur oder höher), Z Index, Transparenz, Transformierung (durch Drehen oder Skalieren) festlegen. ) und &quot;Ursprung transformieren&quot;(durch X und Y-Versatz).

* **Hintergrund** : Enthält Eigenschaften zum Einschließen eines Hintergrundbilds oder einer Farbschattierung. Sie können die Bildgröße (durch Festlegen von Höhe oder Breite), die Hintergrundwiederholung (als Wiederholung, Keine Wiederholung, Runde oder mehr) und die Hintergrundposition (als links oben, rechts, Mitte unten oder mehr) festlegen.
* **Mehrere Spalten** : Enthält Eigenschaften zum Konfigurieren mehrspaltiger Eigenschaften für die Seite oder eines bestimmten Elements, z. B. Kapitel-Inhaltsverzeichnis. Weitere Informationen zu den Eigenschaften und deren Verwendung finden Sie unter _Arbeiten mit mehrspaltigem Seitenlayout_.
