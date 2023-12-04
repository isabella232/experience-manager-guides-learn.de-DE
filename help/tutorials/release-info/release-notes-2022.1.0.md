---
title: Versionshinweise für [!DNL AEM Guides], Version Januar 2022
description: Januar-Version [!DNL Adobe Experience Manager Guides] as a Cloud Service
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '2441'
ht-degree: 0%

---

# Januar-Version [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Aktualisierung auf die Januar-Version

Aktuelles Upgrade durchführen [!DNL Adobe Experience Manager Guides] as a Cloud Service (später genannt) [!DNL AEM Guides] as a Cloud Service Einrichtung) durch Ausführen der folgenden Schritte:
1. Sehen Sie sich den Git-Code des Cloud Service an und wechseln Sie zu der Verzweigung, die in der Cloud Service-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
1. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Service-Git-Codes auf 2022.1.78.
1. Übertragen Sie die Änderungen und führen Sie die Cloud Service-Pipeline aus, um auf die Januar-Version von zu aktualisieren. [!DNL AEM Guides] as a Cloud Service.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die von [!DNL AEM Guides] as a Cloud Service Version Januar 2022.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
| | |


### Sauerstoffanschluss

| [!DNL AEM Guides] Cloud-Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2022.1.0 | 2.4.0 | 2.4.0 | 2,2 | 2,2 |
|  |  |  |  |  |


## Neue Funktionen und Verbesserungen

### Artikelbasierte Veröffentlichung

Mit der Januar-Version haben wir eine artikelbasierte Veröffentlichungsfunktion eingeführt, die im Web Editor integriert ist. Sie können die Funktion zur artikelbasierten Veröffentlichung verwenden, um schrittweise die Ausgabe eines oder mehrerer Themen zu generieren oder Ihre Inhalte auf einer Wissensdatenbankplattform zu veröffentlichen.

Mit dieser Funktion können Benutzer die DITA-Map in einer additive Art erstellen und Themen veröffentlichen, sobald sie bereit sind. Nachdem Sie Ihre Karte veröffentlicht haben, verwenden Sie die Funktion zur artikelbasierten Veröffentlichung , um nur die aktualisierten Artikel inkrementell zu veröffentlichen.

![Artikelbasierte Veröffentlichung](assets/article-based-publishing.png)

Zusätzlich zu AEM können Sie diese einzigartige Funktion verwenden, um Ihre Artikel in allen Wissensdatenbank-Portalen wie Salesforce zu veröffentlichen. Diese Funktion enthält auch eine OOTB-Inhaltsvorlage, die auf AEM Kernkomponenten aufbaut und mit der Sie ein wissensbasiertes Repository der technischen Inhalte erstellen können. Das Beste an dieser Vorlage ist, dass sie vollständig an Ihre organisatorischen Anforderungen angepasst werden kann und auch Anwendungsfälle wie Unternehmens-Intranet-Portale unterstützen kann.
Sie können die Artikel auch nach ihrem Dokumentstatus und ihrer Änderungszeit filtern.

Diese bedarfsbasierte On-the-Go-Veröffentlichung für Artikel ermöglicht Ihnen nicht nur die vollständige Kontrolle über Ihre Inhaltsveröffentlichung, sondern reduziert auch die Gesamtdauer für die Veröffentlichung aktualisierter Inhalte.
Wenn Sie Ihre Artikel mit dieser Vorlage veröffentlichen, können die Metadaten auch an Ihre veröffentlichten Seiten übergeben werden.
Weitere Informationen finden Sie unter *Artikelbasierte Veröffentlichung im Web Editor* im Benutzerhandbuch.

### Verbesserter Web-Editor

Es gibt viele Verbesserungen und neue Funktionen, die im Web Editor eingeführt werden:

* Im Web-Editor wurde auch das Thema-Schema unterstützt. Sie können nun mithilfe des Bedienfelds &quot;Betreff-Schema&quot;ein Subjekt-Schema erstellen und verwenden. Mit dem Zusatz des Betreffschemas können Sie jetzt eigene Unternehmenmetadaten und Taxonomie verwenden.

