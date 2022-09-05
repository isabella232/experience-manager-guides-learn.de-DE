---
title: Native PDF-Veröffentlichungsfunktion | Komponenten einer PDF-Vorlage
description: Lernen Sie die verschiedenen Komponenten einer PDF-Vorlage kennen und erfahren Sie, wie Sie sie anpassen und konfigurieren.
exl-id: 0ddb3b81-42ca-4a66-be7d-051a5175d53a
source-git-commit: a1367a6915e760e533bb984705f4be37596b5477
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# Komponenten einer PDF-Vorlage {#components-pdf-template}

Eine PDF-Vorlage besteht aus vier Komponenten: Seitenlayouts, Stylesheets, Ressourcen und Einstellungen. Sie können eine Vorlage erstellen, indem Sie diese einzelnen Komponenten anpassen und die Vorlage beim Generieren einer PDF-Ausgabe mit einer Ausgabevorgabe verknüpfen. In den folgenden Abschnitten werden diese Komponenten und ihr Anpassungsprozess ausführlich beschrieben.


## Seitenlayouts erstellen und anpassen {#create-customize-page-layout}

Mit den Einstellungen in der Komponente Seitenlayouts können Sie die Struktur einer Seite entwerfen, indem Sie die Kopf- und Fußzeile sowie den Inhaltsbereich auf einer Seite definieren. Mit dem WYSIWYG-Seitenlayouteditor können Sie ein Seitenlayout für verschiedene Bereiche in einer PDF erstellen, z. B. für die Titelseiten vor und zurück, Kapitel, Inhaltsverzeichnis (Inhaltsverzeichnis), Index, leere Seite, Bildliste (LOF), Tabellenliste (LOT), Glossar oder ein Layout für eine benutzerdefinierte Seite. In den PDF-Vorlageneinstellungen können Sie ein Seitenlayout mit verschiedenen Abschnitten innerhalb einer PDF zuweisen, die dann zum Generieren der PDF-Ausgabe verwendet werden.

### Neues Seitenlayout erstellen {#create-page-layout}

>[!NOTE]
>
>Es gibt Beispielseitenlayouts, die standardmäßig bereitgestellt werden. Sie können diese anpassen oder neue Seitenlayouts erstellen.

1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Erweitern Sie die linke Seitenleiste und klicken Sie auf **Vorlagen**.
1. Öffnen Sie die Vorlage, mit der Sie arbeiten möchten.
   >[!NOTE]
   >
   >Sie können eine Vorlage öffnen, indem Sie auf ihren Namen doppelklicken oder auf das Symbol > neben ihrem Namen klicken.
1. Führen Sie einen der folgenden Schritte aus, um ein neues Seitenlayout zu erstellen:
   * Bewegen **Seitenlayouts** und klicken Sie auf (*Optionen* Symbol) **...** und wählen Sie **Neues Seitenlayout**.
   * Im **Vorlagen** auf **+** Symbol neben **Vorlagen** und wählen Sie **Seitenlayout** aus dem Kontextmenü aus.

      Dadurch wird das Dialogfeld Layout hinzufügen geöffnet.

      <img src="assets/add-layout-2.png" alt="Dialogfeld "Layout hinzufügen"" width="250">
1. Geben Sie einen Namen für das neue Seitenlayout an.
   >[!NOTE]
   >
   >Vermeiden Sie die Verwendung von Sonderzeichen bei der Benennung eines Seitenlayouts. Ein Leerzeichen im Namen wird durch einen Unterstrich &quot;_&quot;ersetzt.
1. Klicken Sie auf **Fertig**.

   Das neue Layout wird unter Seitenlayouts erstellt und hinzugefügt.

### Duplizieren eines Seitenlayouts {#duplicate-page-layout}

1. Im **Vorlagen** Bereich der Vorlage, die Sie duplizieren möchten, doppelklicken Sie auf **Seitenlayouts** oder klicken Sie auf **>** Symbol vor **Seitenlayouts**.

   Dadurch wird die Liste der Seitenlayouts in der Vorlage angezeigt.

1. Bewegen Sie den Mauszeiger über das Seitenlayout, das Sie duplizieren möchten, und klicken Sie auf (*Optionen* Symbol) **...** und wählen Sie **Duplizieren** aus dem Kontextmenü aus.

1. Im _Layout duplizieren_ ein, geben Sie einen Namen für das Seitenlayout ein.

1. Klicken Sie auf **Fertig**.
Eine Kopie des ausgewählten Seitenlayouts wird erstellt und unter Seitenlayouts hinzugefügt.

