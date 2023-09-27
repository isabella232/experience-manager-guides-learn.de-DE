---
title: Native PDF-Veröffentlichungsfunktion | Komponenten einer PDF-Vorlage
description: Erfahren Sie mehr über die verschiedenen Komponenten einer PDF-Vorlage und wie Sie diese anpassen und konfigurieren.
exl-id: 0ddb3b81-42ca-4a66-be7d-051a5175d53a
source-git-commit: 5abcc887a24d838caabdf9a34a84ebc851ed4cbf
workflow-type: tm+mt
source-wordcount: '4376'
ht-degree: 0%

---

# Komponenten einer PDF-Vorlage {#components-pdf-template}

Eine PDF-Vorlage besteht aus vier Komponenten: Seitenlayouts, Stylesheets, Ressourcen und Einstellungen. Sie können eine Vorlage erstellen, indem Sie diese einzelnen Komponenten anpassen und die Vorlage beim Generieren einer PDF-Ausgabe mit einer Ausgabevorgabe verknüpfen. In den folgenden Abschnitten werden diese Komponenten und ihr Anpassungsprozess ausführlich beschrieben.


## Seitenlayouts erstellen und anpassen {#create-customize-page-layout}

Mit den Einstellungen in der Komponente Seitenlayouts können Sie die Struktur einer Seite entwerfen, indem Sie die Kopf- und Fußzeile sowie den Inhaltsbereich auf einer Seite definieren. Mit dem WYSIWYG-Seiten-Layout-Editor können Sie ein Seitenlayout für verschiedene Bereiche in einer PDF erstellen, z. B. die Seiten für die Vorder- und Rückseite, Kapitel, Inhaltsverzeichnis, Index, leere Seite, Seiten für die Vorderseite, Seiten für die Rückseite, Bildliste (LOF), Tabellenliste (LOT) oder ein Glossar. Sie können auch ein Layout für eine benutzerdefinierte Seite erstellen. In den PDF-Vorlageneinstellungen können Sie ein Seitenlayout mit verschiedenen Abschnitten innerhalb einer PDF zuweisen, die dann zum Generieren der PDF-Ausgabe verwendet werden.

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

   * Bewegen **Seitenlayouts** und klicken Sie auf (*Optionen* Symbol) **...** und wählen **Neues Seitenlayout**.


   * Im **Vorlagen** auf das **+** Symbol neben **Vorlagen** und wählen **Seitenlayout** aus dem Kontextmenü aus.


     Dadurch wird die **Layout hinzufügen** angezeigt.

     <img src="assets/add-layout-2.png" alt="Dialogfeld &quot;Layout hinzufügen&quot;" width="250">

1. Geben Sie einen Namen für das neue Seitenlayout an.
   >[!NOTE]
   >
   >Vermeiden Sie die Verwendung von Sonderzeichen bei der Benennung eines Seitenlayouts. Ein Leerzeichen im Namen wird durch einen Unterstrich &quot;_&quot;ersetzt.

1. Klicken Sie auf **Fertig**.

   Das neue Layout wird unter Seitenlayouts erstellt und hinzugefügt.


### Duplizieren eines Seitenlayouts {#duplicate-page-layout}

1. Im **Vorlagen** Bereich der Vorlage, die Sie duplizieren möchten, Doppelklicken Sie auf  **Seitenlayouts** oder auf **>** Symbol vor **Seitenlayouts**.

   Dadurch wird die Liste der Seitenlayouts in der Vorlage angezeigt.

1. Bewegen Sie den Mauszeiger über das Seitenlayout, das Sie duplizieren möchten, und klicken Sie auf (*Optionen* Symbol) **...** und wählen **Duplizieren** aus dem Kontextmenü aus.

1. Im _Layout duplizieren_ ein, geben Sie einen Namen für das Seitenlayout ein.

1. Klicken Sie auf **Fertig**.
Eine Kopie des ausgewählten Seitenlayouts wird erstellt und unter Seitenlayouts hinzugefügt.

### Seitenlayout anpassen {#customize-page-layout}

1. Im **Vorlagen** in der Vorlage, die Sie bearbeiten möchten, doppelklicken Sie **Seitenlayouts** oder auf **>** Symbol vor **Seitenlayouts**.

   Dadurch wird die Liste der Seitenlayouts in der Vorlage angezeigt.
1. Führen Sie einen der folgenden Schritte aus, um das Seitenlayout anzupassen:
   * Doppelklicken Sie auf ein beliebiges Seitenlayout.
   * Bewegen Sie den Mauszeiger über ein Seitenlayout und klicken Sie auf (*Optionen* Symbol) **...** und wählen **Bearbeiten** aus dem Kontextmenü aus.

   Dadurch wird der Seitenlayout-Editor zur Anpassung geöffnet.
1. Klicken Sie nach den gewünschten Änderungen auf *Alle speichern* (oder `Crl+S`).

   Weitere Informationen zum Definieren einzelner Layoutelemente wie Kopf- und Fußzeile, Seitenzahl, Titel und mehr finden Sie unter [Seitenlayout erstellen](design-page-layout.md).

