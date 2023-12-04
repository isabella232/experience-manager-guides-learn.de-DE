---
title: Versionshinweise | Aktualisierungsanweisungen und behobene Probleme in der Adobe Experience Manager-Version 4.3.0
description: Erfahren Sie mehr über die Fehlerbehebungen und das Upgrade auf Version 4.3.0 der Adobe Experience Manager-Handbücher.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 1%

---

# Version 4.3.0 von Adobe Experience Manager-Handbüchern (Juli 2023)

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version 4.3.0 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in Version 4.3.0 von Adobe Experience Manager-Handbüchern](./whats-new-4.3-release.md).

## Aktualisierung auf Version 4.3.0 der AEM Handbücher


Sie können Ihre aktuelle Version von AEM Guides einfach auf Version 4.3.0 aktualisieren. Bevor Sie mit der Aktualisierung auf Version 4.3.0 von AEM Guides fortfahren, müssen Sie die folgenden Punkte beachten: Sie können Ihre aktuelle Version von AEM Guides auf Version 4.3.0 aktualisieren.

- Wenn Sie Version 4.2 oder 4.2.x verwenden, können Sie direkt auf Version 4.3.0 aktualisieren.
- Wenn Sie Version 4.1 oder 4.1.x verwenden, müssen Sie auf Version 4.2 oder 4.2.x aktualisieren, bevor Sie auf Version 4.3.0 aktualisieren.
- Wenn Sie Version 4.0 verwenden, müssen Sie vor der Aktualisierung auf Version 4.3.0 auf Version 4.2 aktualisieren.
- Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0 aktualisieren, bevor Sie auf Version 4.2 aktualisieren.
- Wenn Sie eine Version vor 3.8.5 verwenden, finden Sie im Abschnitt AEM Upgrade-Handbuch im produktspezifischen Installationshandbuch weitere Informationen.



>[!NOTE]
>
>Sie müssen AEM Service Pack installieren, bevor Sie AEM Guides-Version aktualisieren.

Weitere Informationen finden Sie unter [Upgrade-Anweisungen](../install-guide/upgrade-xml-documentation.md).

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides 4.3.0 unterstützt werden.

### Adobe Experience Manager

**4.3.0 Nicht-UUID**
Version 6.5 Service Pack 18, 17, 16, 15 oder 14

**4.3.0 UUID**
Version 6.5 Service Pack 18, 17, 16, 15 oder 14

Weitere Informationen finden Sie unter *Technische Anforderungen* im Handbuch &quot;Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern&quot;.

### FrameMaker und FrameMaker Publishing Server

| Freigabe | FMPS 2022 | FMPS 2020 | FM 2022 | FM 2020 |
| --- | --- | --- | --- | --- |
| 4.3.0 (Nicht-UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.3 oder höher |
| 4.3.0 (UUID) | 2022 oder höher | 2020.2 oder höher* | 2022 oder höher | 2020.4 oder höher |
| | | | |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

### Sauerstoffanschluss

| Freigabe | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- |--- |--- |
| 4.3.0 (Nicht-UUID) | 2.3-normal-5 | 2.3-normal-5 | 1,6 | 1,6 |
| 4.3.0 (UUID) | 3.0-uuid-4 | 3.0-uuid-3 | 2,3 | 2,3 |
|  |  |   |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

### Authoring

- Die Themendatei ist im Web Editor nicht entsperrt, obwohl die Option Datei entsperren und die Option Nicht speichern ausgewählt sind. (12558)
- Eine Datei kann nicht im Web Editor ausgecheckt werden, obwohl die Option NO ausgewählt wurde, um die Änderungen vor dem Einchecken zu verwerfen. (12557)
- Die QuickInfos für die Symbole zum Sperren und Entsperren von Dateien in der Hauptsymbolleiste des Web-Editors stimmen nicht mit den in der Repository-Ansicht angezeigten Symbolen überein.(12555)
- Die Option Auschecken abbrechen und Entsperren wird für eine Datei im Web Editor angezeigt, die noch nicht in der Kartenansicht ausgecheckt ist. (12556)
- Die PDF-Assets können nicht in den vorhandenen &quot;topicref&quot;-Links ausgewählt werden. (12477).
- Beim Zusammenführen und Aufteilen in den Tabellen generiert AEM Guides 4.2 zusätzliche Tabellenzellen. (11793)
- In der Repository-Ansicht können Themen oder Bilder nicht nach Verwendung der Such-/Filterfunktion gezogen werden. (12396)
- Suchergebnisse werden im Bereich Suchen und Ersetzen deaktiviert, nachdem eine durchsuchte Datei geöffnet wurde. (12142)
- Die 8-Taste auf der Seitentastatur funktioniert nicht im AEM Guides-Editor. (12106)
- Inline-/Display-Attribute werden nicht in der Layout-Ansicht des Web-Editors angezeigt. (12498)
- Die Konfiguration der globalen Profil-Benutzeroberfläche stimmt nicht mit dem Ordnerprofil überein. (11970)
- Inhaltsreferenzen sind beim Kopieren und Einfügen von DITA-Dateien fehlerhaft. (1959)
- Inhaltsfragment kann nicht in der Spaltenansicht bearbeitet werden, wenn AEM Guides installiert sind. (7342)
- Der Inhalt geht verloren, wenn sich eine entpackte xref unter einem untergeordneten Element-Tag befindet. (12532)
- Der Genehmigungs-Workflow funktioniert nicht, wenn in den Dateieigenschaften des rechten Bedienfelds document in &quot;end state&quot;geändert wird. (11026)
- Asset-Benutzeroberfläche | In der Listenansicht sind die überlagerten verfügbaren Spalten nicht zusammenführbar. (11528)
- Keyref ist in der Kartenansicht nicht aufgelöst. (11490)
- Das obere Menü wird nicht angezeigt, wenn Sie durch den XML-Editor navigieren. (10868)
- `conref` im ph-Tag | Das angezeigte Dialogfeld zum Durchsuchen ist falsch. 9481)
- Lokale Links zu anderen Elementen werden im Web Editor nicht aufgelöst. (8790)
- Die Funktion Matches() funktioniert in der Schematron-Funktion nicht. (11224)



