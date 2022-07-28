---
title: Native PDF-Veröffentlichungsfunktion | Erstellen eines Seitenlayouts
description: Erfahren Sie, wie Sie Ihr Seitenlayout für die Präsentation von Informationen in verschiedenen Bereichen Ihrer PDF-Ausgabe entwerfen.
hide: true
hidefromtoc: true
exl-id: b4d3bdc4-0d01-46eb-b182-540380220485
source-git-commit: 64e8ab1288674437f6182010ce4963b3780e98a9
workflow-type: tm+mt
source-wordcount: '3289'
ht-degree: 0%

---


# Erstellen eines Seitenlayouts

Bei der Erstellung eines PDF-Dokuments würden Sie verschiedene Bereiche für die Darstellung verschiedener Informationstypen haben. Beispielsweise würde ein PDF-Dokument von einer Vorder- oder Titelseite aus beginnen, die das Logo, den Buchtitel oder die Versionsinformationen Ihres Unternehmens enthält. Dann gibt es Kapitel, Anhänge oder Glossarseiten. Jeder Bereich in einem PDF-Dokument sieht anders aus, was durch Erstellen und Anpassen des Seitenlayouts erreicht wird.

Beim Entwerfen des Seitenlayouts können Sie die verschiedenen Elemente einer Seite definieren. Sie können beispielsweise die Seitengröße, die Ränder, Kopf- und Fußzeilen, die Ausrichtung und andere Seitenspezifikationen auf einer Seite definieren. Mit der nativen PDF-Veröffentlichungsfunktion können Sie Ihre Seite gemäß den CSS-Standards für Seitenmedien gestalten. Die meisten Einstellungen, die unter den CSS-Seitenmedien behandelt werden, können einfach über die Benutzeroberfläche der Nativen PDF-Funktion angepasst werden. Für weitere Formatierungen auf erweiterter Ebene können Sie die Quellansicht verwenden, um Ihren eigenen CSS-Code zu schreiben.

Nachdem Sie die Seitenlayouts entworfen haben, müssen Sie diese Layouts mit den entsprechenden Abschnitten in den PDF-Seitenlayouteinstellungen verknüpfen. Siehe _Seitenlayouts erstellen und anpassen_ -Abschnitt für Details zum Erstellen und Öffnen eines Seitenlayouts für die Anpassung.

## Typen von Seitenlayouts und deren Varianten

Ein PDF-Dokument enthält in der Regel die folgenden Abschnitte:

* Titelseite
* Inhaltsverzeichnis
* Aufstockung der Zahlen
* Tabellensteigerung
* Kapitel- oder Themenseiten
* Glossar
* Index
* Zurück-Seite

Diese Abschnitte benötigen ein entsprechendes Seitenlayout, um die Informationen in einem bestimmten Format darzustellen. Darüber hinaus können Sie auch eine leere Seite haben, die als Füller verwendet wird, um ein neues Kapitel von einer ungeraden oder geraden Seite aus zu beginnen. In diesem Fall benötigen Sie ein leeres Seitenlayout.

Die Einstellungen für Seitenlayouts unter **Vorlage > Einstellungen** -Bereich können Sie definieren, welche Vorlage für verschiedene Bereiche Ihrer PDF verwendet werden soll. Jedes Seitenlayout kann außerdem unterschiedliche Erst-, Rechts- oder Links-Seitenkombinationen aufweisen. Diese Regeln werden durch die Regeln bestimmt, die im *CSS-Seitenmedien* -Standards.

## Erstellen der ersten, rechten oder linken Seitenlayouts

Verschiedene Seitenlayouts in Ihrer PDF-Vorlage können weiter angepasst werden, indem Sie unterschiedliche Seitenlayouts auf der ersten, rechten oder linken Seite haben. Sie können diese Seiten mit dem Seitenlayout-Designer unterschiedlich entwerfen.

>[!NOTE]
>
>Wenn Sie ein einseitiges Seitenlayout für einen Abschnitt in Ihrem Buch haben möchten, müssen Sie keine Layouts für die erste, rechte oder linke Seite erstellen.


Beachten Sie beim Erstellen der Seitenlayouts die folgenden Punkte:

