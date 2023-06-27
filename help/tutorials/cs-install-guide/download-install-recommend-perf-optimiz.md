---
title: Recommendations zur Leistungsoptimierung
description: Recommendations zur Leistungsoptimierung
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# Recommendations zur Leistungsoptimierung {#id213BD0JG0XA}

Beachten Sie bei der Leistungsoptimierung die folgenden Punkte:

- Informationen zur Optimierung von Inhalten und Indizierungsfunktionen finden Sie unter [Inhaltssuche und -indizierung optimieren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=de) in AEM Dokumentation.

- Patch Xerces Jar bei Verwendung von benutzerdefiniertem DITA-OT für die Veröffentlichung. Dies ist je nach Anwendungsfall eine obligatorische Konfiguration. Diese Änderung ist nur erforderlich, wenn Sie benutzerdefinierte DITA-OT für die Veröffentlichungsausgabe verwenden.

  *Erforderliche Konfiguration*: Ersetzen Sie die Xerces Jar-Datei in Ihrem benutzerdefinierten DITA-OT-Paket durch das im Lieferumfang enthaltene OOTB. Die Standarddatei OOTB xercesImpl-2.11.0.jar ist in der Datei /libs/fmdita/dita\_resources/DITA-OT.zip verfügbar. Stellen Sie sicher, dass Sie die Datei &quot;xercesImpl-2.11.0.jar&quot;so umbenennen, dass sie mit der alten Jar-Datei &quot;Xerces&quot;übereinstimmt, die ersetzt wird. Dies kann zur Laufzeit erfolgen.

  Diese Änderung reduziert die Veröffentlichungszeit und die Speicherauslastung beim Veröffentlichen von DITA-Maps mit einer großen Anzahl von Themen.


**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)