### Seitenlayout anpassen {#customize-page-layout}

1. Im **Vorlagen** in der Vorlage, die Sie bearbeiten möchten, doppelklicken Sie auf **Seitenlayouts** oder klicken Sie auf **>** Symbol vor **Seitenlayouts**.

   Dadurch wird die Liste der Seitenlayouts in der Vorlage angezeigt.
1. Führen Sie einen der folgenden Schritte aus, um das Seitenlayout anzupassen:
   * Doppelklicken Sie auf ein beliebiges Seitenlayout.
   * Bewegen Sie den Mauszeiger über ein Seitenlayout und klicken Sie auf (*Optionen* Symbol) **...** und wählen Sie **Bearbeiten** aus dem Kontextmenü aus.

   Dadurch wird der Seitenlayout-Editor zur Anpassung geöffnet.
1. Nachdem Sie die gewünschten Änderungen vorgenommen haben, klicken Sie auf *Alle speichern* (oder `Crl+S`).

   Weitere Informationen zum Definieren einzelner Layoutelemente wie Kopf- und Fußzeile, Seitenzahl, Titel und mehr finden Sie unter [Erstellen eines Seitenlayouts](design-page-layout.md).

## Verwenden von Stylesheets zum Anpassen von PDF {#stylesheet-customization}

Mit den Einstellungen in der Komponente &quot;Stylesheets&quot;können Sie die Seitenlayoutkomponenten und DITA-Inhalte mit dem WYSIWYG-Editor gestalten oder direkt mit der CSS-Datei arbeiten. Sie können eigene Stile erstellen oder die Standardstileigenschaften anpassen. Der WYSIWYG-Editor bietet Ihnen Zugriff auf die meisten Eigenschaften, die Sie zum Gestalten Ihres Seitenlayouts oder DITA-Inhalts benötigen. Für erweiterte Anpassungen können Sie direkt in der Quellansicht arbeiten.

### Neues Stylesheet erstellen {#create-stylesheet}

Während CSS-Dateien für Inhalt und Layout bereitgestellt werden, können Sie ein neues Stylesheet erstellen, um mehrere Anpassungen auf einen bestimmten Stiltyp anzuwenden, der dann auf eine Zielkomponente angewendet werden kann. Standardmäßig werden Beispiel-CSS-Dateien innerhalb des Produkts gebündelt. Diese CSS-Dateien sollen Ihnen dabei helfen, Ihre Styling-Informationen über Inhalte und Layouts hinweg zu organisieren. Sie können diese Stile in einer oder mehreren CSS-Dateien zusammenführen.

Jedes Mal, wenn Sie ein neues Seitenlayout erstellen, wird standardmäßig die `layout.css` -Datei im neuen Seitenlayout enthalten ist. Wenn das Seitenlayout Stile aus einer anderen CSS-Datei enthalten soll, können Sie die gewünschte CSS-Datei einfach per Drag-and-Drop in den Inhaltsbearbeitungsbereich des neuen Seitenlayouts ziehen. Um zu überprüfen, ob die CSS-Datei in das Seitenlayout eingebettet wurde, wechseln Sie zur Quellansicht und Sie finden einen Link zur CSS-Datei im `<head>` -Element.


Gehen Sie wie folgt vor, um ein Stylesheet zu erstellen:
1. Im **Vorlagen** einen der folgenden Schritte ausführen:
   * Bewegen Sie den Mauszeiger über die **Stylesheets** und klicken Sie auf (*Optionen* Symbol) **...** und wählen Sie **Neues Stylesheet**.
   * Klicken Sie auf **+** Symbol neben **Vorlagen** und wählen Sie **Stylesheet** aus dem Kontextmenü aus.

   Dadurch wird das Dialogfeld Stylesheet hinzufügen geöffnet.

   <img src="assets/add-stylesheet.png" alt="Stylesheet hinzufügen" width="250">
1. Geben Sie einen Namen für das neue Stylesheet an.
1. Klicken Sie auf **Fertig**.

   Ein neues Stylesheet wird unter dem Abschnitt Stylesheets erstellt und hinzugefügt.

### Neuen Stil erstellen {#create-style}

Standardmäßig enthalten die CSS-Dateien Stile für Überschrift, Absatz, Zeichen, Hyperlink, Bild, Tabelle, div, Seite und andere Stile. Sie können das Standard-Stilformat überschreiben oder einen neuen Stil erstellen.

