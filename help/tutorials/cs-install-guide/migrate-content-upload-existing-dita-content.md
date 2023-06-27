---
title: Vorhandenen DITA-Inhalt hochladen
description: Erfahren Sie, wie Sie vorhandenen DITA-Inhalt hochladen
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 1%

---


# Vorhandenen DITA-Inhalt hochladen {#id176FF000JUI}

Wahrscheinlich verfügen Sie über ein Repository mit vorhandenen DITA-Inhalten, das Sie mit den AEM Guides verwenden möchten. Für solche vorhandenen Inhalte können Sie eine der unterstützten Methoden verwenden, die unter [Hinzufügen digitaler Assets zu Adobe Experience Manager as a Cloud Service Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html).

## Konfigurieren des UUID-Dateinamenmusters

Beim Importieren von Inhalt ist es nicht erforderlich, dass Ihre Dateinamen auf der UUID basieren. In einem System, das UUID-basierte Dateinamen verwendet, ist es obligatorisch, dass alle Dateien mit ihren UUIDs und nicht mit ihren ursprünglichen Dateinamen referenziert werden. Wenn eine importierte Datei keine UUID-basierten Dateinamen aufweist, können Sie das System so konfigurieren, dass eine UUID zu ihrer Dateieigenschaft hinzugefügt wird. Diese UUID wird dann verwendet, um solche Dateien zu referenzieren, bei denen die UUID nicht für die Benennung der Dateien verwendet wird.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(property\) Details an, um das UUID-Dateinamenmuster zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `uuid.regex` | Zeichenfolge, die das Regex für das UUID-Dateinamenmuster angibt. <br> Wenn eine Datei nicht dem angegebenen Muster entspricht, wird der Eigenschaft der Datei eine UUID hinzugefügt und alle Verweise auf die Datei werden mit der der Datei zugewiesenen UUID aktualisiert. <br> **Standardwert**: `"^GUID-(?<id>.*)"` |

## Verwenden von curl-Befehlen

Sie können auch curl-Befehle verwenden, um einen Ordner in DAM zu erstellen, Dateien hochzuladen und Metadaten zum hochgeladenen Inhalt hinzuzufügen.

**Erstellen eines Ordners**

Führen Sie den folgenden Befehl aus, um einen Ordner in AEM Repository zu erstellen:

```
curl --user <username>:<password> --data jcr:primaryType=sling:Folder "<server folder path>"
```

Geben Sie die folgenden Parameter an, um einen Ordner zu erstellen:

- `<username>:<passowrd>`: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf das AEM-Repository an. Dieser Benutzer muss über die Berechtigung zur Ordnererstellung verfügen.

- `jcr:primaryType=sling:Folder`: Geben Sie diesen Parameter an *as is* , um eine Ressource vom Typ Ordner zu erstellen.

- `<server folder path>`: Vollständiger Ordnerpfad einschließlich des Namens des neuen Ordners, den Sie im AEM Repository erstellen möchten. Wenn Sie beispielsweise den Pfad als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides`, dann den Ordner `AEM-Guides` wird innerhalb der `projects` Ordner in DAM.


**Datei hochladen**

Führen Sie den folgenden Befehl aus, um eine Datei in das AEM-Repository hochzuladen:

```
curl --user <username>:<password> -T "<local file path>" "<server folder path>"
```

Geben Sie die folgenden Parameter an, um eine Datei hochzuladen:

- `<username>:<passowrd>`: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf das AEM-Repository an. Dieser Benutzer muss Schreibrechte für die `server folder path`.

- ``local file path``: Füllen Sie den Dateipfad auf Ihrem lokalen System aus, den Sie hochladen möchten.

- `<server folder path>`: Füllen Sie den Ordnerpfad auf dem AEM-Server aus, auf den Sie die Datei hochladen möchten.


**Hinzufügen von Metadaten**

Führen Sie den folgenden Befehl aus, um Metadaten zu einer Datei hinzuzufügen:

```
curl --user <username>:<password> -F<attribute name>=<value> <metadata node path>
```

Geben Sie die folgenden Parameter an, um Metadateninformationen hinzuzufügen:

- `<username>:<passowrd>`: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf das AEM-Repository an. Dieser Benutzer muss Schreibrechte für die ``metadata node path``.

- ``-F<attribute name>=<value>``: Die `<attribute name>` ist der Name des Metadatenattributs, z. B. `audience` und `<value>` könnte `internal`. Sie können mehrere Attributname-Wert-Paare, getrennt durch Leerzeichen, angeben.

- `<metadata node path>`: Vollständiger Ordnerpfad einschließlich Dateiname und Metadatenknoten. Wenn Sie beispielsweise den Pfad als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides/intro.xml/jcr:content/metadata`festgelegt ist, werden die angegebenen Metadateninformationen auf `intro.xml` -Datei.


**Übergeordnetes Thema:**[ Migrieren vorhandener Inhalte](migrate-content.md)

