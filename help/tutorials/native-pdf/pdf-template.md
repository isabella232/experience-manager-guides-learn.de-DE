---
title: Native PDF-Vorlagen erstellen und anpassen
description: Erfahren Sie, wie Sie native PDF-Vorlagen erstellen und anpassen.
exl-id: 7660da8e-8a1e-4493-b99b-9b5de9a7483f
source-git-commit: 49fa930483f48cafd057002ee26c9499ce967c60
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# PDF-Vorlage {#PDF-template}

Die Verwendung einer Vorlage stellt die Konsistenz des Inhaltslayouts und der Inhaltsstruktur sicher. Da Vorlagen vordefiniert sind, können Sie Formatierungsprobleme, die bei jedem neuen Projekt oder jeder neuen Aktualisierung auftreten, vermeiden. Mit Vorlagen können Sie Seitenlayouts entwerfen, Inhalte gestalten und verschiedene Einstellungen anwenden, um Ihre PDF anzupassen.

Während Autoren die PDF-Vorgaben verwenden können, um Ausgaben zu generieren, können Entwickler eigene Vorlagen erstellen. Im Lieferumfang enthalten sind Beispielvorlagen, die von den Entwicklern entsprechend ihren organisatorischen Anforderungen weiter angepasst oder dupliziert werden können.


## Neue PDF-Vorlage erstellen {#create-pdf-template}

Sie können benutzerdefinierte PDF-Vorlagen mit bestimmten Seitenlayouts erstellen und Formatierungen für Seitenlayoutkomponenten (wie Inhaltsverzeichnis, Index, Glossar) oder DITA-Komponenten (wie Überschrift, Absatz, Liste) mithilfe von Stylesheets definieren. Sie können eine neue Vorlage von Grund auf neu erstellen oder mithilfe einer Beispielvorlage erstellen.

Gehen Sie wie folgt vor, um eine neue PDF-Vorlage zu erstellen:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Erweitern Sie die linke Seitenleiste und wählen Sie **Vorlagen**.
<img src="assets/create-pdf-template.png" alt="PDF-Vorlage erstellen" width="400">
1. Wählen Sie im Bedienfeld **Vorlagen** das **+*-Symbol neben **Vorlagen** und dann **PDF-Vorlage**.
1. Geben Sie im Dialogfeld **Neue Vorlage** einen Namen für die Vorlage an.
1. Klicken Sie auf "Fertig".

Die neue Vorlage wird erstellt und im *Vorlagen* Bedienfeld.

## PDF-Vorlage duplizieren {#duplicate-pdf-template}

Wenn Sie eine neue Vorlage mit demselben Seitenlayout und derselben Formatierung wie eine vorhandene Vorlage erstellen möchten, können Sie eine Kopie erstellen. Nachdem eine Vorlage dupliziert wurde, können Sie ihre Komponenten nach Bedarf weiter anpassen.

Gehen Sie wie folgt vor, um eine vorhandene PDF-Vorlage zu duplizieren:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Erweitern Sie die linke Seitenleiste und wählen Sie **Vorlagen**.

   Dadurch wird der Bereich &quot;Vorlagen&quot;geöffnet.
1. Bewegen Sie den Mauszeiger über die Vorlage, die Sie duplizieren möchten, und wählen Sie die (*Optionen* Symbol) **...** und wählen **Duplizieren** aus dem Kontextmenü aus.

   Dadurch wird das Dialogfeld Vorlage duplizieren geöffnet.\
   <img src="assets/duplicate-template.png" alt="PDF-Vorlage duplizieren" width="250">
1. Geben Sie einen Namen für die Vorlage an.

   Die **Name** -Feld wird als Kopie mit demselben Namen wie die Quellvorlage vorausgefüllt.

1. Um einen bevorzugten Namen anzugeben, entfernen Sie den vorausgefüllten Namen und geben Sie einen Namen an.
1. Klicken Sie auf **Fertig**.

   Eine duplizierte Vorlage wird unter Vorlagen erstellt und hinzugefügt.

## PDF-Vorlage anpassen {#customize-pdf-template}

Sie können Vorlagen anpassen, indem Sie die Vorlagenkomponenten anpassen und Stilformate mithilfe von Stylesheets anwenden.

