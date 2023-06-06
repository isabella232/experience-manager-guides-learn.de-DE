---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version Februar 2023
description: Februar-Version der Adobe Experience Manager-Handbücher as a Cloud Service
source-git-commit: 4bb9ce2690a2e76a5b2a93b65db7dd452e15d295
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 0%

---


# Neue Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im Februar 2023

Dieser Artikel behandelt die neuen und verbesserten Funktionen in Version Februar 2023 der Adobe Experience Manager-Handbücher (später auch als *AEM as a Cloud Service Handbücher*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie in der [Versionshinweise](release-notes-2023.2.0.md) Artikel.


## Generieren von Berichten über den Web-Editor

AEM Guides verfügen über eine Funktion im Web Editor, mit der Sie die Gesamtvollständigkeit Ihrer technischen Dokumente überprüfen und Berichte für diese erstellen können.
Sie können die Themenliste anzeigen, die Metadaten verwalten und die in allen Referenzen für die aktuelle Karte verwendeten Multimedia-Dateien aus dem
**Berichte** im Web Editor.

**Ansicht &quot;Topic List&quot;generieren**

Sie können die Themenliste generieren, die detaillierte Informationen zu Ihren Themen enthält, z. B. den Referenztyp, den Dokumentstatus und den Autor. Sie können auch die CSV-Datei generieren, um die aktuelle Momentaufnahme der Themen in der DITA-Map herunterzuladen.

**Metadaten verwalten und Dokumentstatus ändern**

Sie können Tags auf ein einzelnes Thema anwenden oder die Bulk-Tagging-Funktion verwenden, um mehrere Tags auf mehrere Themen, eine DITA-Zuordnung oder eine Unterzuordnung anzuwenden. Sie können auch den Dokumentstatus aller ausgewählten Themen in den nächsten möglichen allgemeinen Dokumentstatus ändern.

<img src="assets/web-editor-metadata-panel.png" alt="Verwalten von Metadaten" width="600">

**Multimedia-Bericht erstellen**

Sie können einen Multimedia-Bericht erstellen, der detaillierte Informationen über die in Ihren Referenzen verwendeten Multimedia-Dateien enthält. Sie haben die Flexibilität, die im Bericht aufgelisteten Multimedia-Dateien zu filtern und zu sortieren.
Sie können auch die CSV-Datei generieren, um die aktuelle Momentaufnahme der in der DITA-Map verwendeten Multimedia-Dateien herunterzuladen.

<img src="assets/web-editor-reports-multimedia.png" alt="Multimedia-Bericht" width="600">

## UX für die Überprüfungsfunktion überarbeitet

Jetzt bieten AEM Handbücher eine verbesserte UX, mit der Sie die Themen, die zur Überprüfung freigegeben wurden, überprüfen können. Im neuesten Erlebnis bietet die Überprüfungsfunktion die folgenden Verbesserungen:

* Die Benutzeroberfläche wurde aktualisiert
* Bereich &quot;Bedingungen&quot;, in dem Sie den Inhalt gemäß den verfügbaren Bedingungen im Thema hervorheben können
* Jeder Kommentar im Kommentarbereich ist mit dem entsprechenden Text im aktuellen Thema verknüpft. Sie können damit den kommentierten Text identifizieren.
* Die Kommentare werden in der Reihenfolge des kommentierten Texts im Dokument angezeigt.
* Der Name der Prüfungsaufgabe wird im Überprüfungs-Workflow angezeigt.
* Wählen Sie die Rootmap für die Überprüfungsaufgabe aus, die zur Auflösung aller wichtigen Verweise und Glossarbegriffe verwendet wird, die im Überprüfungsinhalt verwendet werden.
* Kontextuelle Symbolleiste, die Ihnen beim schnellen Hervorheben oder Durchstreichen von Text hilft
* Menü &quot;Optionen&quot;zum Bearbeiten oder Löschen eigener Kommentare
* Für veraltete Kommentare haben Sie Zugriff auf eine nebeneinander liegende Ansicht, die Ihnen hilft, die vorherige Version des Themas mit der aktuellen Reviewversion zu vergleichen.
* Bei Verwendung der Filter werden die Kommentare im rechten Bereich entsprechend der Auswahl gefiltert und die Anzahl der Kommentare im linken Bereich wird entsprechend aktualisiert.


   <img alt="Prüfungsaufgabe" src="assets/comment-pop-up-panel.png" width="600">



## Verbesserungen bei der Übersetzung

Jetzt verfügen Sie über benutzerfreundlichere Verbesserungen im Dashboard &quot;Übersetzung&quot;, die Ihnen die einfache Übersetzung Ihrer Dokumente aus dem Web-Editor erleichtern.

**Übergeben der Versionsbezeichnung an die Zielversion**

Mit AEM Guides können Sie den Titel der Quelldatei an die Zieldatei übergeben. Auf diese Weise können Sie die Quellversion der übersetzten Datei leicht identifizieren.

<img alt="Übersetzungstitel" src="assets/translation-pass-source-label.png" width="600">

Wenn Sie beispielsweise Quelldateien mit der Versionsbeschriftung Release 1.0 auf sie angewendet haben, können Sie auch die Quellbeschriftung (Release 1.0) an die übersetzte Datei übergeben.

**Synchronisierung für nicht synchronisierte Assets erzwingen**

Wenn Sie Änderungen an einigen Assets vornehmen, kennzeichnet AEM Guides diese als nicht synchronisiert. Sie können die geänderten Assets entweder erneut übersetzen oder den Status Nicht synchronisiert verwerfen auswählen. Wenn Sie beispielsweise einige kleinere Änderungen vorgenommen haben, die eigentlich keine Übersetzung benötigen, können Sie ihren Status als In Sync markieren.

<img src="assets/translation-version-diff.png" alt="Übersetzungsbüro" width="600">

**In Bearbeitung befindliche Übersetzungsprojekte für ein Thema oder eine Zuordnung anzeigen**

Einige Verweise auf Ihr Übersetzungs-Dashboard werden möglicherweise ausgeführt. Jetzt bietet AEM Guides eine Funktion, mit der Sie die Liste aller laufenden Übersetzungsprojekte (zusammen mit der Zielsprache) anzeigen können, die die ausgewählte Referenz enthalten.


## Generieren von Ausgaben in verschiedenen Formaten über den Web Editor

Jetzt können Sie die Ausgabe für Ihre Themen oder DITA-Maps einfach im Web Editor generieren. Sie können verschiedene Ausgabevorgaben wie AEM Site, PDF, HTML5, JSON (Headless-Ausgabeformat) und benutzerdefinierte Ausgabe konfigurieren. Sie können diese dann verwenden, um die entsprechenden Ausgaben zu generieren.

Sie können Attribute in Ihren DITA-Themen definieren und dann die Bedingungsvorgabe verwenden, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Sie können auch die Funktion Grundlinien-Veröffentlichung verwenden, um eine bestimmte Version Ihrer DITA-Map oder Ihres Themas selektiv zu veröffentlichen.


## Suchen und Ersetzen von Text auf Zuordnungsebene

Mit AEM Guides können Sie nach Dateien in einer Zuordnung suchen, die bestimmten Text enthalten. Der gesuchte Text wird in den Dateien hervorgehoben. Jetzt können Sie das gesuchte Wort oder die gesuchte Wortgruppe in allen Dateien durch ein anderes Wort oder eine andere Wortgruppe ersetzen. Sie können **Alle ersetzen** rechts oben in der Liste, um alle Vorkommen des gesuchten Begriffs in allen Dateien zu ersetzen.

<img src="assets/map-find-replace.png" alt="map find replace" width="600">

## Löschen und Duplizieren von Dateien aus dem Repository-Bereich

Jetzt können Sie einfach ein Duplikat oder eine Kopie einer Datei aus der **Optionen** Menü der ausgewählten Datei im Repository-Bereich. Standardmäßig wird die Datei mit einem Suffix erstellt (wie `filename_1.extension`).

<img src="assets/options-menu-repo-view-file-level.png" alt="Menü für Dateioptionen " width="500">


## Weitere Verbesserungen am Webeditor

* In AEM Handbüchern können Sie über das Kontextmenü einige gängige Vorgänge für Bilder und Mediendateien ausführen. Jetzt können Sie auch das ausgewählte Bild oder Medium im Repository suchen oder die Vorschau der Datei in der Assets-Benutzeroberfläche anzeigen.

* Der Name des aktuellen Ordnerprofils wird als Beschriftung für das Symbol Benutzereinstellungen in der Hauptsymbolleiste angezeigt. Auf diese Weise können Sie das Ordnerprofil identifizieren, an dem Sie gerade arbeiten.

* Wenn Sie eine Karte in der Kartenansicht öffnen, wird der Titel der aktuellen Karte in der Mitte der Hauptsymbolleiste angezeigt. Dies ist hilfreich, um den Benutzern mitzuteilen, welche Karte derzeit geöffnet ist.


## Anzeigen des Titels anstelle der UUID im Sauerstoffeditor

Jetzt können Sie AEM Guides auswählen **Verwenden von Titel in Editor und Maps Manager** in den Einstellungen. Wenn Sie diese Option auswählen, wird der Titel der Datei auf der Registerkarte der Datei angezeigt, wenn er im Editor oder im DITA Maps Manager geöffnet wird. Wenn Sie diese Option nicht auswählen, wird die UUID der Datei auf der Registerkarte der Datei angezeigt.

## Microservice-basierte Veröffentlichung für AEM Handbücher as a Cloud Service

Mit dem neuen Publishing-Microservice können Sie große Veröffentlichungsarbeitslasten gleichzeitig auf AEM Handbüchern as a Cloud Service ausführen und die branchenführende Server-lose Plattform von Adobe I/O Runtime nutzen.

Für jede Veröffentlichungsanforderung AEM Handbücher führt as a Cloud Service einen separaten Container aus, der entsprechend den Benutzeranforderungen horizontal skaliert wird. Dadurch können Sie mehrere Veröffentlichungsanfragen ausführen und eine verbesserte Leistung erzielen.

Weitere Informationen finden Sie unter [Neue mikrodienstbasierte Veröffentlichung für AEM Guides as a Cloud Service konfigurieren](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/publishing/configure-microservices.md).

## Native PDF | Hinzufügen eines benutzerdefinierten Lesezeichens in der PDF-Ausgabe

Jetzt können Sie ein benutzerdefiniertes Lesezeichen zu einem bestimmten Inhalt in Ihrer endgültigen PDF-Ausgabe hinzufügen, um die Navigation zu erleichtern. Dies würde zum TOC hinzugefügt, das aus den Themen- oder Abschnittstiteln in Ihrer DITA-Map erstellt wird.

## Native PDF | Anwenden eines benutzerdefinierten Stils auf Inhaltsverzeichniseinträge und Themeninhalte

AEM Guides bieten die Möglichkeit, benutzerdefinierte Stile auf die TOC-Einträge oder ein bestimmtes Thema in der PDF-Ausgabe anzuwenden. Sie können beispielsweise die Textfarbe im Inhaltsverzeichnis und den Titel des Themas ändern. Sie können auch Stile auf den gesamten Inhalt innerhalb des Themas anwenden.


## Native PDF | Formatieren der Seitenmarkierung in der Fußnote-Komponente

Jetzt können Sie die Seitenmarkierung in den Fußnoten gestalten. Sie können beispielsweise Klammern hinzufügen oder ihre Farbe ändern. Diese Stile helfen Benutzern, die Seitenmarkierungen im Dokument einfach zu identifizieren.

## Native PDF | Änderungsleiste zur Anzeige geänderter Themen im Inhaltsverzeichnis

Mit AEM Guides können Sie jetzt die geänderten Themen im Inhaltsverzeichnis der PDF-Ausgabe schnell identifizieren.  Er zeigt eine Änderungsleiste links von den geänderten Themen im Inhaltsverzeichnis an. Sie können auf das Thema im Inhaltsverzeichnis klicken und die detaillierten Änderungen anzeigen.

<img src="assets/change-marker-toc.png" alt="Markierung im Inhaltsverzeichnis ändern " width="500">

