---
title: Native PDF-Veröffentlichungsfunktion | Arbeiten mit allgemeinen Inhaltsstilen
description: Erfahren Sie, wie Sie Stile für Ihren Inhalt erstellen und Stile erstellen.
hide: true
hidefromtoc: true
source-git-commit: fb341dab718b8ae64578748d54a40df7e71af223
workflow-type: tm+mt
source-wordcount: '3500'
ht-degree: 0%

---


# Arbeiten mit allgemeinen Inhaltsstilen

Ein Stylesheet enthält die Stildefinitionen für die Elemente, die in Ihrer PDF-Ausgabe verwendet werden. Sie können zwischen der Arbeit mit den Beispiel-Stylesheets oder der Erstellung neuer Stylesheets wählen. In den meisten Fällen hilft Ihnen das Erstellen einer Kopie des OOTB-Musterstylesheets beim schnellen Einstieg.

Der Stileditor ist ein WYSIWYG-Editor, der alle Komplexität eines CSS-Codes hinter der Benutzeroberfläche ausblendet. Mithilfe des Stileditors können Sie die Stile für die Elemente Ihrer Wahl einfach und schnell anpassen. Die Stile werden unter den folgenden Überschriften kategorisiert:

* Überschriftenstile
* Absatzformate
* Zeichenformate
* Hyperlink-Stile
* Bildstile
* Listenstile
* Tabellenstile
* Div Styles
* Seitenstile
* Weitere Stile

Beim Arbeiten mit strukturierten DITA-Inhalten ist die Stilzuordnung für die meisten DITA-Elemente im Standard-Stylesheet vorhanden. Wenn Sie mit standardmäßigen DITA-Elementen arbeiten, können Sie deren Erscheinungsbild ändern, indem Sie direkt Änderungen an der Stildefinition vornehmen. Diese Stildefinitionen sind unter der Kategorie &quot;Sonstige Stile&quot;verfügbar. Weitere Informationen finden Sie unter *Arbeiten mit anderen Stilen* später in diesem Thema.

In den folgenden Abschnitten werden die am häufigsten verwendeten Stileinstellungen in Form von Beispielen beschrieben.

>[!NOTE]
>
>In den folgenden Beispielen wird davon ausgegangen, dass Sie mit dem mit dem Produkt gelieferten Stylesheet arbeiten.

## Arbeiten mit Überschriftenstilen

Die Überschriftenstile enthalten alle Basisstile für die Überschriften, die in Ihrem Inhalt verwendet werden. OOTB erhalten Sie 6 grundlegende Überschriftenstile und einen Überschriftenstil für das Thema/Kapitel und die Überschrift des Anhangs. In einem strukturierten Dokument stellt H1 den Titel des Themas oder Kapitels dar und H2 bis H6 wird für Unterthemen oder Abschnitte innerhalb eines Themas/Kapitels verwendet. Diese Hierarchie von Überschriften wird automatisch auf Ihren Inhalt angewendet, sobald die entsprechende Überschrift gefunden wird.

>[!NOTE]
>
>Sie können eigene benutzerdefinierte Überschriftenstile erstellen und diese in Ihren Inhalten mit der Ausgabeklasse verwenden. Weitere Informationen finden Sie in Schritt 4 unter *Seitenausrichtung und Anzeigenrotation verwenden* Beispiel.

### Erstellen benutzerdefinierter Überschriften auf Kapitelebene

In einem Buch (oder einer Bookmap) arbeiten Sie mit Kapiteln. Die grundlegenden Überschriftenstile werden so gestaltet, dass sie ohne Anpassungen auf Ihre Überschriften auf Kapitelebene angewendet werden. Wenn Sie jedoch spezielle Überschriften für Ihren Inhalt erstellen möchten, müssen Sie diese Überschriften erstellen. Beispielsweise wird die Standardeinstellung `h1.chapter` -Überschrift wird auf den Titel Ihres Kapitels angewendet. Wenn Ihr Kapiteltitel in einem anderen Stil angezeigt werden soll, müssen Sie die `h1.chapter` Stil. Auf ähnliche Weise können Sie benutzerdefinierte Stile für Unterüberschriften in Ihrem Kapitel erstellen. Wenn Sie beispielsweise einen benutzerdefinierten Stil für alle 2 erstellen möchten<sup>nd</sup> und 3<sup>rd</sup> Ebenenüberschriften in Ihrem Kapitel erstellen Sie dann einen neuen Stil als `h2.chatper` und `h3.chatper`.

