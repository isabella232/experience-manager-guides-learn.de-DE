---
title: Vorhandenen DITA-Inhalt hochladen
description: Erfahren Sie, wie Sie vorhandenen DITA-Inhalt hochladen
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '1200'
ht-degree: 0%

---


# Vorhandenen DITA-Inhalt hochladen {#id176FF000JUI}

Wahrscheinlich verfügen Sie über ein Repository mit vorhandenen DITA-Inhalten, das Sie mit AEM Guides verwenden möchten. Für solche vorhandenen Inhalte können Sie einen der folgenden Ansätze verwenden, um Ihre Inhalte stapelweise in das AEM-Repository hochzuladen.

## WebDAV-Tool verwenden

Wenn Sie Ihre Themen und Maps in einem anderen DITA-Editor erstellen, können Sie jedes WebDAV-Tool verwenden, um Ihre Dateien hochzuladen. Das in diesem Abschnitt beschriebene Verfahren verwendet WinSCP als WebDAV-Tool zum Hochladen von Inhalten.

Führen Sie die folgenden Schritte aus, um WinSCP zum Hochladen von Dateien zu verwenden:

1. Laden Sie WinSCP herunter und installieren Sie es auf Ihrem Computer.

1. Starten Sie die WinSCP-App.

   Das Dialogfeld Anmelden wird angezeigt.

1. Geben Sie im Dialogfeld &quot;Anmelden&quot;die Einstellung Neue Site an, indem Sie WebDAV als **Dateiprotokoll** und weitere Verbindungsdetails bereitstellen, z. B.:

   - die URL, unter der Ihr AEM gehostet wird,

   - die Portnummer \(Standard ist 4502\) und

   - den Benutzernamen und das Kennwort für den Zugriff auf Ihren AEM-Server.

1. Klicken Sie auf **Anmelden**.

   Bei erfolgreicher Verbindung sehen Sie den Inhalt von AEM Assets in der WinSCP-Benutzeroberfläche. Mithilfe des WinSCP-Datei-Explorers können Sie Inhalte einfach durchsuchen, erstellen, aktualisieren oder löschen.


## FrameMaker verwenden

Adobe FrameMaker verfügt über einen leistungsstarken AEM-Connector, mit dem Sie Ihre vorhandenen DITA- und anderen FrameMaker-Dokumente \(.book und .fm\) einfach in AEM hochladen können. Sie können verschiedene Funktionen zum Hochladen von Dateien verwenden, z. B. das Hochladen einer einzelnen Datei, das Hochladen eines vollständigen Ordners mit oder ohne Abhängigkeiten \(z. B. Inhaltsreferenzen, Querverweise und Grafiken\).

Führen Sie die folgenden Schritte aus, um den AEM Connector von FrameMaker zum Hochladen von Inhalten zu verwenden:

1. Starten Sie FrameMaker.

1. Öffnen Sie die **Verbindungs-Manager** angezeigt.

   ![](assets/fm-aem-connector.png){width="550" align="left"}