![Betrifft](assets/subject-scheme-panel.png)

* In dieser Version wurde ein neues Glossar-Hotspot-Tool eingeführt, um Glossare stapelweise zu verwalten. Mit diesem Tool können Sie schnell Text in Glossar und Glossar in Begriffe in großen Mengen für ausgewählte Karten oder offene Themen konvertieren.

![Glossar-Hotspot](assets/glossary-hotspot-tool.png)

* Neue Aktualisierungsfunktion im Bereich Wiederverwendbare Inhalte , mit der Sie den wiederverwendbaren Inhalt in Referenzdateien schnell aktualisieren können.
* Die neue Arbeitskopie-Anzeige zeigt an, ob Ihre aktuelle (Arbeitskopie) Datei mit der gespeicherten Version synchronisiert ist oder nicht.

![Versionskennung](assets/version-update-indicator.png)

* Der Suchfilter im Dialogfeld &quot;Repository-Bedienfeld&quot;und &quot;Dateisuche&quot;wurde verbessert, um weitere Filteroptionen zu erhalten, die weiter angepasst werden können.

![Suchfilter im Repository](assets/repository-filter-search.png)

* Sie können jetzt DOCX-Dateien vom Web Editor hochladen.

### Autor mit FrameMaker

Jetzt können Sie Ihre Dokumente auf FrameMaker erstellen und veröffentlichen. FrameMaker wird mit einem vordefinierten Anschluss an Adobe Experience Manager geliefert. In FrameMaker erhalten Sie eine benutzerfreundliche Oberfläche, die es Ihnen ermöglicht, in einer verteilten und kollaborativen Umgebung Versionen Ihrer Dokumente zu verwalten.

Nachdem Sie Ihren Inhalt erstellt haben, können Sie mit FrameMaker Ihre Dokumente in verschiedenen Formaten - PDF, HTML5, EPUB und DITA - veröffentlichen. Sie können auch die verschiedenen Dateiverwaltungsvorgänge ausführen, z. B. Checkout, Checkout mit abhängigen Elementen, Einchecken, Aktualisieren usw.
Für Autoren mit FrameMaker in [!DNL AEM Guides] as a Cloud Service Verwendung FrameMaker-Version 2020.4 und höher.

### Neues Übersetzungs-Dashboard

Im Web-Editor wurde ein neues Übersetzungs-Dashboard mit folgenden Funktionen eingeführt:

* Sortieren, Suchen und Filtern von Themenlisten
* Inhalt nach Referenztyp filtern - direkte oder indirekte Verweise.
* Einfache Navigation zum Auffinden eines vorhandenen Projekts beim Initiieren einer Übersetzungsanforderung.
* Es wurde ein mehrsprachiger Übersetzungsmechanismus eingeführt, um zu verhindern, dass mehrere Projekte für jede Sprache erstellt werden, wenn eine Übersetzungsanforderung für mehrere Sprachen initiiert wird.
* Es wurde eine Konfiguration zum Ausblenden der Registerkarte &quot;Übersetzung&quot;im Zuordnungs-Dashboard eingeführt. Standardmäßig ist sie sichtbar. Sie können Inhalte entweder über das Landkarten-Dashboard oder den Web-Editor übersetzen.

![Übersetzungs-Dashboard](assets/translation-from-web-editor.png)

### Verbesserte Veröffentlichung

* Autoren können jetzt Metadaten auf Zuordnungs- und Themenebene an die DITA-OT-Veröffentlichung übergeben. Dies ist hilfreich, wenn benutzerdefinierte PDF-Vorlagen für die Verwendung von Dateimetadateneigenschaften wie Tags, Autor, Dokumentstatus und mehr entwickelt wurden.

![DITA-OT-Metadaten](assets/custom-meta-data-output-preset.png)

