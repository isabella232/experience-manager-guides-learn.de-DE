---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version April 2023
description: Neueste Version der Adobe Experience Manager-Handbücher as a Cloud Service
exl-id: 3b09f0b3-cfa4-422d-91b7-733ab1c1896c
source-git-commit: cf612da41f79b0bf9da4c4d7454a0e3c86af7a4c
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 2%

---

# April-Version der Adobe Experience Manager-Handbücher as a Cloud Service

## Aktualisierung auf die neueste Version

Aktualisieren Sie Ihre aktuellen Adobe Experience Manager-Handbücher as a Cloud Service (später als *AEM as a Cloud Service Handbücher*) einrichten, indem Sie die folgenden Schritte ausführen:

1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2023.4.249.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die neueste Version der as a Cloud Service AEM Guides zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts (nur, wenn Sie eine Version vor der September-Version von AEM Guides as a Cloud Service verwenden)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungsebene zu suchen und zu ersetzen:

* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service im April 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM zu Handbüchern as a Cloud - Version | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.04.0 | Nicht kompatibel | 2022 oder höher |
|  |  |  |


### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.04.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Neue Funktionen und Erweiterungen

AEM Guides as a Cloud Service bietet Verbesserungen und neue Funktionen der neuesten Version:

### Erweiterte Metadatenunterstützung beim PDF-Publishing

AEM Guides bieten jetzt erweiterte Unterstützung für die Metadaten, die den Metadaten in Ihrer PDF-Ausgabe zugeordnet sind. Die Metadatenoptionen enthalten Informationen über das Dokument und seinen Inhalt, wie den Namen des Autors, den Dokumenttitel, Schlüsselwörter, Copyright-Informationen und andere Datenfelder.

<img src="assets/pdf-metadata.png" alt=" native PDF-Metadaten">

Sie können eine XMP-Datei importieren und AEM Guides können die Informationen aus der Datei auswählen. Sie können die Metadatennamen und -werte auch über das Dropdown-Menü angeben. Sie können auch benutzerdefinierte Metadaten hinzufügen, indem Sie direkt in das Namensfeld eingeben.


### Verbessertes Bedienfeld für die Gliederungsansicht

AEM Handbücher bietet ein verbessertes Bedienfeld für die Gliederungsansicht, in dem Sie die hierarchische Ansicht der im Dokument verwendeten Elemente erhalten.

<img src="assets/select-element-content-outline-view_cs.png" alt=" native PDF-Metadaten">

Die Gliederung bietet die folgenden Verbesserungen:

* Das Dropdown-Menü &quot;Anzeigeoptionen&quot;wird über dem Bedienfeld &quot;Konturansicht&quot;angezeigt. Wenn ein Element über eine ID, ein Attribut und Text verfügt, können Sie diese aus der Dropdown-Liste auswählen, um sie zusammen mit dem Element anzuzeigen. Die Attribute, die im Bedienfeld &quot;Gliederung&quot;angezeigt werden können, werden durch die Einstellungen für die Anzeigenattribute bestimmt, die von Ihrem Administrator im **Editor-Einstellungen**.

* Mithilfe der Suchfunktion können Sie nach einem Element anhand seines Namens, seiner ID, seines Textes oder seines Attributwerts suchen.


### Microservice-basierte Veröffentlichung für AEM Handbücher as a Cloud Service

AEM Guides as a Cloud Service bietet die Möglichkeit, große Veröffentlichungsarbeitslasten gleichzeitig mit mikrodienstbasierter Veröffentlichung auszuführen und die branchenführende Server-lose Adobe I/O Runtime-Plattform zu nutzen.

Ab der April-Version können Sie mehrere Veröffentlichungsanforderungen gleichzeitig ausführen und mithilfe des Microservice-basierten nativen PDF-Publishing sehr effizient Bulk-PDF-Ausgaben generieren.
Weitere Informationen finden Sie unter [Neue mikrodienstbasierte Veröffentlichung für AEM Guides as a Cloud Service konfigurieren](../knowledge-base/publishing/configure-microservices.md).


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