* Wenn Sie ein einzelnes Seiten-Layout für alle Seiten in einem Kapitel verwenden möchten, erstellen Sie nur ein einzelnes Kapitel-Seitenlayout.
* Wenn Sie ein anderes Erscheinungsbild für die erste Seite für Kapitel in Ihrem Buch haben möchten, müssen Sie ein Layout für die erste Seite für Ihre Kapitel erstellen.
* Wenn Sie für jede linke und rechte Seite Ihres Buches ein anderes Erscheinungsbild wünschen, müssen Sie die Varianten Links und Rechts für Ihr Kapitel-Seitenlayout erstellen.
* Wenn Ihre Kapitel von einer ungeraden oder geraden Seite beginnen sollen, müssen Sie ein leeres Seitenlayout erstellen. Mit diesem Seitenlayout wird die Lücke zwischen zwei Kapiteln gefüllt, um sicherzustellen, dass das Kapitel von der gewünschten ungeraden oder geraden Seite beginnt.

Das folgende Beispiel führt Sie durch den Prozess der Erstellung von Varianten eines Seitenlayouts:

1. Erstellen Sie ein &quot;Kapitel&quot;-Seitenlayout anhand der unter *Neues Seitenlayout erstellen* Verfahren.

   Unter Seitenlayouts wird ein leeres Seiten-Layout für Kapitel erstellt und hinzugefügt.

   Wenn Sie ein Seitenlayout erstellen, wird es standardmäßig auch zur Bearbeitung geöffnet. Im folgenden Screenshot wird ein leeres (standardmäßiges) Seitenlayout angezeigt:

   <img src="./assets/default-blank-page-layout.png" width="300">

   Der Kopf-, Fußzeilen- und Inhaltsbereich in einer Vorlage wird standardmäßig erstellt. Sie können diese Bereiche einfach mithilfe der Tools, Seiteneigenschaften und Inhaltseigenschaften anpassen, die in der Benutzeroberfläche angegeben sind. Für eine erweiterte Konfiguration können Sie die Quellansicht verwenden und Ihren benutzerdefinierten HTML- und CSS-Code hinzufügen.

1. So erstellen Sie eine Variante für das Seiten-Layout &quot;Kapitel&quot;:

   1. Bewegen Sie den Mauszeiger über den **Kapitel** und klicken Sie auf **Optionen** , um das Kontextmenü anzuzeigen.

   1. Klicken oder bewegen Sie den Mauszeiger über **Layout-Variante hinzufügen** und wählen Sie das gewünschte Seitenlayout (Erste, Links oder Rechts), das Sie erstellen möchten.

   Das Layout der ausgewählten Seite wird mithilfe einer Kopie des grundlegenden Kapitellayouts erstellt. Das bedeutet, dass, wenn Sie Änderungen am standardmäßigen Seiten-Layout für Kapitel vorgenommen haben, dieselben Änderungen im Seitenlayout für Varianten repliziert werden.

## Arbeiten mit Bildern in einem Seitenlayout

Je nach Ihren Anforderungen können Sie ein Bild hinzufügen, das auf jeder ersten Seite einer Kapitelausgabe (PDF) angezeigt wird. Die <u>**Bild hinzufügen**</u> im Seitenlayout-Editor verwendet, um Bilder in ein Seitenlayout einzufügen.

Wenn Sie beispielsweise ein Bild in den Kopfzeilenbereich der ersten Seite Ihrer Kapitelausgabe einfügen möchten, führen Sie die folgenden Schritte aus:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie auf die Kopfzeile bearbeiten (<img src="./assets/header-icon.svg" width="25">), um den Cursor in den Kopfzeilenbereich zu bringen.

1. Klicken Sie auf das Inert-Bild (<img src="./assets/insert-image-icon.svg" width="25">) icon.

   Das Popup Pfad auswählen wird angezeigt.

1. Navigieren Sie zur Bildposition und klicken Sie auf Auswählen , um es in den Kopfzeilenbereich einzufügen.

   Der folgende Screenshot zeigt ein Beispielbild, das im Kopfzeilenbereich hinzugefügt wurde.

   <img src="./assets/image-in-header-area.png" width="500">

   Nachdem ein Bild eingefügt wurde, können Sie seine Attribute ändern, um ihm das gewünschte Aussehen zu verleihen. Die einfachste Möglichkeit, die Darstellung eines Bildes oder eines anderen Elements im Seitenlayout zu ändern, besteht darin, dies im Bereich Inhaltseigenschaften vorzunehmen. Siehe _Arbeiten mit dem Bereich &quot;Inhaltseigenschaften&quot;_ für die verschiedenen Eigenschaften, die über die Benutzeroberfläche zur Anpassung verfügbar sind.