Da die Funktion &quot;Native PDF-Veröffentlichung&quot;die grundlegenden Stildefinitionen für die gängigsten Stile enthält, wird der Standardstil auch dann auf den-Inhalt angewendet, wenn Sie versehentlich einen Stil löschen. Wenn beispielsweise in Ihrem Stylesheet keine Stildefinition für den h2-Stil vorhanden ist, wendet die Funktion Native PDF Publishing einen Basisstil auf H2-Inhalt an.

In diesem Beispiel erstellen wir einen Stil für Kapitel der zweiten Ebene:

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.
   >[!NOTE]
   >
   >Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, erweitern Sie die **Überschriftenstile**.
1. Rechtsklick auf **Überschriftenstile** Stil und Auswahl **Neuer Stil**.
1. Im *Stil hinzufügen* speichern Sie **Tag** name als `h2` und eingeben `chapter` im **Klasse** Namensfeld.
1. Klicken Sie auf **Fertig**.

Ein neuer Überschriftenstil mit dem Namen `h2.chapter` wird erstellt und unter der Liste &quot;Überschriftsstile&quot;hinzugefügt.

Nachdem Sie einen Stil erstellt haben, können Sie die erforderlichen Eigenschaften des Stils mit dem Stileditor anpassen.

### Erstellen von Überschriften für automatische Nummern

Einer der am häufigsten verwendeten Ausgabeformate sind automatisch nummerierte Überschriften. Diese Überschriften stellen die Kapitelnummer, Themen und Unterthemennummern dar. Die Überschriften mit automatischer Nummer unterscheiden sich von den Listenstilen, bei denen einer Liste von Elementen innerhalb eines Themas automatische Zahlen zugewiesen werden.

In diesem Beispiel passen wir die Überschriften von Ebene 1 zu Ebene 3 an, um die automatischen Zahlen in verschiedenen Formaten zu verwenden.

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.

   >[!NOTE]
   >
   >Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, erweitern Sie die **Überschriftenstile**.

1. Wählen Sie die **h1** Stil aus der Liste.
Die Eigenschaften für den h1-Stil werden zusammen mit der Vorschau im Bereich Eigenschaften angezeigt.

   >[!NOTE]
   >
   >Im Vorschaufenster erhalten Sie eine Echtzeitansicht aller Stilaktualisierungen, die Sie auf ein Element anwenden.

1. Wählen Sie die **Autonummer** -Eigenschaft.

   Die Stile, die Sie auf die Liste der automatischen Nummern anwenden können, werden unter der Eigenschaft &quot;Autonummer&quot;angezeigt.