* Es wurde eine neue Konfiguration hinzugefügt, mit der Benutzer die Versionen der Themen beibehalten oder löschen können, die beim Löschen gelöscht werden **Löschen und Erstellen** wird bei der Generierung der AEM Site-Ausgabe verwendet.

### Verbesserte Dateiverarbeitung

Beim Arbeiten mit Dateien in AEM Assets sind jetzt folgende Verbesserungen zu sehen:
* Es wurden ein neues Erlebnis für den Datei-Upload und ein neues Dialogfeld zur Auswahl einer Konfliktbeilegungsstrategie eingeführt.

![Konflikt beim Datei-Upload](assets/file-upload-name-conflict.png)

* Möglichkeit, eine neue Version der hochgeladenen Datei zu erstellen, um zu verhindern, dass eine ausgecheckte Datei überschrieben wird.
* Jetzt können Sie eine Vorschau der Bilder direkt in der Ansicht Versionsverlauf anzeigen. Außerdem zeigt der Versionsverlauf für DITA- und Nicht-DITA-Dateien die aktuellen Versionsinformationen separat an.

![Miniaturansicht des Versionsverlaufs](assets/version-history-preview-image.png)

* Wenn der Benutzer eine DITA-Datei erstellt, wird der standardmäßige Dateiname in Kleinbuchstaben angezeigt, sodass er mit dem Szenario der Erstellung nativer AEM übereinstimmt.

### Neue Berichtsexportfunktion

Berichte sind sehr nützlich, um die Gesundheit Ihrer Inhalte zu identifizieren. [!DNL AEM Guides] as a Cloud Service bietet verschiedene Berichte zur Inhaltskontrolle. Jetzt können Sie nicht nur die Berichte anzeigen, sondern auch die Berichtsdaten in eine CSV-Datei exportieren, um sie anzuzeigen und für Ihr größeres Team freizugeben. Berichtsdaten geben Ihnen einen schnellen Überblick über fehlerhafte Links oder fehlende Bilder.

![Export von Berichten](assets/export-report.png)

### Verbesserte Oxygen DAM-Aktualisierungserfahrung

Wenn Sie Dateien von AEM Server in Sauerstoff aktualisieren, wird eine Warnmeldung angezeigt, wenn Sie nicht gespeicherte Dateien in Ihrer aktuellen Sauerstoffsitzung haben. Sie können den Aktualisierungsvorgang abbrechen, um nicht gespeicherte Dateien zu speichern. Ohne diese Funktion verloren Benutzer nicht gespeicherte Informationen in ihren Dokumenten.


### Weitere Funktionsverbesserungen

* Sie können jetzt eine neue **Dita-Projekt** Vorlage unter **/apps/projects/templates** Pfad.
* Laden Sie jetzt die Standardeinstellung herunter **ui_config.json** -Datei aus Ihren Ordnerprofilen. Dies kann verwendet werden, um benutzerdefinierte Änderungen aus den vorhandenen **ui_config.json** -Datei während der Aktualisierung.
* Sie müssen den Browser-Cache nicht löschen, selbst wenn neue Versionen von JS-Dateien vorhanden sind.

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Web-Editor

