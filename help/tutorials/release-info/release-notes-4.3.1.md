---
title: Versionshinweise | Aktualisierungsanweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern 4.3.1
description: Erfahren Sie mehr über die Fehlerbehebungen und das Upgrade auf Version 4.3.1 der Adobe Experience Manager-Handbücher.
source-git-commit: a8f36d020422d9d83ca47e2246dc42278f2c7963
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 5%

---

# Version 4.3.1 von Adobe Experience Manager-Handbüchern (Oktober 2023)

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version 4.3.1 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in Version 4.3.1 von Adobe Experience Manager-Handbüchern](./whats-new-4.3.1-release.md).

## Aktualisierung auf Version 4.3.1 der AEM Handbücher


Sie können Ihre aktuelle Version von AEM Guides einfach auf Version 4.3.1 aktualisieren. Bevor Sie mit der Aktualisierung auf Version 4.3.1 von AEM Guides fortfahren, müssen Sie die folgenden Punkte beachten: Sie können Ihre aktuelle Version von AEM Guides auf Version 4.3.1 aktualisieren.

- Wenn Sie Version 4.2 oder 4.2.x verwenden, können Sie direkt auf Version 4.3.1 aktualisieren.
- Wenn Sie Version 4.1 oder 4.1.x verwenden, müssen Sie auf Version 4.2 oder 4.2.x aktualisieren, bevor Sie auf Version 4.3.1 aktualisieren.
- Wenn Sie Version 4.0 verwenden, müssen Sie vor der Aktualisierung auf Version 4.3.1 auf Version 4.2 aktualisieren.
- Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0 aktualisieren, bevor Sie auf Version 4.2 aktualisieren.
- Wenn Sie eine Version vor 3.8.5 verwenden, finden Sie im Abschnitt AEM Upgrade-Handbuch im produktspezifischen Installationshandbuch weitere Informationen.



>[!NOTE]
>
>Sie müssen AEM Service Pack installieren, bevor Sie AEM Guides-Version aktualisieren.

Weitere Informationen finden Sie unter [Upgrade-Anweisungen](../install-guide/upgrade-xml-documentation.md).

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.3.1 unterstützt werden.

### Adobe Experience Manager

**4.3.1 Nicht-UUID**
Version 6.5 Service Pack 18, 17, 16, 15 oder 14

**4.3.1 UUID**
Version 6.5 Service Pack 18, 17, 16, 15 oder 14

Weitere Informationen finden Sie unter *Technische Anforderungen* im Handbuch &quot;Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern&quot;.

### FrameMaker und FrameMaker Publishing Server