1. Legen Sie die folgenden Eigenschaften fest:
   * **Stil**: Wählen Sie aus einem breiten Spektrum an gebietsschemaspezifischen oder generischen Nummerierungsstilen aus. Sie können Stile wie Arabisch-Indisch, Devanagari, Georgisch, Dezimal, Unteralpha und mehr auswählen. Wählen Sie für das aktuelle Beispiel `upper-alpha`.

   * **Format**: Das Standardformat ist auf `<x>`, wobei `x` durch den Nummerierungsstil ersetzt, den Sie in der Eigenschaft &quot;Style&quot;ausgewählt haben. Wenn Sie beispielsweise `decimal` (1) Stil, dann der Wert von `x` automatische Inkrementierungen für jede Instanz der `h1` -Stil verwendet werden und 2, 3 usw. umfassen. Sie können dem Feld auch benutzerdefinierten Text hinzufügen, um den Überschriftstil zu formatieren. Wenn Sie beispielsweise möchten, dass alle h1-Überschriften ein Präfix von `Chapter`, müssen Sie dieses Feld als `Chapter <x>`.

   * **Zeichen einfügen**: Wenn Sie Sonderzeichen im Format hinzufügen möchten, klicken Sie auf &quot;Zeichen einfügen&quot;(<img src="./assets/insert-chars.png" width="25">) icon. Wählen Sie das gewünschte Zeichen aus, das Sie im Stilformat hinzufügen möchten, und klicken Sie auf &quot;Einfügen&quot;. Es gibt verschiedene Arten von Sonderzeichen, die Sie aus der Dropdownliste Kategorie auswählen auswählen auswählen können. Wählen Sie für unser Beispiel in der Kategorie Interpunktion das Anführungszeichen für doppelte Winkel rechts aus.

      <img src="./assets/insert-special-chars.png" width="400">


   * **Nummerierung starten von**: Wenn die Nummerierung von einer bestimmten Zahl beginnen soll, geben Sie diesen Wert an. Behalten Sie für unser Beispiel den Standardwert 1 bei.

   * **Einzug**: Wenn Sie die Überschrift einrücken möchten, müssen Sie den Einzugswert festlegen. Legen Sie für unser Beispiel den Wert auf 0 Pixel fest.

      >[!NOTE]
      >
      >Sie können den Wert in Einheiten &quot;px&quot;(Pixel), &quot;pt&quot;(Punkte), &quot;rem&quot;, &quot;em&quot;, &quot;%&quot;(Prozent) oder &quot;in&quot;(Zoll) eingeben.

   * **Präfixbreite**: Dies ist der Bereich, der vom Format der automatischen Nummer belegt wird. Er wird automatisch auf eine Größe eingestellt, die das ausgewählte Stilformat einfach aufnehmen kann. Wenn Sie die Größe erhöhen möchten, können Sie den Standardwert ersetzen.

      Versuchen Sie beim manuellen Festlegen dieses Werts, die anderen Eigenschaften zu ändern, die sich auf die Breite auswirken. Ändern Sie beispielsweise die Schriftgröße, das Format mit dem Präfix (Kapitel) oder ein Suffix (:) und legen Sie den Maximalwert in der *Nummerierung starten von* -Eigenschaft und den verschiedenen Schrifteigenschaften, um die optimale Größe zu erhalten.

      Behalten Sie für unser Beispiel den Standardwert bei.

   * **Abstand**: Legen Sie den horizontalen und vertikalen Abstand fest. Behalten Sie für unser Beispiel die Standardwerte bei.

      Mit den oben genannten Anpassungen wird der Stil wie unten gezeigt angepasst:

      <img src="./assets/h1-style-custmization.png" width="500">

   * **Formatierung anwenden auf**: Mithilfe der Eigenschaften unter der Kategorie &quot;Autonummer&quot;können Sie den Nummerierungsstil definieren. Um weitere Anpassungen am Nummerierungsstil oder am Inhalt des Überschriftenformats vorzunehmen, können Sie in diesem Feld Nummerierung oder Absatz auswählen. Wenn Sie &quot;Nummerierung&quot;wählen, werden Änderungen an &quot;Schrift&quot;, &quot;Rand&quot;, &quot;Layout&quot;und anderen Kategorien nur auf den Nummerierungsstil in der Überschrift angewendet. Wenn Sie jedoch &quot;Absatz&quot;auswählen, werden die Änderungen auf den Überschrifteninhalt und nicht auf den Nummerierungsstil angewendet.

   Verwenden Sie die folgenden Einstellungen, um eine Ausgabe zu generieren, die im folgenden Screenshot gezeigt wird:

   |**Überschriftenstil**|**Eigenschaft**|**Wert**|**Zusätzliche Kommentare**| | - | - | - | - | |h1|Style|Decimal|Diese Eigenschaften befinden sich unter der Kategorie Autonummer . | ||Format|`Capter <x>:`|| ||Präfixbreite|160 px|| ||Schrift > Textausrichtung|Links|Stellen Sie sicher, dass &quot;Formatierung anwenden auf&quot;auf &quot;Nummerierung|&quot;eingestellt ist. |h2|Style|Decimal|Diese Eigenschaften befinden sich unter der Kategorie Autonummer . | ||Format|`Section <x>:`|| ||Präfixbreite|125 px|| ||Schrift > Textausrichtung|Links|Stellen Sie sicher, dass &quot;Formatierung anwenden auf&quot;auf &quot;Nummerierung|&quot;eingestellt ist. |h3|Style|Decimal|Diese Eigenschaften befinden sich unter der Kategorie Autonummer . | ||Einfügestufe|2| ||Format|`Section <2>.<x>:`|| ||Präfixbreite|125 px|| ||Schrift > Textausrichtung|Links|Stellen Sie sicher, dass &quot;Formatierung anwenden auf&quot;auf &quot;Nummerierung|&quot;eingestellt ist. ||

   <img src="./assets/auto-number-output.png" width="500">