## Verwenden von Stylesheets zum Anpassen von PDF {#stylesheet-customization}

Mit den Einstellungen in der Komponente &quot;Stylesheets&quot;können Sie die Seitenlayoutkomponenten und DITA-Inhalte mit dem WYSIWYG-Editor gestalten oder direkt mit der CSS-Datei arbeiten. Sie können eigene Stile erstellen oder die Standardstileigenschaften anpassen. Der WYSIWYG-Editor bietet Ihnen Zugriff auf die meisten Eigenschaften, die Sie zum Gestalten Ihres Seitenlayouts oder DITA-Inhalts benötigen. Für erweiterte Anpassungen können Sie direkt in der Quellansicht arbeiten.

### Neues Stylesheet erstellen {#create-stylesheet}

Während CSS-Dateien für Inhalt und Layout bereitgestellt werden, können Sie ein neues Stylesheet erstellen, um mehrere Anpassungen auf einen bestimmten Stiltyp anzuwenden, der dann auf eine Zielkomponente angewendet werden kann. Standardmäßig werden Beispiel-CSS-Dateien innerhalb des Produkts gebündelt. Diese CSS-Dateien sollen Ihnen dabei helfen, Ihre Stilinformationen über Inhalte und Layouts hinweg zu organisieren. Sie können diese Stile in einer oder mehreren CSS-Dateien zusammenführen.

Jedes Mal, wenn Sie ein neues Seitenlayout erstellen, wird standardmäßig die `layout.css` -Datei im neuen Seitenlayout enthalten ist. Wenn das Seitenlayout Stile aus einer anderen CSS-Datei enthalten soll, können Sie die gewünschte CSS-Datei einfach per Drag-and-Drop in den Inhaltsbearbeitungsbereich des neuen Seitenlayouts ziehen. Um zu überprüfen, ob die CSS-Datei in das Seitenlayout eingebettet wurde, wechseln Sie zur Quellansicht und Sie finden einen Link zur CSS-Datei im `<head>` -Element.


Gehen Sie wie folgt vor, um ein Stylesheet zu erstellen:
1. Im **Vorlagen** einen der folgenden Schritte ausführen:
   * Bewegen Sie den Mauszeiger über die **Stylesheets** und klicken Sie auf (*Optionen* Symbol) **...** und wählen **Neues Stylesheet**.
   * Klicken Sie auf **+** Symbol neben **Vorlagen** und wählen **Stylesheet** aus dem Kontextmenü aus.

   Dadurch wird das Dialogfeld Stylesheet hinzufügen geöffnet.

   <img src="assets/add-stylesheet.png" alt="Stylesheet hinzufügen" width="250">
1. Geben Sie einen Namen für das neue Stylesheet an.
1. Klicken Sie auf **Fertig**.

   Ein neues Stylesheet wird unter dem Abschnitt Stylesheets erstellt und hinzugefügt.

### Neuen Stil erstellen {#create-style}

Standardmäßig enthalten die mit der Vorlage bereitgestellten CSS-Dateien Stile für Überschrift, Absatz, Zeichen, Hyperlink, Bild, Tabelle, div, Seite und andere Stile. Sie können das Standard-Stilformat überschreiben oder einen neuen Stil erstellen.


Sie können einen neuen Stil erstellen, um ihn im Seitenlayout der Vorlage zu verwenden, oder einen benutzerdefinierten Stil für ein DITA-Element anwenden. Um diese benutzerdefinierten Stile auf das DITA-Element anzuwenden, müssen Sie sicherstellen, dass der Klassenname des Stils mit dem Namen des DITA-Elements oder dem `outputclass` -Attribut.  Beispiel: `<div>` in DITA wird durch die Variable `.div {}` in CSS oder seiner `outputclass` -Attribut. Wenn Sie eine `<div outputclass="my-div">` In DITA wird sie durch das `.div {}` oder `.my-div {}` in der CSS.



Gehen Sie wie folgt vor, um einen neuen Stil zu erstellen:
1. Erweitern Sie die linke Seitenleiste und doppelklicken Sie auf die Vorlage, in der Sie den Stil erstellen möchten.
1. Erweitern Sie die **Stylesheets** Abschnitt. Er öffnet die **Stile** -Bereich, der alle Stiloptionen enthält.
1. Klicken Sie auf das Symbol + , um einen neuen Stil hinzuzufügen.

   **Stil hinzufügen** wird geöffnet.


   <img src="assets/add-style.png" alt="Neuen Stil hinzufügen" width="500"/>

1. Geben Sie eine **Klasse** name. Um einen Stil auf das DITA-Element anzuwenden, stellen Sie sicher, dass der Klassenname des Stils mit dem Namen des DITA-Elements oder dem `outputclass` -Attribut.
1. Im **Tag** (optional), wählen Sie ein Tag aus, für das Sie einen neuen Stil erstellen möchten.