## Arbeiten mit Feldern

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

Jede dieser Feldkategorien enthält verschiedene Varianten, in die die Feldinformationen eingefügt werden können. Ein Datumsfeld kann beispielsweise unterschiedliche Varianten aufweisen, z. B. `YYYY-MM-DD`, `MM/DD/YY`, `MM/DD/YYYY` und so weiter.

Im folgenden Beispiel werden wir eine Seitenzahl und einen Thementitel in den Fußzeilenbereich unseres Seitenlayouts einfügen.

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Klicken Sie auf Fußzeile bearbeiten (![](./assets/footer-icon.svg)), um den Cursor in den Fußzeilenbereich zu bringen.

1. Fügen Sie ein Absatzelement ein, indem Sie auf HTML &quot;Elemente einfügen&quot;klicken <img src="./assets/insert-html-element-2.svg" width="25"> und wählen Sie Absatz aus der Liste der Elemente aus.

1. Klicken Sie auf Felder einfügen ( ![](./assets/insert-fields-icon.svg)).

   Das Popup Felder wird angezeigt.

1. Wählen Sie die **Seitenzahl** in der Liste &quot;Feld&quot;die **default(1)** Seitennummernformat aus der Liste &quot;Format&quot;und klicken Sie auf **Einfügen**.

   <img src="./assets/insert-page-number-field.svg" width="400">

   <br>

   >[!NOTE]
   >
   >Sie können auch das Format aller Felder mit Ausnahme des Standardformats bearbeiten. Klicken Sie dazu auf das Symbol Bearbeiten neben dem Format, das Sie bearbeiten möchten, nehmen Sie Änderungen vor und klicken Sie auf OK.

   Das standardmäßige Feld für die Seitenzahl wird in den Fußzeilenbereich des Seitenlayouts eingefügt.

   <img src="./assets/page-number-field-in-footer.png" width="400">

   Im oberen Breadcrumb werden die Elemente aufgelistet, in denen die Informationen gespeichert werden.

1. Geben Sie nach dem Feld &quot;Seitenzahl&quot;eine leere Stelle ein und klicken Sie auf die Schaltfläche **Felder einfügen** Symbol.

1. Wählen Sie die **Thementitel** in der Liste &quot;Feld&quot;die **Chapter.ptl** Titelformat in der Liste &quot;Format&quot;und klicken Sie auf &quot;Einfügen&quot;.

   Die `Chapter.ptl` -Feld, das zum Zeitpunkt der Veröffentlichung mit dem Titel des Themas gefüllt wird, wird in den Fußzeilenbereich eingefügt. Derzeit sind die Felder für die Seitenzahl und den Thementitel durch ein Leerzeichen getrennt.

   <img src="./assets/page-number-topic-title-near-footer.png" width="400">

1. Um den Thementitel rechtsbündig auszurichten, führen Sie die folgenden Schritte aus:

   1. Klicken Sie im Breadcrumb auf das Element Feld , um das Feld für den Thementitel auszuwählen.

   1. Klicken Sie im rechten Bereich auf HTML Content Properties.

      <img src="./assets/right-pane-content-properties.png" width="350">

   1. Erweitern Sie die **Layout** Eigenschaftenabschnitt und legen Sie die **Float** Eigenschaftswert auf **right**.

      <img src="./assets/float-prop-html-content.png" width="350">

      Das Feld für den Thementitel ist rechts neben der Fußzeile der Seite ausgerichtet.

      <img src="./assets/topic-title-moved-right-footer.png" width="500">

| Entwicklerecke: | <img src="./assets/developer-corner-icon.svg" width="25"> |
|--- |--- |
| Wenn Sie direkt mit dem CSS- und HTML-Code arbeiten möchten, können Sie dies auch erreichen, indem Sie zur Quellansicht des Seitenlayouts navigieren und Änderungen am Code vornehmen. Das folgende Codefragment zeigt dieselbe Fußzeileneinstellung, die über den Code vorgenommen wurde: |

```md
…
<div data-region="footer">
	<p>
		<span data-field="page-number" data-format="default">1</span>
		<span data-field="title" data-format="default" style="float: right">Chapter.plt</span>
	</p>
</div>
…
```