In der Regel erstellen Sie einen neuen Stil, wenn Sie einen benutzerdefinierten Stil für ein DITA-Element zuweisen möchten. Damit diese benutzerdefinierten Stile funktionieren, müssen Sie sicherstellen, dass Sie den Klassennamen des Stils mit dem Attribut outputclass des DITA-Elements verknüpfen.


Gehen Sie wie folgt vor, um einen neuen Stil zu erstellen:
1. Klicken Sie mit der rechten Maustaste auf einen beliebigen Stil und wählen Sie im Kontextmenü die Option Neuer Stil .

   Dadurch wird das Dialogfeld Stil hinzufügen geöffnet.

   <img src="assets/add-style.png" alt="Neuen Stil hinzufügen" width="300"/>
1. Im **Tag** -Feld ein Tag auswählen, für das Sie einen neuen Stil erstellen möchten.
1. Geben Sie eine **Klasse** name.

   Dieser Klassenname muss mit dem Attribut outputclass des Tags in Ihrem Quellinhalt verknüpft sein.
1. Wählen Sie eine **Pseudo-Klasse** für eine verbesserte Formatierung des Elements.
1. Klicken Sie auf **Fertig**.

   Ein neuer Stil wird erstellt und im Basisstil hinzugefügt.

### Vordefinierten oder neuen Stil anpassen {#customize-style}

Nachdem Sie eine neue CSS-Datei mit Standardstilen erstellt haben oder die Stile in einer vorhandenen CSS-Datei anpassen möchten, können Sie dazu den Stileditor verwenden.

Gehen Sie wie folgt vor, um einen Stil anzupassen:
1. Doppelklicken Sie auf **Stylesheets** oder klicken Sie auf **>** Symbol vor **Stylesheets**.

   Dadurch werden die standardmäßigen (Inhalt und Layout) und benutzerdefinierten CSS-Dateien angezeigt.
1. Öffnen Sie ein Stylesheet zur Bearbeitung.

   Führen Sie einen der folgenden Schritte aus, um das Stylesheet zur Bearbeitung zu öffnen:
   * Doppelklicken Sie auf den Stylesheet-Namen.
   * Bewegen Sie den Mauszeiger über den Namen des Stylesheets und klicken Sie auf das Symbol Optionen ... und wählen Sie Bearbeiten.

   Dadurch wird das Stylesheet zur Bearbeitung geöffnet und die Liste der Stile im Bedienfeld &quot;Stile&quot;angezeigt.

   <img src="assets/customize-style.png" alt="Stil anpassen" width="450">

1. Um einen Stil anzupassen, doppelklicken Sie auf einen Stil oder klicken Sie auf das Symbol > vor einem Stil, um ihn mithilfe des Stileditors anzuzeigen und anzupassen.

Weitere Informationen zum Arbeiten mit den gängigsten Stilen finden Sie unter [Arbeiten mit allgemeinen Inhaltsstilen](stylesheet.md)

## Arbeiten mit Ressourcen {#work-with-resources}

Dies ist ein Container für alle Assets, die zum Entwerfen einer Vorlage verwendet werden. Sie können sich dies als Ordner vorstellen, der Assets wie Hintergrundbilder, benutzerdefinierte Schriftarten, Logos und mehr enthält. Jedes Mal, wenn Sie ein Asset in Ihrer Vorlage hinzufügen, wird es in den Asset-Ordner hochgeladen oder dort eingecheckt. Anschließend können Sie diese Assets verwenden, um Ihre PDF-Vorlagen anzupassen oder zu entwerfen.

Gehen Sie wie folgt vor, um eine Asset-Datei zum Ordner Ressourcen hinzuzufügen:
1. Bewegen Sie den Mauszeiger über die Registerkarte Ressourcen-Ordner , klicken Sie auf das Symbol Optionen ... und wählen Sie Importieren.

   Dadurch wird das Dialogfeld &quot;Assets hochladen&quot;geöffnet.

   <img src="assets/resources-import-assets.png" alt="Hochladen von Assets" width="300">

   Der Pfad, in den die Asset-Datei hochgeladen wird, wird im **Asset-Ordner auswählen** -Feld.
   >[!NOTE]
   >
   >Sie können den Pfad zum Hochladen von Assets nicht ändern. Standardmäßig werden alle Assets unter dem `/content/dam/dita-templates/pdf/<PDF-template-name>` Ordner.

1. Klicken **Dateien auswählen** zum Durchsuchen der Asset-Datei von Ihrem lokalen Computer aus

1. Klicken Sie auf **Hochladen**.
Die ausgewählte Datei wird importiert und im Ordner Ressourcen aufgeführt.

