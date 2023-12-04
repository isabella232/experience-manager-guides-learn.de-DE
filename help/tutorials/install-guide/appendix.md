---
title: Anhang
description: Erfahren Sie, wie Sie InDesign-Dateien für die Konvertierung vorbereiten.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '2851'
ht-degree: 0%

---

# Anhang {#id195AD0L60Y4}

## Vorbereiten von InDesign-Dateien für die Konvertierung {#id195DBF0045Z}

InDesign bietet Autoren eine Vielzahl von Funktionen zur Erstellung attraktiver und komplexer Dokumente. Häufig bedeutet dies, dass die verschiedenen Teile eines Dokuments visuell auf der Seite platziert werden, ohne dass versucht wird, einen Fluss zwischen diesen Textrahmen bereitzustellen. Wenn &quot;*Leserichtung*&#39; der Textrahmen nicht definiert ist, enthält die IDML-Datei Meldungen, die nicht in einer aussagekräftigen Reihenfolge angezeigt werden können. Das Endergebnis ist ein oder mehrere DITA-Themen mit Absätzen, Tabellen und Grafiken in zufälliger Reihenfolge.

Es ist zwar möglich, den DITA-Inhalt in einer vernünftigen Reihenfolge in einem DITA-Editor zu bearbeiten, es ist jedoch viel einfacher, die InDesign-Datei zu reparieren, bevor die IDML-Datei erstellt wird. Dies kann ohne Änderung des Erscheinungsbilds des Quelldokuments erfolgen. Sie hat auch den Vorteil, dass das Quelldokument durch die ordnungsgemäße Definition der Leserichtung zugänglich gemacht wird.

***Textrahmen ausblenden***

