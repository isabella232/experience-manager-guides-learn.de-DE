---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version Oktober 2022
description: Neueste Version der Adobe Experience Manager-Handbücher as a Cloud Service
source-git-commit: f673d53a1f3c76e1089e0a0c633c402722f99d00
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 4%

---

# Neueste Version der Adobe Experience Manager-Handbücher as a Cloud Service

## Aktualisierung auf die neueste Version

Aktualisieren Sie Ihre aktuellen Adobe Experience Manager-Handbücher as a Cloud Service (später als *AEM as a Cloud Service Handbücher*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2022.10.183.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die neueste Version der as a Cloud Service AEM Guides zu aktualisieren.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guide as a Cloud Service vom Oktober 2022 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
|  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2022.10.0 | 2,7,13 | 2,7,13 | 2.3 | 2,3 |
|  |  |  |  |


## Neue Funktionen und Erweiterungen

AEM Guides as a Cloud Service bietet Verbesserungen und neue Funktionen der neuesten Version:


### Bereich &quot;Schnellgenerierung&quot;

Jetzt stellt AEM Guides die **Schnellgenerierung** -Bedienfeld, mit dem Sie schnell die Ausgabe für Vorgaben generieren und anzeigen können, die für Ihre DITA-Zuordnung erstellt wurden.

![Symbol &quot;Quick Generate&quot;](assets/quick-generate-icon.png)

Im **Schnellgenerierung** angezeigt, können Sie die Liste aller für Ihre DITA-Zuordnung erstellten Ausgabevorgaben sehen.

![Bereich &quot;Schnellgenerierung&quot;](assets/quick-generate-panel.png)

Wählen Sie eine oder mehrere Vorgaben aus und generieren Sie schnell die Ausgabe. Sie können auch die für die Vorgaben generierte Ausgabe schnell anzeigen. Bei der Generierung der Ausgabe wird eine Erfolgsmeldung angezeigt. Wenn die Generierung der Ausgabe fehlschlägt, wird eine Fehlermeldung angezeigt. Sie können auch das Fehlerprotokoll anzeigen, um die Details des Fehlers anzuzeigen, der im Generierungsprozess aufgetreten ist.


## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Native PDF | Fehler tritt beim Entfernen von Themen, die nur Ressourcen betreffen, aus der PDF-Ausgabe auf. (10554)
* Native PDF | Leere Keyrefs werden in der PDF-Ausgabe angezeigt. (10553)
* Native PDF | `navtitle` für `topichead` wird nicht geehrt. (10509)
* Native PDF | Unterstützung für Ad64 JDK-Versionen erforderlich. (10465)
* Native PDF | Frontmatter-Themen können nicht aus dem Inhaltsverzeichnis ausgeblendet werden. (10355)
* Native PDF | Beim Neustarten der Seitenzahl im Kapitel-Layout beginnt die Nummerierung zufällig am Ende des vorherigen Kapitels. (10154)
* Chrome-Browser | Beim Ziehen und Ablegen eines Elements aus der Benutzeroberfläche wird der Bildschirm leer. Beispielsweise beim Ziehen einer Bedingung aus dem Bedienfeld &quot;Bedingungen&quot;. (10524)
* Knoteneigenschaften werden nach dem Kopieren und Einfügen eines Assets entfernt. (10053)
* Beim Klicken  **Schließen** -Benutzer zu Assets umgeleitet wurden - das Erlebnis wurde korrigiert, um Benutzer zur AEM-Homepage zu leiten. (9654)