## Arbeiten mit Absatzstilen

Es kann ein Absatzstil erstellt werden, um eine spezielle Formatierung auf einen ganzen Absatz anzuwenden. Mit der Pseudo-Klasse können Sie jedoch einen Stil nur auf einen bestimmten Teil des Textes anwenden. Im folgenden Beispiel erstellen wir einen Absatzstil, um den Stil der Dropcap-Komponente zu verwenden.

### Erstellen des Dropcap-Stils

In Magazinen und literarischen Dokumenten wird ein Tropfendeckel (oder ein fallendes Kapital) verwendet, wobei das erste Zeichen eines Absatzes oder Abschnitts mit einem speziellen Stil versehen ist. Mit der Funktion &quot;Native PDF-Veröffentlichung&quot;können Sie denselben Effekt erzielen.

Im folgenden Beispiel erstellen wir einen Stil für die Dropdownliste:

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.

   >[!NOTE]
   Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, erweitern Sie die **Absatzformate**.

1. Klicken Sie mit der rechten Maustaste auf die **Absatzformat** und wählen Sie **Neuer Stil**.

1. Im *Stil hinzufügen* speichern Sie **Tag** name als p und in **Pseudo** **Klasse** Feld, wählen Sie `::first-letter`.

1. Klicken Sie auf **Fertig**.

   Ein neuer Absatzstil mit dem Namen `::first-letter`  wird erstellt und unter dem **Absatzformate** Liste.

1. Auswählen `::first-letter` und legen Sie die folgenden Eigenschaften fest:

   * **Schriftart**: Legen Sie die gewünschte Schriftart für den ersten Buchstaben in Ihrem Absatz fest. Legen Sie für unser Beispiel die Schriftfamilie auf &quot;Kursiv&quot;, die Schriftgröße auf 500, die Schriftgröße auf 30 pt fest und wählen Sie eine Schriftfarbe.

   * **Layout**: Legen Sie die senkrechte Ausrichtung des Textes um den Stil der Ablagekappe fest. Für unser Beispiel setzen wir die vertikale Ausrichtung auf &quot;Unten&quot;.

Als `p` -Tag mit dem `<p>` -Element in DITA verwenden, müssen Sie diesen Stil nicht explizit mit dem Attribut outputclass hinzufügen. Wohin in Ihrem Inhalt ein `<p>` verwendet wird, wird automatisch der Stil der Dropcap-Komponente angewendet. Im folgenden Screenshot wurden die Elemente Kapiteltitel, Kurzbeschreibung und Definitionsliste nicht mit dem Stil der Dropcap-Komponente formatiert. Nur der Absatzstil ist mit dem Stil der Dropcap-Komponente formatiert:

<img src="./assets/char-style-drop-cap.png" width="500">

## Arbeiten mit Zeichenstilen

Mithilfe der Zeichenstile können Sie Stile zum Formatieren von Zeichen oder Wörtern in Ihrem Inhalt erstellen. Sie können beispielsweise einen Zeichenstil für Inline-Code oder Dateinamen erstellen oder einen Stil erstellen, der mehrere Formatierungsformate für ausgewählten Inhalt verwendet.

### Erstellen eines Inline-Zeichenstils

