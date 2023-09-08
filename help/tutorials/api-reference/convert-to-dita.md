---
title: REST-APIs für Konversions-Workflow
description: Erfahren Sie mehr über die REST-APIs für den Konversions-Workflow
source-git-commit: 8707acf3ba01b7488eea6597c434da73a901d037
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---


# REST-APIs für Konversions-Workflow {#id175UB30E05Z}

Mit den folgenden REST-APIs können Sie Word-, HTML- und InDesign-Dokumente in das DITA-Format konvertieren.

## Konvertieren von Word-Dokumenten

Eine GET, die Word-Dokumente in DITA-Format konvertiert.

**Anforderungs-URL**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/conversion

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |``operation``|String|Ja|Name des aufzurufenden Vorgangs. Der Wert dieses Parameters lautet ``word2dita``. <br> **Hinweis:** Beim Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden. | |`inputFile`|Zeichenfolge|Ja|Absoluter Pfad der Word-Quelldateien im AEM Repository.| |`destPath`|Zeichenfolge|Ja|Absoluter Pfad des Zielorts, an dem die konvertierten DITA-Dateien gespeichert werden.| |`createRev`|Boolesch|Ja|Geben Sie an, ob eine Revision der Dateien erstellt wird \( `true`\) am angegebenen Ziel oder nicht \( `false`\). Dies wird nur berücksichtigt, wenn der Zielspeicherort eine vorhandene Version der konvertierten Dateien enthält.| |`style2tagMap`|Zeichenfolge|Ja|Absoluter Pfad der Stilzuordnungsdatei, die für die Konvertierung verwendet wird.|

**Antwortwerte**: Gibt eine HTTP-Antwort 200 \(erfolgreich\) zurück.

## Konvertieren von HTML-Dokumenten

Eine GET-Methode, die HTML-Dokumente in das DITA-Format konvertiert.

**Anforderungs-URL**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/conversion

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`operation`|String|Ja|Name des aufzurufenden Vorgangs. Der Wert dieses Parameters lautet ``html2dita``. <br> **Hinweis:** Beim Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden.| |`inputFile`|String|Ja|Absoluter Pfad der HTML-Quelldateien im AEM Repository.| |`destPath`|Zeichenfolge|Ja|Absoluter Pfad des Zielorts, an dem die konvertierten DITA-Dateien gespeichert werden.| |`createRev`|Boolesch|Ja|Geben Sie an, ob eine Revision der Dateien erstellt wird \( `true`\) am angegebenen Ziel oder nicht \( `false`\). Dies wird nur berücksichtigt, wenn der Zielspeicherort eine vorhandene Version der konvertierten Dateien enthält.|

**Antwortwerte**: Gibt eine HTTP-Antwort 200 \(erfolgreich\) zurück.

## Konvertieren von InDesign-Dokumenten

Eine GET-Methode, die InDesign-Dokumente in das DITA-Format konvertiert.

**Anforderungs-URL**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/conversion

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |``operation``|String|Ja|Name des aufzurufenden Vorgangs. Der Wert dieses Parameters lautet ``idml2dita``. <br> **Hinweis:** Beim Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden.| |`inputFile`|String|Ja|Absoluter Pfad der InDesign-Quelldateien im AEM Repository.| |`destPath`|Zeichenfolge|Ja|Absoluter Pfad des Zielorts, an dem die konvertierten DITA-Dateien gespeichert werden.| |`createRev`|Boolesch|Ja|Geben Sie an, ob eine Revision der Dateien erstellt wird \( `true`\) am angegebenen Ziel oder nicht \( `false`\). Dies wird nur berücksichtigt, wenn der Zielspeicherort eine vorhandene Version der konvertierten Dateien enthält.|

**Antwortwerte**: Gibt eine HTTP-Antwort 200 \(erfolgreich\) zurück.

