---
title: Versionshinweise | Neue Funktionen in Adobe Experience Manager-Handbüchern, Version Juli 2023
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im Juli 2023.
source-git-commit: 7581085859785c5b8b597ecfeb7dbe58c7c9e2bc
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Neue Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im Juli 2023

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version Juli 2023 der Adobe Experience Manager-Handbücher (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](release-notes-2023.7.0.md).

## Herstellen einer Verbindung zu einer Datenquelle und Einfügen von Daten in Ihre Themen

Jetzt können Sie über vordefinierte Connectoren aus AEM Handbüchern schnell eine Verbindung zu Ihren Datenquellen herstellen. Durch die Verbindung mit einer Datenquelle können Sie Ihre Informationen mit der Quelle synchronisieren, und alle Aktualisierungen der Daten werden automatisch übernommen, was AEM Guides zu einem echten Content-Hub macht. Mit dieser Funktion sparen Sie Zeit und Mühe beim manuellen Hinzufügen oder Kopieren der Daten.

Jetzt können Sie mit AEM Guides die nativen Connectoren für JIRA- und SQL-Datenbanken (MySQL, PostgreSQL, SQL Server, SQLite) konfigurieren. Sie können auch andere Connectoren hinzufügen, indem sie die Standardschnittstellen erweitern.

Nach dem Hinzufügen können Sie die konfigurierten Connectoren anzeigen, die unter der **Data Sources** im Web Editor angezeigt.

![](assets/code-snippet-generator.png){width="300" align="left"}

Sie können einen Generator für Inhaltsfragmente erstellen, um die Daten aus einer verbundenen Datenquelle abzurufen. Anschließend können Sie die Daten in Ihre Themen einfügen und sie bearbeiten.

Nachdem Sie einen Inhaltsfragment-Generator erstellt haben, können Sie ihn wiederverwenden, um die Daten in ein beliebiges Thema einzufügen. Weitere Informationen finden Sie unter [Inhaltsfragment aus Ihrer Datenquelle einfügen](../user-guide/web-editor-content-snippet.md).



## Überprüfungsfenster zur Präsentation von Überprüfungsprojekten und der aktiven Prüfungsaufgaben

Jetzt AEM Guides machen Ihre Rezensionen nahtloser. Es stellt den Bereich &quot;Bewertungen&quot;im Web Editor bereit. Im Bedienfeld &quot;Überprüfungen&quot;werden alle Überprüfungsprojekte und die aktiven Prüfungsaufgaben innerhalb der Überprüfungsprojekte angezeigt, zu denen Sie gehören.

Als Autor können Sie mit dieser Funktion die Prüfungsaufgaben einfach öffnen, die Kommentare anzeigen und die Kommentare schnell in einer zentralen Ansicht bearbeiten.
![](assets/active-review-task-comments.png){width="800" align="left"}
Weitere Informationen finden Sie unter **Überprüfen** Funktionsbeschreibung innerhalb der [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.


## Verbesserungen bei der Zuordnungssammlung

Mit einer Map Collection können Sie mehrere Maps organisieren und sie im Stapel veröffentlichen. An der Zuordnungssammlung wurden viele neue Verbesserungen vorgenommen:

- Jetzt können Sie einer Zuordnungssammlung auch native PDF-Ausgabevorgaben hinzufügen und diese zum Generieren der PDF-Ausgabe verwenden.
- Sie können die von Ihrem Administrator erstellten globalen und Ordnerprofilvorgaben anzeigen und sie zum Generieren der PDF-Ausgabe verwenden.
- Jetzt können Sie nicht nur eine einzelne Vorgabe auswählen, sondern auch alle Ordnerprofilvorgaben für eine DITA-Zuordnung in einem Schritt aktivieren.
  ![](assets/edit-map-collection.png){width="800" align="left"}

Weitere Informationen finden Sie unter [Verwenden der Kartensammlung für die Ausgabegenerierung](../user-guide/generate-output-use-map-collection-output-generation.md).

## Möglichkeit zum Zugriff auf temporäre HTML-Dateien beim Generieren der nativen PDF-Ausgabe

Jetzt können Sie AEM Guides die temporären HTML-Dateien herunterladen, die beim Generieren der nativen PDF-Ausgabe erstellt wurden. Wählen Sie in den Ausgabevorgabeneinstellungen die Option zum Herunterladen der temporären Dateien aus.  AEM Guides können Sie dann die temporären Dateien herunterladen, die beim Generieren der Ausgabe mithilfe dieser Vorgabe erstellt wurden.

Diese Funktion ermöglicht bessere Einblicke in den Generierungsprozess mit Zugriff auf Zwischenstile und Layouts und hilft Ihnen, Ihre CSS-Stile gemäß Ihren Anforderungen zu korrigieren oder zu ändern.

![](assets/native-pdf-advanced-settings.png){width="800" align="left"}

Weitere Informationen finden Sie unter [Erstellen einer PDF-Ausgabevorgabe](../web-editor/native-pdf-web-editor.md#create-output-preset).

## Microservice-basierte Veröffentlichung zum Generieren von HTML5- und benutzerdefinierter Ausgabe

Mit dem neuen Publishing-Microservice können Sie große Veröffentlichungsarbeitslasten gleichzeitig auf AEM Handbüchern as a Cloud Service ausführen und die branchenführende Server-lose Adobe I/O Runtime-Plattform nutzen. Jetzt mit dem Microservice können Sie auch die HTML5 und die benutzerdefinierte Ausgabe generieren.
Sie können mehrere Veröffentlichungsanforderungen ausführen und eine verbesserte Leistung bei der Generierung dieser Ausgabeformate erzielen.
Weitere Informationen finden Sie unter [Konfigurieren der mikrodienstbasierten Veröffentlichung für AEM Guides as a Cloud Service](../knowledge-base/publishing/configure-microservices.md).

## Versionsdetails AEM Handbücher in den Informationen zu

Jetzt mit dem AEM **Info** Informationen können Sie auch die Versionsdetails der AEM Guides anzeigen. Sie können die aktuellen Versionsdetails im **Info** der **Hilfe** auf der AEM Navigationsseite.

![](assets/about-aem-help.png)(width=&quot;800&quot; align=&quot;left&quot;)