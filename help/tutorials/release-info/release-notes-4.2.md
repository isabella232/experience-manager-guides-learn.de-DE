---
title: Versionshinweise | Adobe Experience Manager-Handbücher Version 4.2
description: Erfahren Sie mehr über die Fehlerbehebungen und das Upgrade auf Version 4.2 der Adobe Experience Manager-Handbücher.
exl-id: 8a7fef77-63af-462f-89c5-054ab31e079b
source-git-commit: a54ada55dad4ff8da8eee3dccb5ad9028b4cdc9e
workflow-type: tm+mt
source-wordcount: '1338'
ht-degree: 6%

---

# Version 4.2 von Adobe Experience Manager-Handbüchern (Februar 2023)

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die behobenen Probleme in Version 4.2 der Adobe Experience Manager-Handbücher (später auch als *AEM*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in Version 4.2 von Adobe Experience Manager-Handbüchern](whats-new-4.2-release.md).

## Aktualisierung auf Version 4.2 AEM Handbücher

Sie können Ihre aktuelle Version von AEM Guides einfach auf Version 4.2 aktualisieren. Bevor Sie mit der Aktualisierung auf Version 4.2 von AEM Guides fortfahren, müssen Sie die folgenden Punkte beachten:
* Wenn Sie Version 4.0, 4.1 oder 4.1.x verwenden, können Sie direkt auf Version 4.2 aktualisieren.
* Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0 aktualisieren, bevor Sie auf Version 4.2 aktualisieren.
* Wenn Sie eine Version vor 3.8.5 verwenden, lesen Sie den Abschnitt *AEM* im produktspezifischen Installationshandbuch.

>[!NOTE]
>
>Sie müssen AEM Service Pack installieren, bevor Sie AEM Guides-Version aktualisieren.

