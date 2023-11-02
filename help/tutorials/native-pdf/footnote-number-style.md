---
title: Native PDF-Veröffentlichungsfunktion | Verwenden benutzerdefinierter Stile in Fußnoten
description: Erfahren Sie, wie Sie Stile auf die Zahlen in Fußnoten anwenden.
exl-id: f1068f2f-2ace-4bdb-b5a4-46b03d4e43d6
source-git-commit: cb2aa028330c1e1b8b71e9e928d724cc0d87bf44
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# Anwenden von Stilen für Fußnoten


Fußnoten sind Notizen, die am unteren Rand einer Seite platziert werden und einen Kommentar zu einem bestimmten Teil des Textes enthalten oder darauf verweisen.

Jede Fußnote hat eine Fußnotenmarke am unteren Seitenrand, bei der es sich im Allgemeinen um eine Zahl oder ein Symbol wie ein Sternchen handelt. Innerhalb des Hauptinhalts erscheint dieselbe Fußnote-Markierung als Fußnotenaufruf und wird durch dieselbe Zahl oder dasselbe Symbol wie ein Hochgestellt angezeigt.




## Ändern des Stils von Fußnotenaufrufen und -markierungen

Sie können die Stile der Fußnotenaufrufe und -markierungen ändern und ihr Erscheinungsbild in der PDF-Ausgabe verwalten. Mithilfe dieser Stile können Sie die Fußnoten im Dokument schnell identifizieren.


**Beispiel 1**:

Verwenden Sie das angegebene Beispiel, um eine Klammer vor und nach dem Fußnotenaufruf und der -Markierung hinzuzufügen:

* Fügen Sie das Präfix &quot;(&quot;und das Suffix &quot;)&quot;mithilfe des Inhaltsattributs im `footnote-call` -Stil, der die Klammern um die Fußnotennummer im Themeninhalt hinzufügt.
* Fügen Sie das Präfix &quot;(&quot;und das Suffix &quot;)&quot;mithilfe des Inhaltsattributs im `footnote-marker` -Stil, der die Klammern um die Fußnotennummer am unteren Rand der Seite hinzufügt.

```css
...
.fn::footnote-call { 
content: "(" counter(footnote, decimal) ")"; 
} 

.fn::footnote-marker { 
content: "(" counter(footnote, decimal) ")"; 
} 

...
```



<img src="./assets/pdf-output-footer-numbers.png" alt="Fußzeile in PDF-Ausgabe" width="500" border="2px">

*Fügen Sie Klammern um den Fußnotenaufruf und die Fußnotenmarke hinzu.*

**Beispiel 2**:

Sie können den Fußnotenaufruf und die -Markierung auch mit einem Sternchen oder einem niedrigeren griechischen Zeichen anstelle einer Zahl kennzeichnen.


```css
.fn::footnote-call {
 content: counter(footnote, asterisks);
}
.fn::footnote-marker {
 content: counter(footnote, asterisks) " ";
}
```

In der Ausgabe können Sie Folgendes anzeigen:

<img src="./assets/footnote-number-2.png" alt="Fußzeile in PDF-Ausgabe" width="500" border="2px">

*Fügen Sie einem Fußnotenaufruf und einer -Markierung ein Sternchen hinzu.*

## Fußnotenaufruf ausblenden

Sie können auch einen Stil auf Fußnotenaufrufe mit bestimmten Attributen anwenden. Verwenden Sie beispielsweise den folgenden Stil, um eine Fußnote mit den IDs auszublenden: Der Fußnotenaufruf ist im Hauptinhalt ausgeblendet, die Fußnote-Markierung wird jedoch unten auf der Seite angezeigt.

```css
.fn[id]::footnote-call {
		display: none;
                        }
```

## Format des Fußnotenbereichs

Im Fußnotenbereich werden alle Fußnoten platziert, im Allgemeinen am Ende einer Seite. Sie können den Fußnotenbereich mit den Seitenlayouts oder CSS-Stilen formatieren.


### Seitenlayouts

Sie können die Seiteneigenschaften für Seitenlayouts verwenden, um den Fußnotenbereich in den verschiedenen Abschnitten in einem PDF-Dokument zu gestalten. Sie können beispielsweise die Ränder und Abstände des Fußnotenbereichs in einem Kapitel angeben. Sie können auch die Rahmenseite, den Stil, die Farbe, die Breite und den Radius ändern.

Erfahren Sie mehr über [Arbeiten mit den Seiteneigenschaften eines Seitenlayouts](./design-page-layout.md#page-props-page-layout).

### CSS-Stile

Sie können Stile anwenden und den Fußnotenbereich in einem PDF-Dokument formatieren. Sie können beispielsweise die Rahmenlänge, den Stil, die Farbe und die Breite ändern.

```css
	@page {
	  @footnote {
   		border-top-style: solid;
   		border-top-color: #FF0000;
   		border-top-width: 3px;
 		        }
	      }
```

## Die Nummerierung der Fußnoten neu starten

Standardmäßig werden die Fußnoten fortlaufend in einem Dokument nummeriert. Sie können jedoch Seitenlayouts oder CSS-Stile verwenden, um die Nummerierung von Fußnoten neu zu starten.


### Seitenlayouts

Sie können eine Zahl in den Seitenlayouts angeben, um die Fußnotennummerierung in den verschiedenen Abschnitten eines PDF-Dokuments neu zu starten. Wählen Sie beispielsweise eine Zahl aus dem **Nummerierung von neu starten** im Bereich &quot;Seiteneigenschaften&quot;ein, um die Fußnotennummerierung für jedes Kapitel neu zu starten.

### CSS-Stile

Verwenden Sie den folgenden Stil, um die Fußnotennummerierung auf jeder Seite der PDF-Ausgabe zurückzusetzen:

```css
@page
{
counter-reset: footnote
}
```

Daher werden die Fußnoten auf jeder Seite von 1 neu gestartet.

## Inline-Fußnoten anzeigen

Normalerweise wird jede Fußnote als Block oder beginnt in einer neuen Zeile. Sie können sie aber auch in eine Linie oder nebeneinander platzieren.

```css
.fn{
  	display: inline;
              }
```

## Stile auf Querverweise von Fußnoten anwenden

Sie können auch auf eine Fußnote verweisen und mehrmals in Ihrer PDF-Ausgabe auf dieselbe Fußnote verweisen. Auf diese Weise können Sie die gleiche Erwähnung oder ausführliche Notiz mehrmals im Dokument referenzieren, ohne dafür eine Fußnote zu erstellen.

Der folgende Screenshot zeigt beispielsweise, wie die gleiche Fußnote für alle Städte in der PDF-Ausgabe referenziert wird.
<img width="550" alt="Fußnotenreferenzen in einem PDF-Dokument" src="./assets/link-footnotes.png" border="2px">

*Fügen Sie den Querverweis auf eine Fußnote ein.*





Mithilfe von CSS-Stilen können Sie auch Querverweise auf Fußnoten formatieren. Sie können beispielsweise die Hintergrundfarbe der Querverweise ändern.

```css
    .xref-fn{
	background-color: red;
	}
```



