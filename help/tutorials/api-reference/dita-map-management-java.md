---
title: Java-basierte APIs zum Arbeiten mit DITA-Maps
description: Erfahren Sie mehr über die Java-basierten APIs für die Verwendung mit DITA-Maps
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# Java-basierte APIs zum Arbeiten mit DITA-Maps {#id175UB30E05Z}

Mit den folgenden Java-basierten APIs können Sie in AEM Handbüchern mit DITA-Maps arbeiten. Diese APIs sind in Form eines Bundles verfügbar. Sie müssen dieses Bundle in Ihren Code aufnehmen, um diese APIs verwenden zu können.

Paketdetails:

- Gruppen-ID: **com.adobe.fmdita**

- Artefakt-ID: **api**

- Version: **3,2**

- Package: **com.adobe.fmdita.api.maps**

- Klassendetails:

  ```JAVA
  public class MapUtilities extends Object
  ```

  Die MapUtilities-Klasse enthält Methoden zum Abrufen von Metadateninformationen aus einer DITA-Map-Datei.


## DITA-Map mit abhängigen Elementen herunterladen

Die `zipMapWithDependents` erstellt eine ZIP-Datei, die eine DITA-Zuordnung zusammen mit allen abhängigen Elementen wie referenzierten Themen, Unterkarten, Bildern und DTDs enthält. Die ZIP-Datei für die DITA-Zuordnung wird basierend auf einer gegebenen Grundlinie erstellt.

Außerdem können Sie entweder dieselbe Struktur beibehalten \(über- und untergeordnete Ordner\) oder eine flache Dateistruktur in einem einzigen Ordner für alle abhängigen Dateien erstellen.

>[!IMPORTANT]
>
> Die API gibt eine Ausnahme aus und kann keine ZIP-Datei erstellen, wenn eine der abhängigen Dateien fehlt.

**Syntax**:

```JAVA
public static void zipMapWithDependents(Session session, 
                     String sourcePath, 
                     String baseline, 
                     OutputStream outputStream,
                     boolean flatFS) 
                     throws RepositoryException, IOException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`sourcePath`|Zeichenfolge|Pfad \(im AEM Repository\) der DITA-Map-Datei, die heruntergeladen werden muss.| |`outputStream`|java.io.OutputStream|Der Stream, in den die ZIP geschrieben werden soll.| |`baseline`|Zeichenfolge|Der Titel der Grundlinie, die zum Abrufen des versionierten Inhalts verwendet wird. <br> **Hinweis:** Beim Wert wird zwischen Groß- und Kleinschreibung unterschieden.| |flachFS|Boolesch|\(optional\) Wenn auf &quot;true&quot;gesetzt, wird eine flache Dateistruktur in der ZIP-Datei zurückgegeben. Wenn Ihre DITA-Zuordnung beispielsweise auf Inhalte in mehreren Ordnern verweist, werden alle referenzierten Dateien in einen einzigen Ordner abgerufen. Wenn es Dateien mit demselben Namen gibt, werden diese Dateien umbenannt, indem ein numerisches Suffix hinzugefügt wird. Alle Verweise \(in DITA-Zuordnung und Themen\) werden automatisch verarbeitet, da sie basierend auf dem neuen Speicherort der Dateien in der flachen Ordnerstruktur aktualisiert werden. Wenn der Wert auf &quot;false&quot;gesetzt ist, wird die Ordnerstruktur so beibehalten, wie es in der ZIP-Datei der Fall ist. Wenn sich die DITA-Zuordnung auf Dateien von mehreren Speicherorten bezieht, werden auch alle diese Speicherorte in der ZIP-Datei erstellt. Wenn Sie die ZIP-Datei wiederherstellen, wird die genaue Ordnerstruktur am Zielspeicherort erstellt. <br> Der Standardwert für diesen Parameter ist &quot;false&quot;|.

**Rückgabe**: Der Inhalt des ZIP wird in die `outputStream`.

**Ausnahme**: Threads ``javax.jcr.RepositoryException``, `java.io.IOException`.

## DITA-Map mit abhängigen Elementen herunterladen \(asynchron\)

Alternativ können Sie DITA-Map mit abhängigen Elementen im asynchronen Modus herunterladen. Dieser Ansatz ist für größere DITA-Maps nützlicher.

Die `zipMapWithDependents` erstellt eine ZIP-Datei, die eine DITA-Zuordnung zusammen mit allen abhängigen Elementen wie referenzierten Themen, Unterkarten, Bildern und DTDs enthält. Die ZIP-Datei für die DITA-Zuordnung wird basierend auf einer gegebenen Grundlinie erstellt.

Außerdem können Sie entweder dieselbe Struktur beibehalten \(über- und untergeordnete Ordner\) oder eine flache Dateistruktur in einem einzigen Ordner für alle abhängigen Dateien erstellen.

>[!NOTE]
>
> Dieser Knoten wird nach einiger Zeit basierend auf der Konfiguration output.history.purgetime (sofern definiert) automatisch gelöscht, oder 5 Tage als Standard.

**Syntax**:

```JAVA
public static CompletableFuture<Node> zipMapWithDependencies(Session session,
                     String sourcePath, 
                     String baseline, 
                     boolean flatFS) 
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`sourcePath`|Zeichenfolge|Pfad \(im AEM Repository\) der DITA-Map-Datei, die heruntergeladen werden muss.| |`baseline`|Zeichenfolge|Der Titel der Grundlinie, die zum Abrufen des versionierten Inhalts verwendet wird. <br> **Hinweis:** Beim Wert wird zwischen Groß- und Kleinschreibung unterschieden.| |flachFS|Boolesch|\(optional\) Wenn auf &quot;true&quot;gesetzt, wird eine flache Dateistruktur in der ZIP-Datei zurückgegeben. Wenn Ihre DITA-Zuordnung beispielsweise auf Inhalte in mehreren Ordnern verweist, werden alle referenzierten Dateien in einen einzigen Ordner abgerufen. Wenn es Dateien mit demselben Namen gibt, werden diese Dateien umbenannt, indem ein numerisches Suffix hinzugefügt wird. Alle Verweise \(in DITA-Zuordnung und Themen\) werden automatisch verarbeitet, da sie basierend auf dem neuen Speicherort der Dateien in der flachen Ordnerstruktur aktualisiert werden. Wenn der Wert auf &quot;false&quot;gesetzt ist, wird die Ordnerstruktur so beibehalten, wie es in der ZIP-Datei der Fall ist. Wenn sich die DITA-Zuordnung auf Dateien von mehreren Speicherorten bezieht, werden auch alle diese Speicherorte in der ZIP-Datei erstellt. Wenn Sie die ZIP-Datei wiederherstellen, wird die genaue Ordnerstruktur am Zielspeicherort erstellt.<br> Der Standardwert für diesen Parameter ist &quot;false&quot;|.

