---
title: Anzeige von UUID-basierten Links konfigurieren
description: Erfahren Sie, wie Sie die Anzeige von UUID-basierten Links konfigurieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# Anzeige von UUID-basierten Links konfigurieren {#id2035G20M0QN}

Wenn Sie einen Link mit der Option Verweis einfügen oder Inhalt wiederverwenden im Web-Editor einfügen erstellen, wird der Link standardmäßig mit der UUID des referenzierten Inhalts erstellt. Die **Link** -Eigenschaft \(im Bereich Eigenschaften\) des referenzierten Inhalts kann so konfiguriert werden, dass der relative Dateipfad des referenzierten Inhalts oder der UUID angezeigt wird. Standardmäßig wird die UUID des referenzierten Inhalts im Bereich Eigenschaften angezeigt.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um den relativen Pfad oder die UUID des referenzierten Inhalts im Web Editor anzuzeigen:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.uuid` | Boolesch \(true/false\). Wenn Sie den relativen Pfad des verknüpften Inhalts anzeigen möchten, setzen Sie diese Eigenschaft auf &quot;false&quot;. <br> **Standardwert**: true |

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
