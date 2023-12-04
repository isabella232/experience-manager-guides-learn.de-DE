---
title: Native PDF | Konfigurieren des Knotenprozesses für die native PDF-Veröffentlichung
description: Erfahren Sie, wie Sie den Knotenprozess für die native PDF-Veröffentlichung konfigurieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# Konfigurieren des Knotenprozesses für die native PDF-Veröffentlichung

Die native PDF-Veröffentlichung startet einen separaten NodeJs-Prozess, um die im Veröffentlichungsprozess generierten Dateien in eine endgültige PDF zu konvertieren. Möglicherweise müssen Sie die Konfigurationen dieses Knotenprozesses anpassen, bei dem die native PDF-Veröffentlichung ausgeführt wird, um verschiedene Szenarien zu unterstützen. Um beispielsweise größere Workloads auszuführen, sollten Sie die maximale Heap-Größe erhöhen, die für den generierten NodeJs-Prozess verfügbar ist.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](../cs-install-guide/download-install-additional-config-override.md) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden (Eigenschaft-)Details an:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|---|---|
| `com.adobe.fmdita.config.ConfigManager` | `native.pdf.node.opts` | Zeichenfolgenwert zum Festlegen eines beliebigen Standards `NODE_OPTIONS`.<BR> Standardwert: &quot;&quot; |
