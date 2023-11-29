---
title: Versionshinweise | Neue Funktionen in der Adobe Experience Manager-Anleitung, Version Dezember 2023
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im Dezember 2023.
source-git-commit: 9fcc8faec4631d710dbdfd7e4f8567069d0ba120
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Neue Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service vom Dezember 2023

Dieser Artikel behandelt die neuen und verbesserten Funktionen in der Version Dezember 2023 der Adobe Experience Manager-Handbücher (später auch als *Experience Manager Guides as a Cloud Service*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](release-notes-2023.12.0.md).


## Variablen in der nativen PDF-Ausgabe verwenden

Sie können Variablensätze verwenden, um Informationen dynamisch einzufügen und zu verwalten, die sich basierend auf bestimmten Bedingungen wie Produktnamen und Versionen ändern können. Mit dieser Funktion können Sie dasselbe PDF-Layout verwenden und Ausgaben mit unterschiedlichen Werten generieren. Sie müssen nicht für jeden Wertesatz separate Layouts erstellen.

Sie können beispielsweise für jedes Produkt einen Variablensatz erstellen. Dieser Variablensatz kann aus Variablen für verschiedene Produktdetails wie ProductName, VersionNumber und ReleaseDate bestehen. Anschließend können Sie für diese Variablen unterschiedliche Werte hinzufügen.

**Variable festgelegt 1: Adobe-set1**

* ProductName: Experience Manager-Handbücher
* VersionNumber: 2311
* Releasedatum: 20.11.2023

**Variable festgelegt 1: Adobe-set2**

* ProductName: Experience Manager-Handbücher
* VersionNumber: 2310
* ReleaseDate: 27.09.2023


![native PDF-Variablen](assets/native-pdf-variables.png){width="800" align="left"}

*Erstellen Sie Variablen auf der Registerkarte &quot;Ausgabe&quot;im Web Editor.*

Sie können auch Variablen mit Werten mit HTML-Tags erstellen. Fügen Sie beispielsweise Bilder aus dem Inhalts-DAM hinzu, indem Sie die `<img>` -Tag.

Nachdem Sie die Variablen erstellt haben, können Sie die Variablen mithilfe der Seitenlayouts in den Ausgabevorlagen zu den entsprechenden Stellen im Dokument hinzufügen. Die Werte werden automatisch in der PDF-Ausgabe basierend auf dem in der Ausgabevorgabe ausgewählten Variablensatz ausgewählt.



<img src="./assets/native-pdf-variable-output.png" alt="Fußzeile in PDF-Ausgabe" width="500" border="2px">

*Generieren Sie die native PDF-Ausgabe mithilfe von Variablen im PDF-Layout.*

Mit dieser Funktion können Sie benutzerdefinierte Ausgaben mit dynamischen Inhalten in Ihrer Dokumentation generieren und Änderungen effizient verwalten. Sie können auch Stile anwenden und HTML Markup verwenden, um die Variablen zu formatieren.

Sie können die Werte für jeden beliebigen Variablensatz auch schnell aktualisieren, wann immer dies erforderlich ist, und die Ausgabe neu generieren. Wenn Sie beispielsweise die Details für eine Version aktualisieren müssen, können Sie den Wert der Version in VersionNumber aktualisieren und die Ausgabe neu generieren.


## Umgestaltetes Erlebnis zur Bearbeitung der Attribute

Jetzt erhalten Sie ein überarbeitetes Erlebnis, um die Attribute für ein Element aus der **Inhaltseigenschaften** im Web Editor angezeigt.

![Bedienfeld &quot;Attribute&quot;](assets/attributes-multiple-properties.png){width="300" align="left"}

*Fügen Sie im Bereich &quot;Inhaltseigenschaften&quot;Attribute hinzu.*

Sie können die Attribute auch einfach bearbeiten und löschen.

