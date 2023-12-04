---
title: Java-basierte API zum Erstellen und Aktivieren von Paketen
description: Informationen zur Java-basierten API zum Erstellen und Aktivieren von Paketen
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Java-basierte API zum Erstellen und Aktivieren von Paketen {#id175UB30E05Z}

Mit der folgenden Java-basierten API können Sie CRX-Pakete erstellen und aktivieren. Diese API ist in Form eines Bundles verfügbar. Sie müssen dieses Bundle in Ihren Code aufnehmen, um diese APIs verwenden zu können.

Paketdetails:

- Gruppen-ID: **com.adobe.fmdita**

- Artefakt-ID: **api**

- Version: **3,3**

- Package: **com.adobe.fmdita.api.crxactivate**

- Klassendetails:

  ```JAVA
  public class CRXActivator
  ```

  Die **`CRXActivator`** -Klasse enthält eine Methode zum Erstellen von CRX-Paketen und dessen Replikation auf der Veröffentlichungsinstanz.


## Packages erstellen und aktivieren

Die `activate` -Methode erstellt ein CRX-Paket auf der Autoreninstanz und repliziert es bei Bedarf auf der Veröffentlichungsinstanz. Es wird davon ausgegangen, dass die AEM Replikationsparameter bereits in der Autoreninstanz eingerichtet wurden. Diese Methode erstellt das CRX-Paket basierend auf einer Liste von Regeln, die als Eingabeparameter in einer JSON-Zeichenfolge bereitgestellt werden.
>[!NOTE]
>
> Während der Erstellung oder Aktivierung aufgetretene Fehler werden in die `outputstream`.

**Syntax**:

```JAVA
public static void activate
(
  String json, 
  OutputStream outputstream, 
  Session session
) 
throws GuidesApiException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`json`|Zeichenfolge|JSON-Zeichenfolge, die das zu erstellende CRX-Paket bestimmt. Verwenden Sie das folgende Format, um die JSON-Zeichenfolge zu erstellen: <br>- `activate`: Ist vom Typ Boolesch \(`true`/`false`\). Bestimmt, ob das in der Autoreninstanz erstellte CRX-Paket auf die Veröffentlichungsinstanz repliziert wird. <br> - `rules`: weist den Typ JSON-Array auf. Ein Array von JSON-Regeln, die nacheinander verarbeitet werden, um das CRX-Paket zu erstellen. <br> - `rootPath`: Ist vom Typ String. Der Basispfad, auf dem die Knoten-/Eigenschaftenabfragen ausgeführt werden. Wenn keine Knoten-/Eigenschaftenabfragen vorhanden sind, werden der Stammpfad und alle unter dem Stammpfad vorhandenen Knoten im CRX-Paket enthalten. <br> - `nodeQueries`: ist vom Typ Regex-Array. Ein Array von regulären Ausdrücken, die verwendet werden, um bestimmte Dateien unter dem Stammpfad einzuschließen. <br> - `propertyQueries`: weist den Typ JSON-Array auf. Ein Array von JSON-Objekten mit jedem JSON-Objekt, das aus einer XPath-Abfrage besteht, die auf dem Stammpfad ausgeführt werden soll, und dem Namen einer Eigenschaft, die in jedem JCR-Knoten vorhanden ist, nachdem die Abfrage ausgeführt wurde. Der Wert der Eigenschaft in jedem JCR-Knoten sollte ein Pfad oder ein Array von Pfaden sein. Die in dieser Eigenschaft vorhandenen Pfade werden dem CRX-Paket hinzugefügt.| |`outputstream`|java.io.OutputStream|Dies wird verwendet, um das Ergebnis verschiedener Phasen zu schreiben, z. B. die Ausführung von Abfragen, die Aufnahme von Dateien, die Erstellung von CRX-Paketen oder die Aktivierung. Jeder Fehler, der während des Erstellungs- oder Aktivierungsprozesses auftritt, wird in die `outputstream`. Dies ist für das Debugging nützlich.| |`session`|Zeichenfolge|Eine gültige JCR-Sitzung mit Aktivierungsberechtigung.|

**Ausnahme**: Threads ``java.io.IOException``.

**Beispiel**: Das folgende Beispiel zeigt, wie eine JSON-Abfrage erstellt wird:

```JSON
{
  "activate": true,
  "rules": [
    {
      "rootPath": "/content/dam/nested",
      "nodeQueries": [
        ".*\\.jpg",
        ".*\\.png",
        ".*\\.gif"        
      ]
    },
    {
      "rootPath": "/content/output/sites/hierarchy_ditamap"
    },
    {
      "rootPath": "/content/output/sites/hierarchy_ditamap",
      "propertyQueries": [
        {
          "query": "//*[@fileReference]",
          "property": "fileReference"
        }
      ]
    }
  ]
}
```

Die JSON-Beispielabfrage besteht aus den folgenden Regeln:

- Nur die Bilder .png, .jpg und .gif unter /content/dam/nested werden in das Paket aufgenommen.
- Alle Knoten unter /content/output/sites/hierarchy\_ditamap sind im Paket enthalten.
- Die in der `fileReference` -Eigenschaft von Knoten unter /content/output/sites/hierarchy\_ditamap im Paket enthalten.
