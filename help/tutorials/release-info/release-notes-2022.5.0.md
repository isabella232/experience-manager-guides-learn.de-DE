---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version Mai 2022
description: Adobe Experience Manager-Handbücher as a Cloud Service im Mai
exl-id: 7928a300-5ec9-492c-b9be-02b6f87638c6
source-git-commit: 0f5c1cabdbda9fa2606f67faedbf9a38ca1ec0aa
workflow-type: tm+mt
source-wordcount: '1874'
ht-degree: 4%

---

# Adobe Experience Manager-Handbücher as a Cloud Service im Mai

## Aktualisierung auf die Mai-Version

Aktualisieren Sie Ihre aktuellen Adobe Experience Manager-Handbücher as a Cloud Service (später als *AEM as a Cloud Service Handbücher*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2022.5.144.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die as a Cloud Service Version der AEM im Mai zu aktualisieren.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service vom Mai 2022 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
|  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac |
| --- | --- | --- |
| 2022.5.0 | 2,6,9 | 2,6,9 |
|  |  |  |


## Neue Funktionen und Erweiterungen

AEM Guides as a Cloud Service bietet viele Verbesserungen und neue Funktionen in der Mai-Version:

### Verbesserter Web-Editor

* **Erstellen von Karten basierend auf benutzerdefinierten Vorlagen**

Jetzt erhalten Sie die leistungsstarke Funktion, um benutzerdefinierte Kartenvorlagen zu erstellen. Sie können sie verwenden, um DITA-Maps zusammen mit den Themenvorlagen und Zuordnungsvorlagen zu erstellen, auf die in der Zuordnungsvorlage verwiesen wird.

![Datenvorlagen](assets/dita-templates.png)

Sie können auch auf andere Zuordnungsvorlagen und Themenvorlagen aus der angepassten Zuordnungsvorlage verweisen. Die referenzierten Zuordnungsvorlagen können sich auf verschiedene Zuordnungsvorlagen, Themenvorlagen, Themen, Zuordnungen, Bilder, Videos und andere Assets beziehen.

![Erstellen von Datenvorlagen](assets/create-dita-template.png)

Die benutzerdefinierte Kartenvorlage kann Ihnen dabei helfen, die Zuordnungsvorlagen und die gesamte referenzierte Ordnerstruktur einfach zu replizieren. Diese benutzerdefinierten Vorlagen sind besonders nützlich, um mehrere Karten mit rekursiven Strukturen und Referenzen zu erstellen und neu zu erstellen.

* Die **Suchbegriff einfügen** wurde verbessert. Sie können jetzt einfacher einen Suchbegriff finden, der eingefügt werden soll, da die Suchbegriffe in alphabetischer Reihenfolge aufgelistet sind. Sie können auch nach Keywords suchen, indem Sie eine Suchzeichenfolge in das Suchfeld eingeben.

![Suchbegriff einfügen](assets/insert-keyword.png)

* Jetzt werden die Dateien in der Repository-Ansicht in Batches geladen. Es werden 75 Dateien gleichzeitig geladen. Diese Stapelladung ist effizient und Sie können schneller auf die Dateien zugreifen, als alle in einem Ordner vorhandenen Dateien zu laden.

![Laden weiterer Dateien](assets/load-more-files.png)

* Sie können SVG-Bilder rendern, die eingebettete Daten oder Links in allen Bildschirmen des XML-Editors enthalten, einschließlich, aber nicht beschränkt auf Vorschau und Autorenansicht.

* Die standardmäßige XSD/DTD kann auf die neueste Version aktualisiert werden

### Verbesserter Übersetzungsprozess

* **Möglichkeit zur Erstellung eines Scoping-Übersetzungsprojekts**
Wenn Sie nur den Bereich für die Übersetzung eines Projekts erstellen müssen, können Sie 
**Neues Scoping-Übersetzungsprojekt erstellen**. Dadurch werden die Kopien nicht zur Übersetzung gesendet und der ursprüngliche Übersetzungsstatus der Dateien wird beibehalten.

![Scoping-Übersetzungsprojekt](assets/scoping-translation-project.png)

* Wenn Sie die Übersetzung für ein oder mehrere Themen in einem Übersetzungsauftrag ablehnen, wird der Status In Bearbeitung der Übersetzung aller abgelehnten Themen wieder auf den ursprünglichen Status zurückgesetzt.

* Die **Sprachen** zeigt die Sprachordner sowie deren Sprachcodes an. Zum Beispiel Französisch (fr) und Deutsch (de).

* Die Übersetzungsfunktion unterstützt jetzt auch den Sprachcode, der sowohl Land als auch Sprache enthält. Beispiel, `fr-fr`, `en-us`.

![Übersetzungssprache](assets/translation-languages.png)

* Beim Laden einer DITA-Zuordnung, die sich außerhalb des Sprachordners befindet, wird keine Ausnahme am Backend protokolliert.

Weitere Informationen zur Übersetzung finden Sie unter *Übersetzen von Dokumenten aus dem Web Editor* unter Verwenden von Adobe Experience Manager-Handbüchern as a Cloud Service.


### Verbesserte Veröffentlichung

* Sie können auch auf die **Dashboard veröffentlichen** im Tab Ausgaben , während Sie die Ausgabe aus dem Mapping-Dashboard generieren. Eine Liste aller aktiven Veröffentlichungsaufgaben ist im Dashboard veröffentlichen verfügbar.

![in die Warteschlange gestellte Ausgaben](assets/queued-output.png)

* Im Landkarten-Dashboard können Sie mehrere DITAVAL-Dateien auswählen, um konditionalisierte Inhalte zu generieren. Sie können die Dateireihenfolge beibehalten, indem Sie Dateien hinzufügen oder löschen. Sie können auch mit dem Mauszeiger über den Dateinamen fahren, um den Pfad im AEM Repository anzuzeigen, in dem die Datei gespeichert ist.

* **Veraltete Funktion**
AEM as a Cloud Service unterstützt nicht mehr die Generierung des DITA-Ausgabeformats für FrameMaker-Dokumente. Diese DITA-Option wurde auch aus den Ausgabevorgaben des Map-Dashboards entfernt.

### Verbesserte artikelbasierte Veröffentlichung

Der XML-Editor bietet die Möglichkeit, einem Artikel mehrere Produktkategorien zuzuordnen, während er in einem Salesforce-Profil veröffentlicht wird.

### Weitere Funktionsverbesserungen

* Der Vorschaumodus unterstützt auch `deliveryTarget` bedingtes Verarbeitungsattribut in DITA. Er ist als Option im Dropdown-Filter zusammen mit **audience**, **platform**, **product**, Props, **andere Props**.
* Es wurde die Option zur erzwungenen Synchronisation zwischen dem AEM-Server in Oxygen und dem lokalen System bereitgestellt.

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Im Überprüfungsfenster des Webeditors kann der Benutzer nicht auf die Überprüfungskommentare antworten. (9667)
* Das Programm wird beim Klicken auf einen leeren Ordner nach dem Aktualisieren über das Menü Optionen leer angezeigt. (9639)
* Eine neue Version wird erstellt, wenn wir **Speichern und schließen** die eingecheckte Datei. (9638)
* Die Schaltfläche &quot;Schließen&quot;wird nicht angezeigt, wenn **Als neue Version speichern** aktiviert ist. (9637)
* Die richtige PDF wird nicht veröffentlicht, wenn sie zunächst über eine separate PDF für jedes Kapitel und dann über eine einzelne PDF-Datei veröffentlicht wird (separate PDF-Dateien erstellen ist deaktiviert). (9632)
* Das Zuordnungs-Dashboard gibt für Benutzer, die keine Administratoren sind, ein Metadatenproblem aus. (9620)
* Nachdem eine Grundlinie erstellt wurde, wird der Status in der Benutzeroberfläche auf &quot;Fehlgeschlagen&quot;(Abrufen des Statusaufrufs schlägt fehl) gesetzt, wenn der Server mehr als 10.000 Dateien hat. (9608)
* Das Speichern großer Daten in Eigenschaften führt zu einem Veröffentlichungsfehler, da der Aufspaltungs-Veröffentlichungs-Workflow fehlschlägt. (9586)
* Der Status &quot;Bedingte Attribute: Filter&quot;wird beim Wechseln zwischen Vorschau zu Quelle und dem Modus Vorschau nicht beibehalten. (9553)
* Der Name der Lesekarte wird in der Repository-Ansicht leer angezeigt, falls kein Name über die `mainbooktitle` -Tag. (9538)
* HTTP 400-Fehler tritt beim Öffnen einer mit Sauerstoff hochgeladenen Datei auf. (9535)
* Die Vorgaben einer zuvor geöffneten Karte bleiben beim Öffnen einer Karte ohne definierte Vorgaben auf der Registerkarte &quot;Ausgabe&quot;sichtbar. (9523)
* Die Suchfunktion für Tags und Attribute funktioniert nicht im Bedienfeld &quot;Kontur&quot;. (9506)
* Neu erstellte Sammlung ist erst sichtbar, nachdem der Browser aktualisiert wurde. (9505)
* Beschriftungen für bedingte Attribute (nicht die Werte) werden beim Hinzufügen aller Bedingungen über die Option &quot;Alle Eigenschaften hinzufügen&quot;im Quellmodus angezeigt. (9501)
* Dateien werden beim Zurücksetzen auf eine beliebige Version automatisch ausgecheckt. (9482)
* Beim Zurücksetzen einer Dateiversion werden in der Assets-Benutzeroberfläche falsche Unterschiede beim Zeitstempel angezeigt. (9480)
* Beim Einfügen von Elementen in das topicref -Element der DITA Map werden mehrere Elemente aus Suchergebnissen hinzugefügt. (9474)
* Wenn die Einstellung **Neue Version für hochgeladene Datei erstellen** auf EIN gesetzt ist, wird eine neue Version erstellt, wenn auf einem beliebigen eingefrorenen Knoten der Modus zurückgesetzt und gespeichert wird. (9473)
* Der Anzeigetext der Schlüsselreferenz und der Inhaltsschlüsselreferenz wird beim Ändern der Link-URL nicht beibehalten, wenn beim Definieren der Schlüsselreferenz kein Anzeigetext hinzugefügt wird. (9458)
* Im Versionsverlauf werden Versionsnummer und Titel für die aktuelle Version nicht angezeigt. (9446)
* Der Editor friert ein, wenn bestimmte Inhaltsdateien im Editor geöffnet werden. (9443)
* Die Suche im Bereich &quot;Repository&quot;und das Browserdialogfeld &quot;topicref&quot;frieren den Bildschirm ein, wenn der Inhalt groß ist. (9432)
* Die an AEM Site-Ausgabe übergebenen Metadaten berücksichtigen nicht die Grundlinie des Inhalts. (9416)
* Oxygen überprüft eine falsche Version eines Themas, nachdem eine Version in AEM zurückgesetzt wurde. (9411)
* Fehlgeschlagene Grundlinie deaktiviert die Bearbeitung im Tab Vorgabe des Zuordnungs-Dashboards. (9403)
* Fehler wird bei der Erstellung neuer Inhalte immer protokolliert. (9388)
* Neu erstellte DITA-Assets werden immer von einem anderen Benutzer ausgecheckt. (9387)
* Das Umbenennen eines Elements funktioniert beim Konvertieren von topicref in glossref nicht ordnungsgemäß. (9380)
* Versionsbeschriftung wird nicht als Dropdown-Liste angezeigt in **Als neue Version speichern** angezeigt. (9379)
* Bedingungen werden beim Wechseln zwischen verschiedenen Versionen von nicht angewendet **Diff anzeigen** Dropdown-Liste. (9366)
* Bei der Verwendung von Vorschaufiltern treten mehrere Probleme auf. (9365)
* Nicht-DITA- und DITAVAL-Assets können nicht in topicref eingefügt werden. (9363)
* Die validierte Übersetzung wird nicht in die Zielsprache integriert, wenn der Zielsprachcode fünf Zeichen enthält, z. B. `fr_ca`. (9357)
* Es ist nicht möglich, Dateien mit **Suchen von Dateien im Ordner** von **Weitere Optionen** und die App reagiert nicht mehr. (9337)
* Das Dialogfeld &quot;Durchsuchen&quot;hängt, wenn eine große Anzahl von Schlüsseln vorhanden ist. (9332)
* DITAVAL-Dateien funktionieren nicht bei der artikelbasierten Veröffentlichung. (9330)
* Die Reihenfolge der Fußnoten ist in der Ausgabe der AEM Site falsch. (9327)
* Die Suche wird nicht automatisch durchgeführt, wenn der Auswahlpfad geändert wird. (9323)
* Wenn die Übersetzung abgeschlossen ist, wird eine zusätzliche Version für das übersetzte Asset erstellt. (9310)
* Die Administrator-Benutzer im Ordnerprofil können nicht gelöscht werden. (9306)
* Die über die Inhaltsschlüsselreferenz aktualisierte Stammzuordnung wird erst festgelegt, nachdem die Seite aktualisiert wurde. (9302)
* Webauthentifizierung funktioniert nicht in Sauerstoff. (9296)
* Weblinks mit kodierten Zeichen funktionieren nicht ordnungsgemäß. (9227)
* Die Datei wird beim Öffnen in Sauerstoff nicht ausgecheckt. (9217)
* Die ausgecheckten Dateien aktualisieren funktioniert nicht bei der Protokollierung mit Web-Authentifizierung in Oxygen. (9179)
* Die Registerkarten Übersetzung und Grundlinie sind im Dashboard Landkarte für einige Zeit sichtbar. (9146)
* Beim erneuten Laden des Ordnerprofils treten Erlebnis- oder Funktionsprobleme auf. (9103)
* Beim Löschen des Seitenlayout-Editors wird er nicht im mittleren Bereich der Autorenansicht geschlossen. (9087)
* Im Web Editor tritt beim Entfernen eines Bildes und anschließenden Speichern der neuen Version des Dokuments ein Validierungsfehler auf. (8985)
* Es kann nicht alle `glossrefs` im Glossarbereich (inhaltsspezifisch). (8886)
* `xref` in der artikelbasierten Veröffentlichungsausgabe wird kein Text angezeigt. (8764)
* Verweise werden beim Verschieben von Bildern oder Multimedia-Dateien mit Leerzeichen in den Dateinamen unterbrochen. (8624)
* Verweise wechseln die Auswahl `Select All` und verschieben Sie die Multimedia-Dateien oder DITA-Inhalte in einen anderen Ordner. (8622)
* Ausgabeaufträge mit dem Status &quot;Warten&quot;oder &quot;Ausführen&quot;werden im Dashboard &quot;Veröffentlichen&quot;nicht bereinigt.  (8569)
* Die Bereinigungsfunktion für die Ausgabe schlägt fehl, wenn eine große Anzahl von Knoten des Ausgabestverlaufs vorhanden ist. (8568)
* DITA Add on-Paket verhindert die Erkennung von DAM-doppelten Assets. (8417)
* Schaltfläche Prüfungsaufgabe erstellen für Nicht-DITA-Dateien aktiviert. (8401)
* Das Dialogfeld Referenzen einfügen wird beim Hinzufügen von Subjekten zu einer Zuordnung über die Benutzeroberfläche geöffnet. (8212)
* Unerwarteter Speicherplatz in jedem leeren Feld `entry` Element, wenn das Attribut outputClass hinzugefügt wird `tgroup` -Element. (7532)
* Im Repository-Bereich werden nach Abschluss der Aktion keine Symbole für die Dateisperre angezeigt, die ein- oder ausgecheckt wurden. (5817)
* Das Sperrsymbol wird in der Repository-Ansicht angezeigt, selbst wenn die Datei im Editor eingecheckt wurde.  (5756)
* Sites fehlen in AEM Vorgaben auf der Registerkarte &quot;Ausgabe&quot;. (9567)
* Der XML-Editor hängt davon ab, einige DITA-Dateien zu bearbeiten. (9537)
* Wenn Sie eine Suche im XML-Editor durchführen, friert die Seite ein. (9452)
* Download-Map mit Grundlinie funktioniert nicht, wenn der Inhalt in einen anderen Ordner verschoben wird. (9331)
* Die Neuladung schlägt in Sauerstoff fehl, wenn die Datei(en) bereits in AEM am selben Speicherort vorhanden ist. (9328)
* Die Position der Markierung ist in der Seitenansicht falsch. (9305)
* Nach dem Einchecken eines Dokuments von Sauerstoff in AEM wird der japanische Inhalt im Dokument durch Fragezeichen (???) ersetzt. (9276)
* Das Hochladen von Dateien aus Sauerstoff in AEM schlägt fehl. (9157)
* Wenn eine Prüfungsaufgabe im Posteingang neu zugewiesen wird, wird keine E-Mail-Benachrichtigung gesendet. (8376)

## Bekannte Probleme

Beim Öffnen des Editors wird immer wieder eine leere Seite angezeigt.