## Kapitel-Inhaltsverzeichnis hinzufügen

Ein Kapitel oder ein Mini-Inhaltsverzeichnis dient den Lesern als Kurzübersicht, was im Kapitel enthalten ist. Normalerweise wird ein Kapitel-Inhaltsverzeichnis ganz am Anfang eines Kapitels hinzugefügt. Wenn Sie also ein Kapitel-Inhaltsverzeichnis verwenden möchten, können Sie es zum Hauptseitenlayout für Kapitel oder zum Layout Erste Seite eines Kapitels hinzufügen.

Im folgenden Beispiel wird ein Kapitel-TOC in das Layout Erste Seite eines Kapitels eingefügt:

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

1. Öffnen Sie das Bedienfeld HTML Content Properties , um die Überschriftenebenen des Inhaltsverzeichnisses anzupassen.

   Wenn Sie beispielsweise mit Überschrift 2 beginnen möchten, ändern Sie die erste Dropdown-Liste so, dass sie von 2 beginnt.

   <img src="./assets/customize-chapter-toc.png" width="400">

   Wenn Sie Überschriften bis Ebene 5 haben möchten, ändern Sie die zweite Dropdown-Liste in 5. Das aktualisierte Inhaltsverzeichnis sieht wie folgt aus:

   <img src="./assets/chapter-toc-updated.png" width="400">

   <br>

   >[!NOTE]
   >
   >Die endgültige veröffentlichte PDF zeigt nur die TOC-Einträge basierend auf dem Inhalt in Ihren Kapiteln an. Wenn ein Kapitel keine Überschriften der Stufe 5 enthält, wird es nicht in der endgültigen Ausgabe angezeigt.

## Arbeiten mit mehrspaltigem Seitenlayout

Mehrspaltige Seitenlayouts kommen häufig bei der Veröffentlichung von Zeitschriften oder Indizes in einem Buch vor. Mit der nativen PDF-Veröffentlichungsfunktion können Sie Ihr Dokument einfach in mehrere Spalten aufteilen. Bei unterschiedlichen Seitenlayouts können Sie festlegen, dass nur ein bestimmter Abschnitt in mehrere Spalten unterteilt bleibt, während Sie die anderen Abschnitte in einem einzigen Spalten- (oder normalen) Layout beibehalten.

So erstellen Sie ein Seitenlayout mit mehreren Spalten:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe _Seitenlayout anpassen_ zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Da das mehrspaltige Layout auf den Inhalt angewendet wird, mit Ausnahme des Kopf- und Fußzeilenbereichs, müssen Sie das Inhaltselement im Breadcrumb auswählen.

   Sobald Sie die Inhalts-Breadcrumb ausgewählt haben, werden im Bereich HTML Content Properties die Eigenschaften für Multiple Columns angezeigt.

   <img src="./assets/multiple-columns-properties.png" width="400">

1. Verwenden Sie die Eigenschaften für mehrere Spalten, um das mehrspaltige Seitenlayout anzupassen:

   * **Spaltenanzahl:** Geben Sie die Anzahl der Spalten an, durch die die Seite geteilt werden soll. Verwenden Sie die Pfeilsymbole nach oben und unten oder geben Sie eine Zahl ein, um die Anzahl der Spalten festzulegen.

   * **Spaltenbreite:** Geben Sie die Breite einer Spalte in einem mehrspaltigen Layout an. Standardmäßig wird die Größe in Pixel (px) festgelegt. Sie können sie auch in pt, rem, em, % oder in Einheiten angeben.

      >[!NOTE]
      >
      >Wenn Sie keine Größe angeben, werden die Spalten automatisch an die angegebenen Seitenränder angepasst.

   * **Spalten-Gap** : Geben Sie den Abstand zwischen einzelnen Spalten an.

   * **Spaltenbereich** : Wenn Sie möchten, dass ein Element im Seitenlayout über mehrere Spalten erstreckt, müssen Sie diese Eigenschaft verwenden. Dies wird erreicht, indem der Stil des gewünschten Elements mithilfe der Stylesheets geändert wird. Weitere Informationen finden Sie unter _\&lt;section explaining=&quot;&quot; style=&quot;&quot; customization=&quot;&quot;>_.

   Wenn im Seitenlayout ein bestimmter Text auf der ersten Seite aller Kapitelseitenlayouts angezeigt werden soll, können Sie ihn der ersten Seitenvariante des Kapitelseitenlayouts hinzufügen.

   Wie im folgenden Beispiel gezeigt, ist die Eigenschaft Spalte spalten für den Überschriftentext auf &quot;all&quot;festgelegt. Dadurch wird sichergestellt, dass sich die Überschrift, auch wenn das Dokument mehrspaltig ist, über mehrere Spalten erstreckt.

   <img src="./assets/element-span-across-columns.png" width="400">

   <br>

   >[!IMPORTANT]
   Sie können die Eigenschaft &quot;Span Column&quot;auf jedes DITA-Element anwenden.

   * **Spaltenfüllung** : Geben Sie an, wie Spalten mit Inhalt gefüllt werden sollen. Standardmäßig ist dies auf Balance gesetzt, wodurch jede Spalte mit gleicher Inhaltsmenge gefüllt wird.

   * **Spaltenregel** : Wenn Sie eine Zeile zwischen Spalten haben möchten, verwenden Sie diese Eigenschaft, um die Zeilen- oder Regelstile zu definieren. Geben Sie die Werte für Stil, Farbe und Breite des Lineals an, um eine Linie zwischen den Spalten hinzuzufügen.


