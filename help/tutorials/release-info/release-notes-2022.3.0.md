---
title: Versionshinweise für [!DNL AEM Guides], Version März 2022
description: März-Version [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: 885edbb5-dfe4-4bdc-bb66-0df64addb094
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 2%

---

# März-Version [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Aktualisierung auf die Version vom März

Aktuelles Upgrade durchführen [!DNL Adobe Experience Manager Guides] as a Cloud Service (später genannt) *[!DNL AEM Guides]as a Cloud Service*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2022.3.123.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die März-Version von zu aktualisieren. [!DNL AEM Guides] as a Cloud Service.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die von [!DNL AEM Guides] as a Cloud Service Version März 2022.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
|  |  |


### Sauerstoffanschluss

| [!DNL AEM Guides] Cloud-Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac |
| --- | --- | --- |
| 2022.3.0 | 2,4,0 | 2,4,0 |
|  |  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

## Neue Funktionen und Erweiterungen

### Neues Grundlinien-Dashboard

[!DNL AEM Guides] Die Version vom as a Cloud Service März bietet die Funktion &quot;Grundlinie&quot;im Web Editor. Sie können jetzt Grundlinien aus dem Web Editor erstellen und diese zum Veröffentlichen oder Übersetzen von Themen aus verschiedenen Versionen verwenden.

Hinweis: Für ein aktualisiertes System aktualisieren Sie bitte die neueste **ui_config.json** für das Ordnerprofil.

Verwenden Sie diese Funktion, um eine Grundlinie mit einer bestimmten Version der Themen zu erstellen, die an einem bestimmten Datum und zu einer bestimmten Uhrzeit verfügbar sind. Außerdem erhalten Sie die API-Unterstützung zum Erstellen oder Aktualisieren einer Grundlinie mit einem für eine Themenversion definierten Titel.

![Grundlegende Registerkarte](assets/baseline-manage.png)

Sie können die Dateien anhand von Dateinamen oder Dateispeicherort durchsuchen. Sie können auch die Themen filtern, die im Bearbeitungsfenster der Grundlinie angezeigt werden sollen, und sie nach bestimmten Spalten sortieren.

![Grundlegende Registerkarte](assets/baseline-filter.png)

Die Leistung für die Grundlagenerstellung wurde weiter verbessert. Der Prozess zum Erstellen von Grundlinien ist asynchron, sodass Sie andere Dateien im Web Editor weiter bearbeiten können, während die Grundlinie erstellt wird. Weitere Informationen finden Sie unter *Erstellen und Verwalten von Grundlinien im Web-Editor* im Benutzerhandbuch.

Hinweis: Die Registerkarte &quot;Grundlinie&quot;im Dashboard der Karte ist standardmäßig ausgeblendet. Ihr Administrator kann die Registerkarte &quot;Grundlinie&quot;im Dashboard der Landkarte aktivieren.

### Verbessertes Aktualisierungsverhalten des Web-Editors

Die folgenden Verbesserungen sind jetzt beim Aktualisierungsvorgang des Browsers im Web Editor verfügbar:

* Jetzt können Sie den Browser aktualisieren, während Sie Ihre Inhalte im Web Editor bearbeiten. Wenn Sie auf das Symbol für die Browseraktualisierung klicken, während mindestens eine Datei mit nicht gespeicherten Änderungen zur Bearbeitung geöffnet ist, werden Sie aufgefordert, Ihre Dateien zu speichern oder die Aktualisierungsaktion abzubrechen.

* Selbst beim Aktualisieren des Browsers bleiben die Ansichten des linken und des rechten Bedienfelds erhalten.

* Das aktive Thema oder die DITA-Zuordnung wird im Inhaltsbearbeitungsbereich erneut geöffnet.

### Verbesserungen bei der Veröffentlichung

Der Veröffentlichungsprozess wurde mit der März-Veröffentlichung von [!DNL AEM Guides] as a Cloud Service:

* Grundlinien wurden für die Metadaten AEM Site-Ausgabe berücksichtigt. Sie können die Eigenschaften einer Grundlinienversion auch als Metadaten verarbeiten. Wenn keine Grundlinie definiert ist, werden die Eigenschaften der neuesten Version als Metadaten verarbeitet.

* Die **Dateiname** und **DITA-OT-Befehlszeilenargumente** wurden für HTML5-, EPUB- und benutzerdefinierte Ausgabevorgaben hinzugefügt. Jetzt können Sie den Dateinamen angeben, mit dem Sie die Ausgabe speichern möchten. Sie können auch die zusätzlichen Argumente angeben, die DITA-OT beim Generieren der Ausgabe verarbeiten soll.

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Über die Autorenansicht des Webeditors können in einer Bookmap keine Vordergrund- und Hintergrundelemente hinzugefügt werden. (7652)
* Der Referenzbaum bricht nach dem Entfernen eines Themas und dem Ausführen eines Verschiebevorgangs ab. (8804)
* Beim Anzeigen des Inhalts nach dem Hochladen eines Assets wird eine Ausnahme empfangen. (3638)
* Fehler tritt auf, wenn Dateien, deren übergeordneter Ordner Sonderzeichen im Dateinamen enthält, in Sauerstoff geöffnet werden (mithilfe der **In Sauerstoff bearbeiten** Schaltfläche). (8918)
* Die **Im Repository suchen** -Option die DITA-Zuordnung im XML-Editor nicht lokalisiert und markiert. (8796)
* Beim Filtern werden die entsprechenden Ergebnisse nicht angezeigt, wenn dem Inhalt im XML-Editor mehrere Attribute hinzugefügt werden. (8795)
* Beim Hinzufügen eines Benutzers als Administrator im Ordnerprofil tritt ein Fehler auf, wenn die Benutzer-ID numerisch ist. (8908)

## Bekannte Probleme

Adobe hat das folgende bekannte Problem im [!DNL AEM Guides] as a Cloud Service März-Version.

* Wenn Sie Beschriftungen für direkte Verweise entfernen, werden die Beschriftungen auch aus indirekten Verweisen entfernt.

* Der aktualisierte Grundlinientitel kann nicht wiedergegeben werden, ohne das Grundlinien-Bedienfeld manuell zu aktualisieren.

* Die Versionsvorschaufunktion im Bedienfeld Versionsverlauf zeigt die Vorschau eines ausgewählten Themas nicht an.
