---
title: Automatische Speicherung von Dateien im Web Editor konfigurieren
description: Erfahren Sie, wie Sie die automatische Speicherung von Dateien im Web Editor konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# Automatische Speicherung von Dateien im Web Editor konfigurieren {#id199CC0J0M5Z}

Eine der häufigsten Funktionen im browserbasierten Editor ist die Möglichkeit, Daten nach einem bestimmten Zeitraum zu speichern. Der Web Editor für AEM Guides unterstützt auch das automatische Speichern von Themen- und Zuordnungsdateien im angegebenen Zeitintervall. Wenn diese Funktion ausgelöst wird, wird die Arbeitskopie des Themas oder der Zuordnung gespeichert. Eine neue Version des Themas oder der Zuordnung wird nicht erstellt. Um eine neue Version zu erstellen, müssen Sie in der Symbolleiste des Web-Editors auf das Symbol Revision speichern klicken.

Die Funktion zum automatischen Speichern ist standardmäßig nicht aktiviert und Sie müssen sie mithilfe der Konfigurationsdatei aktivieren.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um das Zeitintervall für das automatische Speichern und automatische Speichern der Datei zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.autosave` | Boolesch \(true/false\).<br> **Standardwert**: false |
| `xmleditor.autosaveinterval` | Geben Sie das Zeitintervall in Sekunden an, um die Funktion zum automatischen Speichern Trigger. |

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