* Conrefs erscheinen in roter Farbe, selbst wenn sie nicht beschädigt sind. (8239)
* Der Wert für das bedingte Attribut wird nicht automatisch ausgefüllt, wenn im DITAVAL-Editor die Option Alle Eigenschaften hinzufügen ausgewählt ist. 8234)
* Autoren können kein Bild mithilfe des relativen Pfads in ein Thema einfügen. (8112)
* Überprüfen Sie die Aufgabenseite, auf der die Multimedia-Dateien nicht angezeigt werden, wenn im Dateinamen Leerzeichen vorhanden sind. 8111
* Die in Tabellenzellen hinzugefügte Ph-conref wird in roter Farbe angezeigt. (8083)
* Links in Prüfungsaufgaben werden nicht aktualisiert, wenn die zu überprüfenden Dateien verschoben werden. (8080)
* Der Web Editor rendert Bilder nicht korrekt, deren Skalierungseigenschaft auf 75 % oder höher festgelegt ist. (8073)
* GIF-Bilder werden im Web Editor als statische Bilder gerendert. (8024)
* Ein conkeyref in einem notenelement wird weder in der Webeditor-Vorschau noch in der Ausgabe angezeigt. (8006)
* xref zu einem Element hinzu, das selbst ein conref ist, wird im Editor nicht aufgelöst. (7933)
* Titel mit Schlüssel werden in der Editor-Vorschau und im Repository-Bedienfeld nicht korrekt wiedergegeben. (7909)
* Snippets mit Sonderzeichen werden nicht korrekt gespeichert. (7908)
* Das Speichern eines Themas nach der Formatierung von MathML-Gleichungen führt zu einem Fehler. (7954)
* keydef mit (tm) werden nicht ordnungsgemäß im Editor gerendert und die AEM Site-Ausgabe enthielt doppelte TM-Symbole. 7859
* Das Ziehen und Ablegen eines Snippets funktioniert gemäß den DTDs nicht. (7758)
* HTML ignoriert benutzerdefinierte definierte Abmessungen für Grafiken. (7718)
* Das Attribut conrefend wird beim Verschieben der Quelldatei nicht aktualisiert. (7698)
* Die Arbeit mit Dokumenten vom Typ Referenzthema führt zu mehreren Problemen in der Benutzeroberfläche. (7656)
* DITAVAL-Dateien werden nicht angezeigt, wenn der Autor ditavalref in einer Zuordnung hinzufügt. (7594)
* Unerwarteter Speicherplatz in jedem leeren Feld `<entry>` Element, wenn das Attribut outputClass hinzugefügt wird `<tgroup>` -Element. (7532)
* Die Schaltfläche Quelle funktioniert nicht für Themen, die über das Zuordnungs-Dashboard geöffnet werden. 7465)
* Pretty Print fügt leere Linien und Leerzeichen ein, die sichtbar sind, wenn die Datei in FrameMaker oder Sauerstoff geöffnet wird. (7408)
* Maps mit href=&quot;/&quot; in einem der Themen veröffentlichen nicht auf AEM Sites. (7405)
* Leistungsprobleme, die im Editor auftreten, wenn die Stammzuordnung über eine große Anzahl von Keydefekten verfügt. (7400)
* Der Dokumentstatus für eine Zuordnung mit einer benutzerdefinierten Vorlage wird nicht vom entsprechenden Statusprofil übernommen. 7359
* `<tm>` -Element falsch als Blockelement gerendert. (7286)
* Doppelte Vorlagen werden bei der Erstellung einer neuen Vorlage im Bedienfeld Bearbeitungsvorlagen angezeigt. (5814)
* In ui_config definierte Vorlagen für Bilder zum Festlegen eines zusätzlichen Attributs gelten nicht für Drag-and-Drop-Fälle. (5713)
* Falsches standardmäßiges Erscheinungsbild von uicontrol in der Menukaskade. 5483
* Benutzerdefinierte Vorlagen für Themen/Landkarten zeigen in der Benutzeroberfläche keinen neuen Namen an. Der Name wird als &quot;Thema&quot;/&quot;Karte&quot;angezeigt, anstatt den konfigurierten Namen anzuzeigen. (4958)
* Möglichkeit, die Rootmap aus den Einstellungen der Benutzereinstellungen zu löschen. 8534
* Eine neu erstellte Zuordnungssammlung wird nicht aufgeführt, selbst wenn die Seite aktualisiert wurde.(8603)
* Entsperrtes Thema kann nicht geschlossen werden. (8545)
* Beim Wechseln zwischen Quell- und Autorenmodus wird das Thema als verschmutzt markiert und der Inhalt muss erneut gespeichert werden.8524)
* Wiederverwenden des Inhaltsbereichs Abstürze bei der Suche nach Sonderzeichen `[` oder `*` .8279)
* Der Cursor wird nicht in der Suchleiste angezeigt, wenn das Dialogfeld &quot;Element einfügen&quot;mit dem Tastaturbefehl Alt+Eingabetaste geöffnet wird.(7912)
* Die Suchoption sucht nur in Dateinamen und nicht im Inhalt. 7784)