## Seiteneigenschaften für unterschiedliche Seitenausrichtung verwenden

Beim Entwerfen eines Seitenlayouts ist es wichtig, die verschiedenen Seiteneigenschaften zu steuern. Die native PDF-Funktion enthält alle wichtigen Seiteneigenschaften im Bereich Seiteneigenschaften . Der Bereich Seiteneigenschaften bietet Zugriff auf verschiedene Eigenschaften in den folgenden Abschnitten:

* **Seitengröße**: Geben Sie die Seitengröße für das Seitenlayout an. In der Dropdownliste Seitengröße können Sie aus über 15 Seitengrößen wählen.

* **Ausrichtung**: Geben Sie die Seitenausrichtung für das Seitenlayout an. Sie können zwischen den Ausrichtungen Hochformat oder Querformat wählen. Beachten Sie, dass Sie in einem Seitenlayout unterschiedliche Ausrichtungen auf verschiedene Seitenvarianten anwenden können. Sie können beispielsweise die Ausrichtung im Hochformat auf der ersten Seite und das Querformat auf den Layouts der linken und rechten Seite festlegen.

* **Rotation anzeigen**: Geben Sie die Ansicht oder Richtung an, in der der Inhalt auf der Seite angeordnet ist. Sie können zwischen dem Uhrzeigersinn 90, dem Uhrzeigersinn 90 oder dem Uhrzeigersinn 180 Grad wählen. Dies ist sehr nützlich in einer Situation, in der Sie eine Kombination aus Hochformat- und Querformat-Layouts in Ihrer Ausgabe verwenden möchten. Sie können beispielsweise Hochformat als generisches Seitenlayout verwenden und für die Erfassung langer Tabellen ein Querformat-Seitenlayout festlegen. In diesem Fall können Sie festlegen, dass der Tabelleninhalt in Uhrzeigersinn 90 Grad angezeigt wird. Dadurch wird die Seite im Querformat ausgerichtet und der Inhalt wird um 90 Grad gedreht, um die Kontinuität im Blick zu wahren. Wir werden sehen, wie dies erreicht wird, als Beispiel weiter unten in diesem Abschnitt.

* **Nummerierung neu starten von**: Geben Sie die Seitenzahl an, von der aus die Nummerierung für dieses Seitenlayout beginnen soll. Sie können beispielsweise ein Seitenlayout für den Abschnitt &quot;Anhang&quot;in Ihrem Buch erstellen und die Nummerierung so einstellen, dass sie von 1 neu gestartet wird.

* **Layout**: Geben Sie die Seitenränder zusammen mit dem Abstand für die oberen, unteren, linken und rechten Seiten an.

* **Hintergrund**: Fügen Sie ein Bild als Hintergrundbild in Ihr Seitenlayout ein. Sie können die Höhe und Breite des Bildes sowie die Wiederholungs- und Positionseigenschaften angeben.

* **Fußnote**: Geben Sie die Eigenschaften an, mit denen Fußnoten in der Ausgabe angezeigt werden sollen. Sie können die Eigenschaften für Ränder und Abstand sowie einen Randstil festlegen.

