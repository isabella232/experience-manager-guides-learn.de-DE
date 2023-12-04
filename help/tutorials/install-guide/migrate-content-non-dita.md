---
title: Nicht-DITA-Inhalt migrieren
description: Erfahren Sie, wie Sie Nicht-DITA-Inhalte migrieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '2761'
ht-degree: 0%

---

# Nicht-DITA-Inhalt migrieren {#id181AH0R02HT}

Dieser Abschnitt führt Sie durch den Migrationsprozess, um Nicht-DITA-Dokumente in das DITA-Format zu migrieren. AEM Guides bieten Migration aus den folgenden Quellen:

- [Microsoft Word](#id1949B040Z5Z)

- [InDesign-Dokumente](#id195AD0B0K5Z)

- [XHTML](#id1949B04L0Y4)

- [Unstrukturierte FrameMaker-Dokumente](#id1949B050VUI)

- [Jedes andere strukturierte Dokument](#id1949B0590YK)


## Migrieren von Microsoft Word-Dokumenten {#id1949B040Z5Z}

Mit AEM Guides können Sie vorhandene Word-Dokumente migrieren \(`.docx`\) in DITA-Thementypdokumente. Sie müssen die Eingabe- und Ausgabeordnerspeicherorte zusammen mit anderen Parametern angeben und das Dokument wird in ein DITA-Dokument konvertiert. Je nach Inhalt können Sie über eine .dita-Datei und eine .ditamap-Datei verfügen.

Um ein Word-Dokument erfolgreich konvertieren zu können, sollte Ihr Dokument gut strukturiert sein. Beispielsweise sollte Ihr Dokument einen Titel, gefolgt von Überschrift 1, Überschrift 2 usw. haben. Jede Überschrift sollte einen Inhalt enthalten. Wenn Ihr Dokument nicht gut strukturiert ist, funktioniert der Prozess möglicherweise nicht wie erwartet.

Standardmäßig verwenden AEM Guides die [Word-to-DITA \(Word2DITA\) Transformations-Framework](http://www.dita4publishers.org/docs/repo/org.dita4publishers.word2dita/word2dita/word2dita-intro.html). Diese Umwandlung hängt von der [Zuordnung von Stil zu Tag](http://www.dita4publishers.org/docs/repo/org.dita4publishers.word2dita/word2dita/style-to-tag-map-overview.html) Konfigurationsdatei. Um die Word2DITA-Transformation erfolgreich verwenden zu können, müssen Sie die folgenden Richtlinien beachten, um Ihr Word-Dokument für die Konvertierung vorzubereiten:

>[!NOTE]
>
> Wenn Sie Änderungen an der standardmäßigen Konfigurationsdatei für die Zuordnung von Stil zu Tag vornehmen, müssen Sie die Richtlinien aktualisieren und verwenden, die Ihre aktualisierte Stilzuordnung bestätigen.

- Stellen Sie sicher, dass Ihr Dokument mit einem Titel beginnt. Dieser Titel ist dem DITA-Map-Titel zugeordnet. Außerdem müssen auf den Titel einige reguläre Inhalte folgen.

- Nach dem Titel sollte Überschrift 1, Überschrift 2 usw. stehen. Jede Überschrift muss Inhalt enthalten. Die Überschriften werden in neue Themen vom Typ Konzept umgewandelt. Die Hierarchie der generierten Themen richtet sich nach den Überschriftenebenen im Dokument. So geht beispielsweise Überschrift 1 der Überschrift 2 voran und Überschrift 2 geht dem Inhalt von Überschrift 3 voran.

- Das Dokument muss mindestens einen Inhalt vom Typ Überschrift enthalten.

- Vergewissern Sie sich, dass Sie keine gruppierten Bilder haben. Wenn Sie Bilder in Ihrem Dokument gruppiert haben, heben Sie die Gruppierung aller dieser Bilder auf.

- Entfernen Sie alle Kopf- und Fußzeilen.

- Inline-Stile wie Fett, Kursiv und Unterstrichen werden in `b`, `i`, und `u` -Elemente.

- Alle sortierten und unsortierten Listen werden in `ol` und `ul` -Elemente. Dies gilt auch für verschachtelte Listen, Listen in Tabellen, Anmerkungen oder Fußnoten.

- Alle Hyperlinks werden in `xref`.

- Der Dateiname der konvertierten Dateien basiert auf dem Überschriftentext gefolgt von einer Dateinummer. Die Dateinummer ist eine sequenzielle Zahl, die auf der Position des Überschriftentextes im Dokument basiert. Wenn beispielsweise ein Überschriftentext &quot;Beispielüberschrift&quot;lautet und er die 10. Überschrift im Dokument ist, ist der resultierende Dateiname für dieses Thema ähnlich dem Beispiel\_Überschrift\_10.dita.


Führen Sie die folgenden Schritte aus, um Ihre vorhandenen Word-Dokumente in DITA-Thementypdokumente zu konvertieren:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zur Standardkonfigurationsdatei, die unter folgendem Speicherort verfügbar ist:

   `/libs/fmdita/config/w2d_io.xml`

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Konfigurationsdatei im `apps` node:

   `/apps/fmdita/config/w2d_io.xml`

   Die `w2d_io.xml` -Datei enthält die folgenden konfigurierbaren Parameter:

   - Im `inputDir` -Element, geben Sie den Speicherort des Eingabeordners an, in dem Ihre Word-Quelldokumente verfügbar sind. Wenn beispielsweise Ihre Word-Dokumente in einem Ordner mit dem Namen `wordtodita` in `projects` und geben Sie den Speicherort als Folgendes an: `/content/dam/projects/wordtodita/`

   - Im`outputDir` -Element den Speicherort des Ausgabeordners angeben oder den Standardspeicherort für die Ausgabe beibehalten, um das konvertierte DITA-Dokument zu speichern. Wenn der angegebene Ausgabeordner nicht in DAM vorhanden ist, erstellt der Konvertierungs-Workflow den Ausgabeordner.

   - Für `createRev` -Element angeben, ob eine neue Version des konvertierten DITA-Themas erstellt werden soll \(`true`\) oder nicht \(`false`\).

   - Im `s2tMap` -Element den Speicherort der Zuordnungsdatei angeben, die Zuordnungen für Word-Dokumentstile zu DITA-Elementen enthält. Die Standardzuordnung wird in der Datei gespeichert, die sich unter:

     ```XML
     /libs/fmdita/word2dita/word-builtin-styles-style2tagmap.xml
     ```

     >[!NOTE]
     >
     > Weitere Informationen zur Struktur von `word-builtin-styles-style2tagmap.xml` und wie Sie sie anpassen können, siehe [Zuordnung von Stil zu Tag](http://www.dita4publishers.org/docs/repo/org.dita4publishers.word2dita/word2dita/style-to-tag-map-overview.html) in *Benutzerhandbuch zu DITA für Herausgeber*.

   - Geben Sie im Element props2Propagate die Eigenschaften an, die an die DITA-Zuordnung übergeben werden sollen. Diese Eigenschaft ist erforderlich, um die Standardmetadaten wie dc:title,dc:subject,dam:keywords,dam:category aus Dokumentmetadaten an konvertierte DITA-Assets zu übergeben.

1. Speichern Sie die Datei `w2d_io.xml`.

1. Nach dem Konfigurieren der erforderlichen Parameter in der `w2d_io.xml` -Datei, melden Sie sich bei AEM an und öffnen Sie die Assets-Benutzeroberfläche.

1. Navigieren Sie zum Eingabeordnerspeicherort \(`wordtodita`\).

1. Laden Sie die Word-Quelldokumente in diesen Ordner hoch. Informationen zum Hochladen von Inhalten in DAM finden Sie unter [Vorhandenen DITA-Inhalt hochladen](migrate-content-upload-existing-dita-content.md#).


Verwenden der `config` `/config` -Block, können Sie einen oder mehrere Konfigurationsblöcke für die Konvertierung definieren. Der Konvertierungs-Workflow wird ausgeführt und die endgültige Ausgabe in Form eines DITA-Themas wird an dem im Abschnitt `outputDir` -Element.

## Migrieren von Adobe InDesign-Dokumenten {#id195AD0B0K5Z}

Mit AEM Guides können Sie InDesign-Dokumente konvertieren. Ähnlich wie beim FrameMaker ermöglicht InDesign auch die Erstellung unstrukturierter und strukturierter Dokumente. Die unstrukturierten Dokumente verwenden die Absätze- und Zeichenstile zum Formatieren von Inhalten. Das strukturierte Dokument verwendet Elemente und die zugehörigen Attribute.

Der Konvertierungsprozess erfordert die Zuordnung der Absätze- und Zeichenstilformate zu relevanten DITA-Elementen. Gleichermaßen enthält die Zuordnungsdatei bei strukturierten Dokumenten eine Eins-zu-Eins-Zuordnung von InDesign-Elementen und -Attributen mit DITA-Elementen und -Attributen.

Der Konvertierungsprozess umfasst die folgenden Aktionen im Backend:

- Die *InDesign Markup-Sprache* Die Datei \(IDML\) wird in ein Arbeitsverzeichnis entpackt.
- Die Datei designmap.xml wird gelesen, um die einzelnen InDesign-Geschichten zu finden.
- Alle Geschichten werden zu einer einzelnen XML-Instanz zusammengeführt, &quot;leere&quot;Geschichten werden verworfen.
- Alle eingebetteten Grafiken werden exportiert.
- Vorkonvertierung von Standardstrukturen wie Tabellen und Grafiken in das DITA-Format.
- Stil- oder Strukturzuordnung zur endgültigen Ausgabe basierend auf der Zuordnungsdatei.
- Erstellung und Validierung einzelner DITA-Themen und DITA-Zuordnungsdateien.
- Löschen temporärer Dateien.

Im Großen und Ganzen erfordert der Konvertierungsprozess Folgendes: [Vorbereiten von InDesign-Dateien für die Konvertierung](appendix.md#id195DBF0045Z) und [Bereiten Sie die Zuordnungsdatei für die InDesign zu DITA-Migration vor.](appendix.md#id194AF0003HT) dann müssen Sie die angegebene Prozedur zur Ausführung des Konvertierungsprozesses befolgen.

Führen Sie die folgenden Schritte aus, um Ihre vorhandenen InDesign-Dokumente in DITA-Thementypdokumente zu konvertieren:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zur Standardkonfigurationsdatei, die unter folgendem Speicherort verfügbar ist:

   `/libs/fmdita/config/idml2dita_io.xml`

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Konfigurationsdatei im `apps` node:

   `/apps/fmdita/config/idml2dita_io.xml`

   Konfigurieren Sie die folgenden Parameter im `idml2dita_io.xml` Datei:

   - Im `inputDir` -Element, geben Sie den Speicherort des Eingabeordners an, in dem die Quelldokumente für InDesign verfügbar sind. Wenn Ihre InDesign-Dokumente beispielsweise in einem Ordner mit dem Namen `indesigntodita` in `projects` und geben Sie den Speicherort als Folgendes an: `/content/dam/idmlfiles/indesigntodita/`

   - Im`outputDir` -Element den Speicherort des Ausgabeordners angeben oder den Standardspeicherort für die Ausgabe beibehalten, um das konvertierte DITA-Dokument zu speichern. Wenn der angegebene Ausgabeordner nicht in DAM vorhanden ist, erstellt der Konvertierungs-Workflow den Ausgabeordner.

   - Im `mapStyle` -Element den Speicherort der Zuordnungsdatei angeben, die Zuordnungen für InDesign-Dokumentstile zu DITA-Elementen enthält. Die Standardzuordnung wird in der Datei gespeichert, die sich unter:

     ```XML
     /stmap.adobeidml.xml
     ```

     >[!NOTE]
     >
     > Weitere Informationen zur Struktur von `stmap.adobeidml.xml` und wie Sie sie anpassen können, finden Sie in der [Bereiten Sie die Zuordnungsdatei für die InDesign zu DITA-Migration vor.](appendix.md#id194AF0003HT) Abschnitt in *Anhang*.

1. Speichern Sie die Datei `idml2dita_io.xml`.

1. Nach dem Konfigurieren der erforderlichen Parameter in der `idml2dita_io.xml` -Datei, melden Sie sich bei AEM an und öffnen Sie die Assets-Benutzeroberfläche.

1. Navigieren Sie zum Eingabeordnerspeicherort \(`indesigntodita`\).

1. Laden Sie die Quelldokumente in diesen InDesign hoch. Informationen zum Hochladen von Inhalten in DAM finden Sie unter [Vorhandenen DITA-Inhalt hochladen](migrate-content-upload-existing-dita-content.md#).


## Migrieren von XHTML-Dokumenten {#id1949B04L0Y4}

Mit AEM Guides können Sie Ihre vorhandenen XHTML-Dokumente in DITA-Thementypdokumente konvertieren. Sie müssen die Eingabe- und Ausgabeordnerspeicherorte zusammen mit anderen Parametern angeben und die Dokumente werden in das DITA-Format konvertiert. Es gibt zwei Methoden zum Konvertieren von strukturierten HTML-Dokumenten:

- Laden Sie alle Dokumente in den Eingabeordner hoch oder
- Erstellen Sie eine ZIP-Datei aller Dokumente zusammen mit den Mediendateien und laden Sie sie in den Eingabeordner hoch. Dieser Ansatz wird im Allgemeinen für eine Reihe von HTML-Dateien verwendet, die miteinander verknüpft sind, und es gibt ein Inhaltsverzeichnis \(index.html\). Die Datei index.html enthält Links zu allen HTML-Dateien im Satz.

Unabhängig davon, ob Sie alle Dateien einzeln oder gebündelt in einer ZIP-Datei hochladen, erstellt der Konvertierungsprozess eine Eins-zu-Eins-Zuordnung zwischen den HTML-Dateien und den resultierenden DITA-Dateien. Dies bedeutet im Wesentlichen, dass für jede HTML-Datei im Eingabeordner eine .dita-Datei erstellt wurde.

Folgende Punkte müssen beim Hochladen Ihrer Dokumente in eine ZIP-Datei berücksichtigt werden:

- Alle referenzierten Themen sollten in der ZIP-Datei platziert werden.

- Alle referenzierten Mediendateien sollten mithilfe des relativen Links in den Themendateien referenziert werden.

- Erstellen Sie eine Datei index.html und fügen Sie Links zu den Themen hinzu, die Sie im Inhaltsverzeichnis hinzufügen möchten. Diese Datei index.html wird zum Erstellen der DITA-Map-Datei verwendet. In der Datei &quot;index.html&quot;können Sie auch verschachtelte Themen erstellen, die wie im folgenden Codebeispiel gezeigt auflisten:

  ```XML
  <?xml version="1.0" encoding="UTF-8"?>
  <html
  xmlns="http://www.w3.org/1999/xhtml">
      <head>
          <title>Sample Index File</title>
      </head>
      <body>
          <h1>Sample Index</h1>
          <div class="content">
              <ul class="book">
                  <li class="topicref">
                      <a href="Topic1.html">Topic 1</a>
                      <ul class="book">
                          <li class="topicref">
                              <a href="Topic1-1.html">Topic 1.1</a>
                          </li>
                          <li class="topicref">
                              <a href="Topic1-2.html">Topic 1.2</a>
                          </li>
                      </ul>
                  </li>
                  <li class="topicref">
                      <a href="Topic2.html">Topic 2</a>
                  </li>
              </ul>
          </div>
      </body>
  </html>
  ```

  Beachten Sie Folgendes: `ul` -Tag muss `class` -Attribut auf `book`. Entsprechend wird jede `li` -Tag `class` muss auf `topicref`.

- Wenn Sie Inline-Stile verwenden, konvertieren Sie die Inline-Stile in CSS-basierte Stilklassen in Ihrer XHTML-Datei. Verwenden Sie dann die Stilattribut-Zuordnung, um diese klassen-basierten Stile in DITA zu konvertieren `outputclass` -Attribut in der konvertierten DITA-Datei.

  Beim Generieren der HTML- oder AEM Site-Ausgabe aus diesen DITA-Dateien wird die `outputclass` -Attribute können verwendet werden, um Stilklassen auf generierte HTML oder AEM Site anzuwenden, die mit Ihren Quell-HTML-Inhalten übereinstimmen.


Neben den Überlegungen zum Erstellen der ZIP-Datei muss Ihr XHTML-Dokument auch gut strukturiert sein. Ihr Dokument sollte beispielsweise über eine *Titel*, gefolgt von *Überschrift 1*, *Überschrift 2* usw. Jede Überschrift sollte einen Inhalt enthalten. Wenn Ihr Dokument nicht gut strukturiert ist, funktioniert der Migrationsprozess möglicherweise nicht wie erwartet.

Führen Sie die folgenden Schritte aus, um Ihr vorhandenes XHTML-Dokument in ein DITA-Thema zu konvertieren:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zur Standardkonfigurationsdatei, die unter folgendem Speicherort verfügbar ist:

   `/libs/fmdita/config/h2d_io.xml`

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Konfigurationsdatei im `apps` node:

   `/apps/fmdita/config/h2d_io.xml`

   Die `h2d_io.xml` -Datei enthält die folgenden konfigurierbaren Parameter:

   - Im `inputDir` -Element den Speicherort Ihres Eingabeordners angeben, in dem Ihre Quell-XHTML-Dokumente verfügbar sind. Wenn Ihre XHTML-Dokumente beispielsweise in einem Ordner mit dem Namen `xhtmltodita` in `projects` und geben Sie den Speicherort als Folgendes an: `/content/dam/projects/xhtmltodita/`

   - Im`outputDir` -Element den Speicherort Ihres Ausgabeordners angeben oder den Standardspeicherort für die Ausgabe beibehalten. Wenn der angegebene Ausgabeordner nicht in DAM vorhanden ist, erstellt der Konvertierungs-Workflow den Ausgabeordner.

   - Für `createRev` -Element angeben, ob eine neue Version des konvertierten DITA-Themas erstellt werden soll \(`true`\) oder nicht \(`false`\).

1. Speichern Sie die Datei `h2d_io.xml`.

1. Nach dem Konfigurieren der erforderlichen Parameter in der `h2d_io.xml` -Datei, melden Sie sich bei AEM an und öffnen Sie die Assets-Benutzeroberfläche.

1. *\(Optional\)* Sie können auch den Abschnitt zu den entsprechenden Links zu den konvertierten Dokumenten hinzufügen. Führen Sie die folgenden Schritte aus, um diese Funktion zu aktivieren:

   >[!NOTE]
   >
   > Standardmäßig wird der Abschnitt für zugehörige Links nicht in den konvertierten Dokumenten erstellt.

   1. Navigieren Sie zur Datei h2d.xsl im folgenden Verzeichnis:

      /libs/fmdita/html2dita/

   2. Suchen Sie nach dem folgenden Parameter:

      `<xsl:param name="generate-related-links" select="false()"/>`

   3. Setzen Sie den Wert des obigen Parameters auf `true()`.
   4. Speichern und schließen Sie die Datei.
1. Navigieren Sie zum Eingabeordnerspeicherort \(`xhtmltodita`\).

1. Laden Sie die XHTML-Quelldokumente in diesen Ordner hoch. Informationen zum Hochladen von Inhalten in DAM finden Sie unter [Vorhandenen DITA-Inhalt hochladen](migrate-content-upload-existing-dita-content.md#).


Verwenden der `<config> </config>` -Block, können Sie einen oder mehrere Konfigurationsblöcke für die Konvertierung definieren. Der Konvertierungs-Workflow wird ausgeführt und die endgültige Ausgabe in Form eines DITA-Themas wird an dem im Abschnitt `outputDir` -Element.

## Migrieren von unstrukturierten FrameMaker-Dokumenten {#id1949B050VUI}

Mit AEM Guides können Sie Ihre vorhandene unstrukturierte FrameMaker \(`.fm` und `.book`\) Dokumente in DITA-Dokumente. Der erste Schritt besteht darin, Stilzuordnungen mithilfe von FrameMaker zu erstellen und diese Einstellungen in einer .sts-Datei zu speichern. Wenn Sie als Nächstes benutzerdefiniertes DITA verwenden, können Sie Ihre benutzerdefinierten Elemente den Quell-FrameMaker-Formaten in der `ditaElems.xml` -Datei. Wenn Sie beispielsweise ein benutzerdefiniertes Element mit dem Namen `impnote` um alle wichtigen Hinweise zu bearbeiten, können Sie dieses benutzerdefinierte Element im `ditaElems.xml` -Datei. Sobald dieses benutzerdefinierte Element definiert wurde, lösen AEM Guides beim Konvertieren eines FrameMaker-Dokuments mit `impnote` -Element.

Wenn Sie zusätzliche Attribute mit Ihrem benutzerdefinierten oder gültigen DITA-Element angeben möchten, können Sie diese auch in der Datei style2attrMap.xml definieren. Sie können beispielsweise die `type` -Attribut mit dem Wert von `important` mit der `impnote` -Element. Diese zusätzlichen Informationen können in der Datei style2attrMap.xml angegeben werden.

Zusätzlich zur Angabe von

Gehen Sie wie folgt vor, um Ihre bestehenden unstrukturierten FrameMaker-Dokumente in das DITA-Format zu konvertieren:

1. Erstellen Sie Stilzuordnungen in FrameMaker und speichern Sie diese Einstellungen in einer .sts-Datei.

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Wenn Sie benutzerdefinierte DITA-Elemente haben, definieren Sie diese im `ditaElems.xml` -Datei verfügbar unter dem folgenden Speicherort:

   `/libs/fmdita/config/ditaElems.xml`

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Konfigurationsdatei im `apps` node:

   `/apps/fmdita/config/ditaElems.xml`

   Die `ditaElems.xml` -Datei enthält einen einzelnen konfigurierbaren Parameter:

   - Im `elem` den Namen des benutzerdefinierten Elements angeben, das Sie in Ihren konvertierten DITA-Dokumenten verwenden möchten. Dieses Element wird wie in den generierten DITA-Dokumenten übergeben.

1. Wenn Sie zusätzliche Attribute angeben möchten, definieren Sie diese im `style2attrMap.xml` -Datei verfügbar unter dem folgenden Speicherort:

   `/libs/fmdita/config/style2attrMap.xml`

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Konfigurationsdatei im `apps` node:

   `/apps/fmdita/config/style2attrMap.xml`

   Die `style2attrMap.xml` -Datei enthält die folgenden konfigurierbaren Parameter:

   - Im `fmStyle` -Parameter das Quellformat angeben, das im FrameMaker-Dokument verwendet wird, das Sie zuordnen möchten.

   - Im`ditaAttr` -Element das DITA-Attribut angeben, das Sie dem Quellformat zuordnen möchten.

   - Im `ditaVal` -Element den Wert für das zugeordnete Attribut angeben. Wenn Sie keinen Wert haben, können Sie diesen Eintrag leer lassen.

1. Speichern Sie die Datei `style2attrMap.xml`.

1. Nach dem Konfigurieren der erforderlichen Parameter in der `style2attrMap.xml` -Datei, melden Sie sich bei AEM an und öffnen Sie die Assets-Benutzeroberfläche.

1. Navigieren Sie zum FrameMaker-Dokument, das Sie konvertieren möchten, und klicken Sie darauf.

   Die DITA-Zuordnungskonsole wird mit der Liste der zum Generieren der Ausgabe verfügbaren Ausgabevorgaben angezeigt.

1. Wählen Sie das DITA-Ausgabeformat aus und konfigurieren Sie die erforderlichen Parameter.

   >[!NOTE]
   >
   > Sie müssen dieselbe Einstellungsdatei \(.sts\) verwenden, die Sie in FrameMaker erstellt haben. Geben Sie außerdem den Einstellungsnamen und den Zielpfad an.

1. Klicken Sie auf **Erzeugen** -Symbol, um den Prozess zur Generierung der Ausgabe zu starten.


Verwenden der `<attrMap> </attrMap>` -Block, können Sie einen oder mehrere Konfigurationsblöcke für die Konvertierung definieren. Abhängig vom Inhalt können Sie als konvertierte Dateien eine .dita-Datei und eine .ditamap-Datei verwenden.

## Migrieren anderer strukturierter Dokumente {#id1949B0590YK}

Mit AEM Guides können Sie Ihre vorhandenen strukturierten Dokumente in gültige DITA-Dokumente konvertieren. Sie müssen die Speicherorte für Eingabe- und Ausgabeordner, den Speicherort der Umwandlungsdatei, die Erweiterung, mit der die endgültige Ausgabe gespeichert wird, und angeben, ob eine neue Version des Dokuments erforderlich ist oder nicht.

Führen Sie die folgenden Schritte aus, um Ihre vorhandenen strukturierten Dokumente in das DITA-Format zu konvertieren:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zur Standardkonfigurationsdatei, die unter folgendem Speicherort verfügbar ist:

   `/libs/fmdita/config/XSLConfig.xml`

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Konfigurationsdatei im `apps` node:

   `/apps/fmdita/config/XSLConfig.xml`

   Die `XSLConfig.xml` -Datei enthält die folgenden konfigurierbaren Parameter:

   - Im `inputDir` -Element, geben Sie den Speicherort Ihres Eingabeordners an, in dem die strukturierten Quelldokumente verfügbar sind. Wenn Ihre strukturierten Dokumente beispielsweise in einem Ordner mit dem Namen `xsltodita` in `projects` und geben Sie den Speicherort als Folgendes an: `/content/dam/projects/xsltodita/`

   - Im`outputDir` -Element den Speicherort Ihres Ausgabeordners angeben oder den Standardspeicherort für die Ausgabe beibehalten. Wenn der angegebene Ausgabeordner nicht in DAM vorhanden ist, erstellt der Konvertierungs-Workflow den Ausgabeordner.

   - Im `xslFolder` -Element den Speicherort des Ordners angeben, in dem die XSL-Transformationsdateien gespeichert werden.

   - Im ``xslPath`` -Element den Speicherort der primären .XSL-Datei angeben, die zum Initiieren des Konvertierungsprozesses verwendet wird.

   - Im ``outputExt`` -Element die Dateierweiterungen der endgültigen Ausgabedatei angeben, die aus dem Transformationsstream erstellt wird.

   - Für `createRev` -Element angeben, ob eine neue Version des konvertierten DITA-Themas erstellt werden soll \(`true`\) oder nicht \(`false`\).

1. Speichern Sie die Datei `XSLConfig.xml`.

1. Nach dem Konfigurieren der erforderlichen Parameter in der `XSLConfig.xml` -Datei, melden Sie sich bei AEM an und öffnen Sie die Assets-Benutzeroberfläche.

1. Navigieren Sie zum Eingabeordnerspeicherort \(`xsltodita`\).

1. Laden Sie die strukturierten Quelldokumente in diesen Ordner hoch. Informationen zum Hochladen von Inhalten in DAM finden Sie unter [Vorhandenen DITA-Inhalt hochladen](migrate-content-upload-existing-dita-content.md#).


Verwenden der `<config> </config>` -Block, können Sie einen oder mehrere Konfigurationsblöcke für die Konvertierung definieren. Der Konvertierungs-Workflow wird ausgeführt und die endgültige Ausgabe in Form eines DITA-Themas wird an dem im Abschnitt `outputDir` -Element.

**Übergeordnetes Thema:**[ Migrieren vorhandener Inhalte](migrate-content.md)