### Sauerstoffanschluss

* Dateien, deren übergeordneter Ordner Sonderzeichen enthält, geben beim Laden in Sauerstoff Fehler. 8054)
* Wenn ein neu erstelltes Dokument in Sauerstoff geöffnet wird, wird der Fehler &quot;GUID kann nicht gefunden werden&quot;ausgegeben. (7856)
* Die Option &quot;Einchecken&quot;ist deaktiviert, nachdem die Datei unter Verwendung von &quot;In Sauerstoff bearbeiten&quot;aus AEM ausgecheckt wurde. (7471)


### Überprüfung

* Die Echtzeit-Synchronisierung funktioniert nicht für Kommentare. (7661)

### Landkarten-Dashboard

* Der Conref-Inhalt kann nicht im Titel eines Themas auf der Registerkarte &quot;Themen oder Berichte&quot;des Map-Dashboards angezeigt werden. (8263)
* AEM Sites-Ausgabe | jcr:title der generierten Site-Seite wird nicht aktualisiert, wenn der DITA-Thementitel aktualisiert wird. (8131)
* Download-MAP lädt die in den Themen verwendeten Videodateien nicht herunter. (8070)
* Mediendateien werden nicht heruntergeladen, wenn das Objekt-Tag über die Download-Bookmap-API verwendet wird. (8057)
* Der falsche Bericht wird auf der Registerkarte Berichte angezeigt, wenn ein Thema eine Referenz zu einer Datei hat, deren Titel mit conref beginnt. (4698)
* Das Dialogfeld &quot;Beschriftungen anwenden&quot;auf der Registerkarte &quot;Grundlinie&quot;zeigt keine Beschriftungen in der Dropdown-Liste an. 8455

### Veröffentlichung

* Die PDF-Erstellung schlägt beim ersten Mal fehl, wenn die Option Versionierung aktivieren ausgewählt ist. (8053, 8294)
* Das Leerzeichen wird in AEM Site-Ausgabe automatisch nach dem Tag &quot;tm;&quot;hinzugefügt. 7964)
* YouTube-Videos können nicht in AEM Site-Ausgabe angezeigt werden. (7401)
* Das Filtern nach Titel schlägt für referenzierte Inhalte fehl, nachdem der Benutzer auf alle Themen auf der Registerkarte &quot;Grundlinie&quot;des Map-Dashboards klickt. 7388)
* Thema mit Element veröffentlichen `<tm>` Der Eigenschaftswert SM oder reg wird in der generierten Ausgabe falsch angezeigt. 7239.
* Bei der Grundlinienveröffentlichung mit dem Bild wird die neueste Version des Bildes in der veröffentlichten Ausgabe nicht ausgewählt. (7231)
* Verknüpfungsfähige referenzierte Themen werden auf der Registerkarte &quot;Grundlinie&quot;angezeigt. 5424
* Die inkrementelle Veröffentlichung für ein Thema mit &quot;conkeyref&quot;im Titel funktioniert nicht erwartungsgemäß. 4474)
* Der Seitentitel wird nicht für die Ausgabe-URL-Generierung verwendet, obwohl diese Einstellung aktiviert ist. 8257
* Grundlinien-Publishing zur Auswahl der aktuellen Version der Bilder anstelle des eingefrorenen Knotens Dies wird auch angezeigt, wenn ein Bild Leerzeichen oder Sonderzeichen im Dateinamen enthält. (8274, 8322)
* Die inkrementelle Veröffentlichung schlägt bei DITA-Maps mit dem Typ &quot;subject schema&quot;mit mapref fehl. (8218)
* Null wird hinzugefügt, sobald eine Zuordnung zum Massen-Veröffentlichungs-Dashboard hinzugefügt wird. (8695)
* Bei Verwendung der Grundlinien-Veröffentlichung mit dem Bild als conref im Thema wird das Bild nicht in der Ausgabe veröffentlicht. (8564)
* Die Veröffentlichung schlägt mit einer Ausnahme fehl, wenn die Grundlinie, die für AEM Website-Veröffentlichung verwendet wird, gelöscht wird. (8572)
* Die Themenregeneration funktioniert nicht. (8091)
* Es gibt Probleme mit der Veröffentlichung von Fußnoten in Tabellen. (4709)