1. Geben Sie die folgenden Details ein, um eine Verbindung zum AEM-Repository herzustellen:

   - **Name**: Geben Sie einen beschreibenden Namen ein, um die Verbindung zu Ihrem AEM-Server zu identifizieren.
   - **Server**: Geben Sie die URL und die Portnummer Ihres AEM-Servers ein.

   - **Benutzername**/**Passwort**: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf den AEM-Server ein.

1. Klicken Sie auf **Verbinden**.

   Nachdem die Verbindung erfolgreich hergestellt wurde, werden Assets aus dem AEM Repository im Fenster Repository Manager angezeigt.

   ![](assets/fm-repo-manager.png){width="550" align="left"}

   Wenn Sie mit der rechten Maustaste auf eine beliebige Datei oder einen Ordner klicken, können Sie damit verbundene Vorgänge ausführen. Wenn Sie beispielsweise mit der rechten Maustaste auf einen Ordner klicken, erhalten Sie Optionen zum Hochladen einer Datei, zum Hochladen einer Datei mit Abhängigkeiten, zum Hochladen eines ganzen Ordners usw.


## Konfigurieren des UUID-Dateinamenmusters

Beim Importieren von Inhalt ist es nicht erforderlich, dass Ihre Dateinamen auf der UUID basieren. In einem System, das UUID-basierte Dateinamen verwendet, ist es obligatorisch, dass alle Dateien mit ihren UUIDs und nicht mit ihren ursprünglichen Dateinamen referenziert werden. Wenn eine importierte Datei keine UUID-basierten Dateinamen aufweist, können Sie das System so konfigurieren, dass eine UUID zu ihrer Dateieigenschaft hinzugefügt wird. Diese UUID wird dann verwendet, um solche Dateien zu referenzieren, bei denen die UUID nicht für die Benennung der Dateien verwendet wird.

Führen Sie die folgenden Schritte aus, um Dateinamen mit einem UUID-Muster zu vergleichen und UUID Dateien zuzuweisen, denen keine UUID zugewiesen ist:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf *com.adobe.fmdita.config.ConfigManager* Bundle.

1. Im **UUID-Dateinamenmuster** -Eigenschaft ein Muster angeben, um die Namen der importierten Datei zu überprüfen.

   Wenn eine Datei nicht dem angegebenen Muster entspricht, wird der Eigenschaft der Datei eine UUID hinzugefügt und alle Verweise auf die Datei werden mit der der Datei zugewiesenen UUID aktualisiert.

1. Klicken Sie auf **Speichern**.


## Hochladen von Inhalten mit UUID mithilfe eines WebDav-Tools {#id201MI0I04Y4}

Sie können eine der folgenden Methoden verwenden, um Ihre Inhalte mit UUID hochzuladen:

- Ziehen Sie Inhalte per Drag-and-Drop aus Ihrem lokalen System.
- Verwenden Sie die **Erstellen** \> **Dateien** Workflow über AEM Assets-Benutzeroberfläche.
- Verwenden Sie ein Tool wie WinSCP.

Wenn Sie ein Tool wie WinSCP verwenden, können Sie die Aktion definieren, die für eine duplizierte Datei ausgeführt werden soll, indem Sie die **Alte Datei mit derselben UUID in neuen Ordner verschieben** in der configMgr. Diese Option definiert, welche Aktion für eine Datei ausgeführt wird, die an einem anderen Speicherort im AEM-Repository verfügbar ist. Diese Einstellung ist im *com.adobe.fmdita.config.ConfigManager* Bundle in der configMgr.

Standardmäßig wird die **Alte Datei mit derselben UUID in neuen Ordner verschieben** aktiviert ist. Dies bedeutet, dass die hochgeladene Datei in einem anderen Ordner im Repository vorhanden ist, die vorhandene Datei an den aktuellen Speicherort verschoben und mit der hochgeladenen Datei überschrieben wird. Wenn Sie diese Option nicht auswählen, wird die Datei an ihrem vorhandenen Speicherort überschrieben.

**Zusätzliche Hinweise zum Arbeiten mit UUID-basierten Dateien**:

Beim Verschieben oder Kopieren von Inhalten im AEM-Repository müssen die folgenden Punkte berücksichtigt werden:

- Beim Kopieren einer oder mehrerer Dateien von einem Speicherort an einen anderen Speicherort wird für Dateien ohne UUID eine neue UUID generiert. Diese UUID wird den Metadaten der Datei hinzugefügt.

- Wenn eine Datei einen Konflikt oder ein Duplikat aufweist, wird ein eindeutiger Dateiname für die neue Datei generiert, die kopiert oder verschoben wird.

- Keine zwei Dateien können dieselbe UUID aufweisen. Allen neuen Dateien wird eine eindeutige UID zugewiesen.


Beim Verschieben oder Kopieren von Inhalten aus Ihrem lokalen System in das AEM-Repository müssen die folgenden Punkte berücksichtigt werden:

- Wenn eine Datei von zwei verschiedenen Benutzern gleichzeitig hochgeladen wird, überschreibt die später verarbeitete Datei die frühere Datei. Eine solche Praxis ist jedoch selten und sollte vermieden werden.

- Wenn Sie Inhalte aus dem AEM-Repository auschecken und Änderungen auf Ihrem lokalen System vornehmen, stellen Sie sicher, dass der Dateiname zum Zeitpunkt des Hochladens der Datei nicht geändert wird.


## Verwenden von curl-Befehlen

Sie können auch curl-Befehle verwenden, um einen Ordner in DAM zu erstellen, Dateien hochzuladen und Metadaten zum hochgeladenen Inhalt hinzuzufügen.

**Erstellen eines Ordners**

Führen Sie den folgenden Befehl aus, um einen Ordner in AEM Repository zu erstellen:

```curl
curl --user <username>:<password> --data jcr:primaryType=sling:Folder "<server folder path>"
```

Geben Sie die folgenden Parameter an, um einen Ordner zu erstellen:

- `<username>:<passowrd>`: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf das AEM-Repository an. Dieser Benutzer muss über die Berechtigung zur Ordnererstellung verfügen.

- `jcr:primaryType=sling:Folder`: Geben Sie diesen Parameter an *as is* , um eine Ressource vom Typ Ordner zu erstellen.

- `<server folder path>`: Vollständiger Ordnerpfad einschließlich des Namens des neuen Ordners, den Sie im AEM Repository erstellen möchten. Wenn Sie beispielsweise den Pfad als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides`, dann den Ordner `AEM-Guides` wird innerhalb der `projects` Ordner in DAM.


**Datei hochladen**

Führen Sie den folgenden Befehl aus, um eine Datei in das AEM-Repository hochzuladen:

```curl
curl --user <username>:<password> -T "<local file path>" "<server folder path>"
```

Geben Sie die folgenden Parameter an, um eine Datei hochzuladen:

- `<username>:<passowrd>`: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf das AEM-Repository an. Dieser Benutzer muss Schreibrechte für die `server folder path`.

- ``local file path``: Füllen Sie den Dateipfad auf Ihrem lokalen System aus, den Sie hochladen möchten.

- `<server folder path>`: Füllen Sie den Ordnerpfad auf dem AEM-Server aus, auf den Sie die Datei hochladen möchten.


**Hinzufügen von Metadaten**

Führen Sie den folgenden Befehl aus, um Metadaten zu einer Datei hinzuzufügen:

```curl
curl --user <username>:<password> -F<attribute name>=<value> <metadata node path>
```

Geben Sie die folgenden Parameter an, um Metadateninformationen hinzuzufügen:

- `<username>:<passowrd>`: Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf das AEM-Repository an. Dieser Benutzer muss Schreibrechte für die ``metadata node path``.

- ``-F<attribute name>=<value>``: Die `<attribute name>` ist der Name des Metadatenattributs, z. B. `audience` und `<value>` könnte `internal`. Sie können mehrere Attributname-Wert-Paare, getrennt durch Leerzeichen, angeben.

- `<metadata node path>`: Vollständiger Ordnerpfad einschließlich Dateiname und Metadatenknoten. Wenn Sie beispielsweise den Pfad als `http://192.168.1.1:4502/content/dam/projects/AEM-Guides/intro.xml/jcr:content/metadata`festgelegt ist, werden die angegebenen Metadateninformationen auf `intro.xml` -Datei.


**Übergeordnetes Thema:**[ Migrieren vorhandener Inhalte](migrate-content.md)