### Verwaltung

- Das Feld &quot;title&quot;in den Metadateneigenschaften von DITA-Maps wird von `<title>` -Element für die Zuordnung. (10702)
- Wenn Sie versuchen, die Version der Themen in der Grundlinie zu öffnen oder zu aktualisieren, wird der Lader &quot;Informationen vom Server abrufen&quot; unbegrenzt ausgeführt.(12478)


### Überprüfung

- Neue Überprüfungsbenutzeroberfläche | Die Bedingungen markieren und zeigen Verstecken funktioniert anders als im Web-Editor. (11628)

### Veröffentlichung

- Die Veröffentlichung schlägt beim Umbenennen einer nativen PDF-Vorgabe fehl. (12564)
- Beim Duplizieren einer nativen PDF-Vorlage wird der Standardspeicherort der Vorlage anstelle des angegebenen benutzerdefinierten Vorlagenspeicherorts übernommen. (12563)
- Native PDF | Die Sprachmetadaten können im generierten PDF nicht so festgelegt werden, dass sie WCAG 2.0 entsprechen. (12407)
- Das Veröffentlichen auf AEM Site schlägt fehl, wenn temporäre Dateien aus Pod gelesen werden, die möglicherweise aktualisiert oder neu gestartet wurden. (12113)
- Native PDF | Benutzerdefinierte Attribute werden nicht an temporäre HTML- oder PDF-Engine übertragen. (DXML-12005)
- Native PDF | Java OutOfMemoryError tritt beim Veröffentlichen großer Inhalte auf. (11789)
- Native PDF | Xref druckt den Inhalt des href-Thementitels anstelle der Xref-Beschriftung. (11322)
- Native PDF | Die PDF-Vorlageneinstellungen können nicht gespeichert werden. (10751)
- Native PDF | Der Text geht über die Spaltenbreite hinaus und schließt mehrere xrefs ein. (10876)
- Native PDF | `<note>``</note>` -Element generiert keinen zusätzlichen span-Titel seines Typs. (10549)
- JSON-Ausgabe | Die `fmUuid` -Eigenschaft im Knoten jcr:content von JSON unterscheidet sich von der &quot;id&quot;innerhalb der JSON. (11564)
- JSON-Ausgabe | Wenn die Zuordnung und das Thema mit demselben Dateinamen vorhanden sind, wird JSON für die Zuordnung entfernt. (11524)

## Bekanntes Problem

Adobe hat das folgende bekannte Problem für AEM Guides 4.3.0-Version identifiziert:

- Das allgemeine Seitenlayout, das in der Basisvorlage definiert ist, wird nicht als Standardvorlage angewendet.

  Problemumgehung: Fügen Sie ein allgemeines Seitenlayout als Vorder- und Rückseite hinzu und dann wird es für jede Seite angezeigt.
- Ein Problem tritt bei der Site-Suche auf, während Sie auf der AEM Seite der Ausgabe auf AEM Service Pack 16 oder 17 suchen.

  Problemumgehung:

   1. Öffnen Sie die Datei mit dem Pfad: `/libs/foundation/components/search/search.jsp` in `crx/de`
   1. Ersetzen Sie die Zeile 234 durch den folgenden Code:

      ```
      <a href="<c:url value="${hit.URL}" context="/"/>" onclick="trackSelectedResult(this, ${status.index + 1})"><%= xssAPI.filterHTML(((Search.Hit) pageContext.getAttribute("hit")).getTitle()) %></a>
      
      *(Add the missing closing anchor tag at the end).
      ```

   1. Speichern Sie die Datei.
