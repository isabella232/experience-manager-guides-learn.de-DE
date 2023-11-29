---
title: Native PDF-Vorlagen erstellen und anpassen
description: Erfahren Sie, wie Sie native PDF-Vorlagen erstellen und anpassen.
exl-id: 7660da8e-8a1e-4493-b99b-9b5de9a7483f
source-git-commit: 9e806ae9a06eb77441e47413981f27f6e69bd2f9
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# PDF-Vorlage {#PDF-template}

Die Verwendung einer Vorlage stellt die Konsistenz des Inhaltslayouts und der Inhaltsstruktur sicher. Da Vorlagen vordefiniert sind, können Sie Formatierungsprobleme, die bei jedem neuen Projekt oder jeder neuen Aktualisierung auftreten, vermeiden. Mit Vorlagen können Sie Seitenlayouts entwerfen, Inhalte gestalten und verschiedene Einstellungen anwenden, um Ihre PDF anzupassen.

## Werkseitige und benutzerdefinierte PDF-Vorlagen

Es sind einige werksmäßig bereitgestellte Beispielvorlagen vorhanden, die die Entwickler als Basisvorlagen verwenden können, um benutzerdefinierte Vorlagen entsprechend ihren organisatorischen Anforderungen zu erstellen.



## Neue PDF-Vorlage erstellen {#create-pdf-template}

Sie können benutzerdefinierte PDF-Vorlagen mit bestimmten Seitenlayouts erstellen und Formatierungen für Seitenlayoutkomponenten (wie Inhaltsverzeichnis, Index, Glossar) oder DITA-Komponenten (wie Überschrift, Absatz, Liste) mithilfe von Stylesheets definieren.

Gehen Sie wie folgt vor, um eine neue PDF-Vorlage zu erstellen:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Auswählen **Vorlagen** <img src="./assets/template.svg" alt= "Vorlagensymbol" width="25"> im linken Bereich.
<img src="assets/create-pdf-template.png" alt="PDF-Vorlage erstellen" width="400">
1. Wählen Sie im Fenster **Vorlagen** das **+*-Symbol neben **Vorlagen** und danach **PDF-Vorlage** aus.
1. Wählen Sie im Dialogfeld **Neue PDF-Vorlage** eine Werksvorlage aus, die Sie als Grundlage für die Erstellung der benutzerdefinierten Vorlage verwenden möchten. Sie können auch das Suchfeld verwenden, um nach einer Vorlage zu suchen.
1. Geben Sie einen Titel für die Vorlage an.

