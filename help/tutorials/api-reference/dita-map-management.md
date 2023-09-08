---
title: REST-API für die Verwendung mit DITA-Maps
description: Erfahren Sie mehr über die REST-API für die Verwendung mit DITA-Maps
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# REST-API für die Verwendung mit DITA-Maps {#id175UB30E05Z}

Mit der folgenden REST-API können Sie in AEM Handbüchern mit DITA-Maps arbeiten.

## DITA-Map mit abhängigen Elementen herunterladen

Eine GET, die eine DITA-Zuordnung mit allen abhängigen Elementen wie referenzierten Themen, Unterkarten, Bildern und DTDs herunterlädt, die in der Zuordnung und den Themen verwendet werden.

**Anforderungs-URL**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/exportditamap

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`ditamap`|Zeichenfolge|Ja|Absoluter Pfad der DITA-Map-Datei im AEM Repository.| |`baseline`|Zeichenfolge|Ja|Der Titel der Grundlinie, die zum Abrufen des versionierten Inhalts verwendet wird. <br> **Hinweis:** Beim Wert wird zwischen Groß- und Kleinschreibung unterschieden. |

**Antwortwerte**: Eine ZIP-Datei, deren Inhalt in den Ausgabestream der Antwort geschrieben wird.

## Initiieren des Exports für DITA-Map mit abhängigen Elementen

Eine POST-Methode, die einen Export für eine DITA-Zuordnung mit allen abhängigen Elementen wie referenzierten Themen, Unterkarten, Bildern und DTDs initiiert, die in der Zuordnung und den Themen verwendet werden. Der Status kann später abgefragt werden und die Download-URL kann abgerufen werden, sobald sie fertig ist.

**Anforderungs-URL**: http:*//&lt;aem-guides-server>: &lt;port-number>/bin/dxml/async-export*

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`ditamap`|Zeichenfolge|Ja|Absoluter Pfad der DITA-Map-Datei im AEM Repository.| |`baseline`|String|Nein|Der Titel der Grundlinie, die zum Abrufen des versionierten Inhalts verwendet wird. <br> **Hinweis:** Beim Wert wird zwischen Groß- und Kleinschreibung unterschieden.| |`flatFS`|Boolesch|Nein|\(Optional\) Wenn auf &quot;true&quot;gesetzt, wird eine flache Dateistruktur in der ZIP-Datei zurückgegeben. Wenn Ihre DITA-Zuordnung beispielsweise auf Inhalte in mehreren Ordnern verweist, werden alle referenzierten Dateien in einen einzigen Ordner abgerufen. Wenn es Dateien mit demselben Namen gibt, werden diese Dateien umbenannt, indem ein numerisches Suffix hinzugefügt wird. Alle Verweise \(in DITA-Zuordnung und Themen\) werden automatisch verarbeitet, da sie basierend auf dem neuen Speicherort der Dateien in der flachen Ordnerstruktur aktualisiert werden. Wenn der Wert auf &quot;false&quot;gesetzt ist, wird die Ordnerstruktur so beibehalten, wie es in der ZIP-Datei der Fall ist. Wenn sich die DITA-Zuordnung auf Dateien von mehreren Speicherorten bezieht, werden auch alle diese Speicherorte in der ZIP-Datei erstellt. Wenn Sie die ZIP-Datei wiederherstellen, wird die genaue Ordnerstruktur am Zielspeicherort erstellt. <br> Der Standardwert für diesen Parameter ist &quot;false&quot;|.

**Antwortwerte**: |Element|Beschreibung| |—|—| |`status`|Der Rückgabestatus für den ausgeführten Vorgang. Die möglichen Optionen sind: GESTARTET, FEHLGESCHLAGEN, FORTSCHRITTE, ERFOLG, FEHLGESCHLAGEN, GELÖSCHT| |`jobId`|Die eindeutige ID des Auftrags. Kann später zur Statusabfrage verwendet werden.| |errorMessage|Die Fehlermeldung des Auftrags im Fall eines Fehlers \(wenn der Status FEHLGESCHLAGEN, FISSING oder GELÖSCHT ist\).| |`filePath`|Der Dateipfad der ZIP-Datei. Sie ist nur vorhanden, wenn der Auftrag abgeschlossen ist und der Status SUCCEED lautet. Dies kann zum Herunterladen der ZIP-Datei verwendet werden.|

## DITA-Map-Status des Abfrageexports

Eine GET-Methode, die den Exportstatus für eine DITA-Zuordnung mit allen zugehörigen Elementen abruft. Sie kann in einem Intervall abgerufen werden, wenn der Status STARTED oder INPROGRESS lautet, bis sie abgeschlossen ist \(erfolgreich oder mit einem Fehler\).

**Anforderungs-URL**: http:*//&lt;aem-guides-server>: &lt;port-number>/bin/dxml/async-export*

**Parameter**
|Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`jobId`|Zeichenfolge|Ja|Die Auftrags-ID, die abgerufen wird, wenn der Exportauftrag initiiert wird.|

**Antwortwerte**: |Element|Beschreibung| |—|—| |`status`|Der Status des Exportvorgangs. Die möglichen Optionen sind: GESTARTET, FEHLGESCHLAGEN, FORTSCHRITTE, ERFOLG, FEHLGESCHLAGEN, GELÖSCHT| |`jobId`|Die eindeutige ID des Auftrags. Kann später zur Statusabfrage verwendet werden.| |`errorMessage`|Die Fehlermeldung des Auftrags im Fall eines Fehlers \(wenn der Status FEHLGESCHLAGEN, FEHLGESCHLAGEN oder GELÖSCHT ist\).| |`filePath`|Der Dateipfad der ZIP-Datei. Sie ist nur vorhanden, wenn der Auftrag abgeschlossen ist und der Status SUCCEED lautet. Dies kann zum Herunterladen der ZIP-Datei verwendet werden.|

