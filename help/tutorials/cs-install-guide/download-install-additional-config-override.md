---
title: Konfigurationsüberschreibungen
description: Erfahren Sie, wie Konfigurationsüberschreibungen
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Konfigurationsüberschreibungen {#id216IFC003XA}

Für Konfigurationsaktualisierungen sollte der folgende allgemeine Ansatz verwendet werden:

1. Greifen Sie auf das Git-Repository von Cloud Manager zu.

1. Erstellen Sie eine neue JSON-Datei am folgenden Speicherort:

   src/main/content/jcr\_root/apps/fmditaCustom/config/

1. Benennen Sie die Datei im folgenden Format:

   $\{PID\}.cfg.json

   Hier ist die PID die Prozess-ID der Konfiguration.

1. Fügen Sie Eigenschaften in der JSON-Datei im folgenden Format hinzu:

   ```
   {
      "aem.adminuname": "updatedUserjson",
      "valid.characters": "[-a-zA-Z0-9_@$]",
      "dita.serialization": true
   }
   ```

1. Übertragen Sie die Änderungen und führen Sie die Cloud Manager-Pipeline aus, um die aktualisierte Konfiguration bereitzustellen.


**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)

