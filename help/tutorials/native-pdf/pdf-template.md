---
title: Native PDF-Veröffentlichungsfunktion | Anpassen und Konfigurieren der nativen PDF-Funktion
description: Erfahren Sie, wie Sie die verschiedenen Komponenten der nativen PDF-Funktion anpassen und konfigurieren.
hide: true
hidefromtoc: true
source-git-commit: 0f18d9f7d7967b6f25c5d05b54a22f65e9fc20f7
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# PDF-Vorlage

Die Verwendung einer Vorlage stellt die Konsistenz des Inhaltslayouts und der Inhaltsstruktur sicher. Da Vorlagen vordefiniert sind, können Sie Formatierungsprobleme, die bei jedem neuen Projekt oder jeder neuen Aktualisierung auftreten, vermeiden. Mit Vorlagen können Sie Seitenlayouts entwerfen, Inhalte gestalten und verschiedene Einstellungen anwenden, um Ihre PDF anzupassen.

Während Autoren die PDF-Vorgaben verwenden können, um Ausgaben zu generieren, können Entwickler eigene Vorlagen erstellen. Im Lieferumfang enthalten sind Beispielvorlagen, die von den Entwicklern entsprechend ihren organisatorischen Anforderungen weiter angepasst oder dupliziert werden können.


## Neue PDF-Vorlage erstellen {#create-pdf-template}

Sie können benutzerdefinierte PDF-Vorlagen mit bestimmten Seitenlayouts erstellen und Formatierungen für Seitenlayoutkomponenten (wie Inhaltsverzeichnis, Index, Glossar) oder DITA-Komponenten (wie Überschrift, Absatz, Liste) mithilfe von Stylesheets definieren. Sie können eine neue Vorlage von Grund auf neu erstellen oder mithilfe einer Beispielvorlage erstellen.

Gehen Sie wie folgt vor, um eine neue PDF-Vorlage zu erstellen:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Erweitern Sie die linke Seitenleiste und klicken Sie auf **Vorlagen**.
<img src="assets/create-pdf-template.png" alt="PDF-Vorlage erstellen" width="400">
1. Klicken Sie im Bedienfeld **Vorlagen* auf das **+*-Symbol neben **Vorlagen** und wählen Sie **PDF-Vorlage**.
1. Geben Sie im Dialogfeld **Neue Vorlage** einen Namen für die Vorlage an.
1. Klicken Sie auf **Fertig**.

Die neue Vorlage wird erstellt und im *Vorlagen* Bereich.

## PDF-Vorlage duplizieren

Wenn Sie eine neue Vorlage mit demselben Seitenlayout und derselben Formatierung wie eine vorhandene Vorlage erstellen möchten, können Sie eine Kopie erstellen. Nachdem eine Vorlage dupliziert wurde, können Sie ihre Komponenten nach Bedarf weiter anpassen.

Gehen Sie wie folgt vor, um eine vorhandene PDF-Vorlage zu duplizieren:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Erweitern Sie die linke Seitenleiste und klicken Sie auf **Vorlagen**.

   Dadurch wird der Bereich &quot;Vorlagen&quot;geöffnet.
1. Bewegen Sie den Mauszeiger über die Vorlage, die Sie duplizieren möchten, und wählen Sie die (*Optionen* Symbol) **...** und wählen Sie **Duplizieren** aus dem Kontextmenü aus.

   Dadurch wird das Dialogfeld Vorlage duplizieren geöffnet.\
   <img src="assets/duplicate-template.png" alt="PDF-Vorlage duplizieren" width="250">
1. Geben Sie einen Namen für die Vorlage an.

   Die **Name** -Feld wird als Kopie mit demselben Namen wie die Quellvorlage vorausgefüllt.

1. Um einen bevorzugten Namen anzugeben, entfernen Sie den vorausgefüllten Namen und geben Sie einen Namen an.
1. Klicken Sie auf **Fertig**.

   Eine duplizierte Vorlage wird unter Vorlagen erstellt und hinzugefügt.