### AEM Assets

* Leistungsprobleme bei der Auswahl/Löschung eines riesigen Inhaltssatzes in der Assets-Benutzeroberfläche. (8238)
* Die Funktion &quot;Gespeicherte Suche&quot;(Smart-Sammlung) beschädigt, wenn DITA-Eigenschaft zu Suchfiltern hinzugefügt wird. (8048)
* Das Zurücksetzen des Bildes auf eine ältere Version funktioniert nicht. (DXML-7903)
* Die Löschoption ist auch für Autoren sichtbar, die keine Berechtigung zum Löschen haben. (7322)
* Die CCMS-Überlagerung für den Assets-Editor unterbricht das Rendering der Löschoption. (8093)
* Das Dokumentprofil wird nicht gelöscht. (8604)
* Verweise funktionieren nicht mit &quot;Alle auswählen&quot;und verschieben den multimedia/Dita_Content in einen anderen Ordner. (8621)
* Beim Verschieben der Assets treten in der Quelle falsche Verweise auf. (8627)
* Die feste Listenansicht wird nicht geladen. (8542)

### Inhaltsimport

* HTML zu DITA-Konversion | Die Tabelle mit &quot;tr&quot;mit leeren &quot;td&quot;-Einträgen führt zu zusätzlichen Zeilen in der Ausgabe. (8132)
* HTML zu DITA-Konversion | HTML mit einer Tabelle mit mehreren Textteilen schlägt mit Ausnahme fehl. (7940)
* HTML zu DITA-Konversion | Fehler bei Quell-HTML-Kommentaren. (7937)
* Beim Importieren von DITA 1.3 DITA-Dateien werden einige href in fehlerhafte Links umgewandelt. (8019)

## Bekannte Probleme

Adobe hat die folgenden bekannten Probleme für [!DNL AEM Guides] as a Cloud Service Version Januar 2022.


### Bekannte Probleme mit Problemumgehung

Verwenden Sie die bereitgestellte Problemumgehung für die folgenden bekannten Probleme:

* Die Webauthentifizierung funktioniert nicht für den Oxygen-Connector in Mac.
  **Workaround**: Verwenden Sie zunächst den Sauerstoff-Connector unter Windows.

* Im Firefox-Browser können die Überprüfungskommentare nicht importiert werden, ohne die Ansicht nebeneinander zu öffnen.
  **Workaround**: Verwenden Sie zunächst den Chrome-Browser.

* Verweise werden beim Verschieben von Bildern oder Multimedia-Dateien mit Leerzeichen in den Dateinamen nicht berücksichtigt.
  **Workaround**: Benennen Sie die Datei um und entfernen Sie die Leerzeichen aus dem Dateinamen, bevor Sie sie verschieben.

* Das Zuordnungs-Dashboard wird nicht zeitweise in die neueste Version des Chrome-Browsers geladen.
  **Workaround**: Aktualisieren Sie die Landkarten-Dashboard-Seite.

### Andere bekannte Probleme

* Wenn Oxygen mit [!DNL AEM Guides] -Lösung mit Web-Authentifizierung verwendet, schlägt die Abmeldung fehl.
* Überprüfungsaufgaben können den Benutzern nicht neu zugewiesen werden.
* Probleme treten in der Benutzeroberfläche für die Zuordnungssammlung auf, da der Text verzerrt ist und **Alle auswählen** funktioniert nicht ordnungsgemäß.
