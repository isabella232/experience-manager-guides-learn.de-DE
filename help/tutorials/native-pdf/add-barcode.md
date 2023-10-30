---
title: Native PDF-Veröffentlichungsfunktion | Barcode hinzufügen
description: Erfahren Sie, wie Sie Barcodes hinzufügen.
source-git-commit: 31225583f45337b209f325174176b9a4199db648
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 2%

---

# Barcode zur PDF-Ausgabe hinzufügen

Barcodes sind nützlich, um Informationen einzuschließen, die einfach von Maschinen verarbeitet werden können. Ebenso werden QR-Codes für die Links verwendet, die Leser mit ihren Mobilgeräten öffnen können.

Dieses Tutorial hilft Ihnen, Barcodes über jeder Seite in der PDF-Ausgabe hinzuzufügen.

## Schritte zum Generieren eines Barcodes

Führen Sie die folgenden Schritte aus, um einen Barcode zu generieren:

### Hinzufügen einer Ressourcen-ID zur DITA-Zuordnung

Fügen Sie der DITA-Zuordnung ein Ressourcen-ID-Element hinzu. Die Ressourcen-ID dient als Haupteingabe zum Generieren des Barcodes.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "technicalContent/dtd/map.dtd">
<map id="GUID-3c330691-4dac-4020-904a-d2d6246aeeb1-en">
  <title>Barcode Sample</title>
  <topicmeta>
    <resourceid id="7a5bda1c-b1db-4fd8-8763-a731e2e8abba">
    </resourceid>
  </topicmeta>
  <topicref href="GUID-139f6c64-bea3-4f17-8b22-ee131557e249-en.dita" type="topic">
  </topicref>
</map>  
```

Sie können die Ressourcen-ID auch im Authoring-Modus bearbeiten.

<img src="./assets/barcode-map.png" alt="Beispielausgabe mit Barcode" width="700" border="2px solid blue">


### Hinzufügen eines Barcode-Platzhalters in der Vorlagenkopfzeile

Ändern Sie die `Common.plt` in der Datei **Allgemein** Vorlage , um einen Barcode nach dem Projekttitel hinzuzufügen.

```html
...
  <div data-region="header">
    <p class="chapter-header"><span data-field="project-title" data-format="default">Project Title</span> </p>
    <p><span class="barcode" data-field="metadata" data-format="default" data-subtype="//resourceid/@id">Resource ID (barcode)</span></p>
  </div>
} 
...
```


### CSS der Vorlage aktualisieren, um einen Barcode-Wert zu rendern

Ändern Sie die `content.css` -Datei, um einen Barcode während der PDF-Erstellung wiederzugeben. Es werden verschiedene Barcode-Typen wie &quot;qrcode&quot;und &quot;pdf417&quot;unterstützt.  Weitere Informationen finden Sie unter [Barcode-Typen](#barcode-types).



```css
...
.barcode {
  -ro-replacedelement: barcode;
  -ro-barcode-type: code128;
}
...
```

Nachdem Sie die vorherigen Schritte ausgeführt haben, können Sie die PDF-Ausgabe mit einem Barcode generieren.

Der folgende Screenshot zeigt einen Beispiel-Barcode in einer PDF-Ausgabe.

<img src="./assets/barcode-output-sample.png" alt="Beispielausgabe mit Barcode" width="700">


## Barcode-Typen {#barcode-types}

| Typ | CSS-Attribut | Zusätzliche Attribute |
| ------------------------------- | ----------------------- | -------------------------- |
| QR-Code | qrcode |                            |
| PDF417 | pdf417 |                            |
| DataMatrix | data-matrix |                            |
| Aztec Code | aztec-code |                            |
| Rastermatrix | grid-matrix |                            |
| Maxicode | maxicode mode-4 |                            |
| Micro QR | microqr |                            |
| Code 1 | code-one |                            |
| Codablock F | codablockf |                            |
| GS1 Databar Limited | datenbankgebunden |                            |
| GS1 Databar Omnidirektional | Datenbank omnidirektional |                            |
| EAN-13 | ean-13 |                            |
| GS1-128 (AN-128) | code128 | -ro-barcode-encoding: gs1; |
| ITF-14 | itf14 |                            |
| UPC-A | upc-a |                            |
| Code 128 | code128 |                            |
| Interleaved 2 von 5 | Code2of5 interleaved |                            |
| POSTNET | postnet |                            |
| Niederländische Post-Kixcode | kixcode |                            |
| Korea Post | korea-post |                            |
| Deutsche Post Leitcode | dp-leitcode |                            |
| Australia Post | auspost |                            |
| Logmars | logmars |                            |
| Pharmakovigilanz | Pharmakokinetik |                            |
| USPS OneCode (Intelligent Mail) | usps-onecode |                            |


