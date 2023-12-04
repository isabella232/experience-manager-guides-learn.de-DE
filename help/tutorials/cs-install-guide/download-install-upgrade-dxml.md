---
title: Upgrade AEM Handbücher
description: Erfahren Sie, wie Sie AEM aktualisieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Upgrade AEM Handbücher {#id213BD050YPH}

1. Greifen Sie auf das Git-Repository von Cloud Manager zu.

1. Aktualisieren Sie die Datei dox/dox.installer/pom.xml .

1. Aktualisieren Sie den Wert der Variable &quot;dox.version&quot;auf die von Adobe bereitgestellten Versionsdetails.

1. Übertragen Sie die Änderungen und führen Sie die Cloud Manager-Pipeline aus, um das aktualisierte Paket bereitzustellen.


>[!NOTE]
>
> Weitere Informationen zur Verwendung der CI/CD-Pipeline finden Sie unter [Verwenden der CI/CD-Pipeline in Adobe Cloud Manager](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/cloud-manager/use-the-cicd-pipeline-in-cloud-manager-for-aem.html).

## Löschen des Browser-Cache

Nach Abschluss des Aktualisierungsprozesses müssen alle Benutzer den Browser-Cache löschen, bevor die aktualisierte Version der AEM-Handbücher verwendet werden kann.

**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)