Sehen wir uns ein Beispiel an, in dem eine Kombination aus Seitenausrichtung im Hoch- und Querformat und Seitendrehungseigenschaften verwendet wird. In diesem Beispiel wird eine PDF mit standardmäßiger Hochformatausrichtung erstellt, eine Tabelle wird jedoch im Querformat mit Inhalten in der 90-Grad-Ansicht im Uhrzeigersinn gerendert. Die endgültige Ausgabe sieht in etwa wie folgt aus:

<img src="./assets/portrait-landscape-page-layouts.png" width="400">

In der obigen Ausgabe werden die Kontaktlisten-Informationen im Querformat angezeigt, wobei der Inhalt ebenfalls um 90 Grad gedreht wird. Der restliche Inhalt wird im normalen Hochformat angezeigt.

Um diese Art von Ausgabe zu erzielen, müssen wir die folgenden Hauptaufgaben durchführen:

1. Erstellen Sie ein Seitenlayout mit der Ausrichtung &quot;Querformat&quot;.
1. Ändern Sie die Eigenschaft &quot;View Rotation&quot;, um Inhalte im Uhrzeigersinn in 90 Grad zu rendern.
1. Erstellen Sie einen benutzerdefinierten Stil, um das neue Seitenlayout zu verwenden.
1. Fügen Sie den Stil in der Ausgabedefinition der Tabelle hinzu, die wir im Querformat-Seitenlayout rendern möchten.

Führen Sie die folgenden Schritte aus, um die oben genannten Aufgaben zu erledigen:

1. Erstellen Sie ein Seitenlayout mit der Ausrichtung &quot;Querformat&quot;.
   1. Erstellen Sie ein &quot;Querformat&quot;-Seitenlayout anhand der unter &quot;Neues Seitenlayout erstellen&quot;beschriebenen Schritte.

   1. Klicken Sie im rechten Bereich auf **Seiteneigenschaften**.

      <img src="./assets/page-properties-panel.png" width="300">
   1. Ändern Sie die **Ausrichtung** nach **Querformat**.

1. Ändern Sie die Eigenschaft &quot;View Rotation&quot;, um Inhalte im Uhrzeigersinn in 90 Grad zu rendern.

   1. Auswählen **Im Uhrzeigersinn 90°** aus der Dropdown-Liste Drehung anzeigen .

   1. Klicken **Alle speichern** , um die aktualisierten Seitenlayouteigenschaften zu speichern.

1. Erstellen Sie einen benutzerdefinierten Stil, um das neue Seitenlayout zu verwenden.
   1. Erweitern Sie die linke Seitenleiste und doppelklicken Sie auf die Vorlage, in der Sie den Stil erstellen möchten.

   1. Erweitern Sie den Abschnitt Stylesheets .

   1. Bewegen Sie den Mauszeiger über das Layout-Stylesheet und klicken Sie auf (_Optionen_ Symbol) **...** und wählen Sie **Bearbeiten**.

      Das Stylesheet Layout wird zur Bearbeitung geöffnet.

   1. Rechtsklick **Weitere Stile** und wählen Sie **Neuer Stil**.

      <img src="./assets/stylesheet-other-new-style.png" width="300">

   1. Im **Stil hinzufügen** Popup, Eingabe `landscape-style` im **Klasse** Namensfeld.

      <img src="./assets/stylesheet-new-landscape-style.png" width="400">

   1. Klicken Sie auf **Fertig**.

      Ein neuer Stil mit dem Namen `.landscape-style` wird erstellt und am Ende von **Weitere Stile** Liste.

   1. Doppelklicken Sie auf die `.landscape-style` -Stil, um ihn zur Bearbeitung zu öffnen.

   1. Erweitern Sie die **Paginierung** -Eigenschaft.

   1. Eingabe `Landscape` im **Seitenlayout** -Eigenschaft.

      <img src="./assets/new-style-with-landscape-layout.png" width="500">

