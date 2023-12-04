---
title: Versionshinweise | Adobe Experience Manager Guides as a Cloud Service, Version April 2023
description: Version der Adobe Experience Manager-Handbücher as a Cloud Service vom April 2023
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service vom April 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version April 2023 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM as a Cloud Service Guides*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version von AEM Guides as a Cloud Service im April 2023](whats-new-2023.4.0.md).

## Aktualisierung auf die Version vom April 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der AEM Guides zu aktualisieren:

1. Sehen Sie sich den Git-Code des Cloud Service an und wechseln Sie zu der Verzweigung, die in der Cloud Service-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Service-Git-Codes auf 2023.4.249.
3. Nehmen Sie die Änderungen vor und führen Sie die Cloud Service-Pipeline aus, um auf die as a Cloud Service Version der AEM Guides vom April 2023 zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts (nur, wenn Sie eine Version vor der September-Version von AEM Guides as a Cloud Service verwenden)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungsebene zu suchen und zu ersetzen:

* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: http://&lt;_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service im April 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM-Handbücher für Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023,04,0 | Nicht kompatibel | 2022 oder höher |
| | | |


### Sauerstoffanschluss

| AEM-Handbücher für Cloud | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023,04,0 | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |  |  |



## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Native PDF | Das Veröffentlichen von Inhalten mit einer Ausgabeklasse mit Klammern() führt zum Einfrieren der Veröffentlichung. (11596)
* Problem tritt beim Verschieben (per Drag-and-Drop) anstelle eines vorhandenen Listenelements auf, bei dem &quot;Änderungen verfolgen&quot;aktiviert ist. (11570)
* Beim Verschieben (per Drag &amp; Drop) als neues Listenelement mit aktivierter Option Änderungen verfolgen tritt ein Problem auf. (11569)
* Einzug- oder Ausschlusslistenelemente funktionieren bei &quot;Änderungen verfolgen&quot;in nicht erwartungsgemäß. (11568)
* Wenn Sie Inhalte in einer Zeile mit aktivierter Option &quot;Änderungen verfolgen&quot;hinzufügen und die Option &quot;Änderungen verfolgen&quot;dann deaktivieren, wird dies nicht deaktiviert. (11567)
* Schwierigkeiten beim Ziehen und Ablegen eines Listenelements besteht darin, dass Text anstelle des Listenelements verschoben wird. (11566)
* Die abgeschlossene Überprüfung wird nicht im schreibgeschützten Modus geöffnet. (11387)
* Problem tritt bei AEM Site-Suche auf (funktioniert nicht über 2-3-Level-Knoten hinaus). (11352)
* Beim Authoring im Element, das grün (Änderungen verfolgen) angezeigt wird, wird der neue Inhalt als Verfolgungsänderung angezeigt, auch wenn die Verfolgungsänderung deaktiviert ist. (7021)

### Bekanntes Problem mit Problemumgehung

Adobe hat das folgende bekannte Problem für AEM Guides as a Cloud Service Version April 2023 identifiziert.

* Native PDF | Die alten Metadaten werden erst gefüllt, wenn die Ausgabevorgabe explizit geöffnet wurde.
