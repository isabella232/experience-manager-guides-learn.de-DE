---
title: Versionshinweise | Neue Funktionen in der Adobe Experience Manager-Anleitung, Version November 2023
description: Erfahren Sie mehr über die neuen und verbesserten Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im November 2023.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 0%

---

# Neue Funktionen in der Version von Adobe Experience Manager Guides as a Cloud Service im November 2023

Dieser Artikel behandelt die neuen und verbesserten Funktionen in der Version November 2023 der Adobe Experience Manager-Handbücher (später auch als *Experience Manager Guides as a Cloud Service*).

Weitere Informationen zu den Upgrade-Anweisungen, der Kompatibilitätsmatrix und den in dieser Version behobenen Problemen finden Sie unter [Versionshinweise](release-notes-2023.11.0.md).

## Native PDF-Verbesserungen

Die folgenden nativen PDF-Verbesserungen wurden in der Version vom November 2023 vorgenommen:

### Verwenden und Duplizieren von nativen PDF-Vorlagen

Experience Manager Guides bieten vordefinierte oder werksmäßige PDF-Vorlagen. Duplizieren Sie die werkseitigen PDF-Vorlagen, um die benutzerdefinierten PDF-Vorlagen zu erstellen.

Jetzt können Sie auch beim Erstellen und Duplizieren einer Vorlage eine Vorschau des Miniaturbilds für eine Vorlage anzeigen. Sie können dieses Bild auch bearbeiten oder löschen. Diese Funktion ist nützlich für das Branding oder die Unterscheidung von Vorlagen mit ähnlichen Namen.
Weitere Informationen zum [PDF-Vorlage](../native-pdf/pdf-template.md).

![Dialogfeld &quot;PDF-Vorlage duplizieren&quot;](assets/duplicate-template.png){width="550" align="left"}

*Duplizieren Sie eine vorhandene PDF-Vorlage.*


### Ändern der Reihenfolge von Seiten und Veröffentlichen mehrerer Seiten pro Blatt

Sie können die Seiten nicht nur gemäß dem Quelldokument veröffentlichen, sondern auch die Seitenreihenfolge im PDF ändern, während Sie ein mehrseitiges Dokument veröffentlichen.  So können Sie die Seiten in verschiedenen Bestellungen veröffentlichen, wie z.B. alle ungeraden oder alle geraden Seiten zuerst. Sie können auch als Broschüre veröffentlichen und die Seiten wie ein Buch lesen. Sie können auch festlegen, wie viele Seiten Sie auf einem einzigen Blatt veröffentlichen möchten. Weitere Informationen finden Sie unter [Seitenorganisation](../native-pdf/components-pdf-template.md#page-organization) Abschnitt.

### Sortieren Sie Glossarbegriffe basierend auf Sortierschlüsseln

Jetzt können Sie die Glossarbegriffe auch anhand von Sortierschlüsseln sortieren. Sie können das Tag &quot;sort-as&quot;verwenden, um einen Sortierschlüssel für die Glossarbegriffe zu definieren. Anschließend können Sie sie anhand von Sortierschlüsseln anstelle der Begriffe sortieren. Auf diese Weise können Sie die Glossarbegriffe nach Begriffen sortieren, die in verschiedenen Sprachen verwendet werden. Sie können auch einen einzigen Sortierschlüssel für einen Glossarbegriff mit einem Satz oder einer Wortgruppe definieren.
Weitere Informationen finden Sie unter [Erweiterte PDF-Einstellungen](../native-pdf/components-pdf-template.md#advanced-pdf-settings).


### Verbesserte Ressourcenverwaltung für native PDF-Vorlagen

Experience Manager Guides haben die Ressourcenverwaltung für native PDF-Vorlagen verbessert. Sie können jetzt Ressourcen wie Bilder, CSS-Dateien und Schriftartdateien für mehrere native PDF-Vorlagen freigeben und wiederverwenden. Durch diese Verbesserung ist die Verwaltung der Ressourcen für eine große Anzahl von Vorlagen wesentlich einfacher. Sie müssen keine doppelten Ressourcen für jede Vorlage erstellen und diese in einem freigegebenen Ordner speichern und in allen nativen PDF-Vorlagen verwenden.
Weitere Informationen finden Sie unter [PDF-Vorlage](../native-pdf/pdf-template.md).

## Verbesserungen am Webeditor

Die folgenden Verbesserungen am Webeditor wurden in der Version November 2023 vorgenommen:


### Anzeigen von Dateien nach Titel oder Dateinamen

Sie können jetzt die Standardmethode zum Anzeigen der Dateien im Web-Editor wählen. Sie können die Liste der Dateien anhand der Titel oder Dateinamen aus den verschiedenen Bedienfeldern in der Autorenansicht anzeigen.

![Dialogfeld &quot;Benutzereinstellungen&quot;](assets/user-preferences-2311.png){width="550" align="left"}

*Ändern Sie die Standardmethode zum Anzeigen der Dateien aus dem **Benutzereinstellungen**angezeigt.*


### Verwalten von Bedingungsvorgaben

Sie können Bedingungsattribute in Ihren DITA-Themen definieren. Verwenden Sie dann die Bedingungsattribute in der Bedingungsvorgabe, um den Inhalt in einer DITA-Zuordnung zu veröffentlichen. Mit den Experience Manager-Handbüchern können Sie jetzt auch Bedingungsvorgaben im Web-Editor erstellen und verwalten. Sie können sie auch einfach bearbeiten, duplizieren oder löschen.

![Bedingungsvorgaben auf der Registerkarte &quot;Verwalten&quot;des Web-Editors ](assets/web-editor-manage-condition-presets.png){width="550" align="left"}

Weitere Informationen finden Sie unter [Verwenden von Bedingungsvorgaben](../user-guide/generate-output-use-condition-presets.md).

### Dateiregisterkarten beim Aktualisieren des Browsers wiederherstellen

Experience Manager-Handbücher stellen beim Aktualisieren des Browsers den Status der geöffneten Dateiregisterkarten im Web Editor wieder her. Weitere Informationen finden Sie unter **Aktualisieren des Browsers beim Bearbeiten der Dateien** Abschnitt unter [Bearbeiten von Themen im Web-Editor](../user-guide/web-editor-edit-topics.md).

### Einfaches Entpacken eines Elements

Jetzt können Sie mit der Option im Kontextmenü eines Elements im Web Editor die Einbindung eines Elements einfach aufheben. Auf diese Weise können Sie den Text des Elements einfach mit seinem übergeordneten Element zusammenführen.
Weitere Informationen finden Sie unter **Umbruch eines Elements aufheben** aus dem [andere Funktionen im Web Editor](../user-guide/web-editor-other-features.md).

### Tastaturbefehle zum Verschieben des Cursors

Experience Manager-Handbücher ermöglichen es Ihnen jetzt auch, Tastaturbefehle zu verwenden, um den Cursor in den Web-Editor zu verschieben. Sie können die Tastaturbefehle verwenden, um ein Wort schnell nach links oder rechts zu verschieben. Mithilfe der Tastaturbefehle können Sie auch zum Anfang oder Ende der Zeile wechseln.
Jetzt können Sie auch Tastaturbefehle verwenden, um den Cursor an den Anfang des nächsten Elements oder an das Ende des vorherigen Elements zu verschieben.
Weitere Informationen zum [Tastaturbefehle im Web-Editor](../user-guide/web-editor-keyboard-shortcuts.md).
