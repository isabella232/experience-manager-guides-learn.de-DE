---
title: Versionshinweise | Aktualisierungsanweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern 4.2.1
description: Erfahren Sie mehr über die Fehlerbehebungen und das Upgrade auf Version 4.2.1 der Adobe Experience Manager-Handbücher.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 1%

---

# Version 4.2.1 von Adobe Experience Manager-Handbüchern (Mai 2023)

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version 4.2.1 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in Version 4.2.1 von Adobe Experience Manager-Handbüchern](whats-new-4.2.1-release.md).

## Aktualisierung auf Version 4.2.1 der AEM Handbücher


Sie können Ihre aktuelle Version von AEM Guides einfach auf Version 4.2.1 aktualisieren. Bevor Sie mit der Aktualisierung auf Version 4.2.1 von AEM Guides fortfahren, müssen Sie die folgenden Punkte beachten: Sie können Ihre aktuelle Version von AEM Guides auf Version 4.2.1 aktualisieren.
* Wenn Sie Version 4.1, 4.1.x oder 4.2 verwenden, können Sie direkt auf Version 4.2.1 aktualisieren.
* Wenn Sie Version 4.0 verwenden, müssen Sie vor der Aktualisierung auf Version 4.2.1 auf Version 4.2 aktualisieren.
* Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0 aktualisieren, bevor Sie auf Version 4.2 aktualisieren.
* Wenn Sie eine Version vor 3.8.5 verwenden, finden Sie im Abschnitt AEM Upgrade-Handbuch im produktspezifischen Installationshandbuch weitere Informationen.

>[!NOTE]
>
>Sie müssen AEM Service Pack installieren, bevor Sie AEM Guides-Version aktualisieren.

Weitere Informationen finden Sie unter [Upgrade-Anweisungen](../install-guide/upgrade-xml-documentation.md).

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.2 unterstützt werden. Version 1.

### Adobe Experience Manager

**Nicht-UUID**
Version 6.5 Service Pack 15, 14, 13 oder 12

**UUID**
Version 6.5 Service Pack 15, 14, 13 oder 12

Weitere Informationen finden Sie unter *Technische Anforderungen* im Handbuch &quot;Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern&quot;.

### FrameMaker und FrameMaker Publishing Server

| Freigabe | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.2.1 (Nicht-UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.3 oder höher |
| 4.2.1 (UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.4 oder höher |
| | | | |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Freigabe | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.2.1 (Nicht-UUID) | 2.2-normal-3 | 2.2-normal-3 | 1,6 | 1,6 |
| 4.2.1 (UUID) | 2.9-uuid-2 | 2.9-uuid-2 | 2,3 | 2,3 |
|  |  |   |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

* Navtitle wird beim Wechsel von der Layoutansicht zur Autoren- oder Quellansicht aus dem Inhalt entfernt. (12174)
* Schaltfläche &quot;Schließen&quot;im Web Editor führt nicht zu AEM Navigationsseite. (1948)
* Manchmal tritt beim Klicken auf eine DITA Map ein Anwendungsfehler auf. (11842)
* Problem tritt beim Verschieben (per Drag-and-Drop) anstelle eines vorhandenen Listenelements auf, bei dem &quot;Änderungen verfolgen&quot;aktiviert ist. (11570)
* Beim Verschieben (per Drag &amp; Drop) als neues Listenelement mit aktivierter Option Änderungen verfolgen tritt ein Problem auf. (11569)
* Einzug- oder Ausschlusslistenelemente funktionieren bei &quot;Änderungen verfolgen&quot;in nicht erwartungsgemäß. (11568)
* Wenn Sie Inhalte in einer Zeile mit aktivierter Option &quot;Änderungen verfolgen&quot;hinzufügen und die Option &quot;Änderungen verfolgen&quot;dann deaktivieren, wird dies nicht deaktiviert. (11567)
* Schwierigkeiten beim Ziehen und Ablegen eines Listenelements besteht darin, dass Text anstelle des Listenelements verschoben wird. (11566)
* Beim Authoring im Element, das grün (Änderungen verfolgen) angezeigt wird, wird der neue Inhalt als Verfolgungsänderung angezeigt, auch wenn die Verfolgungsänderung deaktiviert ist. (7021)
* Der Browser (Web Editor) friert beim Laden von Inhalten mit benutzerdefiniertem Schema ein. (1121)
* Native PDF | Beim Erstellen einer Ausgabevorgabe mit der Option &quot;Zum Ordnerprofil hinzufügen&quot;schlägt die PDF-Erstellung mit einer Nullzeiger-Ausnahme fehl. (10950)
* Native PDF | Bild-Tag fügt allen Bildern das Attribut display-inline hinzu. (10653)
* Das Einfügen von Audio- und Video-Multimediadateien schlägt im YouTube-Format unter dem **Multimedia einfügen** Symbol. (11320)
* Der Validierungsfehler tritt auf, wenn eine Zuordnung mithilfe der Vorlage erstellt wird, die über ein spezielles Titelelement verfügt. (11212)
* Web-Editor | Beim Bearbeiten eines Themas wird im XML-Editor geschütztes Leerzeichen hinzugefügt. (11786)

### Verwaltung

* Auf der Registerkarte Berichte in der Web Editor-Benutzeroberfläche wird nicht die Themenliste der alten DITA-Maps angezeigt, die vor der Aktualisierung 4.2 erstellt wurden. (11708)

* Die Schaltfläche &quot;Dateien hochladen&quot;in der Assets-Benutzeroberfläche ist in Version 4.2 nicht mehr verfügbar. (11633)


### Veröffentlichung

* Native PDF | Das Veröffentlichen von Inhalten mit einer Ausgabeklasse mit Klammern() führt zum Einfrieren der Veröffentlichung. (1936)
* JSON-Ausgabe | Zuordnen von Metadaten mit Eigenschaftswert als `"value in spaces and double quotes"` führt zu einem Veröffentlichungsfehler. (1933)
* Problem tritt bei AEM Site-Suche auf (funktioniert nicht über 2-3-Level-Knoten hinaus). (11352)
* Web-Editor | Ausgabepfad und Vorlage können nicht in der AEM-Vorgabe ausgewählt werden. (11530)
* Bei der Aktualisierung von Version 4.1.x auf Version 4.2 funktioniert die Native PDF Engine nicht und gibt auch für das unterstützte Betriebssystem eine NullPointerException aus.(11526)
* Der Download-PDF-Prozess funktioniert im Web-Editor nicht ordnungsgemäß. (11496)
* Native PDF | Entwurfskommentare sind standardmäßig in der generierten Ausgabe ausgeblendet. (10560)
* Native PDF | navtitle wird für topichead nicht geehrt. (10509)
* Native PDF | Hinzufügen `xref` in ein Bild wird das Bild nicht auf der generierten PDF gerendert. (11346)
* Native PDF | Die Fußnote in der Tabellenüberschrift führt zu fett und zentriert ausgerichtetem Text in der entsprechenden Fußzeile der PDF-Ausgabe. (10610)

### Übersetzung

* Bei der Aktualisierung auf Version 4.2 werden alle Übersetzungsinhalte als &quot;Nicht synchronisiert&quot;oder &quot;Fehlende Kopie&quot;angezeigt. (11834)

### Überprüfung

* Die abgeschlossene Überprüfung wird nicht im schreibgeschützten Modus geöffnet. (11387)