## PDF-Vorlage anpassen

Sie können Vorlagen anpassen, indem Sie die Vorlagenkomponenten anpassen und Stilformate mithilfe von Stylesheets anwenden.

Gehen Sie wie folgt vor, um eine PDF-Vorlage anzupassen:
1. Gehen Sie im Web Editor zur Registerkarte Ausgabe .
1. Erweitern Sie die linke Seitenleiste und klicken Sie auf Vorlagen .

   Dadurch wird der Bereich &quot;Vorlagen&quot;geöffnet.
1. Führen Sie einen der folgenden Schritte aus, um die Komponenten einer Vorlage anzuzeigen:

   * Klicken Sie auf das Symbol > neben einer Vorlage oder doppelklicken Sie auf den Vorlagennamen.
   * Bewegen Sie den Mauszeiger über eine Vorlage, klicken Sie auf das Symbol ... (Optionen) und wählen Sie im Kontextmenü die Option Bearbeiten aus.

      Standardmäßig wird dadurch das Einstellungsbedienfeld im Vorlagen-Editor geöffnet.
   <img src="assets/customize-pdf-template.png" alt="Anpassen von PDF Teamplte" width="350">

   Die verschiedenen Vorlagenkomponenten, die Sie anpassen können, werden in die folgenden Abschnitte kategorisiert:
   * Seitenlayouts: Eine typische PDF enthält verschiedene Seiten, wie z. B. ein Titelblatt oder eine Titelseite, ein Inhaltsverzeichnis, ein Kapitel, einen Index usw. Im Bereich Seitenlayouts können Sie das Erscheinungsbild verschiedener Seiten entwerfen, aus denen sich Ihre PDF zusammensetzt. Zusätzlich zum Erscheinungsbild können Sie auch die Anordnung der Seitenelemente wie Kopf- und Fußzeilen sowie Inhaltsbereiche auf einer Seite definieren. Weitere Informationen zum Anpassen des Seitenlayouts finden Sie unter ***Seitenlayouts erstellen und anpassen***.
   * Stylesheets: Mit den Einstellungen im Abschnitt Stylesheets können Sie das Erscheinungsbild der Seitenlayoutkomponenten anpassen, wie das Inhaltsverzeichnis, den Index, das Glossar und mehr. Darüber hinaus können Sie die Stile für den DITA-Inhalt wie Überschriften, Absätze, Listen und mehr anpassen. Weitere Informationen zur Verwendung der Stylesheets finden Sie unter ***Verwenden von Stylesheets zum Anpassen von PDF***.
   * Ressourcen: Speichern Sie Asset-Dateien, die Sie zum Anpassen oder Entwerfen von PDF-Vorlagen benötigen. Assets wie Logos, benutzerdefinierte Schriftarten, Hintergrundbilder und mehr werden in den Ressourcen gespeichert. Weitere Informationen zur Verwendung von Ressourcen finden Sie unter ***Arbeiten mit Ressourcen***.
   * Einstellungen: Konfigurieren Sie die Ausgabeeinstellungen zum Generieren einer PDF mithilfe der Vorlage. In diesem Abschnitt können Sie die Vorlagenzuordnung für verschiedene Seiten in einer PDF, Kapitel-Startseite, Druckmarken und mehr definieren. Weitere Informationen zum Anwenden von Einstellungen finden Sie unter ***Erweiterte PDF-Einstellungen***.
1. Doppelklicken Sie zum Anpassen einer Vorlagenkomponente auf eine Vorlagenkomponente oder klicken Sie davor auf das Symbol > .

   Doppelklicken Sie beispielsweise auf *Seitenlayouts* oder klicken Sie auf *>* Symbol vor *Seitenlayouts* um die verfügbaren Seitenlayouts anzuzeigen.
1. Nachdem Sie die gewünschten Änderungen vorgenommen haben, klicken Sie auf *Alle speichern* (oder `Ctrl+S`).