| Freigabe | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.3.1 (Nicht-UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.3 oder höher |
| 4.3.1 (UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.4 oder höher |
| | | | |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Freigabe | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.3.1 (Nicht-UUID) | 2.3-normal-5 | 2.3-normal-5 | 1.6 | 1.6 |
| 4.3.1 (UUID) | 3.2-uuid-5 | 3.2-uuid-5 | 2.3 | 2.3 |
|  |  |   |



### Knowledgebase-Vorlagenversion

| Name des Komponentenpakets | Komponentenversion | Vorlagenversion |
|---|---|---|
| Inhaltspaket für AEM Guides-Komponenten für Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

- Nachmittagsstunden werden nicht im **Datum** zur Erstellung von Grundlinien. (12712)
- Der JSON-Code kann nicht in die `<codeblock>` -Element des Web-Editors. (12326)
- Nicht gespeicherte Versionsänderungen und die zugehörigen Indikatoren werden nicht für große Dateien angezeigt. (11784)
- Bei der Bearbeitung in koreanischer Sprache wird das erste Zeichen in den Standard geändert. (10049)

- Das Präfix wird im Vorschaumodus des Web-Editors dupliziert. (13133)
- `Choicetable` -Zeilen nicht angezeigt werden oder nicht ausgewählt werden können. (12616)
- Der Web Editor gibt bei der Erstellung eines Themas mit einem benutzerdefinierten Schema in bestimmten Szenarien Validierungsfehler aus. (12576)
- Die Referenzen der Ditaval-Themenvorlage erstellen beim Erstellen einer Zuordnung aus der Zuordnungsvorlage keine Kopie im Inhaltsordner. (12150)

- Das Suchfeld in DITA-Maps hat keine Schließen-Schaltfläche. (11867)
- Beim Speichern langer Dateien im Web-Editor `DirtyChecker` gibt eine Ausnahme mit einer langen Stacktrace aus und füllt die Protokolldateien. (11860)
- Für das Erstellen von DITA-Themen ist eine Löschberechtigung für den entsprechenden Ordnerknoten erforderlich, obwohl die Zuordnung mit Schreibberechtigung erstellt werden kann. (11706)
- Der Web Editor zeigt einen falschen Titel an, wenn ein Schrägstrich vorhanden ist. (10949)

- Wenn der Titel eines Themas einen Schrägstrich (/) enthält, werden auf der Registerkarte im Editor nur die folgenden Buchstaben angezeigt. (13455)
- Die Bildvorschau wird nach der Anzeige der Vorschau im Editor nicht ausgeblendet. (13454)
- Einige der vorhandenen Versionen oder deren Beschriftungen werden nach dem Upgrade auf 4.x nicht im Versionsverlauf angezeigt. (13247)
- Der Bereich Versionsverlauf in der Assets-Benutzeroberfläche zeigt einen falschen Zeitstempel für die **Aktuell** -Feld. (12624)
- Das Thema mit conref title wird in der Repository-Ansicht oder Kartenansicht nicht aufgelöst.(13304)


### Veröffentlichung

- Native PDF | Die Reihenfolge der Themen wird nicht festgelegt, wenn die PDF-Ausgabe erzeugt wird. (13157)
- Native PDF | Es ist kein standardmäßiges Stil-Tag verfügbar für `<p>`-Element. (12559)
- Native PDF | Inline-Stile, die auf den Inhaltsbereich angewendet werden, werden nicht auf die Themen in der Vordergrund- und der RückMaterie angewendet. (13510)
- Die `DeliveryTarget` -Attribut wird beim Generieren der AEM Site-Ausgabe nicht übernommen.  (13132)
- Die **Veröffentlichen** Workflow hängt beim Generieren AEM Site-Ausgabe für Inhalte mit bestimmten Fehlern nicht mehr zusammen. (12000)

- Native PDF | Durch die Verwendung mehrerer xrefs wird der Text über die Spaltenbreite hinaus erweitert. (13004)
- Native PDF | Wenn das Thema und der Titel dieselbe ID aufweisen, führt dies zu einer fehlerhaften Generierung der PDF-Ausgabe. (12644)
- Native PDF | Beim Hinzufügen einer Ausgabeklasse zu einer übergeordneten Klasse `<topicref>` -Element in einer DITA-Zuordnung und durch Anwendung eines benutzerdefinierten Stils auf die Ausgabeklasse wird die Formatierung auf Elemente im Themenhauptteil angewendet, einschließlich Abschnittstitel. (12166)
- Inkrementelle Veröffentlichung funktioniert nicht, wenn eine DITA-Map über mehrere Ditavalrefs verfügt. (12117)
- AEM Site | Beim Erstellen einer Zuordnung mit Keydef, die auf ein Thema als Variable verweist, und beim Hinzufügen von processing-role=resource-only werden einige unerwartete Seiten erstellt. (12099)
- Wenn Assets aus AEM DAM in einer anderen Ausgabe als der AEM-Site verwendet werden, spiegeln die Metadaten &quot;jcr:createdBy&quot;nicht den Namen des Herausgebers oder den Namen des Benutzers wider, der die DITA-Map oder das Thema zuletzt geändert hat. (12090)
- AEM Sites | DITA-Zuordnung mit topichead im Navigationstitel (mit nicht unterstützten Zeichen) führt zu fehlerhaften Seiten-URLs. (11978)
- Native PDF | Probleme treten zur Unterstützung von topichead/topicmeta/navtitle in Frontmatter und Backmatter auf. (11969)
- Native PDF | Das Generieren von PDF für große Dokumente ist zeitaufwendig. (11955)
- Native PDF | Beim Umbenennen einer Vorgabe wird beim Generieren einer PDF-Ausgabe eine NullPointerException ausgelöst. (11889)
- Die `<conref>` -Inhalt wird nicht in der PDF-Ausgabe angezeigt. (11131)
- Innerhalb der `<div>` Elemente zum Wechseln zwischen der Autoren- und der Quellansicht im Seitenlayout-Editor. (10750)
- Der im AEM Cloud Manager replizierte Inhalt ist nicht in der Veröffentlichungsinstanz sichtbar. (9564)


### Verwaltung

- Versionsverlauf wird nicht angezeigt, auch wenn die `dc:format` -Eigenschaft für ein Asset nicht vorhanden ist. (10463)
- Der Inhaltsverweis ist beim Kopieren und Einfügen von DITA-Dateien beschädigt, wenn die Themen-ID nicht mit der GUID übereinstimmt. (12614)
- In dynamischen Grundlinien wird die Liste der Beschriftungen nicht aus den direkten Verweisen der Arbeitskopie einer DITA-Zuordnung abgerufen. (11917)
- Die Grundlinie zeigt die falsche Anzahl von Dateien im Map Dashboard an, wenn die Funktion &quot;Alle Themen durchsuchen&quot;verwendet wird. (13265)
- Im Web-Editor zeigt die Grundlinie den Titel der vorherigen Version anstelle der ausgewählten Version der DITA-Datei an. (13444)

### Überprüfung

- Die Themenüberprüfung zeigt falsche Kommentare an. (13453)
- Über die Schaltfläche Schließen auf der Seite Überprüfen in den Experience Manager-Handbüchern gelangen die Benutzer zur AEM-Startseite. (13535)
- Anlagen werden nicht im rechten Bereich des Editors für ein Thema im Review angezeigt. (13011)



### Übersetzung

- Die aus der **Übersetzung** Dashboard schlägt fehl und wird nicht in der Zielsprache geöffnet. (13466)

- Anstatt den ausgewählten Übersetzungsprojekten neue Aufträge hinzuzufügen, werden neue Übersetzungsprojekte erstellt.  (10214)
- Der Titel der übersetzten Datei wird anstelle des Titels der Quelldatei angezeigt. (11630)
- Die automatische Genehmigung funktioniert manchmal nicht und es treten Ausnahmen auf, wenn für den Übersetzungsstatus ein falscher Wert festgelegt ist. (13607)
- Die über das Dashboard &quot;Übersetzung&quot;exportierte Grundlinie schlägt fehl und wird nicht in der Zielsprache geöffnet. (12993)
- Einige Dateien fehlen bei der Verwendung von Grundlinien in der Übersetzung. (13021)