Die Formatierung von Inline-Zeichen oder Wörtern in einem Absatz ist ein sehr häufiger Stil. Der Prozess der Erstellung eines Inline-Stils umfasst zwei Aufgaben: Erstellen Sie zunächst einen neuen Stil im Stylesheet und wenden Sie anschließend den Stil in Ihren Inhalt mithilfe der `outputclass` -Attribut.

Im folgenden Beispiel wird ein Inline-Zeichenstil erstellt:

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.

   >[!NOTE]
   Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, erweitern Sie die **Zeichenstile**.

1. Klicken Sie mit der rechten Maustaste auf die **Zeichenformat** und wählen Sie **Neuer Stil**.

1. Behalten Sie im Dialogfeld Stil hinzufügen die **Tag** als span und geben Sie `BoldItalic` im **Klasse** Namensfeld.

   <img src="./assets/create-char-style.png" width="400">

1. Klicken Sie auf **Fertig**.

   Ein neuer Zeichenstil namens Code wird erstellt und unter der Liste &quot;Zeichenstile&quot;hinzugefügt.

1. Auswählen `span.BoldItalic` von **Zeichenformat** und legen Sie die folgenden Eigenschaften fest:

   * **Schriftart**: In diesem Abschnitt können Sie alle Schrifteigenschaften anpassen. Standardmäßig sind einige Schriftarten im Paket mit dem Produkt enthalten. Sie können die gewünschte Schriftart für den Zeichenstil auswählen. Legen Sie für unser Beispiel die Schriftfamilie auf *serif,* und wählen Sie *Fett* und *Kursiv* in der Eigenschaft &quot;Font Style&quot;. Sie können auch andere Schrifteigenschaften anpassen, z. B. Schriftstärke (fett, heller), Textdekoration (z. B. Unterstreichung, Überstreichung), Schriftgröße, Schriftfarbe, Textausrichtung und mehr.

      >[!NOTE]
      Sie können Ihrer Vorlage auch Schriftarten hinzufügen, die im Bereich Ressourcen Ihrer Vorlage gespeichert sind. Weitere Informationen zum Hinzufügen von Schriftarten und zum Arbeiten mit Ressourcen finden Sie unter **Link zum Abschnitt Ressourcen hinzufügen**.

   * **Layout**: Sie können die Layout-bezogenen Eigenschaften festlegen, z. B. Höhe und Breite, Rand, Abstand, Ausrichtung usw.

   * **Hintergrund**: Mit den Eigenschaften im Hintergrund können Sie die Hintergrundfarbe eines bestimmten Stils formatieren. Sie können die Hintergrundfarbe oder das Bild für einen beliebigen Stil definieren.

Nachdem Sie den Inline-Zeichenstil erstellt haben, müssen Sie ihn in Ihren Inhalt übernehmen. Um den Inline-Code-Stil anzuwenden, wechseln Sie zur Quellansicht und fügen Sie die `outputclass` -Attribut im gewünschten Inhalt:

`outputclass="BoldItalic"`

Das folgende Beispiel zeigt das Format &quot;Fett kursiv&quot;, das an verschiedenen Stellen im laufenden Text angewendet wird:

<img src="./assets/char-format-applied.png" width="500">

## Listenstil anpassen

Die Listenstile enthalten die standardmäßigen Stileinstellungen für die sortierten und unsortierten Listen. Sie können diese Listenstile einfach an Ihre Dokumentationsanforderungen anpassen.

Im folgenden Beispiel wird der Stil einer nummerierten oder sortierten Liste angepasst:

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.

   >[!NOTE]
   Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, erweitern Sie die **Listenstile**.

1. Wählen Sie die **ol** Stil aus der Liste.

   Die Eigenschaften für den alten Stil werden zusammen mit der Vorschau im Bereich Eigenschaften angezeigt.

   <img src="./assets/list-style-default.png" width="500">

1. Wählen Sie die **Erweiterte Formatierung** -Option.

   Eine Bestätigungsmeldung wird angezeigt.