## Erweiterte PDF-Einstellungen {#advanced-pdf-settings}

Verwenden Sie den Bereich Einstellungen , um das Layout der erweiterten PDF zu konfigurieren, das PDF von ungeraden oder geraden Seiten zu starten, die Formate für die Querverweise zu konfigurieren und Druckmarkierungen in der endgültigen PDF zu aktivieren, die mithilfe der Vorlage generiert wird.

Klicken Sie zum Konfigurieren auf **Einstellungen** im **Vorlagen** -Bereich, um die folgenden Optionen anzuzeigen:

**Allgemein**

Legen Sie die grundlegenden Konfigurationseinstellungen für das Starten eines Kapitels von einer ungeraden oder geraden Seite, die TOC-Struktur fest und definieren Sie das Füllzeichenzeilenformat für die TOC-Einträge. Sie können die folgende Einstellung definieren:

* **Kapitel immer starten von**: Damit können Sie festlegen, wie die einzelnen Kapitel im endgültigen PDF veröffentlicht werden. Sie können aus einer **Neue Seite**, **Ungerade Seite** oder **Gerade Seite** Optionen. Wenn Sie ein neues Kapitel von einer ungeraden Seite aus beginnen möchten, wird nach einem Kapitel, das auf einer ungeraden Seite endet, eine leere Seite eingefügt. Wenn Ihr Kapitel beispielsweise auf Seite 15 endet, fügt der Veröffentlichungsprozess eine leere 16 ein<sup>th</sup> -Seite, damit das neue Kapitel mit der 17 beginnen kann.<sup>th</sup> Seite.

* **Jedes Thema von einer neuen Seite aus starten**: Wenn jedes Thema in Ihrem Kapitel von einer neuen Seite aus beginnen soll, wählen Sie **Jedes Thema von einer neuen Seite aus starten** -Option. Wenn Sie Ihre Themen ohne Seitenlücken fortsetzen möchten, deaktivieren Sie diese Option.

* **Inhaltsstruktur**: Hiermit können Sie die Hierarchie des Inhaltsverzeichnisses anpassen. Es werden die folgenden zusätzlichen Einstellungen verwendet:

   * **Überschriften bis zur Ebene verwenden**: Damit können Sie die Anzahl der Überschriftenebenen anpassen, die in der TOC-Struktur Ihrer PDF angezeigt werden.
   * **Zeigt keine Seitenzahl für die erste Ebene im Inhaltsverzeichnis an**: Wählen Sie diese Option, um die entsprechenden Seitenzahlen für alle Kapitel auszublenden, die verschachtelte oder untergeordnete Themen enthalten. Betrachten Sie das folgende Beispiel, in dem eine Ausgabe erstellt wird, ohne diese Option auszuwählen.

   <img src="assets/page-number-in-toc.png" alt="Hochladen von Assets" width="250">

   Im obigen Beispiel sind Erweiterte PDF-Einstellungen, Anhang und rechtliche Themen die ersten Themenüberschriften oder Kapiteltitel. Allen diesen Überschriften wird eine Seitenzahl zugewiesen.

   Wenn Sie jetzt diese Option auswählen und die Ausgabe generieren, erhalten Sie das folgende Inhaltsverzeichnis:
   <img src="assets/page-number-missing-in-toc.png" alt="Hochladen von Assets" width="250">

   Hier können Sie bemerken, dass die erweiterten PDF-Einstellungen des ersten Kapitels keine Seitenzahl erhalten, da sie verschachtelte oder untergeordnete Themen haben. Eine Seitenzahl hingegen, wenn sie Anhang und Legal zugewiesen wird, da es sich um eigenständige Themen ohne untergeordnetes Thema handelt.