1. Fügen Sie den Stil in der Ausgabedefinition der Tabelle hinzu, die wir im Querformat-Seitenlayout rendern möchten.

   1. Öffnen Sie im Web Editor die Datei, auf die Sie das neue Seitenlayout anwenden möchten.

   1. Suchen Sie die `<table>` -Element, das im Querformat gerendert werden soll.

   1. Klicken Sie im Breadcrumb auf die `table` -Element, um die Tabelle auszuwählen.

      <img src="./assets/new-style-table-element.png" width="400">

   1. Klicken Sie im rechten Bereich auf und öffnen Sie die **Inhaltseigenschaften** Bereich.

   1. Im **Inhaltseigenschaften** Bedienfeld hinzufügen, eine neue `outputclass` Eigenschaft mit `landscape-style` als Eigenschaftswert.

      <img src="./assets/new-style-table-outputclass.png" width="300">

   1. Klicken **Alle speichern** , um die aktualisierte Datei zu speichern.

   1. Generieren Sie die PDF-Ausgabe.

Der Tabelleninhalt wird am Anfang des PDF im Querformat gerendert.

## Arbeiten mit dem Bereich &quot;Inhaltseigenschaften&quot;

Im Bereich &quot;Inhaltseigenschaften&quot;können Sie das Erscheinungsbild der Elemente auf Ihrer Seite einfach aktualisieren. Die Eigenschaften im Bereich Inhaltseigenschaften sind in die folgenden Abschnitte unterteilt:

>[!NOTE]
Weitere Informationen zur Verwendung dieser Eigenschaften finden Sie in der Dokumentation zu den W3C CSS Page Media Standards .

* **Attribute**: Enthält Eigenschaften für ID, Klasse und Übersetzen. Wenn Sie die Eigenschaft &quot;Translate&quot;auf &quot;nein&quot;setzen, wird der Inhalt in diesem bestimmten Element nicht übersetzt.

* **Schriftart**: Enthält schriftbezogene Eigenschaften. Sie können Schriftfamilie, Gewichtung, Größe, Textdekoration (als Unterstrichen, Überstrichen, Zeilenumbruch), Textstil (als Fett, kursiv usw.), Textausrichtung (als links, rechts, zentriert oder ausgerichtet) festlegen, Leerzeichen (als vordefiniertes Format, kein Umbruch, Zeilenhöhe, Zeichenabstand und Textinzug) verarbeiten.

* **Rahmen**: Enthält Eigenschaften zum Hinzufügen und Formatieren eines Rands zu einem Element im Seitenlayout. Sie können &quot;Rahmenseitig&quot;(wie alle, &quot;Oben&quot;, &quot;Unten&quot;, &quot;Rechts&quot;oder &quot;Links&quot;), &quot;Rahmenstil&quot;(als &quot;Durchgehend&quot;, &quot;Gestrichelt&quot;, &quot;Gestapelte Linien&quot;oder mehr), &quot;Rahmenfarbe&quot;, &quot;Breite&quot;und &quot;Radius&quot;festlegen, um einen gekrümmten Rahmen zu erhalten. Im folgenden Beispiel wurde im Kopfzeilenbereich der Seite ein gekrümmter Rand hinzugefügt.

   <img src="./assets/border-properties.png" width="500">

* **Layout**: Enthält Eigenschaften zum Konfigurieren des Layouts eines Elements im Seitenlayout. Sie können Höhe, Breite, Spannen und Abstand (für oben, unten, links oder rechts), Horizontale oder vertikale Ausrichtung, Gleitkommazahl (als links, rechts oder ohne), Löschen (als links, rechts, beides oder ohne), Position des Elements (als absolut, fest, relativ oder größer), Anzeige (als Block, Inhalt, Korrektur oder höher), Z-Index, Transparenz, Umformung (durch Drehen oder Skalieren) festlegen. ) und &quot;Ursprung transformieren&quot;(durch X und Y-Versatz).

* **Hintergrund**: Enthält Eigenschaften zum Einschließen eines Hintergrundbilds oder einer Farbschattierung. Sie können die Bildgröße (durch Festlegen von Höhe oder Breite), die Hintergrundwiederholung (als Wiederholung, Keine Wiederholung, Runde oder mehr) und die Hintergrundposition (als links oben, rechts, Mitte unten oder mehr) festlegen.

* **Mehrere Spalten**: Enthält Eigenschaften zum Konfigurieren mehrspaltiger Eigenschaften für die Seite oder eines bestimmten Elements, z. B. Kapitel-Inhaltsverzeichnis. Weitere Informationen zu den Eigenschaften und deren Verwendung finden Sie unter _Arbeiten mit mehrspaltigem Seitenlayout_.
