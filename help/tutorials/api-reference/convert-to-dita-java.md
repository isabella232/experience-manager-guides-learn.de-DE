---
title: Java-basierte APIs für Konversions-Workflow
description: Erfahren Sie mehr über die Java-basierten APIs für den Konvertierungs-Workflow
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Java-basierte APIs für Konversions-Workflow {#id175UB30E05Z}

Mit den folgenden Java-basierten APIs können Sie HTML- und Word-Dokumente in das DITA-Format konvertieren. Diese APIs sind in Form eines Bundles verfügbar. Sie müssen dieses Bundle in Ihren Code aufnehmen, um diese APIs verwenden zu können.

**Paketdetails**:

- Gruppen-ID: **com.adobe.fmdita**

- Artefakt-ID: **api**

- Version: **3,2**

- Package: **com.adobe.fmdita.api.conversion**

- Klassendetails:

  ```JAVA
  public class ConversionUtils extends Object
  ```

  Die **ConversionUtils** -Klasse enthält Methoden zum Konvertieren von HTML- und Word-Dokumenten in das DITA-Format.


## Konvertieren von HTML-Dokumenten

Die `convertHtmlToDita` -Methode konvertiert HTML-Dokumente in das DITA-Format.

**Syntax**:

```JAVA
public static void convertHtmlToDita(Session session, 
                  String inputFile, 
                  String destPath, 
                  boolean createRev) 
                  throws RepositoryException, WorkflowException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`inputFile`|String|Absoluter Pfad der HTML-Quelldateien im AEM Repository.| |`destPath`|Zeichenfolge|Absoluter Pfad des Zielorts, an dem die konvertierten DITA-Dateien gespeichert werden.| |`createRev`|Boolesch|Geben Sie an, ob eine Revision der Dateien erstellt wird \( `true`\) am angegebenen Ziel oder nicht \( `false`\). Dies wird nur berücksichtigt, wenn der Zielspeicherort eine vorhandene Version der konvertierten Dateien enthält.|

**Ausnahme**: Threads `RepositoryException`.

## Konvertieren von Word-Dokumenten

Die ``convertWordToDita`` -Methode konvertiert Word-Dokumente in das DITA-Format.

**Syntax**:

```JAVA
public static void convertWordToDita(Session session, 
                  String inputFile,
                  String destPath, 
                  String style2tagMap, 
                  boolean createRev) 
                  throws RepositoryException, WorkflowException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`inputFile`|String|Absoluter Pfad der Word-Quelldateien im AEM Repository.| |`destPath`|Zeichenfolge|Absoluter Pfad des Zielorts, an dem die konvertierten DITA-Dateien gespeichert werden.| |`style2tagMap`|Zeichenfolge|Absoluter Pfad der Stilzuordnungsdatei, die für die Konvertierung verwendet wird.| |`createRev`|Boolesch|Geben Sie an, ob eine Revision der Dateien erstellt wird \( `true`\) am angegebenen Ziel oder nicht \( `false`\). Dies wird nur berücksichtigt, wenn der Zielspeicherort eine vorhandene Version der konvertierten Dateien enthält.|

**Ausnahme**: Threads `RepositoryException`.