1. Wählen Sie eine **Pseudo-Klasse** um ein Element zu formatieren. Mit einer Pseudo-Klasse können Sie einen speziellen Status des Elements definieren. Verwenden Sie beispielsweise die Pseudo-Klasse, um ein Element zu formatieren, wenn Sie den Mauszeiger darüber bewegen oder wenn Sie den Fokus darauf legen. Sie können auch mehrere Pseudoklassen auswählen. Sie können beispielsweise pseudo-class verwenden `a::visited {color: blue;}` , um die besuchten Links zu formatieren.

1. Fügen Sie die Auswahl für den neuen Stil hinzu. Die **Selektor** -Feld unterstützt Sie beim Hinzufügen benutzerdefinierter Selektoren neben der Kombination aus Klasse, Tag und Pseudo-Klasse . Sie können beispielsweise `table a.link` -Stil für alle Hyperlinks in einer Tabelle.

   Weitere Informationen zu CSS-Tags finden Sie unter [Siehe CSS-Stilgrammatik .](https://www.w3.org/TR/CSS21/syndata.html#characters).

1. Klicken Sie auf **Fertig**.

   Ein neuer Stil wird erstellt und der Stilliste hinzugefügt.

### Vordefinierten oder neuen Stil anpassen {#customize-style}

Nachdem Sie eine neue CSS-Datei mit Standardstilen erstellt haben oder die Stile in einer vorhandenen CSS-Datei anpassen möchten, können Sie dazu den Stileditor verwenden.

Gehen Sie wie folgt vor, um einen Stil anzupassen:
1. Doppelklicken **Stylesheets** oder auf **>** Symbol vor **Stylesheets**.

   Dadurch werden die standardmäßigen (Inhalt und Layout) und benutzerdefinierten CSS-Dateien angezeigt.
1. Öffnen Sie ein Stylesheet zur Bearbeitung.

   Führen Sie einen der folgenden Schritte aus, um das Stylesheet zur Bearbeitung zu öffnen:
   * Doppelklicken Sie auf den Stylesheet-Namen.
   * Bewegen Sie den Mauszeiger über den Namen des Stylesheets und klicken Sie auf das Symbol Optionen ... und wählen Sie Bearbeiten.

   Dadurch wird das Stylesheet zur Bearbeitung geöffnet und die Liste der Stile im Bedienfeld &quot;Stile&quot;angezeigt.

   <img src="assets/customize-style.png" alt="Stil anpassen" width="800">

1. Um einen Stil anzupassen, wählen Sie den Stil aus, der angezeigt werden soll, und passen Sie ihn mithilfe des Stileditors an.


### Eigenschaften von Stilen

Im mittleren Bereich können Sie die Eigenschaften bearbeiten. Es kann jedoch schwierig sein, eine Momentaufnahme aller vorhandenen Werte zu erhalten.  Die **Eigenschaften** gibt einen schnellen Überblick über alle Attribute und Werte des Stils.

Im mittleren Bereich können Sie die häufig verwendeten Eigenschaften bearbeiten, jedoch nicht alle von CSS unterstützten Eigenschaften. Im **Eigenschaften** können Sie alle von CSS unterstützten Eigenschaften bearbeiten und eine Vorschau davon anzeigen. Sie müssen nicht zur Quellansicht wechseln, um Eigenschaften zu bearbeiten.


Erfahren Sie mehr über die Verwendung des Stileditors zum [Arbeiten mit allgemeinen Inhaltsstilen](stylesheet.md).

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

1. Klicks **Dateien auswählen** zum Durchsuchen der Asset-Datei von Ihrem lokalen Computer aus

1. Klicken Sie auf **Hochladen**.
Die ausgewählte Datei wird importiert und im Ordner Ressourcen aufgeführt.

## Erweiterte PDF-Einstellungen {#advanced-pdf-settings}

Verwenden Sie den Bereich Einstellungen , um das Layout der erweiterten PDF zu konfigurieren, das PDF von ungeraden oder geraden Seiten zu starten, die Formate für die Querverweise zu konfigurieren und Druckmarken in der endgültigen PDF zu aktivieren, die mithilfe der Vorlage generiert wird.

Klicken Sie zum Konfigurieren auf **Einstellungen** im **Vorlagen** -Bereich, um die folgenden Optionen anzuzeigen:

### Allgemein

Legen Sie die grundlegenden Konfigurationseinstellungen für das Starten eines Kapitels von einer ungeraden oder geraden Seite, die TOC-Struktur fest und definieren Sie das Füllzeichenzeilenformat für die TOC-Einträge. Sie können die folgende Einstellung definieren:

* **Starten Sie ein neues Kapitel aus**: Hiermit können Sie festlegen, wie die einzelnen Kapitel im endgültigen PDF veröffentlicht werden. Sie können aus einer **Neue Seite**, **Ungerade Seite**, **Gerade Seite** oder **Aktuelle Seite**  Optionen. Wenn Sie ein neues Kapitel von einer ungeraden Seite aus beginnen möchten, wird nach einem Kapitel, das auf einer ungeraden Seite endet, eine leere Seite eingefügt. Wenn Ihr Kapitel beispielsweise auf Seite 15 endet, fügt der Veröffentlichungsprozess eine leere 16 ein<sup>th</sup> -Seite, damit das neue Kapitel mit der 17 beginnen kann.<sup>th</sup> Seite.  Wenn Sie die **Aktuelle Seite** -Option, werden alle Kapitel als Fortsetzung ohne Seitenumbrüche veröffentlicht. Wenn ein Kapitel beispielsweise in der Mitte von Seite 15 endet, wird das nächste Kapitel auch von der 15. Seite selbst aus gestartet.

* **Jedes Thema von einer neuen Seite aus starten**: Wenn jedes Thema in Ihrem Kapitel von einer neuen Seite aus beginnen soll, wählen Sie **Jedes Thema von einer neuen Seite aus starten** -Option. Wenn Sie Ihre Themen ohne Seitenlücken fortsetzen möchten, deaktivieren Sie diese Option.

* **Inhaltsverzeichnis-Struktur**: Hiermit können Sie die Hierarchie des Inhaltsverzeichnisses anpassen. Es werden die folgenden zusätzlichen Einstellungen verwendet:

   * **Überschriften bis zur Ebene verwenden**: Hiermit können Sie die Anzahl der Überschriftenebenen anpassen, die in der TOC-Struktur Ihrer PDF angezeigt werden sollen.
   * **Zeigt keine Seitenzahl für die erste Ebene im Inhaltsverzeichnis an**: Wählen Sie diese Option, um die entsprechenden Seitenzahlen für alle Kapitel auszublenden, die verschachtelte oder untergeordnete Themen enthalten. Betrachten Sie das folgende Beispiel, in dem eine Ausgabe erstellt wird, ohne diese Option auszuwählen.

  <img src="assets/page-number-in-toc.png" alt="Hochladen von Assets" width="250">

  Im obigen Beispiel sind Erweiterte PDF-Einstellungen, Anhang und rechtliche Themen die ersten Themenüberschriften oder Kapiteltitel. Allen diesen Überschriften wird eine Seitenzahl zugewiesen.

  Wenn Sie jetzt diese Option auswählen und die Ausgabe generieren, erhalten Sie das folgende Inhaltsverzeichnis:

  <img src="assets/page-number-missing-in-toc.png" alt="Hochladen von Assets" width="250">

  Hier können Sie bemerken, dass die erweiterten PDF-Einstellungen des ersten Kapitels keine Seitenzahl erhalten, da sie verschachtelte oder untergeordnete Themen haben. Eine Seitenzahl hingegen, wenn sie Anhang und Legal zugewiesen wird, da es sich um eigenständige Themen ohne untergeordnetes Thema handelt.

* **Kapitelnummer im Inhaltsverzeichnis nicht anzeigen** : Wählen Sie diese Option, um die Kapitelnamen ohne die Kapitelnummern im Inhaltsverzeichnis anzuzeigen.   Standardmäßig werden die Kapitelnummern im TOC Ihrer PDF-Ausgabe angezeigt.
* **Füllzeichenformat**: Verwenden Sie die Dropdown-Liste, um die Füllzeichenlinien &quot;Gepunktet&quot;, &quot;Durchgehend&quot;oder &quot;Leerzeichen&quot;auszuwählen, um die Überschriftenebenen mit den entsprechenden Seitenzahlen zu verbinden.
Informationen zum Anwenden der TOC-Struktur und der Styling-Überschriftenebenen finden Sie unter [Kapitel-Inhaltsverzeichnis hinzufügen](design-page-layout.md#add-chapter-toc).

  >[!NOTE]
  >
  >Wenn Sie CSS-Entwickler sind, können Sie das Füllzeichenformat auch direkt in der CSS-Datei definieren.

* **Verwenden der Tabellenfortsetzungsmarkierung**: Wählen Sie diese Option, um Markierungen für lange Tabellen zu definieren, die über mehrere Seiten verteilt sind.
Sie können den Text definieren, der vor und nach dem Umbruch angezeigt werden soll. Beispielsweise wird eine Tabelle auf Seite 5 umgebrochen, und Sie definieren `<Continued on page %page-num%>` für **Text vor Umbruch**.  Im Text wird unten auf Seite 5 &quot;Fortsetzung auf Seite 6&quot;angezeigt.

  Verwenden Sie Sprachvariablen, um den Text für die Fortsetzung der Markierung vor und nach der Pause zu definieren. Abhängig von Ihrer ausgewählten Sprache wird der lokalisierte Wert automatisch in der PDF-Ausgabe ausgewählt. Sie können beispielsweise `Continued on page %page-num%` als Text in Englisch und `Fortsetzung auf Seite %page-num%` auf Deutsch.

  Bewegen <img src="./assets/info-details.svg" alt= "Infosymbol" width="25"> neben der Option, um weitere Details dazu anzuzeigen.
* **Glossarbegriffe mit der Glossarseite verknüpfen**: Wählen Sie diese Option, um die Glossarbegriffe als Hyperlinks im Inhalt anzuzeigen und sie mit den Begriffen auf der Glossarseite zu verknüpfen. Dies hilft den Lesern, die Definition eines Begriffs im Glossar schnell anzuzeigen.

  Um die Glossarbegriffe in Hyperlinks zu konvertieren, gehen Sie folgendermaßen vor:
   * Aktivieren **Glossar** im **Seitenreihenfolge** für eine DITA-Zuordnung.
   * Fügen Sie das Glossar in die &quot;Back Matter Pages&quot;für eine Buchkarte ein.

  Wenn Sie die Glossarseite nicht aktivieren, werden die Glossarbegriffe im Inhalt nicht in Hyperlinks in der PDF-Ausgabe konvertiert.
  <!--For more information on using table continuation markers, see Use table continuation markers.-->

### Seitenlayouts {#page-layouts}

Mit den Einstellungen für Seitenlayouts können Sie vollständig festlegen, welches Seitenlayout für einen bestimmten Abschnitt Ihres Dokuments verwendet werden soll. Um beispielsweise ein Layout für das Inhaltsverzeichnis auszuwählen, klicken Sie auf das Dropdown-Menü unter dem Feld Inhaltsverzeichnis und wählen Sie das Layout aus, das Sie zum Generieren des Inhaltsverzeichnisses entwickelt haben.

Beachten Sie, dass die Einstellungen für die Lesekarte Vorrang vor den Einstellungen für das Seitenlayout haben.

Die folgenden Einstellungen sind im Abschnitt Seitenlayout verfügbar:

<img src="assets/template-page-layout.png" alt="Seitenlayouts" width="550">


**Standardseitenlayout**: Wählen Sie ein Seitenlayout, das als Standardlayout für alle Seiten in Ihrer PDF dient. Dies ist das grundlegende Seitenlayout, das auf die Abschnitte oder Themen angewendet wird, in denen Sie kein dediziertes Seitenlayout erstellt haben.

**Seitenlayout für verschiedene Abschnitte**: Sie können ein Seitenlayout den folgenden Abschnitten Ihrer PDF-Ausgabe zuordnen. Wenn Sie ein Seitenlayout für den zugehörigen Abschnitt entworfen haben, wählen Sie es aus der Dropdownliste aus. Wenn für bestimmte Abschnitte keine Seitenlayouts erstellt wurden, wird das standardmäßige Seitenlayout angewendet.

* **Kapitel und Themen**: Sie können das Seitenlayout für die Kapitel und Themen festlegen. Das ausgewählte Layout wird auf alle Kapitel und Themen angewendet.

* **TOC**: Wenn Sie das Seitenlayout für das Inhaltsverzeichnis entworfen haben, wählen Sie **TOC** in der Dropdown-Liste und alle TOC-Seiten in Ihrem Dokument haben das Layout der Inhaltsverzeichnis-Seite.

* **Liste der Abbildungen und Tabellen**: Sie können auch das Seitenlayout für Zahlen und Tabellen festlegen. Das ausgewählte Layout wird auf alle Abbildungen und Tabellen angewendet.

* **Index**: Wenn Sie ein Indexseitenlayout entworfen haben, ordnen Sie es der Option Index zu. Mithilfe der Stylesheets können Sie verschiedene Indexelemente in der PDF-Ausgabe formatieren. Indexstile verwenden `.idx-header`, `.idx-footer`, `.idx-body`, `.idx-title`, `.idx-keyword-group`, `.idx-unit`,  `.idx-keyword`, `.idx-name`, `.idx-link` und `.idx-child` , um die Stile für die Elemente des Index anzupassen.

* **Glossar**: Wenn Sie ein Glossar-Seitenlayout haben, ordnen Sie es der Glossaroption zu.  Die Begriffe im Glossar Ihrer PDF-Ausgabe werden immer in alphabetischer Reihenfolge sortiert.

  Mithilfe der Stylesheets können Sie verschiedene Glossarelemente in der PDF-Ausgabe gestalten. Glossarstile verwenden `.glo-header`, `.glo-footer`, `.glo-body`, `.glo-title`, `.glo-unit`, `.glo-link`, und `.glo-term` , um die Stile für die Elemente des Glossars anzupassen.

  Erfahren Sie mehr über die Verwendung des Stileditors zum [Arbeiten mit allgemeinen Inhaltsstilen](stylesheet.md).

* **Seiten mit VorMaterie und Seiten mit Rücken**: Diese Seitenlayouts definieren die Formatierung für Seiten mit Vorder- oder Rückseite Ihres Buches. Wenn Sie das Layout der Vorderteile entworfen haben, ordnen Sie es dem **Seiten mit Vordergrund** -Option. Wenn Sie das Layout der Vorderseite aus dem Dropdown-Menü auswählen, wird das Layout der Vorderseite auf alle in der Vorderseite vorhandenen Themen angewendet.

  Wenn Sie das Layout für die Hintergrundmatte entworfen haben, ordnen Sie es dem **Zurück Matter Pages** -Option. Wenn Sie das Layout für die Hintergrundmatte aus der Dropdown-Liste auswählen, wird das Layout für die Hintergrundmatte auf alle Themen angewendet, die in der Hintergrundmatte vorhanden sind.

  **Seiten mit Vordergrund** wird auch als Fallback-Layout für die **TOC**, **Bildliste** und Liste der Tabellen.  Ebenso **Zurück Matter Pages** wird auch als Fallback-Layout für die **Index** und **Glossar** Layouts. Wenn Sie das Layout für diese Seiten nicht ausgewählt haben, wird das ausgewählte Seiten-Layout &quot;Vorder-&quot;und &quot;RückMatter-Seiten&quot;angewendet.  Wenn Sie das Layout Seiten mit Vorder- oder RückMaterie nicht ausgewählt haben, wird das standardmäßige Seitenlayout auf sie angewendet.

* **Seitenlayout für leere Seiten**: Sie können auch das Seitenlayout für leere Seiten festlegen. Das ausgewählte Layout wird auf alle leeren Seiten angewendet. Wenn Sie beispielsweise ein leeres Seitenlayout für alle leeren Seiten entworfen haben, wählen Sie **Leer** in der Dropdown-Liste und alle leeren Seiten in Ihrem Dokument haben das Layout Leere Seite .

* **Titelseite und Rückseite**: Wenn Sie ein Deckblatt-Layout entworfen haben, ordnen Sie es dem **Titelseite** -Option. Wenn Sie ein Layout für die Rückseite haben, ordnen Sie es dem **Zurück-Seite** -Option. Wenn keine Deckblatt- oder Rückseite-Layouts erstellt wurden, wird das standardmäßige Seitenlayout angewendet.



Weitere Informationen zu Seitenlayouts finden Sie unter [Seitenlayout erstellen](design-page-layout.md).

### Seitenreihenfolge {#page-order}

Sie können die folgenden Bereiche in Ihrer PDF ein- oder ausblenden und auch die Reihenfolge anordnen, in der sie in Ihrer endgültigen PDF-Ausgabe angezeigt werden sollen:



* IHV
* Kapitel und Themen
* Bildliste
* Tabellenliste
* Index
* Glossar
* Zitat

  <img src="assets/page-order-advance-settings.png" alt="Seitenreihenfolge" width="550">

  Wenn Sie in Ihrer PDF-Ausgabe keinen bestimmten Bereich anzeigen möchten, können Sie dies verbergen, indem Sie den Umschalter ausschalten.

  Sie können auch die Reihenfolge definieren, in der diese unterschiedlichen Bereiche in Ihrer PDF erstellt werden. Um die Standardreihenfolge dieser Abschnitte zu ändern, wählen Sie die gepunkteten Balken aus, um die Abschnitte per Drag-and-Drop an die gewünschte Position zu ziehen.

  >[!NOTE]
  >
  > Die Einstellungen für Reihenfolge und Einbindung gelten nur für eine DITA-Zuordnung. Bei einer Lesekarte sind diese Einstellungen nicht anwendbar. Die Seiten in einer Lesekarte werden gemäß der Reihenfolge der Abschnitte in der Lesekarte angezeigt.


.
**Kapitel und Themen** Das Layout ist standardmäßig immer aktiviert. Sie können sie nicht umschalten.

**Seiten zusammenführen**

Standardmäßig beginnen alle Abschnitte auf einer neuen Seite. Wählen Sie die **Vorherige Seite** oder **Nächste Seite** Option aus der **Zusammenführen mit** Dropdown, um einen Abschnitt mit einer vorherigen oder nächsten Seite zusammenzuführen. Dadurch wird der Abschnitt in Weiterführung mit der ausgewählten Seite in der PDF-Ausgabe veröffentlicht. Dadurch gibt es keinen Seitenumbruch dazwischen.

>[!NOTE]
>
> Diese Einstellung gilt nur für den Abschnitt und nicht für dessen Komponenten.  Wenn Sie beispielsweise die **Vorherige Seite** -Option für **Kapitel und Themen**, die **Kapitel und Themen** -Abschnitt wird mit der vorherigen Seite zusammengeführt. Die verschiedenen Kapitel und Themen werden gemäß **Allgemein** settings.Wenn beispielsweise in **Starten Sie ein neues Kapitel, indem Sie** auswählen **Ungerade Seite**, wird nach einem Kapitel, das auf einer ungeraden Seite endet, eine leere Seite eingefügt.

Wenn Sie einen Abschnitt mit der vorherigen Seite oder der nächsten Seite zusammenführen, wird der Inhalt zusammengeführt und der Stil des Zielabschnitts, in dem der Inhalt zusammengeführt wird, wird angewendet.

Wenn Sie beispielsweise **TOC** und **Kapitel und Themen** und wählen Sie die **Nächste Seite** für **TOC**, die **TOC** führt mit dem nächsten Abschnitt zusammen, d. h. dem **Kapitel und Themen**. Der Stil des **Kapitel und Themen** wird auf den zusammengeführten Inhalt beider Abschnitte angewendet.

Die Option &quot;Zusammenführen&quot;funktioniert nacheinander, wenn Sie also **Nächste Seite** für mehrere fortlaufende Abschnitte werden sie alle mit dem ersten Abschnitt (in die nächste Richtung) zusammengeführt, für den diese Eigenschaft nicht festgelegt ist. Sie können beispielsweise **TOC**, **Kapitel und Themen**, **Bildliste**, und **Index**. Wenn Sie **Nächste Seite** für **TOC**, **Kapitel und Themen**, **Bildliste**, und **Keines** für **Index**, werden alle mit  **Index**.


**Statische Seiten**

Die verschiedenen Seitenlayouts helfen Ihnen dabei, die Ausgabe der verschiedenen Abschnitte zu entwerfen. Diese Abschnitte werden beim Veröffentlichen der Ausgabe aus der DITA-Zuordnung generiert.
Sie können auch benutzerdefinierte Seitenlayouts erstellen und diese als statische PDF-Seiten veröffentlichen. Auf diese Weise können Sie statischen Inhalt wie Notizen oder leere Seiten hinzufügen.

Führen Sie die folgenden Schritte aus, um ein benutzerdefiniertes Seitenlayout hinzuzufügen:

1. Auswählen **Hinzufügen** ![](assets/add-icon.svg) , um ein neues Seitenlayout hinzuzufügen. Das Bedienfeld &quot;Seitenlayout hinzufügen&quot;wird geöffnet.
2. Wählen Sie das Seitenlayout aus der Liste aus und klicken Sie auf Hinzufügen. Das neue Seitenlayout wird der Liste der Seitenlayouts hinzugefügt.


Sie können auch die folgenden Aktionen durchführen:

* Wählen Sie die gepunkteten Balken aus, um das Seitenlayout an die gewünschte Position zu ziehen.

* Auswählen **Layout entfernen** ![](assets/delete-icon.svg)  um ein Layout zu entfernen.

* Sie können auch eine statische Seite mit der vorherigen oder der nächsten Seite zusammenführen.

* Sie können auch ein benutzerdefiniertes Layout mehrmals hinzufügen und sortieren. Auf diese Weise können Sie statischen Inhalt entsprechend veröffentlichen.

  Beispielsweise können Sie ein benutzerdefiniertes Layout verwenden, um eine statische Warnung mehrmals in der PDF-Ausgabe zu veröffentlichen.




### Druck

Konfigurieren Sie die Druckproduktionseinstellungen, um Druckermarkierungen zuzuweisen, Farbmodelle auszuwählen und Eigenschaften für den Druck Ihrer PDF-Ausgabe anzugeben.

* **Druckermarken**: Wenn Sie ein Dokument für die Druckproduktion vorbereiten, werden den Seitengrenzen Druckmarkierungen hinzugefügt, um die korrekte Ausrichtung, Beschneidung und Farbauswahl beim Drucken zu unterstützen. Durch Auswahl eines Druckerzeichens wird die Seitenbegrenzung erweitert, um die Markierung aufzunehmen, die beim Drucken abgeschnitten wird. Sie können die folgenden Druckermarkierungen in Ihrer PDF-Ausgabe anzeigen lassen:
   * **Schnittmarken**: Wählen Sie die Option aus, um an jeder Ecke des Schnittbereichs eine Markierung zu platzieren und anzugeben, wo das Papier nach dem Drucken beschnitten werden soll.
   * **Anschnittmarken**: Wählen Sie diese Option, um eine Markierung an jeder Ecke des Anschnittrahmens zu platzieren, um den Schnittbereich für das erweiterte Bild anzugeben.
   * **Registrierungszeichen**: Wählen Sie diese Option, um eine Markierung außerhalb des Zuschnittbereichs zu platzieren, damit die verschiedenen Trennlinien in einem Farbdokument ausgerichtet werden.
   * **Farbbalken**: Wählen Sie diese Option, um einen Farbstreifen außerhalb des Schnittbereichs hinzuzufügen, um die Farbkonsistenz zu gewährleisten und die Farbdichte beim Drucken anzupassen.

  Legen Sie Dimensionen für die ausgewählten Druckermarkierungen mithilfe der **Linienbreite**, **Linienfarbe**, und **Breite des Anschnittrahmens** Optionen.

* **Größe des Medienfelds**: Dies ist die Gesamtseitengröße einschließlich des erweiterten Bereichs, der von Druckermarkierungen belegt wird. Verwenden Sie die Dropdown-Option, um die Seitengröße für Ihre PDF-Ausgabe auszuwählen oder eine eigene benutzerdefinierte Größe zu erstellen.

* **Farbraum**: Sie haben die Möglichkeit, aus RGB- oder CMYK-Farbräumen auszuwählen, um Ihr PDF-Dokument zu drucken. Wählen Sie RGB aus, um die generierte PDF digital und CMYK für den physischen Druck anzuzeigen. Die im Dokument definierten Farben werden in den ausgewählten Farbraum konvertiert.
  >[!NOTE]
  >
  >Für die Erstellung von PDF/A ist bei Verwendung des CMYK-Farbraums ein ICC-Farbprofil erforderlich.

  <!--For more information on applying these print settings, see *Printing preferences*.-->

### Querverweise {#cross-references}

Verwenden Sie die **Querverweis** um festzulegen, wie die Querverweise auf der PDF veröffentlicht werden. Sie können die Querverweise für Thementitel, Tabellen, Zahlen und mehr formatieren.

Sie können auch Variablen verwenden, um einen Querverweis zu definieren.  Wenn Sie eine Variable verwenden, wird ihr Wert aus den Eigenschaften ausgewählt. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um einen Querverweis zu definieren. Sie können auch eine Kombination aus Zeichenfolge und Variable verwenden.

Sie können beispielsweise `View details on {chapter}`. Wenn der Kapitelname &quot;Allgemeine Einstellungen&quot;lautet, lautet der Querverweis in der Ausgabe &quot;Siehe Details zu den allgemeinen Einstellungen&quot;.

AEM Guides bieten die folgenden nativen Variablen:

* {title}: Erstellt einen Querverweis zum Titel des Themas. Siehe beispielsweise Nützliche Links auf Seite 2.
* {page} Fügt einen Querverweis zu den Seitenzahlen hinzu. Siehe beispielsweise auf Seite 1.
* {description}: Fügt einen Querverweis zum Text der Beschreibung hinzu. Siehe beispielsweise die Details AEM Handbücher.
* {chapter}: Fügt einen Querverweis zu den Kapitelnummern hinzu. Siehe beispielsweise Kapitel 1.
* {bookmarkText}: Erstellt einen Querverweis zum mit Lesezeichen versehenen Text. Siehe beispielsweise stop_words auf Seite 5.
* {captionText}: Erstellt einen Querverweis zur Beschriftung der Abbildung oder Tabelle in Ihrem Thema. Siehe zum Beispiel Flugfluss auf Seite 2.
* {figure}: Fügt einen Querverweis zur Zahl hinzu. Wählt die Zahl aus den automatischen Nummernstilen aus, die Sie für die Beschriftung definiert haben.  Sie können beispielsweise &quot;Siehe {figure} auf Seite {page}&quot;. Der Querverweis in der Ausgabe enthält die automatisch generierte Zahlen- und Seitenzahl &quot;Siehe Abbildung 1 auf Seite 5&quot;.
* {table}: Fügt einen Querverweis zur Tabellennummer hinzu. Wählt die Tabellennummer aus den automatischen Nummernstilen aus, die Sie für die Beschriftung definiert haben. Sie können beispielsweise &quot;Siehe {table} auf Seite {page}&quot;. Der Querverweis in der Ausgabe enthält die automatisch generierte Tabellennummer und die zugehörige Seitenzahl &quot;Siehe Tabelle 1 auf Seite 5&quot;.



  >[!NOTE]
  >
  >Sie können für Beschriftungs- und Beschriftungs-Tags einen automatischen Nummernstil erstellen.


#### Sprachvariablen in Querverweisen

Sie können auch Sprachvariablen verwenden, um lokalisierte Querverweise zu definieren. Abhängig von Ihrer ausgewählten Sprache wird der lokalisierte Wert automatisch in der PDF-Ausgabe ausgewählt.

Beispielsweise können Sie eine Sprachvariable &quot;reference-label&quot;hinzufügen und die Werte in Englisch und Deutsch definieren.

* Englisch - &quot;Ansicht auf Seite {page}&quot;
* Deutsch - &quot;ANZEIGE auf der Seite&quot; {page}&quot;


Wenn Sie `${lng:<variable name>}` im Abschnitt Absatz enthalten die Querverweise in den Absätzen der Ausgabe den lokalisierten Text und die Seitenzahl.\
Beispielsweise zeigen die folgenden Screenshots die Querverweise &quot;View on the Page 1&quot; auf Englisch und &quot;View auf der Seite 1&quot; auf Deutsch.

<img src="./assets/english-output-corss-reference.png" alt="Englische Ausgabe eines Querverweises in einer Schreibweise" width ="800">

*Ein Querverweis innerhalb eines Absatzes, wenn er in englischer Sprache veröffentlicht wird.*

<img src="./assets/german-output-corss-reference.png" alt="Ausgabe eines Querverweises in einer Schreibweise" width ="800">

*Ein Querverweis innerhalb eines Absatzes, wenn er in deutscher Sprache veröffentlicht wird.*

<!--For more information, see *Format cross-references*.-->