* **Füllzeichenformat**: Verwenden Sie die Dropdown-Liste, um die Füllzeichenlinien &quot;Gepunktet&quot;, &quot;Durchgehend&quot;oder &quot;Leerzeichen&quot;auszuwählen, um die Überschriftenebenen mit den entsprechenden Seitenzahlen zu verbinden.
Informationen zum Anwenden der TOC-Struktur und der Styling-Überschriftenebenen finden Sie unter [Kapitel-Inhaltsverzeichnis hinzufügen](design-page-layout.md#add-chapter-toc).

   >[!NOTE]
   >
   >Wenn Sie CSS-Entwickler sind, können Sie das Füllzeichenformat auch direkt in der CSS-Datei definieren.
* **Verwenden der Tabellenfortsetzungsmarkierung**: Wählen Sie diese Option aus, um Markierungen für lange Tabellen zu definieren, die über mehrere Seiten verteilt sind. <!--For more information on using table continuation markers, see Use table continuation markers.-->

**Seitenlayouts**

Mit den Einstellungen für Seitenlayouts können Sie vollständig festlegen, welches Seitenlayout für einen bestimmten Abschnitt Ihres Dokuments verwendet werden soll. Um beispielsweise ein Layout für das Inhaltsverzeichnis auszuwählen, klicken Sie auf das Dropdown-Menü unter dem Feld Inhaltsverzeichnis und wählen Sie das Layout aus, das Sie zum Generieren des Inhaltsverzeichnisses entwickelt haben.

Wenn Sie für einen bestimmten Bereich in Ihrem Dokument kein Layout erstellt haben, können Sie einfach ein Layout wählen, das als Standardlayout für diese Abschnitte oder Themen dient. Das standardmäßige Seitenlayout wird dann auf alle Abschnitte angewendet, die kein dediziertes Seitenlayout aufweisen.

Wenn Sie ein Deckblatt und eine Rückseite wünschen, muss in den Einstellungen ein Seitenlayout erstellt und angewendet werden. Andernfalls enthält Ihre PDF keine Deckblatt- und Hinterseiten.


Weitere Informationen zu Seitenlayouts finden Sie unter [Erstellen eines Seitenlayouts](design-page-layout.md).

**Druck**

Konfigurieren Sie die Druckproduktionseinstellungen, um Druckermarkierungen zuzuweisen, Farbmodelle auszuwählen und Eigenschaften für den Druck Ihrer PDF-Ausgabe anzugeben.

* **Druckermarken**: Wenn Sie ein Dokument für die Druckproduktion vorbereiten, werden die Seitengrenzen um Druckmarkierungen erweitert, um eine korrekte Ausrichtung, Beschneidung und Farbauswahl beim Drucken zu ermöglichen. Durch Auswahl eines Druckerzeichens wird die Seitenbegrenzung erweitert, um die Markierung aufzunehmen, die beim Drucken abgeschnitten wird. Sie können die folgenden Druckermarkierungen in Ihrer PDF-Ausgabe anzeigen lassen:
   * **Schnittmarken**: Wählen Sie die Option aus, um an jeder Ecke des Schnittbereichs eine Markierung zu platzieren und anzugeben, wo das Papier nach dem Drucken beschnitten werden soll.
   * **Anschnittmarken**: Wählen Sie diese Option aus, um an jeder Ecke des Anschnittrahmens eine Markierung zu platzieren, um den Schnittbereich für das erweiterte Bild anzugeben.
   * **Registrierungszeichen**: Wählen Sie diese Option, um eine Markierung außerhalb des Zuschnittbereichs zu platzieren, damit die verschiedenen Trennlinien in einem Farbdokument ausgerichtet werden.
   * **Farbbalken**: Wählen Sie diese Option, um einen Farbstreifen außerhalb des Schnittbereichs hinzuzufügen, um die Farbkonsistenz zu gewährleisten und die Farbdichte beim Drucken anzupassen.

   Legen Sie Dimensionen für die ausgewählten Druckermarkierungen mithilfe der **Linienbreite**, **Linienfarbe** und **Breite des Anschnittrahmens** Optionen.

* **Größe des Medienfelds**: Dies ist die Gesamtseitengröße einschließlich des erweiterten Bereichs, der von Druckermarkierungen belegt wird. Verwenden Sie die Dropdown-Option, um die Seitengröße für Ihre PDF-Ausgabe auszuwählen oder eine eigene benutzerdefinierte Größe zu erstellen.

* **Farbraum**: Sie haben die Möglichkeit, aus RGB- oder CMYK-Farbräumen auszuwählen, um Ihr PDF-Dokument zu drucken. Wählen Sie RGB aus, um die generierte PDF digital und CMYK für den physischen Druck anzuzeigen. Im Dokument definierte Farben werden in den ausgewählten Farbraum konvertiert.
   >[!NOTE]
   >
   >Für die Erstellung von PDF/A ist bei Verwendung des CMYK-Farbraums ein ICC-Farbprofil erforderlich.

   <!--For more information on applying these print settings, see *Printing preferences*.-->

**Querverweise**

Auf der Registerkarte &quot;Querverweis&quot;können Sie definieren, wie Querverweise auf der PDF veröffentlicht werden. Sie können die Querverweise für Thementitel, Tabellen, Zahlen und mehr formatieren. <!--For more information, see *Format cross-references*.-->