Weitere Informationen finden Sie im Abschnitt **Inhaltseigenschaften** Funktionsbeschreibung innerhalb der [Rechter Bereich](../user-guide/web-editor-features.md#id2051EB003YK) Abschnitt.


## Bearbeiten von Metadaten beim Authoring

Jetzt können Sie beim Authoring die Metadaten-Tags der Datei mithilfe des Dropdown-Menüs **Dateieigenschaften** im rechten Bereich. Sie können auch **Weitere Eigenschaften bearbeiten** , um weitere Metadaten zu aktualisieren.

![file-properties](assets/file-properties-general.png){width="300" align="left"}

*Aktualisieren Sie die Metadaten und bearbeiten Sie die Dateieigenschaften im rechten Bereich.*

Weitere Informationen finden Sie im Abschnitt **Dateieigenschaften** Funktionsbeschreibung innerhalb der [Rechter Bereich](../user-guide/web-editor-features.md#id2051EB003YK) Abschnitt.

## Möglichkeit der Veröffentlichung von Inhalten in der ServiceNow-Wissensdatenbank

Sie können Ihre Inhalte jetzt auch in der ServiceNow Knowledge Base-Plattform veröffentlichen.

Mit der Version von Dezember 2023 können Sie als Administrator ein Veröffentlichungsprofil für den ServiceNow Knowledge Base-Server erstellen. Als Autor oder Herausgeber können Sie dann dieses ServiceNow-Veröffentlichungsprofil in der Ausgabevorgabe auswählen, um die Ausgabe in der angegebenen Wissensdatenbank zu veröffentlichen.

Mit dieser Funktion können Sie Inhalte wie Text, Videos und Bilder in der ServiceNow Knowledge Base-Plattform veröffentlichen und ein umfassendes Repository verwalten.


![Service now Knowledge Base-Vorgabe](assets/knowledgebase--output-preset.png){width="300" align="left"}

*Erstellen Sie eine Ausgabevorgabe für die ServiceNow-Wissensdatenbank.*


## Verbessertes Landkartenkollektions-Dashboard

Experience Manager-Handbücher bieten ein erweitertes Dashboard für die Zuordnungssammlung. In einer Zuordnungssammlung können Sie die Metadateneigenschaften für die DITA-Maps schnell stapelweise konfigurieren. Diese Funktion ist praktisch, da Sie die Metadateneigenschaften nicht für jede DITA-Zuordnung einzeln aktualisieren müssen.

Jetzt können Sie den Dateinamen der DITA-Map anzeigen. Sie können auch die Grundlinien anzeigen. Auf diese Weise können Sie schnell die für eine Vorgabe verwendete Grundlinie finden.

![Sammlungs-Dashboard zuordnen](assets/map-collection-dashboard.png){width="800" align="left"}

*Anzeigen, Bearbeiten und Generieren der Ausgabe über das Dashboard der Zuordnungssammlung.*

## Anzeigen von Schlüsselattributen in der Kartenansicht

Wenn Sie Schlüsselattribute für das Thema oder die Zuordnungsreferenzen definieren, können Sie auch den Titel, das entsprechende Symbol und den Schlüssel im linken Bereich anzeigen. Der Schlüssel wird angezeigt als `key=<key-name>`.

Weitere Informationen finden Sie im Abschnitt **Kartenansicht** Funktionsbeschreibung in [Linke Leiste](../user-guide/web-editor-features.md#id2051EA0M0HS) Abschnitt.

![Schlüssel in der Kartenansicht](assets/view-key-title-map-view.png) {width="300" align="left"}

*Zeigen Sie das Schlüsselattribut in der Kartenansicht an.*

## Möglichkeit, eine Grundlinie basierend auf der Bezeichnung zu duplizieren

Experience Manager-Handbücher bieten jetzt ein verbessertes Benutzererlebnis zum Erstellen der Grundlinien im Web-Editor.\
![Erstellen neuer Grundlinien](assets/create-new-baseline.png) {width="300" align="left"}
*Erstellen Sie eine Grundlinie im Web Editor.*

Außerdem können Sie damit eine Grundlinie basierend auf der Bezeichnung duplizieren. Die Referenzversion wird beim Duplizieren anhand der angegebenen Bezeichnung ausgewählt (sofern vorhanden) oder wählt die Version aus der duplizierten Grundlinie aus.


![Grundlinie duplizieren ](assets/duplicate-baseline.png) {width="300" align="left"}

*Duplizieren Sie eine Grundlinie basierend auf einem Titel oder erstellen Sie eine exakte Kopie.*

## Verbesserter Prozess für die Erstellung der Massen-Aktivierungszuordnung

Die Erstellung einer Massen-Aktivierungskarten-Sammlung ist jetzt harmonischer. Wenn nun die Seite Aktivierungsergebnisse angezeigt wird, können Sie die Ergebnisse der Aktivierung und Protokolle anzeigen.
Weitere Informationen finden Sie unter [Erstellen einer Massen-Aktivierungszuordnung](../user-guide/conf-bulk-activation-create-map-collection.md).



## Auflösen von Cross-Map-Links in der Ausgabe der AEM Site

Cross-Map-Links (XREF mit Perimeter Peer), die in der AEM Site-Ausgabe gerendert werden, werden jetzt gemäß dem Dateinamen des Veröffentlichungskontexts aufgelöst, der für die generierte Zuordnung festgelegt wurde.


## URL der Ausgabe der AEM Site zur Verwendung des Dokumenttitels konfigurieren

Mit Experience Manager-Handbüchern können Sie als Administrator die URL der AEM Site-Ausgabe konfigurieren. Wenn der Dateiname nicht vorhanden ist oder alle Sonderzeichen enthält, können Sie konfigurieren, dass er in der URL der AEM Site-Ausgabe durch ein Trennzeichen ersetzt wird. Sie können sie auch durch den Namen des ersten untergeordneten Themas ersetzen. Erfahren Sie, wie [die URL der AEM Site-Ausgabe zur Verwendung des Dokumenttitels konfigurieren](../cs-install-guide/conf-output-generation.md#configure-the-url-of-the-aem-site-output-to-use-the-document-title).