>[!NOTE]
>
>  Sie können auch beim Erstellen und Duplizieren einer Vorlage eine Vorschau einer Miniaturansicht für die Vorlage anzeigen. Bearbeiten oder löschen Sie die Miniaturansicht mit [**Eigenschaften**](#properties-option) im **Optionen** nach der Erstellung der Vorlage.

1. Klicken Sie auf **Erstellen**.

   Die neue Vorlage wird erstellt und im **Vorlagen** Bedienfeld.

## PDF-Vorlage duplizieren {#duplicate-pdf-template}

Wenn Sie eine neue Vorlage mit demselben Seitenlayout und derselben Formatierung wie eine vorhandene Vorlage erstellen möchten, können Sie eine Kopie erstellen. Nachdem eine Vorlage dupliziert wurde, können Sie ihre Komponenten nach Bedarf weiter anpassen.

Gehen Sie wie folgt vor, um eine vorhandene PDF-Vorlage zu duplizieren:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Auswählen **Vorlagen** <img src="./assets/template.svg" alt= "Vorlagensymbol" width="25"> im linken Bereich. Dadurch wird die **Vorlagen** Fenster.
1. Bewegen Sie den Mauszeiger über die Vorlage, die Sie duplizieren möchten, und wählen Sie die **...** *Optionen* Symbol und wählen Sie **Duplizieren** aus dem Kontextmenü aus.

   Dadurch wird die **PDF-Vorlage duplizieren** angezeigt.

   <img src="assets/duplicate-template.png" alt="PDF-Vorlage duplizieren" width="350">

   *Wählen Sie eine Vorlage zum Duplizieren, zeigen Sie eine Vorschau der Miniaturansicht an und aktualisieren Sie den Titel im **PDF-Vorlage duplizieren**angezeigt.*

1. Geben Sie einen Titel für die Vorlage an.

   Die **Titel** -Feld wird als Kopie des gleichen Titels wie die Quellvorlage vorausgefüllt. Wenn die Vorlage mit demselben Titel vorhanden ist, wird eine Fehlermeldung angezeigt.



1. Um einen bevorzugten Titel anzugeben, entfernen Sie den vorausgefüllten Titel und geben Sie einen Titel an.
1. Klicks **Duplizieren**.

   Eine duplizierte Vorlage wird erstellt und unter dem **Vorlagen**.

## Sonstige Vorgänge auf Vorlagen

Sie können auch die folgenden Vorgänge für die Vorlagen über die **Optionen** Menü:

<img src="assets/PDF-template-options.png" alt="PDF-Vorlage duplizieren" width="350">

### Löschen

Wählen Sie die Option Löschen , um die ausgewählte Vorlage zu löschen. Wählen Sie dann in der Bestätigungsaufforderung Ja aus.
Die Vorgabe wird aus dem **Vorlagen**.

### Eigenschaften{#properties-option}

Wählen Sie diese Option aus, um die Eigenschaften der Vorlage anzuzeigen und zu bearbeiten. Sie können eine Vorschau der vorhandenen Miniaturansicht für die Vorlage anzeigen. Sie können die Miniaturansicht auch bearbeiten oder löschen. Sie können auch den Titel und die Beschreibung der Vorlage ändern.

### Anzeigen in der Assets-Benutzeroberfläche

Wählen Sie diese Option aus, um die Vorlage in der Assets-Benutzeroberfläche anzuzeigen. Da der Stammspeicherort der Vorlage geöffnet wird, können Sie alle Ressourcen der Vorlage anzeigen.

Nachdem Sie die benutzerdefinierte Vorlage erstellt haben, können Sie sie aus den Seitenlayouts in der PDF-Ausgabevorgabe auswählen.
Erfahren Sie, wie [PDF-Ausgabe veröffentlichen](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/user-guide/output-gen/web-editor/native-pdf-web-editor.html?lang=en).

>[!NOTE]
>
>Wenn für Ihren Ordner ein Ordnerprofil konfiguriert ist, werden nur die im Ordnerprofil konfigurierten PDF-Vorlagen angezeigt.

Je nach Einrichtung kann Ihr Administrator die Vorlagen konfigurieren:

<details>
<summary> Cloud Services </summary>

Weitere Informationen zum Einrichten von globalen Profilen und Profilen auf Ordnerebene finden Sie unter [Vorlagen konfigurieren](../cs-install-guide/conf-folder-level.md#id1889D0IL0Y4) im Installations- und Konfigurationshandbuch für Cloud Service.

</details>

<details>    
<summary>  On-Premise Software </summary>

Weitere Informationen zum Einrichten von globalen Profilen und Profilen auf Ordnerebene finden Sie unter [Authoring-Vorlagen konfigurieren](../install-guide/conf-folder-level.md#create-custom-authoring-template-id1917d0eg0hj) im On-Premise-Installations- und Konfigurationshandbuch.

</details>

## PDF-Vorlage anpassen {#customize-pdf-template}

Sie können Vorlagen anpassen, indem Sie die Vorlagenkomponenten anpassen und Stilformate mithilfe von Stylesheets anwenden.

Gehen Sie wie folgt vor, um eine PDF-Vorlage anzupassen:
1. Navigieren Sie im Web-Editor zum **Ausgabe** Registerkarte.
1. Erweitern Sie die linke Seitenleiste und wählen Sie **Vorlagen**.

   Dadurch wird die **Vorlagen** Bedienfeld.
1. Führen Sie einen der folgenden Schritte aus, um die Komponenten einer Vorlage anzuzeigen:

   * Wählen Sie das Symbol > neben einer Vorlage aus oder doppelklicken Sie auf den Vorlagennamen.
   * Bewegen Sie den Mauszeiger über eine Vorlage und wählen Sie die Option ... (**Optionen** und wählen Sie **Bearbeiten** aus dem Kontextmenü aus.

     Standardmäßig wird dadurch die **Einstellungen** im Vorlagen-Editor.
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
   * Ressourcen: Speichern Sie Asset-Dateien, die Sie zum Anpassen oder Entwerfen von PDF-Vorlagen benötigen. Assets wie Logos, benutzerdefinierte Schriftarten, Hintergrundbilder und mehr werden in den Ressourcen gespeichert.
Sie können auch Ressourcen verwenden, die sich an einem anderen Speicherort im Repository befinden. Sie müssen keine doppelten Ressourcen für jede Vorlage erstellen und diese in einem freigegebenen Ordner speichern und in allen nativen PDF-Vorlagen verwenden.

     Weitere Informationen zur Verwendung von Ressourcen finden Sie unter [Arbeiten mit Ressourcen](components-pdf-template.md#work-with-resources).
   * Einstellungen: Konfigurieren Sie die Ausgabeeinstellungen zum Generieren einer PDF mithilfe der Vorlage. In diesem Abschnitt können Sie das Vorlagen-Mapping für verschiedene Seiten in einer PDF, Kapitel-Startseite, Druckmarken, Zitaten und mehr definieren.
Sie können auch die Reihenfolge anordnen, in der sie in Ihrer endgültigen PDF-Ausgabe erscheinen sollen.
Weitere Informationen zum Anwenden von Einstellungen finden Sie unter [Erweiterte PDF-Einstellungen](components-pdf-template.md#advanced-pdf-settings).


1. Doppelklicken Sie zum Anpassen einer Vorlagenkomponente auf eine Vorlagenkomponente oder wählen Sie das Symbol > vor der Komponente aus.

   Doppelklicken Sie beispielsweise auf *Seitenlayouts* oder wählen Sie die *>* Symbol vor *Seitenlayouts* um die verfügbaren Seitenlayouts anzuzeigen.

   >[!NOTE]
   >
   >Sie können auch eine Miniaturansicht und die Beschreibung für die Vorlage mit der [**Eigenschaften**](#properties-option) im **Optionen** Menü.

1. Nachdem Sie die gewünschten Änderungen vorgenommen haben, wählen Sie *Alle speichern* (oder `Ctrl+S`).