1. Klicken **Ja** auf *Bestätigung* Nachricht zum Öffnen **Erweiterte Formatierung** Eigenschaften.

   Die folgenden Eigenschaften sind standardmäßig verfügbar:

   * **Ebene**: Standardmäßig gibt es 6 Ebenen mit nummerierten Listen. Die Ebene, die Sie in dieser Dropdown-Liste auswählen, steuert die Stiländerungen auf der ausgewählten Ebene und auf allen nachfolgenden Ebenen. Wenn Sie beispielsweise Ebene 4 auswählen, werden alle von Ihnen angewendeten Stiländerungen auf die Ebenen 4, 5 und 6 festgelegt.

   * **List Style Type**: Es gibt eine Reihe von Stilen für die Listennummerierung, aus denen Sie wählen können. Die Liste enthält gebietsschemaspezifische und allgemeine Nummerierungsstile, die zum Erstellen einer nummerierten Liste verwendet werden. Einige der Arten von Listenstilen sind Arabisch, Kambodschanisch, Devanagari, Äthiopisch, Hangul, Hebräisch, Japanisch, Koreanisch, Einfaches Chinesisch, Urdu und mehr.

   Außerdem können Sie mit den folgenden erweiterten Formatierungseigenschaften arbeiten:

   * **Zahlenformat**: Das Standardformat ist auf `<x>`, wobei `x` durch den Nummerierungsstil ersetzt, den Sie in der Eigenschaft &quot;List Style Type&quot;ausgewählt haben. Wenn Sie beispielsweise `decimal` (1) Stil, dann der Wert von `x` inkrementiert automatisch für jede Instanz des Listenelements und wechselt zu 2, 3 usw. Sie können dem Feld auch benutzerdefinierten Text hinzufügen, um den Listenstil zu formatieren. Wenn Sie beispielsweise möchten, dass alle Listenstile der ersten Ebene ein Suffix haben sollen:`)`&quot;, müssen Sie dieses Feld für den Listenstil der ersten Ebene auf &quot;`<x>)`&quot;.

   * **Zeichen einfügen**: Wenn Sie Sonderzeichen im Zahlenformat hinzufügen möchten, klicken Sie auf &quot;Zeichen einfügen&quot;(<img src="./assets/insert-chars.png" width="25">). Wählen Sie das gewünschte Zeichen aus, das Sie im Stilformat hinzufügen möchten, und klicken Sie auf &quot;Einfügen&quot;. Es gibt verschiedene Arten von Sonderzeichen, die Sie aus der Dropdownliste Kategorie auswählen auswählen auswählen können.

   * **Einfügeebene**: Sie können die Zahl aus einer der vorangehenden Ebenen in Ihr Zahlenformat aufnehmen. Wenn Sie beispielsweise das Zahlenformat von 5. Ebene in das Format der 6. Ebene aufnehmen möchten, wählen Sie 5 in der Dropdown-Liste &quot;Einfügeebene&quot;. Beachten Sie, dass in der Dropdown-Liste &quot;Einfügeebene&quot;die Zahlen nur der vorhergehenden Ebenen und nicht der folgenden Ebene angezeigt werden. Wenn Sie sich beispielsweise auf Ebene 3 befinden, zeigt die Liste &quot;Einfügeebene&quot;nur die Ebenen 1 und 2 an.

      <img src="./assets/list-insert-level.png" width="400">

      Sie können auch das Zahlenformat ändern, um die Listenwerte nach Bedarf anzuzeigen. Wenn Sie beispielsweise einen verschachtelten Nummerierungsstil für Stufe 3 verwenden, können Sie ihn als`<2>.<x>))`&quot;. Daraufhin werden die Liste Nr. 2, ein Zeitraum, gefolgt von der Listennummer 3 und dann zwei Klammern angezeigt `2.3))`.

   * **Einzug**: Wenn Sie die Liste mit Einzug versehen möchten, müssen Sie den Einzugswert festlegen. Alle Änderungen im Einzug können im Vorschaufenster überprüft und angepasst werden.

      >[!NOTE]
      Sie können den Wert in Einheiten &quot;px&quot;(Pixel), &quot;pt&quot;(Punkte), &quot;rem&quot;, &quot;em&quot;, &quot;%&quot;(Prozent) oder &quot;in&quot;(Zoll) eingeben.

   * **Präfixbreite**: Dies ist der Bereich, der vom Zahlenformat belegt wird. Er wird automatisch auf eine Größe eingestellt, die das ausgewählte Format einfach aufnehmen kann. Wenn Sie die Größe erhöhen möchten, können Sie den Standardwert ersetzen.

      Versuchen Sie beim manuellen Festlegen dieses Werts, die anderen Eigenschaften zu ändern, die sich auf die Breite auswirken. Ändern Sie beispielsweise die Schriftgröße, das Format mit dem Präfix oder dem Suffix und die verschiedenen Schrifteigenschaften, um die optimale Größe zu erhalten.

   * **Abstand**: Geben Sie den horizontalen Abstand zwischen dem Listennummernformat und dem Inhalt an. Der vertikale Abstand steuert die Lücke zwischen den beiden Listenelementen.

      Der folgende Screenshot zeigt die angepasste geordnete Liste für jede Ebene:

      <img src="./assets/list-number-format-final.png" width="500">