Weitere Informationen finden Sie unter [Upgrade-Anweisungen](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.2 unterstützt werden.

### Adobe Experience Manager

**Nicht-UUID**
Version 6.5 Service Pack 15, 14, 13 oder 12

**UUID**
Version 6.5 Service Pack 15, 14, 13 oder 12

Weitere Informationen finden Sie unter *Technische Anforderungen* im Handbuch &quot;Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern&quot;.

### FrameMaker und FrameMaker Publishing Server

| Release | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (Nicht-UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.3 oder höher |
| 4.2 (UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.4 oder höher |
|  |  |  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Release | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.2 (Nicht-UUID) | 2.1-normal-4 | 2.1-normal-4 | 1.6 | 1.6 |
| 4.2 (UUID) | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

* Beim Hinzufügen einer Registerkarte wird der linke Bereich umgebrochen. (11126)
* Änderungen im HTML-Code des Web Editors verursachen Probleme mit `<dl>` und `<dlentry>`. (11024)
* Einige Attribute werden nicht als bedingt behandelt und verursachen Probleme. (10895)
* Drei Ebenen oder mehr verschachtelt `<indexterm>` sind beim nativen PDF-Export nicht verschachtelt. (10799)
* Der Inhalt verschwindet beim Wechsel von der Autoren- zur Quellansicht im Hauptteil einer Aufgabe. (10735)
* Überprüfungskommentare werden in einer Prüfungsaufgabe nicht platziert. (10625)
* `<conref>` Hinweis innerhalb eines para-Tags wird nicht im Vorschaumodus angezeigt. (10559)
* Wenn Sie die Rücktaste am Ende eines Listenelements drücken, wird die gesamte Liste entfernt. (10540)
* Der Bildschirm wird in Chrome v106 beim Ziehen und Ablegen eines Elements aus der Benutzeroberfläche (z. B. aus dem Bedienfeld &quot;Bedingungen&quot;) als leer angezeigt. (10524)
* Die Schaltfläche &quot;Automatischer Einzug&quot;fehlt in der Symbolleiste in **Quelle** anzeigen. (10448)
* Das erste Zeichen eines Listenelements geht manchmal verloren, wenn die Liste im Editor erstellt wird.( 10447)
* **Rückgängig** oder **Wiederholen** funktioniert bei einigen Dateien nicht richtig. (10373)
* Benutzerdefinierte Metadaten werden beim Kopieren und Einfügen nicht beibehalten. (10367)
* Beim Kopieren (Strg+C) und Einfügen (Strg+V) des Inhalts tritt ein Fehler auf. (10304)
* Im Bedienfeld &quot;Kontur&quot;werden keine Inhalte angezeigt, wenn von der Autoreninstanz in den Quellmodus gewechselt wird. (10296)
* Submap wird nicht erstellt, wenn sie auf eine Hauptkarte in DITA-Vorlagen verweist. (10231)
* Navigationsprobleme treten im Web Editor nach der Aktualisierung auf Version 4.0 auf. (10159)
* Die Option &quot;Rückgängig&quot;im XML-Editor bringt den Benutzer zum Anfang der Seite. (10091)
* Knoteneigenschaften werden nach dem Kopieren und Einfügen eines Assets entfernt. (10053)
* SVG-Dateien, die zu DITA-Themen hinzugefügt wurden, werden im Vorschaumodus des Editors nicht angezeigt. (10010)
* Suchergebnisse für Suchen und Ersetzen im Web Editor sind im Dunkelmodus nicht lesbar. (9978)
* Beim Erstellen einer Zuordnung aus der Zuordnungsvorlage existiert kein Ladeprogramm. (9891)
* Conref in der Themenvorlage funktioniert nicht und die kopierte Hash-ID wird in der Inhaltskopie nicht aktualisiert. (9890)
* Es wird keine Option zum Durchsuchen der Themen oder Zuordnungsvorlagen in den Unterordnern des Themen- oder Zuordnungsordners angezeigt. (9889)
* Keine Option zum Erstellen einer neuen Vorlage in den Unterordnern von Themen oder Maps. (9888)
* Der XML-Editor aktualisiert die Bilder nicht zu Themen. (9500)
* mimeType ist für die Erstellung und Aktualisierung von DITA-Assets hartcodiert. (8979)
* Ein normaler Bindestrich wird bei der Auswahl von geschützten Bindestrichen im **Sonderzeichen einfügen** angezeigt. (8919)
* Der Name des Erstellers der Version im Versionsverlauf ist &quot;fmdita-service-user&quot;für die Dateien, die über die Assets-Benutzeroberfläche hochgeladen wurden. (8910)
* Die Option &quot;Bearbeiten&quot;funktioniert nicht für Bilder, während Sie in der Spaltenansicht der Assets-Benutzeroberfläche arbeiten. (8758)
* DITA-Thema wird nicht automatisch mit Änderungen aktualisiert, die am **Eigenschaften** Seite. (8745)
* Beim Verschieben von Elementen innerhalb des Themas im Web Editor werden die zugewiesenen IDs für Elemente durch automatisch zugewiesene IDs überschrieben. (7895)

### Verwaltung

* Das Kopieren eines DITA-Map-Assets (aus der Asset-Benutzeroberfläche ) verursacht fehlerhafte Grundlinien im kopierten Asset. (11218)
* Beim Hochladen einer Datei, die die in AEM zulässige Größe überschreitet, wird keine Warnmeldung angezeigt (standardmäßig 2 GB). (10817)
* Web Editor-Grundlinie | Das Verhalten der Spalte &quot;Neueste&quot;unterscheidet sich im neuen Dashboard für die Grundlinie im Web Editor. (10808)
* Übersetzung | Der Übersetzungsauftrag wird aufgrund von ungültigen /libs/fmdita/i18n/ja.json nicht gestartet. (10543)
* Übersetzung | In einem Scoping-Übersetzungsprojekt, das über das Übersetzungs-Dashboard (Menschliche Übersetzung) erstellt wurde, tritt ein Fehler auf. (10526)
* Übersetzung | Die Nachbearbeitung wird für den gesamten Sprachordner blockiert, dessen Assets in einem aktiven Übersetzungsprojekt vorhanden sind. (10332)
* Übersetzung | Metadaten und Tags werden nicht an die übersetzten Kopien weitergegeben. (4696)
* Für jedes Asset werden mehrere Popups angezeigt, wenn die Version geändert und im Baseline-Editor gespeichert wird. (10399)
* SitzungsLeak tritt unter com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210) auf. (10279)
* Die Videodatei fehlt in der Grundlinie, wenn der übergeordnete Ordner Leerzeichen im Namen enthält. (10031)

### Veröffentlichung

* Die Themenregenerierung funktioniert in einigen Szenarien nicht. (10635)
* PDF-Publishing schlägt beim Generieren der Ausgabe für eine Vorgabe (einer vorhandenen Vorgabe) fehl. (10584)
* Die Schaltfläche Protokoll anzeigen funktioniert nicht, falls die PDF-Erstellung für eine Vorgabe fehlschlägt. (10576)
* Der Herausgeber zeigt die angeforderten Daten nicht in den Infoprotokollen an und enthält auch einige Junk-Protokolle.( 10567)
* Native PDF | PDF-Generierung schlägt mit einer Nullzeiger-Ausnahme fehl. (10950)
* Native PDF | conkeyref wird in der generierten Ausgabe nicht aufgelöst. (10564)
* Native PDF | Probleme treten mit den Metadaten einer Zuordnung auf, auf die in der PDF-Ausgabe verwiesen werden muss.( 10556)
* Native PDF | Beim Drehen der Tabellenüberschrift treten Probleme auf. (10555)
* Native PDF | Beim Entfernen von Themen mit Verarbeitungsrolle=&#39;resource-only&#39; treten Probleme auf. (10554)
* Native PDF | Leere Keyrefs werden in der PDF-Ausgabe angezeigt. (10553)
* Native PDF | Verschachtelt `<indexterm>` sind beim nativen PDF-Export nicht verschachtelt. (10521)
* Native PDF | Native PDF verwendet für die generierten Tags den Inline-Stil anstelle des Klassennamens. (10498)
* Native PDF | Verschachtelte topicref in Anhängen werden alle in der temporären HTML in h1 umgewandelt.( 10454)
* Native PDF | Frontmatter-Themen können nicht aus dem Inhaltsverzeichnis ausgeblendet werden. (10355)
* Native PDF | Tabellenframe-Attribut wird nicht auf die temporäre HTML übertragen (als Klasse). (10353)
* Native PDF | Temporäre HTML-Dateien fügen die Klassen colsep und rowsep zu <td> und <th> auch wenn ihr Wert 0 in der Quell-DITA beträgt. (10352)
* Native PDF | Beim Neustarten von Seitennummern im Kapitel-Layout wird die Nummerierung nach dem Zufallsprinzip am Ende des vorherigen Kapitels begonnen. (10154)
* Native PDF | Schlüsselreferenzen für Keydefs mit Bild- oder externen Links werden nicht aufgelöst. (10063)
* Native PDF | Anlage wird als Kapitel in der generierten PDF angezeigt. (9829)
* Die Registerkarte &quot;Vorlage&quot;im XML-Editor wird den Ordnerprofil-Administratoren nicht angezeigt. (10266)
* Die Grundlinienveröffentlichung schlägt bei PDF fehl, die mit FrameMaker Publishing Server 2020 erstellt wurden. (10551)
* Anwendungsfehler tritt beim Klicken auf die Schaltfläche &quot;Bearbeiten&quot;auf, nachdem im Popup &quot;Quick Generate&quot;das Kontrollkästchen Alle Vorgaben über Ausgabevorgaben ausgewählt wurden. (10388)
* Wenn die Registerkarte &quot;Ausgabe&quot;im Web Editor über mehr Vorgaben verfügt, ist der Bereich &quot;Vorgaben&quot;nicht vertikal durchlaufbar und zeigt nicht alle verfügbaren Vorgaben an. (9787)
* Vorgaben können beim Veröffentlichen über den Editor nicht aus dem Output-Workflow gelöscht werden. (9100)
* Peer-Link wird als normaler Text statt als Link auf der generierten Seite gerendert. (7774)

## Bekanntes Problem

Adobe hat das folgende bekannte Problem für AEM Guides 4.2-Version identifiziert:

* Benutzer können Überprüfungsvorgänge auch nach Abschluss der Prüfungsaufgabe durchführen.
