---
title: Versionshinweise | Adobe Experience Manager-Handbücher Version 4.1
description: Aktuelle Version der Adobe Experience Manager-Handbücher
exl-id: c70b3bbc-3332-4626-bc30-641034f8fd06
source-git-commit: 0bddd791e7fb6e6f8eb0f8e2ad73146a758ffc47
workflow-type: tm+mt
source-wordcount: '3400'
ht-degree: 3%

---

# Version 4.1.x der Adobe Experience Manager-Handbücher

Diese Versionshinweise behandeln die Upgrade-Anweisungen, neuen Funktionen und Verbesserungen in Version 4.1.x der Adobe Experience Manager-Handbücher (später auch als *AEM*).

## Aktualisierung auf die neueste Version

Sie können Ihre aktuelle Version von AEM Guides einfach auf Version 4.1.2 aktualisieren. Bevor Sie mit der Aktualisierung auf Version 4.1.2 von AEM Guides fortfahren, müssen Sie die folgenden Punkte beachten:
* Wenn Sie Version 4.1 oder 4.1.x verwenden, können Sie direkt auf Version 4.1.2 aktualisieren.
* Wenn Sie Version 4.0.x verwenden, müssen Sie auf Version 4.1 oder 4.1.x aktualisieren, bevor Sie auf Version 4.1.2 aktualisieren.
* Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0.x aktualisieren, bevor Sie auf Version 4.1 aktualisieren.
* Wenn Sie eine Version vor 3.8.5 verwenden, lesen Sie den Abschnitt zur Aktualisierung im produktspezifischen Installationshandbuch.