## Arbeiten mit Tabellenstil

Mit den Stylesheets können Sie *n* Anzahl der Tabellenstile. Mithilfe der Tabellenstile können Sie entwerfen, wie die gesamte Tabelle, eine bestimmte Zeile oder Spalte dargestellt wird. Mit Steuerung auf Zellenebene können Sie sehr anschauliche Tabellenstile erstellen.

Im folgenden Beispiel sehen wir, wie Sie einen Tabellenstil und die verschiedenen Tabellenstil-Optionen erstellen, die Sie anpassen können:

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.

   >[!NOTE]
   Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, klicken Sie mit der rechten Maustaste auf die **Tabellenformat** und wählen Sie **Neuer Stil**.

1. Im *Stil hinzufügen* speichern Sie **Tag** name als `table` und eingeben `double-border` im **Klasse** Namensfeld.

1. Klicken Sie auf **Fertig**.

   Ein neuer Tabellenstil mit dem Namen `table.double-border` wird erstellt und unter der Liste &quot;Tabellenstile&quot;hinzugefügt.

1. Auswählen `table.double-border` von **Tabellenstile** und legen Sie die folgenden Eigenschaften fest:

   * **Formatierung anwenden auf**: Sie können die Stilformatierung auf die gesamte Tabelle, ungerade/gerade Zeilen oder Spalten oder erste/letzte Zeile oder Spalte anwenden.

      >[!NOTE]
      Die folgenden Einstellungen sind im **Allgemein** Abschnitt, wenn **Formatierung anwenden auf** auf **Ganzzahl**.

   * **Textumbruch**: Wählen Sie aus, wie Text um die Tabelle herum eingefügt werden soll. Dies ist nützlich, wenn sich die Tabelle in einem anderen Element auf Blockebene befindet und die Tabelle zusammen mit anderen Inhalten im Block-Element gerendert werden muss. Die Wrapping-Optionen sind *left* oder *right* ausgerichtet oder *Keine*.

   * **Rahmenreduzierung**: Wählen Sie das Erscheinungsbild des Tabellenrahmens aus. Wenn Sie &quot;Reduzieren&quot;auswählen, wird nur eine einzige Rahmenlinie zwischen den Tabellenzellen gezogen. Für einen separaten Stil ist der Rahmen jedoch um jede Zelle mit zusätzlichem Abstand sichtbar.

      <img src="./assets/table-style-collapse-separate.png" width="500">

   * **Rahmenabstand**: Diese Einstellung ist nur verfügbar, wenn für &quot;Grenzerkollaps&quot;die Option &quot;Separat&quot;ausgewählt ist. Mit dieser Einstellung können Sie den vertikalen und horizontalen Abstand zwischen Zellenrahmen festlegen.

      <img src="./assets/table-border-spacing.png" width="500">

      >[!NOTE]
      Die folgenden Einstellungen sind im **Zelle** Abschnitt, wenn **Formatierung anwenden auf** auf **Ganzzahl**.

   * **Auffüllung**: Geben Sie den Abstand zwischen Tabellenzellen an. Sie können für die oberen, unteren, linken und rechten Seiten unterschiedliche Füllzeichenwerte festlegen.

   * **Vertikale Ausrichtung**: Geben Sie die vertikale Ausrichtung für den Zelleninhalt an. Verfügbare Optionen sind: Oben, Mitte und Unten.

   * **Rahmenseite, Stil, Farbe, Breite, Radius:** Geben Sie die grenzbezogenen Eigenschaften an. Sie können festlegen, dass nur Rahmen auf bestimmten Seiten wie links oder rechts angezeigt werden. Im Rahmenstil werden die verfügbaren Randstile wie &quot;Durchgehend&quot;, &quot;Gestrichelt&quot;, &quot;Doppelt&quot;und mehr aufgeführt. Geben Sie die Rahmenfarbe über die Farbpalette an. Sie können die Rahmenbreite in Px, pt, rem, em, % und in Einheiten angeben. Der Radius definiert die Kurve, um kreisförmige Ecken zu bilden.

   Die anderen Eigenschaften unter &quot;Schriftart&quot;, &quot;Rand&quot;, &quot;Layout&quot;, &quot;Paginierung&quot;und &quot;Hintergrund&quot;werden unter anderen Beispielen in diesem Thema erläutert. Abhängig von Ihrer Auswahl im **Formatierung anwenden auf** -Eigenschaft können Sie diese Werte auf die gesamte Tabelle oder auf ausgewählte Zeilen oder Spalten anwenden.

   Nachfolgend finden Sie eine Vorschau einer Beispieltabelle mit verschiedenen Zeilen, die anders formatiert sind:

   <img src="./assets/table-final-design.png" width="500">