**Rückgabe**: Der Knoten der ZIP-Datei wird in die `CompletableFuture`-Klasse. Der Benutzer kann die asynchrone Verarbeitung fortsetzen und `.get()`-Methode der Zukunft, um den Thread zu blockieren, wenn der Knoten benötigt wird. Der zurückgegebene Wert kann auch mit einem Fehler enden, der mit `.exceptionally()` -Methode.

## Liste der Grundlinien abrufen

Die ``getBaselineList`` -Methode ruft eine Liste aller Grundlinien ab, die für eine bestimmte DITA-Zuordnung vorhanden sind.

**Syntax**:

```JAVA
public static List<HashMap<String,String>> getBaselineList( 
                  javax.jcr.Session session, 
                  String sourcePath)
                  throws javax.jcr.RepositoryException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`sourcePath`|Zeichenfolge|Pfad \(im AEM Repository\) der DITA-Map-Datei, für die die Grundlinien-Informationen abgerufen werden sollen.|

**Rückgabe**: Eine Liste von `HashMap` Objekte. Jeder `HashMap` -Objekt stellt eine Grundlinie dar und enthält den Namen und Titel der Grundlinie.

**Ausnahme**: Threads ``javax.jcr.RepositoryException``.

## Liste bedingter Vorgaben abrufen

Die ``getConditionalPresetList`` -Methode ruft eine Liste aller bedingten Vorgaben ab, die für eine bestimmte DITA-Zuordnung vorhanden sind.

**Syntax**:

```JAVA
public static List<HashMap<String,String>> getConditionalPresetList (
                  javax.jcr.Session session,
                  String sourcePath)
                  throws javax.jcr.RepositoryException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`sourcePath`|Zeichenfolge|Pfad \(im AEM Repository\) der DITA-Map-Datei, für die die bedingten Vorgabeninformationen abgerufen werden sollen.|

**Rückgabe**: Eine Liste von `HashMap` Objekte. Jeder `HashMap` -Objekt stellt eine bedingte Vorgabe dar und enthält den Namen und den Titel der bedingten Vorgabe.

**Ausnahme**: Threads ``javax.jcr.RepositoryException``.

## Abrufen der DITAVAL-Dateiinformationen für eine bedingte Vorgabe

Die ``getDitavalFromConditionalPreset`` -Methode ruft den Pfad der DITAVAL-Datei ab, der einer bedingten Vorgabe für eine bestimmte DITA-Zuordnung entspricht.

**Syntax**:

```JAVA
public static String getDitavalFromConditionalPreset
    (Session session,
    String sourcePath, 
    String cpName) throws RepositoryException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.| |`sourcePath`|String|Pfad \(im AEM Repository\) der DITA-Map-Datei, für die die DITAVAL-Datei abgerufen werden soll.| |`cpName`|Zeichenfolge|Name der bedingten Vorgabe in der DITA-Zuordnung, für die die DITAVAL-Datei abgerufen werden soll.|

**Rückgabe**: Der Pfad der DITAVAL-Datei, die der in der DITA-Map-Datei definierten bedingten Vorgabe entspricht.

## Abrufen aller Abhängigkeiten für einen Knoten

Die ``getAllDependencies`` -Methode gibt alle Abhängigkeiten eines angegebenen Knotens zurück.

**Syntax**:

```JAVA
public static List
<Node> getAllDependencies 
(Node rootNode) throws GuidesApiException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`rootNode`|javax.jcr.Node|Der Stammknoten, für den alle Abhängigkeiten abgerufen werden sollen.|

**Rückgabe**: Eine Knotenliste, die alle Abhängigkeiten des Stammknotens enthält.