Weitere Informationen finden Sie unter [Upgrade-Anweisungen](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4.1.2 | Versionshinweise

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.1.2 unterstützt werden.

### Adobe Experience Manager

**Nicht-UUID**
Version 6.5 Service Pack 13, 12, 11 oder 10

**UUID**
Version 6.5 Service Pack 13, 12, 11 oder 10

Weitere Informationen finden Sie im Abschnitt Technische Anforderungen im Handbuch Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern.


### FrameMaker und FrameMaker Publishing Server

| Release | FMPS 2020 | FMPS 2019 | FM 2020 | FM 2019 |
| --- | --- | --- | --- | --- |
| 4.1.2 (Nicht-UUID) | 2020.2 oder höher* | 2019 | 2020.3 oder höher | 2019.8 (neueste Aktualisierung) |
| 4.1.2 (UUID) | 2020.2 oder höher* | Nicht kompatibel | 2020.4 oder höher | Nicht kompatibel |
|  |  |  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.1.2 (Nicht-UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1.2 (UUID) | 2.7 | 2,7 | 2.3 | 2,3 |
|  |  |  |


## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Bei der Auswahl aller Ordnerprofile wird ein unsichtbares Ordnerprofil angezeigt (das falsch ist). (10393)
* Bei der Grundlagenerstellung wird nicht die neueste Version ausgewählt, wenn sich die Zeitzone des Benutzers von der Zeitzone des Servers unterscheidet. (10336)
* Mit der Tastenkombination Strg+F wird das Browser-Suchmodul nach der Installation der AEM Guides 4.1 nicht in der Konsole &quot;Assets&quot;geöffnet. (10339)
* Es tritt ein Fehler bei der Grundlagenerstellung für das Thema auf, das auf einen Ordner verweist. (10383)
* Die Registerkarte &quot;Ausgabevorgaben&quot;zeigt gelegentlich einen leeren Bildschirm an, und in einigen Fällen werden nicht bearbeitbare Vorgaben angezeigt. (10390)
* Das Keyspace-Management führt zu Ausnahmen und Fehlern. (10449)

### Bekannte Probleme mit Problemumgehung

* Die während der Übersetzung exportierte Grundlinie wird nicht auf der Registerkarte &quot;Grundlinie&quot;des Editors geladen.

   **Problemumgehung**: Verwenden Sie die Registerkarte &quot;Grundlinie&quot;des DITA-Map-Dashboards.

## 4,1 | Versionshinweise

Diese Versionshinweise behandeln die Upgrade-Anweisungen, neuen Funktionen und Verbesserungen in Version 4.1.x der Adobe Experience Manager-Handbücher (später auch als *AEM*).

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.1 unterstützt werden.

### Adobe Experience Manager

**Nicht-UUID**
Version 6.5 Service Pack 13, 12, 10 oder 11

**UUID**
Version 6.5 Service Pack 13, 12, 10 oder 11

Weitere Informationen finden Sie im Abschnitt Technische Anforderungen im Handbuch Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern.




### FrameMaker und FrameMaker Publishing Server

| Version | FMPS 2020 | FMPS 2019 | FM 2020 | FM 2019 |
| --- | --- | --- | --- | --- |
| 4.1 (Nicht-UUID) | 2020.2 oder höher* | 2019 | 2020.3 oder höher | 2019.8 (neueste Aktualisierung) |
| 4.1 (UUID) | 2020.2 oder höher* | Nicht kompatibel | 2020.4 oder höher | Nicht kompatibel |
|  |  |  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.1 (Nicht-UUID) | 2,0 | 2,0 | 1,6 | 1,6 |
| 4.1 (UUID) | 2,7 | 2,7 | 2,3 | 2,3 |
|  |  |  |


## Neue Funktionen und Erweiterungen

AEM-Handbücher bieten viele Verbesserungen und neue Funktionen in Version 4.1:

### Native PDF-Veröffentlichung

Die Version 4.1 von AEM Guides unterstützt auch die Erstellung einer nativen PDF. Eine neue Publishing-Engine wurde mit den folgenden Funktionen eingeführt:
* Erstellen einer CSS-Vorlage
* Erstellen verschiedener Seitenvorlagen
* Design-PDF-Vorlagen mit CSS- und Seitenvorlagen
* Veröffentlichen von Zuordnungs- und Themeninhalten im PDF-Format

### Unterstützung für den Knowledgebase-Site-Pfad in der artikelbasierten Veröffentlichung

AEM Handbücher bieten die Funktion zum artikelbasierten Veröffentlichen, um schrittweise eine Ausgabe eines oder mehrerer Themen zu generieren oder Ihre Inhalte auf einer Knowledgebase-Plattform zu veröffentlichen. Mit Version 4.1 haben Sie eine zusätzliche Option, den Knowledgebase-Site-Pfad auszuwählen, zu dem das Thema/die Karte veröffentlicht werden muss. Nachdem Sie den Pfad ausgewählt haben, wird die Ausgabe am angegebenen Pfad generiert.

### Verbesserter Web-Editor

* **Verbesserte Schlüsselauflösung**

Ein DITA-Inhaltsschlüsselverweis fügt einen Teil des Inhalts von einem Thema in ein anderes. Es verwendet einen Schlüssel zum Suchen des Inhalts. Die Schlüsselverweise, die mit einem DITA-Thema verknüpft sind, müssen aufgelöst werden. Die ausgewählte Stammzuordnung hat die höchste Priorität, um Schlüsselverweise aufzulösen.

![Dialogfeld &quot;Benutzereinstellungen&quot;](assets/user-preferences.png)

Jetzt werden die Schlüsselverweise auf der Grundlage der in der folgenden Prioritätsreihenfolge festgelegten Stammzuordnung aufgelöst:

1. Benutzereinstellungen
2. Bedienfeld &quot;Landkartenansicht&quot;
3. Ordnerprofil

Weitere Informationen finden Sie unter *Schlüsselverweise auflösen* im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.

* **Hinzufügen eines benutzerdefinierten Bedienfelds im linken Bereich**

Jetzt können Sie ein benutzerdefiniertes Bedienfeld im linken Bereich des Web-Editors hinzufügen. Sie können ein benutzerdefiniertes Bedienfeld für verschiedene Zwecke verwenden, z. B. Hilfe bereitstellen oder Tests für ein Projekt durchführen. Wenn ein benutzerdefiniertes Bedienfeld konfiguriert wurde, wird es auch in der Liste der Bedienfelder innerhalb der **Editor-Einstellungen**. Sie können den Schalter umschalten, um das benutzerdefinierte Bedienfeld ein- oder auszublenden.

* **Möglichkeit, den Dokumentstatus von Themen in einer DITA-Zuordnung zu ändern**

Jetzt können Sie den Dokumentstatus ausgewählter Themen in einer DITA-Zuordnung einfach ändern. Sie können die Eigenschaften ausgewählter Themen auch in einer DITA-Zuordnung über die **Weitere Optionen** Menü unten im Bedienfeld &quot;Kartenansicht&quot;.

![ausgewählte Themeneigenschaften](assets/map-view-properties.png)

* **Im Vorschaumodus angezeigte Versionsinformationen**

Der Web Editor hilft Ihnen bei der Verwaltung Ihrer Versionen. Jetzt können Sie auch die Version des aktiven Themas oder der DITA-Zuordnung oben rechts auf der Registerkarte &quot;Datei&quot;des Themas im Vorschaumodus eines Themas sehen.

![Vorschau Version](assets/preview-version.png)


* **Verbessertes Aktualisierungsverhalten des Web-Editors**

Die folgenden Verbesserungen sind jetzt beim Aktualisierungsvorgang des Browsers im Web Editor verfügbar:

* Jetzt können Sie den Browser aktualisieren, während Sie Ihre Inhalte im Web Editor bearbeiten. Wenn Sie auf das Symbol für die Browseraktualisierung klicken, während mindestens eine Datei mit nicht gespeicherten Änderungen zur Bearbeitung geöffnet ist, werden Sie aufgefordert, Ihre Dateien zu speichern oder die Aktualisierungsaktion abzubrechen.

* Selbst beim Aktualisieren des Browsers bleiben die Ansichten des linken und des rechten Bedienfelds erhalten.

* Das aktive Thema oder die DITA-Zuordnung wird im Inhaltsbearbeitungsbereich erneut geöffnet.

* **Erstellen von Karten basierend auf benutzerdefinierten Vorlagen**

Jetzt erhalten Sie die leistungsstarke Funktion, um benutzerdefinierte Kartenvorlagen zu erstellen. Sie können sie verwenden, um DITA-Maps zusammen mit den Themenvorlagen und Zuordnungsvorlagen zu erstellen, auf die in der Zuordnungsvorlage verwiesen wird.

![Datenvorlagen](assets/dita-templates.png)

Sie können auch auf andere Zuordnungsvorlagen und Themenvorlagen aus der angepassten Zuordnungsvorlage verweisen. Die referenzierten Zuordnungsvorlagen können sich auf verschiedene Zuordnungsvorlagen, Themenvorlagen, Themen, Zuordnungen, Bilder, Videos und andere Assets beziehen.

![Erstellen von Datenvorlagen](assets/create-dita-template.png)

Die benutzerdefinierte Kartenvorlage kann Ihnen dabei helfen, die Zuordnungsvorlagen und die gesamte referenzierte Ordnerstruktur einfach zu replizieren. Diese benutzerdefinierten Vorlagen sind besonders nützlich, um mehrere Karten mit rekursiven Strukturen und Referenzen zu erstellen und neu zu erstellen.

* **Schematron-Unterstützung**
&quot;Schematron&quot;bezieht sich auf eine regelbasierte Validierungssprache, die zum Definieren von Tests für eine XML-Datei verwendet wird. Mithilfe einer Schematron-Datei können Sie bestimmte Regeln definieren und sie dann für ein DITA-Thema oder eine Zuordnung validieren. Der Webeditor unterstützt Schematron-Dateien. Sie können die Schemadateien importieren und sie auch im Web-Editor bearbeiten. Die Schemaunterstützung im Web Editor hilft Ihnen dabei, die Dateien anhand eines Regelsatzes zu validieren und Konsistenz und Korrektheit über die Themen hinweg zu gewährleisten.

![Schematron validieren](assets/schematron-validate.png)

* **Verbessertes Dialogfeld beim Schließen einer Datei**

In AEM Handbüchern werden Sie aufgefordert, Ihre Änderungen zu speichern und Ihre gesperrten Dateien zu entsperren, wenn Sie versuchen, eine im Web Editor geöffnete Datei zu schließen. Die Eingabeaufforderungen werden auf der Grundlage der **Beim Schließen Einchecken anfordern** und **Neue Version beim Schließen anfordern** von Ihrem Administrator konfigurierte Einstellungen.

Basierend auf der Konfiguration erhalten Sie die Option, die Änderungen zu speichern und eine neue Version Ihres Dokuments zu erstellen. Sie können auch die Datei einchecken und die Änderungen in der aktuellen Version speichern.

![Dateischließen](assets/file-close-save-changes-unlock.png)

Weitere Informationen finden Sie unter *Szenarien zum Schließen und Speichern von Dateien* im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.* Die **Suchbegriff einfügen** wurde verbessert. Sie können jetzt einfacher einen Suchbegriff finden, der eingefügt werden soll, da die Suchbegriffe in alphabetischer Reihenfolge aufgelistet sind. Sie können auch nach Keywords suchen, indem Sie eine Suchzeichenfolge in das Suchfeld eingeben.

![Suchbegriff einfügen](assets/insert-keyword.png)

* **Unterstützung für Markdown-Dokumente**
Markdown ist eine einfache Markup-Sprache, mit der Sie Formatierungselemente zu Nur-Text-Dokumenten hinzufügen können. Mit dem Web Editor können Sie Markdown-Dokumente (.md) zusammen mit Ihren DITA-Dokumenten verwenden. Sie können ein Markdown-Dokument einfach im Web-Editor erstellen und in der Vorschau anzeigen und es auch über den DITA-Map-Editor in Ihre Map-Datei einfügen.  Weitere Informationen finden Sie unter 
*Erstellen von Markdown-Dokumenten aus dem Web Editor* Abschnitt im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.

![Support-Markdown](assets/create-markdown-dita-topic.png)

* **Möglichkeit, eine standardmäßige Tag-Ansicht zu konfigurieren**
Wenn ein Benutzer die Tags-Ansicht über den Web-Editor aktiviert, bleibt sie auch während der gesamten Sitzungen aktiviert.  Dies bedeutet, dass Sie die Tag-Ansicht nicht erneut aktivieren müssen, um später darauf zugreifen zu können. Ihr Administrator kann den Standardstatus für die Tag-Ansicht im Web Editor konfigurieren. Der Standardwert für die Tags-Ansicht für die Sitzung eines neuen Benutzers wird durch die Eigenschaft tagsView in der Datei ui_config.json bestimmt.

* Jetzt werden die Dateien in der Repository-Ansicht in Batches geladen. Alle Dateien im Hauptverzeichnis oder `/content/dam folder` aufgelistet sind. Von der nächsten Ebene oder dem sekundären Ordner werden jedoch 75 Dateien gleichzeitig geladen. Diese Stapelladung ist effizient und Sie können schneller auf die Dateien zugreifen, als alle in einem Ordner vorhandenen Dateien zu laden.

![Laden weiterer Dateien](assets/load-more-files.png)

### Neues Grundlinien-Dashboard

AEM Version 4.1 von Guides bietet die Funktion &quot;Grundlinie&quot;, die im Web Editor integriert ist. Sie können jetzt Grundlinien aus dem Web Editor erstellen und diese zum Veröffentlichen oder Übersetzen von Themen aus verschiedenen Versionen verwenden.

**Hinweis**: Für ein aktualisiertes System aktualisieren Sie bitte die neueste **ui_config.json** für das Ordnerprofil.

Verwenden Sie diese Funktion, um eine Grundlinie mit einer bestimmten Version der Themen zu erstellen, die an einem bestimmten Datum und zu einer bestimmten Uhrzeit verfügbar sind. Außerdem erhalten Sie die API-Unterstützung zum Erstellen oder Aktualisieren einer Grundlinie mit einem für eine Themenversion definierten Titel.

![Grundlegende Registerkarte](assets/baseline-manage.png)

Sie können die Dateien anhand von Dateinamen oder Dateispeicherort durchsuchen. Sie können auch die Themen filtern, die im Bearbeitungsfenster der Grundlinie angezeigt werden sollen, und sie nach bestimmten Spalten sortieren.

![Grundlegende Registerkarte](assets/baseline-filter.png)

Die Leistung für die Grundlagenerstellung wurde weiter verbessert. Der Prozess zum Erstellen von Grundlinien ist asynchron, sodass Sie andere Dateien im Web Editor weiter bearbeiten können, während die Grundlinie erstellt wird. Weitere Informationen finden Sie unter *Erstellen und Verwalten von Grundlinien im Web-Editor* im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.

Hinweis: Die Registerkarte &quot;Grundlinie&quot;im Dashboard der Karte ist standardmäßig ausgeblendet. Ihr Administrator kann die Registerkarte &quot;Grundlinie&quot;im Dashboard der Landkarte aktivieren.

* Der Grundlinienparameter in den APIs zum Herunterladen von Landingpages verwendet jetzt den Titel der Grundlinie, um den versionierten Inhalt abzurufen.

### Verbesserter Übersetzungsprozess

* **Möglichkeit zur Erstellung eines Scoping-Übersetzungsprojekts**
Wenn Sie nur den Bereich für die Übersetzung eines Projekts erstellen müssen, können Sie 
**Neues Scoping-Übersetzungsprojekt erstellen**. Dadurch werden die Kopien nicht zur Übersetzung gesendet und der ursprüngliche Übersetzungsstatus der Dateien wird beibehalten.

![Scoping-Übersetzungsprojekt](assets/scoping-translation-project.png)

* Die **Sprachen** zeigt die Sprachordner sowie deren Sprachcodes an. Zum Beispiel Französisch (fr) und Deutsch (de).

![Übersetzungssprache](assets/translation-languages.png)

Weitere Informationen zur Übersetzung finden Sie unter *Übersetzen von Dokumenten aus dem Web Editor* Abschnitt im Handbuch Verwenden von Adobe Experience Manager-Handbüchern.


### Verbesserte Veröffentlichung

* Sie können auch auf die **Dashboard veröffentlichen** im Tab Ausgaben , während Sie die Ausgabe aus dem Mapping-Dashboard generieren. Eine Liste aller aktiven Veröffentlichungsaufgaben ist im Dashboard veröffentlichen verfügbar.

![in die Warteschlange gestellte Ausgaben](assets/queued-output.png)

* Im Landkarten-Dashboard können Sie mehrere DITAVAL-Dateien auswählen, um konditionalisierte Inhalte zu generieren. Sie können die Dateireihenfolge beibehalten, indem Sie Dateien hinzufügen oder löschen. Sie können auch mit dem Mauszeiger über den Dateinamen fahren, um den Pfad im AEM Repository anzuzeigen, in dem die Datei gespeichert ist.

* Grundlinien wurden für die Metadaten AEM Site-Ausgabe berücksichtigt. Sie können die Eigenschaften einer Grundlinienversion auch als Metadaten verarbeiten. Wenn keine Grundlinie definiert ist, werden die Eigenschaften der neuesten Version als Metadaten verarbeitet.

* Die **Dateiname** und **DITA-OT-Befehlszeilenargumente** wurden für HTML5-, EPUB- und benutzerdefinierte Ausgabevorgaben hinzugefügt. Jetzt können Sie den Dateinamen angeben, mit dem Sie die Ausgabe speichern möchten. Sie können auch die zusätzlichen Argumente angeben, die DITA-OT beim Generieren der Ausgabe verarbeiten soll.

### Landkarten-Dashboard

Wenn Sie die DITA-Map herunterladen, wird die Anfrage in die Warteschlange gestellt und Sie erhalten eine Benachrichtigung, sobald die Karte zum Herunterladen bereit ist. Sie können die Zuordnungsdatei sofort herunterladen oder später über den im Posteingang für AEM Benachrichtigungen angegebenen Link herunterladen.

![Map download](assets/download-map-prompt.png)

### Weitere Funktionsverbesserungen

* AEM Guides unterstützen nun die Oxygen XML Author Version 24.1.
* Der Grundlinienparameter in den APIs zum Herunterladen von Landingpages verwendet jetzt den Titel der Grundlinie, um den versionierten Inhalt abzurufen.

### Veraltete Funktion

AEM Guides unterstützen nicht mehr die Generierung des DITA-Ausgabeformats für FrameMaker-Dokumente. Diese DITA-Option wurde auch aus den Ausgabevorgaben des Map-Dashboards entfernt.

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Die Authoring-Unterstützung ist nicht als Alternative für dateipfadbasierte Verweise auf Veröffentlichungen verfügbar. (8076)
* DITA Add on-Paket verhindert die Erkennung von DAM-doppelten Assets. (8417)
* Nach dem Einchecken eines Dokuments von Sauerstoff in AEM wird der japanische Inhalt im Dokument durch Fragezeichen (???) ersetzt. (9124)
* Die ausgecheckten Dateien aktualisieren funktioniert nicht bei der Protokollierung mit Web-Authentifizierung in Oxygen. (9179)
* Die Datei wird beim Öffnen in Sauerstoff nicht ausgecheckt. (9192)
* Nach dem Einchecken eines Dokuments von Sauerstoff in AEM wird der japanische Inhalt im Dokument durch Fragezeichen (???) ersetzt. (9276)
* Webauthentifizierung funktioniert nicht in Sauerstoff. (9296)
* Die Neuladung schlägt in Sauerstoff fehl, wenn die Datei(en) bereits in AEM am selben Speicherort vorhanden ist. (9328)
* Option nicht verfügbar, um Inhalte zwischen AEM und dem lokalen System erzwungen zu synchronisieren. (9439)
* Die ID wird nicht automatisch für das Element generiert, das mit **Wiederverwendbaren Inhalt einfügen** von der sekundären Symbolleiste aus. (5826)
* Beim Hochladen eines Bildes mit demselben Namen wie einer vorhandenen Datei über den Editor wird kein Bestätigungsdialogfeld angezeigt. (6011)
* Ein geschütztes Leerzeichen ist in der Zeichensatzpalette nicht verfügbar. (7523)
* Die Elementliste (Alt+Eingabetaste) wird im dunklen/dunkelsten Design grau dargestellt. (7913)
* Die Version wird beim Speichern der Revision eines Themas in der Symbolleiste des Zuordnungsbereichs nicht aktualisiert. (8228)
* xref kann nicht selbst an gültigen Stellen eingefügt werden. (8354)
* Der Vorgang &quot;getversionlabel&quot;weist Einschränkungen auf und bietet keine erwartete Leistung. (8513)
* Probleme treten beim Bestätigungsdialogfeld beim Schließen einer gesperrten oder bearbeiteten Datei auf, die derzeit nicht im Editor geöffnet ist. (8692)
* Beim Hinzufügen eines Benutzers als Administrator im Ordnerprofil tritt ein Fehler auf, wenn die Benutzer-ID numerisch ist. (8908)
* Das Übersetzungsfenster ist auch beim Öffnen der DITA-Karte im Map Editor sichtbar. (9053)
* Sprachcode wird nicht mit der Sprache im Übersetzungsbereich angezeigt. (9108)
* Die Registerkarten Übersetzung und Grundlinie sind im Dashboard Landkarte für einige Zeit sichtbar. (9146)
* Wenn die Übersetzung abgeschlossen ist, wird eine zusätzliche Version für das übersetzte Asset erstellt. (9310)
* Die validierte Übersetzung wird nicht in die Zielsprache integriert, wenn der Zielsprachcode fünf Zeichen enthält, z. B. `fr_ca`. (9357)
* Übersetzte Inhalte sind fehlerhaft, wenn der erstellte Zielsprachcode als `fr-fr, `, `en-us`. (9527)
* Beim Laden einer DITA-Zuordnung, die sich außerhalb des Sprachordners befindet, wird eine Ausnahme am Backend protokolliert.(9543)
* DITA-Datei kann nicht mit der benutzerdefinierten DITA-Vorlage aus dem Editor erstellt werden. (7262)
* Die DITA-Karte geht beim Veröffentlichen einer UUID-DITA-Karte über FMPS verloren. (7278)
* AEM Guides kopieren nicht die nicht eindeutigen Eigenschaften eines Assets, wenn ein Asset kopiert und eingefügt wird. (8241)
* Der Dateiname der DITA-Zuordnung wird bei der Erstellung nicht in Kleinbuchstaben umgewandelt. (8383)
* Eine Beschreibung der Prüfungsaufgabe wird nicht in der E-Mail-Benachrichtigung angezeigt, die gesendet wird, wenn eine neue Prüfungsaufgabe zugewiesen wird. (8507)
* Landkarte-API herunterladen | Temporäre Ordner werden nicht bereinigt, falls beim Download Fehler auftreten. (8523)
* `columnpreview.jsp` ist von SP abhängig.  (8543)
* Ausgabeaufträge mit dem Status &quot;Warten&quot;oder &quot;Ausführen&quot;werden im Dashboard &quot;Veröffentlichen&quot;nicht bereinigt.  (8569)
* Standardsymbol, das beim Generieren eines Berichts mithilfe der Schaltfläche Erzeugen ausgewählt wird, selbst wenn die Symboleigenschaft definiert ist. (8573)
* Beim Upgrade von 3.8.X auf 4.0 treten Probleme im Überprüfungsprozess auf. (8788)
* Wenn ein Benutzername lang ist, werden die Symbole, die angenommen/abgelehnt werden, im Überprüfungsfenster des Web Editors nicht klar angezeigt. (8793)
* Der Referenzbaum bricht nach dem Entfernen eines Themas und dem Ausführen eines Verschiebevorgangs ab. (8804)
* Benutzerdefinierte DTD, die vom Benutzer definiert wird, hat keinen Vorrang vor standardmäßiger DITA-DTD, die in DITA-OT eingebettet ist. (9104)
* Die Position der Markierung ist in der Seitenansicht falsch. (9305)
* Die Fußnote &quot;Verwendung nach Referenz&quot;scrollt nicht zum Fußnote-Abschnitt in AEM Site-Ausgabe. (9061)
* Die Reihenfolge der Fußnoten ist in der Ausgabe der AEM Site falsch. (9327)
* Neu erstellte DITA-Assets werden immer von einem anderen Benutzer ausgecheckt. (9387)
* Fehler wird bei der Erstellung neuer Inhalte immer protokolliert. (9388)
* Der dritte Bildschirm im Erstellungsprozess einer Prüfungsaufgabe zeigt nicht die Liste der Glossare an. (4558)
* Beim Hochladen mehrerer Dateien aus FrameMaker/Sauerstoff Connector wurden falsche UUID-Referenzen zugewiesen. (8269)
* Wenn eine Prüfungsaufgabe im Posteingang neu zugewiesen wird, wird keine E-Mail-Benachrichtigung gesendet. (8376)
* Der zweite Administrator-Benutzer kann nicht als erster Administrator-Benutzer zu einem Ordner hinzugefügt werden. (8430)
* **Beschriftungen anwenden** auf der Registerkarte &quot;Grundlinie&quot;werden keine Beschriftungen in der Dropdown-Liste angezeigt. (8455)
* Bei Verwendung der Grundlinien-Veröffentlichung mit dem Bild als conref im Thema wird das Bild nicht in der Ausgabe veröffentlicht. (8564)
* Die Bereinigungsfunktion für die Ausgabe schlägt fehl, wenn eine große Anzahl von Knoten des Ausgabestverlaufs vorhanden ist. (8568)
* Im Bedienfeld Versionsverlauf zeigt der aktuelle Versionsabschnitt einen falschen Zeitstempel an und wurde durch Informationen geändert. (8765)
* Die Grundlinie wird nicht anhand des definierten Titels aktualisiert. (8799)
* Fehler tritt auf, wenn Dateien, deren übergeordneter Ordner Sonderzeichen im Dateinamen enthält, in Sauerstoff geöffnet werden (mithilfe der **In Sauerstoff bearbeiten** Schaltfläche). (8918)
* Das Hochladen von Dateien aus Sauerstoff in AEM schlägt fehl. (9157)
* Download-Map mit Grundlinie funktioniert nicht, wenn der Inhalt in einen anderen Ordner verschoben wird. (9331)
* Oxygen überprüft eine falsche Version eines Themas, nachdem eine Version in AEM zurückgesetzt wurde. (9411)
* Die Suche im Bereich &quot;Repository&quot;und das Browserdialogfeld &quot;topicref&quot;frieren den Bildschirm ein, wenn der Inhalt groß ist. (9432)
* Wenn die Einstellung **Neue Version für hochgeladene Datei erstellen** auf EIN gesetzt ist, wird eine neue Version erstellt, wenn auf einem beliebigen eingefrorenen Knoten der Modus zurückgesetzt und gespeichert wird. (9473)
* Beim Zurücksetzen einer Dateiversion werden in der Assets-Benutzeroberfläche falsche Unterschiede beim Zeitstempel angezeigt. (9480)
* Dateien werden beim Zurücksetzen auf eine beliebige Version automatisch ausgecheckt. (9482)
* Das Sperrsymbol wird in der Repository-Ansicht angezeigt, selbst wenn die Datei im Editor eingecheckt wurde.  (5756)
* Über die Autorenansicht des Webeditors können in einer Bookmap keine Vordergrund- und Hintergrundelemente hinzugefügt werden. (7652)
* Der Vorschaumodus unterstützt nicht `deliveryTarget` bedingtes Verarbeitungsattribut in DITA. (7685)
* AEM beim Öffnen eines Glossarthemas im XML-Editor erzwingt, es zu speichern, auch wenn es nicht geändert wurde. (8105)
* Das Dialogfeld Referenzen einfügen wird beim Hinzufügen von Subjekten zu einer Zuordnung über die Benutzeroberfläche geöffnet. (8212)
* Wiederverwenden des Inhaltsbereichs Abstürze bei der Suche nach Sonderzeichen `[` oder `*` .(8279)
* Beim Authoring-Glossar zeigt der Web Editor den Inhalt als Hinweis an. (8384)
* Der XML-Editor entfernt Zeilenumbrüche im Codeblock. (8522)
* Beim Wechseln zwischen Quell- und Autorenmodus wird das Thema als verschmutzt markiert und der Inhalt muss erneut gespeichert werden.(8524)
* Ein entsperrtes Thema kann nicht geschlossen werden. (8545)
* Es gibt keine Option zum Auswählen des Knowledgebase-Pfads in artikelbasierten Veröffentlichungsvorgaben. (8636)
* Beim Hinzufügen eines Kapitels zu einer Lesekarte über Drag &amp; Drop aus der Favoriten-Ansicht fehlen Attribute. (8746)
* Das Dialogfeld &quot;Suchbegriff einfügen&quot;verfügt nicht über die Suchfunktion und Suchbegriffe werden nicht in sortierter Reihenfolge aufgelistet. (9094)
* Wenn Sie eine Suche im XML-Editor durchführen, friert die Seite ein. (9452)
* Sites fehlen in AEM Vorgaben auf der Registerkarte &quot;Ausgabe&quot;. (9567)
* SVG von Bildern, die in den Autorenmodi des XML-Editors nicht korrekt dargestellt werden. (9426)
* Die Grundlinie wird beim Veröffentlichen über Salesforce nicht berücksichtigt. (8953)
* Die Möglichkeit, die Rootmap aus den Einstellungen der Benutzereinstellungen zu löschen, ist nicht vorhanden. (8534)
