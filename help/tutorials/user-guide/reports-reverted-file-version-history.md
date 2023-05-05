---
title: Versionsverlauf wiederhergestellter Dateien - Bericht
description: Erfahren Sie, wie Sie den Versionsverlaufbericht für zurückgegebene Dateien
exl-id: fa90b373-742a-4102-b00f-07e4113fef98
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Versionsverlauf wiederhergestellter Dateien - Bericht {#id205BBC00PRK}

Wenn Sie an mehreren gleichzeitigen Versionen zusammen mit mehreren Autoren arbeiten, ist es erforderlich, dass Ihr Inhalt über mehrere Versionen verfügt. Es kann einige allgemeine Informationen über mehrere Versionen hinweg geben, die verschiedene Autoren in ihrem Projekt verwenden können. Um solche Arbeitszuweisungen zu verarbeiten, könnten Autoren mehrere Versionen von Dateien erhalten. Bei solchen Versionen kann es sich einfach um eine neuere Version einer Datei oder um eine frühere Version handeln. Es ist eine komplexe Aufgabe, zu ermitteln, wann und warum eine Datei zurückgesetzt wurde.

Mit AEM Guides können Sie einen Versionsverlaufsbericht für eine einzelne Datei oder für alle Dateien in einem Ordner erstellen. Dieser Versionsverlauf gibt Ihnen einen Überblick über alle Versionen einer Datei, die zurückgesetzt wurden und die diese Versionen erstellt haben, sowie den Grund für die Erstellung dieser Versionen.

Der Zugriff auf diesen Bericht ist an folgenden Stellen möglich:

- **Assets-Benutzeroberfläche**: durch Auswahl einer Datei und Öffnen der **Versionsverlauf** über die linke Leiste. Die **Versionsverlauf** Ansicht enthält **Versionsprotokolle wiederherstellen** -Link am unteren Rand des Bedienfelds. Wenn Sie auf diesen Link klicken, wird der Verlauf der ausgewählten Datei mit den wiederhergestellten Versionen angezeigt.

   ![](images/revert-log-from-assets-ui.png){width="300" align="left"}

- **Themenvorschau**: Wenn Sie ein Thema in der Vorschau anzeigen, können Sie auch die **Versionsverlauf** aus der linken Leiste. Sie erhalten ein Bedienfeld ähnlich der Assets-Benutzeroberfläche, von dem aus Sie auf die **Versionsprotokolle wiederherstellen** -Link, um auf den Verlauf der wiederhergestellten Version des aktiven Dokuments zuzugreifen.

- **Abschnitt &quot;AEM&quot;**: Sie können auch über den Bereich AEM Tools auf diesen Bericht zugreifen. Im folgenden Verfahren wird erläutert, wie Sie über den Abschnitt AEM Tools auf den Verlauf der Zurückkehrversion zugreifen können.


Führen Sie die folgenden Schritte aus, um auf den Bericht Verlauf zurücksetzen zuzugreifen:

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools.

1. Klicken Sie auf **Versionsverlauf wiederherstellen** Kachel.

   Es wird eine leere Seite Versionsverlauf wiederherstellen angezeigt, auf der Sie eine Datei oder einen Ordner durchsuchen und auswählen müssen, um den Bericht zu generieren.

1. Klicken **Protokolle anzeigen** , um den Bericht für die ausgewählte Datei oder den ausgewählten Ordner zu generieren.

   ![](images/revert-version-history-report.png){width="800" align="left"}

   Der Bericht enthält folgende Details:

   - **Dateiname**: Der Titel des Themas. Durch Klicken auf den Titel-Link des Themas wird die Themenvorschau geöffnet.

   - **Zeitstempel**: Datum und Uhrzeit, zu der das Thema auf eine frühere Version zurückgesetzt wurde.

   - **Benutzer**: Name des Benutzers, der zu einer früheren Version zurückgekehrt ist.

   - **Zurück von**: Die ursprüngliche Versionsnummer der Datei, von der sie zurückgesetzt wurde.

   - **Wiederherstellen auf**: Die Version, auf die die Datei zurückgesetzt wurde.

   - **Kommentar**: Alle Kommentare des Benutzers, der die Datei zurückgesetzt hat.


**Übergeordnetes Thema:**[ Berichte](reports-intro.md)