Gehen Sie wie folgt vor, um eine PDF-Vorlage anzupassen:
1. Gehen Sie im Web Editor zur Registerkarte Ausgabe .
1. Erweitern Sie die linke Seitenleiste und wählen Sie Vorlagen aus.

   Dadurch wird der Bereich &quot;Vorlagen&quot;geöffnet.
1. Führen Sie einen der folgenden Schritte aus, um die Komponenten einer Vorlage anzuzeigen:

   * Wählen Sie das Symbol > neben einer Vorlage aus oder doppelklicken Sie auf den Vorlagennamen.
   * Bewegen Sie den Mauszeiger über eine Vorlage, wählen Sie das Symbol ... (Optionen) und wählen Sie im Kontextmenü die Option Bearbeiten ...

     Standardmäßig wird dadurch das Einstellungsbedienfeld im Vorlageneditor geöffnet.
   <img src="assets/customize-pdf-template.png" alt="Anpassen von PDF Teamplte" width="350">

   >[!NOTE]
   >
   >  Ihr Administrator kann die neuesten Vorlagen aus dem folgenden Pfad herunterladen und die vorhandenen ersetzen:
   >
   > `/libs/fmdita/pdf`

   Die verschiedenen Vorlagenkomponenten, die Sie anpassen können, werden in die folgenden Abschnitte kategorisiert:
   * Seitenlayouts: Eine typische PDF enthält verschiedene Seiten, wie z. B. ein Titelbild oder eine Titelseite, Inhaltsverzeichnis, Kapitel, Index, Zitate und mehr. Im Bereich Seitenlayouts können Sie das Erscheinungsbild verschiedener Seiten entwerfen, aus denen sich Ihre PDF zusammensetzt. Weitere Informationen finden Sie unter [Seitenlayouts](../native-pdf/components-pdf-template.md#page-layouts).

     Zusätzlich zum Erscheinungsbild können Sie auch die Anordnung der Seitenelemente wie Kopf- und Fußzeilen sowie Inhaltsbereiche auf einer Seite definieren. Weitere Informationen zum Anpassen des Seitenlayouts finden Sie unter [Seitenlayouts erstellen und anpassen](components-pdf-template.md#create-customize-page-layout).

   * Stylesheets: Mit den Einstellungen im Abschnitt &quot;Stylesheets&quot;können Sie das Erscheinungsbild der Seitenlayoutkomponenten anpassen, z. B. Inhaltsverzeichnis, Index, Glossar, Zitate und mehr. Darüber hinaus können Sie die Stile für den DITA-Inhalt wie Überschriften, Absätze, Listen und mehr anpassen. Weitere Informationen zur Verwendung der Stylesheets finden Sie unter [Verwenden von Stylesheets zum Anpassen von PDF](components-pdf-template.md#stylesheet-customization).
   * Ressourcen: Speichern Sie Asset-Dateien, die Sie zum Anpassen oder Entwerfen von PDF-Vorlagen benötigen. Assets wie Logos, benutzerdefinierte Schriftarten, Hintergrundbilder und mehr werden in den Ressourcen gespeichert. Weitere Informationen zur Verwendung von Ressourcen finden Sie unter [Arbeiten mit Ressourcen](components-pdf-template.md#work-with-resources).
   * Einstellungen: Konfigurieren Sie die Ausgabeeinstellungen zum Generieren einer PDF mithilfe der Vorlage. In diesem Abschnitt können Sie das Vorlagen-Mapping für verschiedene Seiten in einer PDF, Kapitel-Startseite, Druckmarken, Zitaten und mehr definieren.
Sie können auch die Reihenfolge anordnen, in der sie in Ihrer endgültigen PDF-Ausgabe erscheinen sollen.
Weitere Informationen zum Anwenden von Einstellungen finden Sie unter [Erweiterte PDF-Einstellungen](components-pdf-template.md#advanced-pdf-settings).


1. Doppelklicken Sie zum Anpassen einer Vorlagenkomponente auf eine Vorlagenkomponente oder wählen Sie das Symbol > vor der Komponente aus.

   Doppelklicken Sie beispielsweise auf *Seitenlayouts* oder wählen Sie die *>* Symbol vor *Seitenlayouts* um die verfügbaren Seitenlayouts anzuzeigen.
1. Nachdem Sie die gewünschten Änderungen vorgenommen haben, wählen Sie *Alle speichern* (oder `Ctrl+S`).
