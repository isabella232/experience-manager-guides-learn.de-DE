---
title: Recommendations zur Leistungsoptimierung
description: Recommendations zur Leistungsoptimierung
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Recommendations zur Leistungsoptimierung {#id213BD0JG0XA}

Beachten Sie bei der Leistungsoptimierung die folgenden Punkte:

- Informationen zur Optimierung von Inhalten und Indizierungsfunktionen finden Sie unter [Inhaltssuche und -indizierung optimieren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=de) in AEM Dokumentation.

- Patch Xerces Jar bei Verwendung von benutzerdefiniertem DITA-OT für die Veröffentlichung. Dies ist je nach Anwendungsfall eine obligatorische Konfiguration. Diese Änderung ist nur erforderlich, wenn Sie benutzerdefinierte DITA-OT für die Veröffentlichungsausgabe verwenden.

  *Erforderliche Konfiguration*: Ersetzen Sie die Xerces-JAR-Datei in Ihrem benutzerdefinierten DITA-OT-Paket durch die im Lieferumfang enthaltene OOTB. Die Standarddatei OOTB xercesImpl-2.11.0.jar ist in der Datei /libs/fmdita/dita\_resources/DITA-OT.zip verfügbar. Stellen Sie sicher, dass Sie die Datei &quot;xercesImpl-2.11.0.jar&quot;so umbenennen, dass sie mit der alten Jar-Datei &quot;Xerces&quot;übereinstimmt, die ersetzt wird. Dies kann zur Laufzeit erfolgen.

  Diese Änderung reduziert die Veröffentlichungszeit und die Speicherauslastung beim Veröffentlichen von DITA-Maps mit einer großen Anzahl von Themen.


**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)