## Arbeiten mit anderen Stilen

Wenn Sie mit strukturiertem (DITA-)Inhalt arbeiten, werden Sie feststellen, dass fast alle DITA-Elemente im Standard-Stylesheet über ein Stilmapping verfügen. Beispiel: eine `<shortdesc>` Der Stil des Elements wird unter definiert. **Sonstige Stile** > **.shortdesc** Stildefinition. Sie können diese Stile einfach anpassen und sie werden automatisch in der PDF-Ausgabe angewendet, die aus Ihrem strukturierten Inhalt generiert wird. Das bedeutet, dass Sie im Gegensatz zu anderen benutzerdefinierten Stilen keine `outputclass` -Attribut auf den Inhalt für diese Stile.

Wenn Sie eine Stildefinition für ein Element erstellen möchten, das nicht standardmäßig verfügbar ist, oder wenn Sie ein benutzerdefiniertes Element haben, können Sie es einfach im Stylesheet erstellen. Der einzige Punkt, den Sie beachten müssen, ist die Erstellung des Stils mit demselben Namen wie der des strukturierten Elements.

Im folgenden Beispiel wird der Titel eines neuen Fensters (`wintitle`) style:

1. Öffnen Sie das erforderliche Stylesheet zur Bearbeitung.

   >[!NOTE]
   Siehe *Vordefinierten oder neuen Stil anpassen* zum Öffnen eines Stylesheets zur Anpassung oder Bearbeitung.

1. Im **Stile** Liste, erweitern **Weitere Stile**.

1. Klicken Sie mit der rechten Maustaste auf die **Sonstige Stile** und wählen Sie **Neuer Stil**.

1. Im *Stil hinzufügen* speichern Sie **Tag** name als *blank* und eingeben `wintitle` im **Klasse** Namensfeld.

   As `wintitle` ist ein erkannter DITA-Elementname, dessen Stildefinition automatisch dem `<wintitle>` -Element in Ihrer Quelle.

1. Klicken Sie auf **Fertig**.

   Ein neuer Stil mit dem Namen `.wintitle` wird erstellt und unter dem **Weitere Stile** Liste.

1. Wählen Sie &quot;.wintitle&quot;aus dem **Weitere Stile** und legen Sie die Eigenschaften nach Bedarf fest.

Der folgende Screenshot zeigt den wintitle-Stil, der auf den Text &quot;Primäre Kontrolle&quot;angewendet wird.

<img src="./assets/other-style-wintitle.png" width="500">