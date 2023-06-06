---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version April 2023
description: Version der Adobe Experience Manager-Handbücher as a Cloud Service vom April 2023
source-git-commit: 4bb9ce2690a2e76a5b2a93b65db7dd452e15d295
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Neue Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im April 2023

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version April 2023 der Adobe Experience Manager-Handbücher (später auch als *AEM as a Cloud Service Handbücher*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie in der [Versionshinweise](release-notes-2023.4.0.md) Artikel.

## Erweiterte Metadatenunterstützung beim PDF-Publishing

AEM Guides bieten jetzt erweiterte Unterstützung für die Metadaten, die den Metadaten in Ihrer PDF-Ausgabe zugeordnet sind. Die Metadatenoptionen enthalten Informationen über das Dokument und seinen Inhalt, wie den Namen des Autors, den Dokumenttitel, Schlüsselwörter, Copyright-Informationen und andere Datenfelder.

<img src="assets/pdf-metadata.png" alt=" native PDF-Metadaten">

Sie können eine XMP-Datei importieren und AEM Guides können die Informationen aus der Datei auswählen. Sie können die Metadatennamen und -werte auch über das Dropdown-Menü angeben. Sie können auch benutzerdefinierte Metadaten hinzufügen, indem Sie direkt in das Namensfeld eingeben.


## Verbessertes Bedienfeld für die Gliederungsansicht

AEM Handbücher bietet ein verbessertes Bedienfeld für die Gliederungsansicht, in dem Sie die hierarchische Ansicht der im Dokument verwendeten Elemente erhalten.

<img src="assets/select-element-content-outline-view_cs.png" alt=" native PDF-Metadaten">

Die Gliederung bietet die folgenden Verbesserungen:

* Das Dropdown-Menü &quot;Anzeigeoptionen&quot;wird über dem Bedienfeld &quot;Konturansicht&quot;angezeigt. Wenn ein Element über eine ID, ein Attribut und Text verfügt, können Sie diese aus der Dropdown-Liste auswählen, um sie zusammen mit dem Element anzuzeigen. Die Attribute, die im Bedienfeld &quot;Gliederung&quot;angezeigt werden können, werden durch die Einstellungen für die Anzeigenattribute bestimmt, die von Ihrem Administrator im **Editor-Einstellungen**.

* Mithilfe der Suchfunktion können Sie nach einem Element anhand seines Namens, seiner ID, seines Textes oder seines Attributwerts suchen.


## Microservice-basierte Veröffentlichung für AEM Handbücher as a Cloud Service

AEM Guides as a Cloud Service bietet die Möglichkeit, große Veröffentlichungsarbeitslasten gleichzeitig mit mikrodienstbasierter Veröffentlichung auszuführen und die branchenführende Server-lose Adobe I/O Runtime-Plattform zu nutzen.

Ab der April-Version können Sie mehrere Veröffentlichungsanforderungen gleichzeitig ausführen und mithilfe des Microservice-basierten nativen PDF-Publishing sehr effizient Bulk-PDF-Ausgaben generieren.
Weitere Informationen finden Sie unter [Neue mikrodienstbasierte Veröffentlichung für AEM Guides as a Cloud Service konfigurieren](../knowledge-base/publishing/configure-microservices.md).

