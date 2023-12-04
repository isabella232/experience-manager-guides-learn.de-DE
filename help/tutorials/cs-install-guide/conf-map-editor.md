---
title: Festlegen des Erweiterten Map-Editors als Standard
description: Erfahren Sie, wie Sie den erweiterten Map-Editor als Standard festlegen.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Festlegen des Erweiterten Map-Editors als Standard {#id181AI0003PN}

AEM Guides verfügen über einen einfachen Map-Editor und einen erweiterten Map-Editor. Der Basic Map Editor bietet Ihnen alle notwendigen Funktionen zum Erstellen Ihrer Zuordnungsdatei. Der erweiterte Map-Editor ist wesentlich umfangreicher und im Web-Editor integriert. Mit dem erweiterten Map Editor können Autoren DITA-Zuordnungsdateien mit einer benutzerfreundlichen Benutzeroberfläche erstellen und bearbeiten.

Standardmäßig wird eine neue Zuordnungsdatei bei der Erstellung im Basic Map Editor geöffnet. Sie können dieses Verhalten ändern, indem Sie die Einstellung aktivieren, um den erweiterten Map-Editor standardmäßig zu öffnen.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um den Basic Map Editor zu aktivieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | ``fmdita.hide.oldmapeditor`` | Boolesch \(true/false\). Wenn Sie den erweiterten Map-Editor standardmäßig verwenden möchten, legen Sie diese Eigenschaft auf &quot;true&quot;fest.<br> **Standardwert**: false |

>[!NOTE]
>
> Wenn ein Autor eine Zuordnungsdatei erstellt und sie zur Bearbeitung öffnet, wird standardmäßig der Basic Map Editor gestartet. Wenn die Option &quot;Bearbeiten&quot;für eine Zuordnungsdatei aus der Assets-Benutzeroberfläche ausgewählt ist, wird sie auch im Basic Map Editor geöffnet.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