InDesign verwendet den Begriff *&quot;threading&quot;* für die Verknüpfung von einem Frame mit einem anderen. Weitere Informationen zum Übergeben von Textrahmen finden Sie unter *[Text ausblenden](https://helpx.adobe.com/in/indesign/using/threading-text.html)* Thema in der InDesign-Dokumentation.

***Überschneidende Frames***

Einige InDesign-Dokumente verwenden aus Layoutgründen überlappende Rahmen ohne Thread. Es kann sehr schwierig sein, diesen Inhalt in den Haupt-Thread zusammenzuführen. Die beste Option kann sein, das Ergebnis in der DITA-Umgebung zu bearbeiten.

***InDesign***

Jeder Thread-Ablauf von Inhalten in einem InDesign-Dokument wird als &quot;&quot;bezeichnet *Geschichte*&quot;. Um optimale Ergebnisse zu erzielen, wird empfohlen, die Anzahl der Meldungen zu begrenzen. Es gibt jedoch einige Teile Ihres Dokuments, die in der DITA-Ausgabe möglicherweise nicht benötigt werden. Seitenfußzeilen sind beispielsweise selten erforderlich, können jedoch in der Mitte eines Themas angezeigt werden, wenn sie nicht mit Vorsicht behandelt werden.

Die einfachste Möglichkeit, Text auszuschließen, der im Dokument nicht benötigt wird, besteht darin, ihm eine spezielle *Absatz-Tag* wird nur für unerwünschte Inhalte verwendet. Anstatt beispielsweise eine *\[Grundlegender Absatz\]* Erstellen Sie für die Fußzeile einen *Fußzeile* -Tag. Legen Sie dann in der MapStyle-Datei einfach die *Fußzeile* Absätze, die wie folgt entfernt werden sollen:

```XML
<paraRule style="Footer" local="0" refactor="drop">
   <attributeRules createID="false"/>
</paraRule>
```

***Mapping zu DITA-Doctypes***

Es ist wichtig, dass Ihr Quelldokument über mindestens einen Absatzstil oder ein Element verfügt, das bzw. das den Anfang eines Themas markieren kann. Für Dokumente wird häufig Folgendes verwendet *Überschrift1* als Name der Überschriften der obersten Ebene im Dokument. Anschließend können Sie eine Zuordnung von diesem Stil zu einem bestimmten DITA-Doctype erstellen. Wenn Ihr Dokument gut organisiert ist und die Verwendung *Überschrift1* ist konstant, dann erhalten Sie gute Ergebnisse.

***Mehrere DITA-Doctypes***

Wenn einige der *Überschrift1* -Absätze müssen in verschiedene DITA-Doctypes konvertiert und dann den Absatzstil im InDesign dupliziert werden. Geben Sie diesen Stilen einen leicht erkennbaren Namen wie *Überschrift1\_genTask* oder *Überschrift1\_Fehlerbehebung* gegebenenfalls. Richten Sie dann die Datei &quot;mapStyle&quot;wie unten gezeigt ein:

```XML
<doctypes>
   <doctypeParaRule style="Heading1" local="0" mapToDoctype="concept">
      <attributeRules createID="true"/>
   </doctypeParaRule>
   <doctypeParaRule style="Heading1_genTask" local="0" mapToDoctype=" generalTask">
      <attributeRules createID="true"/>
   </doctypeParaRule>
   <doctypeParaRule style="Heading1_troubleshooting" local="0"mapToDoctype=" troubleshooting">
      <attributeRules createID="true"/>
   </doctypeParaRule>
</doctypes>
```

***Strukturierte InDesign-Dokumente***

InDesign hat eine lockere Beziehung zu XML. Während ein Dokument eine XML-DTD enthalten kann und die Hauptgeschichte möglicherweise für diese DTD gültig ist, ist es auch möglich, hybride Dokumente zu erstellen, in denen ein Teil des Inhalts XML ist, aber keine DTD enthalten ist. Dies sind die unerwünschten Fälle für eine erfolgreiche Konvertierung in DITA. Wenn ein Dokument XML-Teile enthält, versuchen Sie, die Ausgabe in XML zu speichern und zu prüfen, ob die Ergebnisse akzeptabel sind. Andernfalls enthalten DITA-Inhalte auch ungültige Inhalte oder können vollständig fehlschlagen.

***Tabellenformatierung***

Die Konvertierung von InDesign-Tabellenformatierungsregeln in die entsprechende Tabellenformatierung in DITA ist ein komplexer Vorgang. Dies liegt an den umfangreichen Formatierungsfunktionen, die in den Quelldateien verfügbar sind, verglichen mit den grundlegenden Optionen, die vom Oasis \(CALS\)-Tabellenmodell bereitgestellt werden, das in DITA verwendet wird. Eine vertikale und horizontale Textausrichtung wird bereitgestellt und liefert ähnliche Ergebnisse, obwohl Rechtetext immer entsprechend der Textrichtung ausgerichtet ist, während InDesign die Option Linker Rechtshinweis und Rechtshinweis erlaubt.

Die Handhabung von Spalten- und Zeilentrennzeichen durch InDesign ist wiederum wesentlich leistungsfähiger als die grundlegenden Optionen des Oasis-Tabellenmodells. InDesign bietet vier Zellenrahmen: Rahmentyp \(solide oder Muster\), Rahmenstärke, Rahmenfarbe, Rahmenfarbe, Rahmentint, Rahmenlückenfarbe und Rahmenlückentint. Alle diese Elemente müssen den Rahmen rechts und unten in jeder Zelle (Einstiegselement\) zugeordnet werden, wobei die einzigen Optionen 0 oder 1 sind - Rahmen ausblenden oder Rahmen anzeigen.

Die Rahmenregelung in InDesign kann auf folgenden Ebenen angewendet werden:

- Tabellenstile
- Zellstile
- Lokale Überschreibungen für jede Zelle

Der InDesign zu DITA-Konvertierungsprozess wendet die Rahmenregel wie folgt an:

- Tabellenstile werden dem `colspec/@colsep` -Attribut für vertikale Regeln. Horizontale Regeln werden dem `row/@rowsep` -Attribut. Wenn der Rahmen nicht definiert ist, wird das Attribut in beiden Fällen nicht erstellt.
- Zellstile werden dem `entry/@colsep` und `entry/@rowsep` -Attribute. Diese Werte überschreiben alle von Tabellenformat abgeleiteten Begrenzungslinien.
- Lokale Überschreibungen wenden die Formatierung direkt auf die Zelle an und überschreiben Tabellenstile und Zellstile.

***Alternative Muster***

InDesign Tabellenstile ermöglichen es, dass Spalten- und Zellenausrichtung einem abwechselnden Muster folgen. Diese Funktion wird zwar für die Konvertierung unterstützt, die Ergebnisse sind jedoch nur dann offensichtlich, wenn eine Mustergruppe zugeordnet ist, um die Regel \(1\) anzuzeigen, und die andere Mustergruppe zugeordnet wird, um die Regel \(0\) auszublenden.

## Bereiten Sie die Zuordnungsdatei für die InDesign zu DITA-Migration vor. {#id194AF0003HT}

Für die korrekte DITA-Konvertierung ist eine Zuordnungsdatei erforderlich, die mit dem Inhalt des Quelldokuments übereinstimmt. Bei unstrukturierten InDesign-Dokumenten bedeutet dies, dass alle verfügbaren Absatzstile und Zeichenstile zugeordnet werden müssen. Bei XML-strukturierten InDesign-Dokumenten müssen alle Elemente in der zugehörigen DTD zugeordnet werden.

Die Zuordnungsdateien für unstrukturierte und strukturierte InDesign-Dokumente unterscheiden sich. Dies liegt an den komplexeren Verarbeitungsanforderungen für die Konvertierung von unstrukturierten Quellinhalten in DITA.

Nachfolgend finden Sie ein Beispiel für die Zuordnungsdatei:

```XML
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE styleMap SYSTEM "mapStyle.dtd">
<styleMap xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="mapStyle.xsd" >
   <doctypes>
      <mapDoctypeParaRule root="itpx:stories" mapToDoctype="map">
         <attributeRules createID="true">
            <addNew name="outputclass" value="map"/>
         </attributeRules>
      </mapDoctypeParaRule>
      <doctypeParaRule style="Heading 1" local="0" mapToDoctype="concept">
         <attributeRules createID="true"/>
      </doctypeParaRule>
      <doctypeParaRule style="Heading A" local="0" mapToDoctype="topic">
         <attributeRules createID="true"/>
      </doctypeParaRule>
   </doctypes>
   <wrappingRules>
      <wrap elements="li+" context="number" wrapper="ol">
         <attributeRules createID="true"/>
      </wrap>
      <wrap elements="li+" context="bullet" wrapper="ul">
         <attributeRules createID="true"/>
      </wrap>
   </wrappingRules>
   <paragraphStyleRules>
      <paraRule style="Heading 2" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Heading 3" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="List Paragraph" local="p[-|-|-|-|-|b|-|-]" context="bullet" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="List Paragraph" local="p[-|-|-|-|-|n|-|-]" context="number" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="List Paragraph" local="0" context="bullet" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Normal" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Normal" local="p[-|-|-|-|-|b|-|-]" context="bullet" mapTo="li">
         <attributeRules createID="true"/>
      </paraRule>
      <paraRule style="Title" local="0"  mapTo="p">
         <attributeRules createID="true"/>
      </paraRule>
   </paragraphStyleRules>
   <characterStyleRules>
      <charRule style="Bold" local="0" mapTo="b">
         <attributeRules createID="false"/>
      </charRule>
      <charRule style="Code" local="0" mapTo="codeph">
         <attributeRules createID="false"/>
      </charRule>
      <charRule style="[No character style]" local="c[Bold|-|-|-|-|-|-|-]" mapTo="b">
         <attributeRules createID="false"/>
      </charRule>
      <charRule style="[No character style]" local="c[Italic|-|-|-|-|-|-|-]" mapTo="i">
         <attributeRules createID="false"/>
      </charRule>
   </characterStyleRules>
</styleMap>
```

Die Zuordnungsdatei ist eine XML-Datei mit einer einfachen Struktur, die alle Quellabsatzstile und Zeichenstilcodes auflistet. Der Dateiinhalt wird nachfolgend erläutert:

**Stilzuordnung**

Im `styleMap` -Element können Sie zwei optionale Attribute angeben: `@map_date` und `@map_version` zur Aufzeichnung der Version der Zuordnungsdatei.

**Dokumenttyp**

Die `doctypes` -Element listet die unterstützten DITA-Mappings und Themenzuordnungen auf.

**Absatzregeln für Dokumenttypen zuordnen**

Die `mapDoctypeParaRule` -Element ist obligatorisch. Die Attribute dieses Elements dürfen nicht bearbeitet werden, da das Stammelement der Quell-XML immer dem Stamm der DITA-Map zugeordnet ist `map` -Element.

**Absatzregel für Dokumenttyp**

Die `doctypeParaRule` -Element ist obligatorisch. Dadurch kann der Konvertierungsprozess den Beginn eines neuen Themas identifizieren. Normalerweise wird die `@style` -Attribut allein verwendet wird, wobei `@local` auf 0 gesetzt. Wenn jedoch immer lokale Formatierungsüberschreibungen für den ausgewählten Stil vorhanden sind, müssen Sie eine Regel für jeden Stil und dessen lokale Überschreibungen hinzufügen. Dies ist in der generierten Mapping-Datei einfach zu erkennen, wo dies oder Ähnliches gefunden werden könnte:

```XML
<paraRule style="Heading 1" local="0" mapTo="p">
   <attributeRules createID="true"/>
</paraRule>
<paraRule style="Heading 1" local="p[Italic|-|-|-|-|-|-|-]" mapTo="p">
   <attributeRules createID="true"/>
</paraRule>
```

Im obigen Beispiel gibt es zwei `paraRule` -Elemente für `@style` = &quot;Überschrift1&quot;. Erstellen Sie einfach eine Entsprechung `doctypeParaRule` -Elemente mit `@mapToDoctype` -Attribut nach Bedarf festlegen.

Die in der `doctypeParaRule` werden nachfolgend erläutert:

- `@style`: Der Name eines Stils im Quelldokument-InDesign.
- `@local`: Siehe [\#id194CG0V005Z](#id194CG0V005Z).
- `@mapToDoctype`: Der Name eines DITA-Thementyps aus einer nummerierten Liste aller gültigen `doctypes`.

**Element-Umbruchregeln**

Die Elementumbruchregeln definieren die Möglichkeiten, Elemente im eingehenden Dokument gemäß einem Satz von Attributwerten in ein vordefiniertes Element einzuschließen oder zu verschieben.

***`wrap`element***

Dies ist ein optionales Element. Die `wrap` -Element listet die Elemente auf, die umschlossen oder verschoben werden. Umbruch wird normalerweise verwendet, wenn einer Reihe von Elementen ein gemeinsames übergeordnetes Element zugewiesen werden muss. Beispiel: mehrere `li` Elemente, die in eine `ol` -Element. Zusätzlich `wrap` kann für das Verschieben von Elementen verwendet werden, z. B. Titel für Zahlen und Tabellen.

Die in der `wrap` werden nachfolgend erläutert:

- `@element`: Ein Pluszeichen hinter einem Elementnamen zeigt an, dass alle benachbarten Elemente mit demselben Namen in das Element mit dem Namen im `@wrapper`-Attribut.
- `@wrapper`: Der Name des einschließenden Elements.
- `@context`: Bietet eine Möglichkeit, die Wrapper eines bestimmten Elements weiter einzugrenzen. Das folgende Beispiel zeigt eine Möglichkeit, eine Reihe von `li` Elemente in einer geordneten Liste `ol` oder eine ungeordnete Liste `ul` gemäß `@context` Wert \(der Kontext wird für die `paraRule` element\):

  ```XML
  <wrap elements="li+" context="number" wrapper="ol">
     <attributeRules createID="true"/>
  </wrap>
  <wrap elements="li+" context="bullet" wrapper="ul">
     <attributeRules createID="true"/>
  </wrap>
  ```


Das folgende Beispiel zeigt, wie Sie eine `fig` -Element aus einem `title` und `image` element:

- `@elements`: Die durch ein Komma getrennten Elemente werden in das Element mit dem Namen `@wrapper` -Attribut. Aufgrund der gängigen Praxis, Bildtitel unter das Bild aufzunehmen, wird der Titel der `title` -Element unmittelbar nach dem `image`.

  Die folgende Umbruchregel:

  ```XML
  <wrap elements="title, image" context="FigTitle" wrapper="fig">
     <attributeRules createID="true"/>
  </wrap>
  ```

  Konvertiert die folgende XML-Zwischendatei:

  ```XML
  <image href="Links/myImage.png" scale="59">
     <title>IDML2DITA workflow</title>
  ```

  In die folgende gültige DITA-Zielleistenstruktur:

  ```XML
  <fig id="id397504">
     <title>IDML2DITA workflow</title>
     <image href="Links/myImage.png" scale="59">
  </fig>
  ```

- `@wrapper`: Der Name des einschließenden Elements.
- `@context`: Bietet eine Möglichkeit, weiter zu verfeinern, wie ein bestimmtes Element umschlossen wird \(der Kontext wird im `paraRule` Element\).

Das folgende Beispiel zeigt, wie Sie eine `title` in `table`:

- `@elements`: Die `title` -Element, das sich entweder unmittelbar vor oder unmittelbar nach einer `table` wird in das Element mit dem Namen im `@wrapper` -Attribut. Ein XPath-Prädikat kann die Position des Titelelements als `[before]` oder `[after]`.

  Beispiel: Die folgende Umbruchregel:

  ```XML
  <wrap elements="title[before]" context="TableTitle" wrapper="table">
     <attributeRules createID="true"/>
  </wrap>
  ```

  Konvertiert die folgende XML-Zwischendatei:

  ```XML
  <title>IDML2DITA workflow</title>
  <table id="id289742" outputclass="BasicTable">
     <tgroup cols="2">
        <colspec colname="0" colwidth="0.7*">
           <colspec colname="1" colwidth="0.3*">
  ```

  In diese gültige DITA-Ziffernstruktur:

  ```XML
  <table id="id289742" outputclass="BasicTable">
     <title>IDML2DITA workflow</title>
     <tgroup cols="2">
        <colspec colname="0" colwidth="0.7*">
           <colspec colname="1" colwidth="0.3*">
  ```

- `@wrapper`: Der Name des einschließenden Elements.

- `@context`: Bietet eine Möglichkeit, weiter zu verfeinern, wie ein bestimmtes Element umschlossen wird \(der Kontext wird im `paraRule` Element\).


**Absatzstilregeln**

Die `<paragraphStyleRule>` -Elemente werden nachfolgend beschrieben:

***`paraRule`element***

Die `paraRule` -Element ist obligatorisch. Dadurch werden die Zuordnungsregeln für alle Absatzstile festgelegt. In einem InDesign-Dokument ist der gesamte Text in der Unterstruktur von Absatzstilen enthalten, selbst Absätze ohne Stil werden benannt `[No paragraph style]`. Die eckigen Klammern geben einen eingebauten InDesign-Stilnamen an.

>[!NOTE]
>
> Die eckigen Klammern geben einen integrierten InDesign-Stilnamen an.

Die in der `paraRule` werden nachfolgend erläutert:

- `@style`: Der Name eines Stils im Quelldokument-InDesign.
- `@local`: Siehe [\#id194CG0V005Z](#id194CG0V005Z).
- `@mapTo`: Der Name eines DITA-Zielelements.

- `@context`: Dieses Attribut wird verwendet, um eine Relation zu einer bestimmten **wrap** Regel, wenn mehr als eine Wrapper-Auswahl verfügbar ist. Beispiel: die `li` -Element kann entweder in ein `ol`oder `ul` -Element. Zur Identifizierung der verschiedenen Listentypen können Sie einen bestimmten Stilnamen oder die `@local` -Attribut, das Folgendes anzeigen kann:
   - `local="p[-|-|-|-|-|b|-|-]"` Bei dem`b`&quot; in Feld 6 bedeutet, dass ein Listenelement mit Aufzählungszeichen angezeigt wird. In diesem Fall `@context` zu &#39;`bullet`&quot;.
   - `local="p[-|-|-|-|-|n|-|-]"` Bei dem`n`&quot; in Feld 6 ein nummeriertes Listenelement. In diesem Fall `@context` zu &#39;`number`&quot;.

- `@commentOut`: Dieses Attribut ermöglicht das Umbrechen des Zielelements in XML-Kommentaren, sodass die Informationen nicht verloren gehen, sondern vom Benutzer manuell verarbeitet werden können. Dies ist nützlich, wenn der Quellinhalt nicht gezwungen werden kann, die DITA-Strukturregeln einzuhalten.

- `@refactor`: Dieses optionale Attribut hat zwei Werte:

- `unwrap`: Das übereinstimmende Element wird entfernt, während der Inhalt beibehalten wird.

- `drop`: Das übereinstimmende Element und alle zugehörigen Inhalte werden entfernt.


**Zeichenstilregeln**

Die `charRule` -Elemente werden nachfolgend beschrieben:

>[!NOTE]
>
> Es gibt keine Zuordnung für den integrierten Zeichenstil `[No character style]` when `local="0"`, da sie während der Vorverarbeitung entfernt werden.

***`charRule`element***

Dies ist ein optionales Element.

Dies sind die Zuordnungsregeln für alle Zeichenstile. In einem InDesign-Dokument ist der gesamte Text in untergeordneten Elementen von Zeichenstilen enthalten.

Die in der `charRule` werden nachfolgend erläutert:

- `@style`: Der Name eines Stils im Quelldokument-InDesign.
- `@local`: Siehe [\#id194CG0V005Z](#id194CG0V005Z).
- `@mapTo`: Der Name eines DITA-Zielelements.
- `@refactor`: Dieses optionale Attribut hat zwei Werte:
   - `unwrap`: Das übereinstimmende Element wird entfernt, während der Inhalt beibehalten wird.

   - `drop`: Das übereinstimmende Element und alle zugehörigen Inhalte werden entfernt.


**Attributregeln**

Dieses Element kann ein untergeordnetes Element der folgenden Elementkontexte sein:

- `mapDoctypeParaRule`
- `mapDoctypeElemRule`
- `doctypeParaRule`
- `doctypeElemRule`
- `paraRule`
- `charRule`
- `elementRule`

Attributregeln dienen dazu, die Attribute für die übereinstimmenden Elemente zu verwalten.

Je nach Kontext stehen die folgenden Attribute zur Verfügung: `attributeRules` element:

- `@createID`: Generiert eine eindeutige ID für die übereinstimmenden Elemente. Zulässige Werte `true` oder `false`. In allen Kontexten verfügbar.
- `@copyAll`: Kopiert alle Attribute nur aus dem XML-Quellinhalt für strukturierte Quelldateien. Zulässige Werte sind `true` oder `false`. Verfügbar für Kontexte `mapDoctypeParaRule`, `mapDoctypeElemRule`, `doctypeElemRule` und `elementRule`.


Die in der `attributeRules` werden nachfolgend erläutert:

>[!NOTE]
>
> Dieses Element kann mehrere untergeordnete Elemente enthalten.

- `addNew`: Fügt dem übereinstimmenden Element ein neues Attribut hinzu. Verfügbar für alle Kontexte. Es hat zwei Attribute:
   - `@name`: Muss ein offizieller XML-Name sein, vorzugsweise gültig für den DITA-Kontext.
   - `@value`: Kann Literaltext oder ein einfacher XPath-Ausdruck sein.
- `copyAtt`: Kopiert ein einzelnes Attribut in das Ziel, während es optional im Prozess umbenannt wird. Der Wert wird nicht geändert. Verfügbar für Kontexte `mapDoctypeParaRule`, `mapDoctypeElemRule`, `doctypeElemRule` und `elementRule`. Wenn dieses Element vorhanden ist, wird die `@copyAllAtts` wird angenommen, dass `false`. Es hat zwei Attribute:
   - `@name`: Muss der Name eines Attributs sein, das im XML-Quellelement vorhanden ist.
   - `@mapTo`: Muss ein offizieller XML-Name sein, vorzugsweise gültig für den DITA-Kontext.

**Lokale Formatierungscodes**

In jedem InDesign-Dokument ist es möglich, dass Absatzstile und Zeichenstile mehrere Hundert verschiedene Formatierungsüberschreibungen enthalten. Die meisten dieser Eigenschaften bieten keine nützliche Rolle im Konvertierungsprozess. Wir haben jedoch eine Reihe von Formatierungsfunktionen ermittelt, die sich auf die Semantik des Dokuments auswirken und den Konvertierungsprozess beeinflussen müssen.

Die `@local` -Attribute werden als spezielles, durch Trennzeichen getrenntes Format angezeigt, in dem acht Felder zusammen mit einem Präfix bereitgestellt werden, um die Art der Formatierung zu überschreiben. Die Felder für Formatierungscodes sind unten aufgeführt:

- Präfix **p** für die lokale Überschreibung im Para-Stil oder **c** für die lokale Überschreibung des Zeichenstils.
- **Schriftschnitt** , der den Familiennamen und Eigenschaften wie &quot;***Fett kondensiert Kursiv***&quot;.
- **Schriftgröße** in den Buchstaben.
- **Zeichenposition** für Hochgestellt oder Tiefgestellt.
- **under** für Unterstriche.
- **Strike** für Durchstreichung.
- **Listencode** um den Listentyp als Aufzählungszeichen oder Nummeriert zu kennzeichnen - nicht immer von InDesign verwendet.
- **Aufzählungscode** listet alle definierten Aufzählungstypen im Dokument auf.
- **Zahlencode** listet alle definierten Nummerierungsstile im Dokument auf.

Eine sorgfältige Verwendung dieser Funktion ermöglicht andernfalls verloren gegangene lokale Formatierung und kann dazu beitragen, die Qualität einer Übertragung von formatierten Inhalten in DITA zu verbessern. Dieses Beispiel kann so aufgelöst werden, dass es kursiv 16 pt Text in einer Liste mit Aufzählungszeichen bedeutet: `p[Italic|16|-|-|-|b|-|-]`.

**Strukturzuordnung**

Die Strukturzuordnungsdatei ähnelt der Stilzuordnungsdatei mit einer einfachen Struktur, die alle Quellelemente und relevanten Attributtypen auflistet. Zwei Attribute, `@map_date` und `@map_version` werden für die Aufzeichnung der Version der zu verwendenden Mapping-Datei bereitgestellt.

**Dokumenttyp**

Die `doctypes` -Element listet die unterstützten DITA-Mappings und Themenzuordnungen auf.

**Dokumenttyp-Elementregeln zuordnen**

Die `mapDoctypeElemRule` -Element ist obligatorisch. Die Attribute dieses Elements dürfen nicht bearbeitet werden, da das Stammelement der Quell-XML immer dem Stamm der DITA-Map zugeordnet ist `map` -Element.

**Element-Umbruchregeln**

**`elementRules`element** Hier werden alle Elemente aufgelistet.

**`elementRule`element** Die `elementRule` -Element ist obligatorisch. Dies sind die Zuordnungsregeln für alle Quellelemente. Während ein InDesign-Dokument unstrukturierte Stilelemente enthält, werden diese bei strukturierten Inhalten ignoriert, es sei denn, die ***Hybridmodus*** Die Verarbeitung ist aktiviert.

Die in der `elementRule` werden nachfolgend erläutert:

- `@elementName`: Der Name eines Elements im Quelldokument-InDesign.

- `@local`: Siehe [\#id194CG0V005Z](#id194CG0V005Z). \(Nur bei Hybriddokumenten nützlich\).

- `@mapTo`: Der Name eines DITA-Zielelements.

- `@refactor`: Dieses optionale Attribut hat zwei Werte:

   - `unwrap`: Das übereinstimmende Element wird entfernt, während der Inhalt beibehalten wird.

   - `drop`: Das übereinstimmende Element und alle zugehörigen Inhalte werden entfernt.

- `@context`: Dieses Attribut wird verwendet, um eine Verknüpfung zu einer bestimmten Wrapper-Regel herzustellen, wenn mehr als eine Wrapper-Auswahl verfügbar ist. Beispiel: die `li` -Element kann entweder in ein `ol`oder `ul` -Element.

- `@commentOut`: Dieses Attribut ermöglicht das Umbrechen des Zielelements in XML-Kommentaren, sodass die Informationen nicht verloren gehen, sondern vom Benutzer manuell verarbeitet werden können. Dies ist nützlich, wenn der Quellinhalt nicht gezwungen werden kann, die DITA-Strukturregeln einzuhalten.


## Fehlerbehebung AEM Handbücher

Nachdem Sie AEM Handbücher installiert und konfiguriert haben, können Sie die Probleme beheben.

## Validieren von Verweisen

Sie können die angegebenen Skripte ausführen, um die Verweise zu überprüfen. Diese Skripte können Ihnen dabei helfen, die fehlerhaften Verweise zu identifizieren und sie dann zu patchen oder zu beheben.

- `/bin/fmdita/validatebtree?operation=validate` - meldet fehlerhafte Inhaltsverweise, behebt sie jedoch nicht.
- `/bin/fmdita/validatebtree?operation=patch`- listet die fehlerhaften Inhaltsverweise auf und behebt oder behebt sie.

**Skript überprüfen**

Führen Sie die folgenden Schritte aus, um die Verweise mithilfe des im Produktpaket verfügbaren Überprüfungsskripts zu überprüfen:

1. Ausführen des Überprüfungsskripts \[`/bin/fmdita/validatebtree?operation=validate`\] , um zu überprüfen, ob neue fehlerhafte Verweise vorhanden sind.
1. Falls das Überprüfungsskript Fehler meldet, können Sie diese mithilfe des Patch-Skripts patchen.
1. Notieren Sie sich die unten aufgeführten Details und geben Sie sie bei Bedarf für Ihr Customer Success Team frei:
1. 
   - Von Überprüfungsskript gedruckte Protokolle
- Paket von &quot;`/content/fmdita/references`&quot;
- Alle anderen erforderlichen Details, je nach gemeldetem Szenario

**Patch script**

Führen Sie die folgenden Schritte aus, um fehlerhafte Verweise mithilfe des im Produktpaket verfügbaren Patch-Skripts zu patchen:

1. Ausführen des Patch-Skripts `[/bin/fmdita/validatebtree?operation=patch]` , um die fehlerhaften Verweise zu beheben. Die Ausführung des Skripts dauert einige Minuten und druckt die Protokolle im Laufe des Prozesses. Nach Abschluss der Ausführung wird &quot;`Done`&quot; am Ende.

   **Hinweis:* Es wird empfohlen, die Protokolle zu Referenzzwecken zu kopieren und zu speichern.

1. Nachdem das Patch-Skript erfolgreich ausgeführt wurde, können Sie die folgenden Prüfungen durchführen:
1. 
   - Überprüfen Sie den neuen Knoten &quot;`references_backup_<timestamp>"` wurde erstellt unter `/content/fmdita`
- Überprüfen, ob die Verweise korrigiert wurden

**Logger**

Sie können für diese Skriptausführung auch einen separaten Logger erstellen, wie im Folgenden beschrieben:

- Logger zur Klasse hinzufügen &quot;`adobe.fmdita.common.BTreeReferenceValidator`&quot;
- Legen Sie `DEBUG`

Die erstellte Protokolldatei zeichnet alle Informationen auf, die mit der Skriptausführung zusammenhängen, und ist nützlich für den Fall, dass bei der Browsersitzung ein Timeout auftritt, während das Skript vom Browser ausgelöst wird.
