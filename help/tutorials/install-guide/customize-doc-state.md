---
title: Dokumentstatus konfigurieren
description: Erfahren Sie, wie Sie Dokumentstatus konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 0%

---

# Dokumentstatus konfigurieren {#id181GB0400UI}

Mit AEM-Handbüchern können Sie die Dokumentzustände für Ihre DITA-Themen entsprechend den Anforderungen Ihres Unternehmens definieren. Sie können verschiedene Status Ihres Dokuments von Anfang bis Ende definieren. Der erste Status kann beispielsweise Entwurf sein und zu Überprüfen, Genehmigt, Übersetzt und schließlich zu Veröffentlicht wechseln.

Es gibt zwei Möglichkeiten, wie ein Thema von einem Status zum anderen übergehen kann: manuelle und automatische. Die in einem Profil definierten Dokumentstatus können zum manuellen Ändern des Dokumentstatus verwendet werden. Dies kann über die Seite Eigenschaften einer Themendatei erfolgen. Sie können auch definieren, wer das Dokument von einem Status in einen anderen verschieben kann. Ein Autor kann beispielsweise ein Dokument erstellen und der Standardstatus des Dokuments kann &quot;Entwurf&quot;lauten. Wenn der Autor das Dokument zur Überprüfung sendet, kann er den Dokumentstatus in &quot;In Überprüfung&quot;ändern. Der Überprüfer kann den Dokumentstatus basierend auf dem Überprüfungsprozess entweder zu Genehmigt oder zu Entwurf erneut ändern. Wenn das Dokument genehmigt ist, kann der Herausgeber den Dokumentstatus abhängig vom Workflow in Übersetzt oder Veröffentlicht ändern.

>[!NOTE]
>
> Wenn ein Benutzer zum *Administratoren* -Gruppe kann der Benutzer den Status eines Dokuments von einem beliebigen Status ändern, unabhängig von den im System definierten Dokumentstatusübergängen.

## Erstellen eines Dokumentstatus

AEM Guides werden mit einer Reihe von Standarddokumentstatus ausgeliefert. Diese Status sind:

- Entwurf
- Bearbeiten
- In Review
- Genehmigt
- Überarbeitet
- Fertig

Diese Standardstatus sind für alle DITA-Themen verfügbar, die unter DAM erstellt wurden. Sie können Ihre eigenen Dokumentstatus erstellen und sie einem bestimmten Ordner zuweisen. Alle DITA-Dateien, die unter diesem Ordner erstellt wurden, haben dann Zugriff auf die neu erstellten Dokumentstatus.

Um Dokumentstatus mithilfe des Ordnerprofils zu erstellen, führen Sie die folgenden Schritte aus:

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools.
1. Klicken Sie auf die Kachel Dokumentstatus .

   Die Seite &quot;Asset-Status&quot;wird angezeigt. Standardmäßig zeigt die Seite ein Standardprofil an.

1. Klicks **Profil erstellen** und geben Sie die folgenden Details ein:
   - Geben Sie im Feld Profil den Namen für das Profil ein.
   - Geben Sie den Pfad an, auf den Sie das neue Profil anwenden möchten.
   - Geben Sie den Status des Dokuments im **Zugelassene Status** under **Staaten**. Die standardmäßigen Dokumentstatus sind &quot;Entwurf&quot;, &quot;Bearbeiten&quot;, &quot;In Review&quot;, &quot;Genehmigt&quot;und &quot;Fertig&quot;.

     Klicken Sie auf **Hinzufügen** Schaltfläche zum Hinzufügen eines Dokumentstatus.

      - Klicken Sie auf das Symbol Löschen , um einen Dokumentstatus zu löschen.

     >[!NOTE]
     >
     > Löschen Sie keinen Dokumentstatus, wenn sich Dokumente noch in diesem Status befinden. Wenn Sie einen Dokumentstatus löschen, können Sie den Dokumentstatus solcher Dokumente nur ändern, wenn Sie zum *administrator* Benutzergruppe.

   - Geben Sie den Anfangsstatus des Dokuments im **Startstatus**.
   - Geben Sie den Endstatus des Dokuments im **Endzustand**.
   - Geben Sie die Statustransition des Dokuments in **Von** und **nach** under **Statusübergang**.

      - Geben Sie die Benutzer und Benutzergruppen an, die den Dokumentstatus in **Gruppen**.

      - Klicken Sie auf **Hinzufügen** -Schaltfläche, um eine Statustransition hinzuzufügen.

      - Klicken Sie auf das Symbol Löschen , um eine Statustransition zu löschen.

     >[!NOTE]
     >
     > Löschen Sie keine Statusübergänge, wenn sich Dokumente noch in der `From` state. Wenn Sie eine Statustransition löschen, können Sie den Dokumentstatus solcher Dokumente nur ändern, wenn Sie zum *administrator* Benutzergruppe.

1. Klicken Sie auf **Fertig**.

## Erstellen einer Kopie eines Dokumentstatusprofils

Je nach Anforderung können Sie eine Kopie eines vorhandenen Dokumentstatusprofils erstellen. Sie können die Kopie als Grundlage für die Erstellung eines anderen Dokumentprofils verwenden.

Um eine Kopie eines Dokumentstatusprofils zu erstellen, führen Sie die folgenden Schritte aus:

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools.
1. Klicken Sie auf die Kachel Dokumentstatus .

   Die Seite &quot;Asset-Status&quot;wird angezeigt.

1. Wählen Sie das zu duplizierende Dokumentstatusprofil aus und klicken Sie auf **Profil duplizieren**.
1. Nehmen Sie die erforderlichen Änderungen vor und klicken Sie auf **Fertig**.

## Löschen von Dokumentstatus- oder Statusübergängen

>[!NOTE]
>
> Löschen Sie keine Dokumentstatus- oder Statusübergänge, wenn sich Dokumente noch im Status- oder Statusübergang befinden. Wenn Sie einen Status- oder Statusübergang löschen, können Sie den Dokumentstatus solcher Dokumente nur ändern, wenn Sie zum *administrator* Benutzergruppe.

Führen Sie die folgenden Schritte aus, um einen Dokumentstatus- oder Statusübergang aus einem Dokumentstatusprofil zu löschen:

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools.
1. Klicken Sie auf die Kachel Dokumentstatus .

   Die Seite &quot;Asset-Status&quot;wird angezeigt.

1. Wählen Sie das Dokumentstatusprofil aus, aus dem Sie den Dokumentstatus löschen möchten, und klicken Sie auf **Profil bearbeiten**.
1. Löschen Sie den Dokumentstatus bzw. die Statustransition und klicken Sie auf **Fertig**.

## Löschen von Dokumentstatusprofilen

Um ein Dokumentenstatusprofil zu löschen, führen Sie die folgenden Schritte aus:

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.
1. Auswählen **Handbücher** aus der Liste der Tools.
1. Klicken Sie auf die Kachel Dokumentstatus .

   Die Seite &quot;Asset-Status&quot;wird angezeigt.

1. Wählen Sie das zu löschende Dokumentstatusprofil aus und klicken Sie auf **Profil löschen**.

## Dokumentstatusänderung automatisieren

Wenn Sie den Dokumentstatus nicht manuell ändern möchten, können Sie einen Workflow erstellen und die Änderung des Dokumentstatus automatisieren.

>[!NOTE]
>
> Automatisierte Workflows sollten den in der Konfiguration definierten Dokumentstatus und Transitionen entsprechen. Das System führt keine Prüfungen auf Statusänderungen durch, die über automatisierte Workflows durchgeführt werden.

Führen Sie die folgenden Schritte aus, um die Änderung des Dokumentstatus zu automatisieren:

1. Öffnen Sie die Workflow-Seite über die AEM-Server-URL.

   `<AEM_Server_URL>:<port>/workflow`

1. Öffnen Sie einen Workflow auf der Workflow-Seite. Beispiel: Thema überprüfen.
1. Auswählen **Prozessschritt** aus dem **Workflow** und ziehen Sie den Workflow per Drag-and-Drop in den AEM.

   ![](assets/process-step-workflow.png)

1. Doppelklicken Sie auf den Prozess und öffnen Sie die **Schritt-Eigenschaften** angezeigt.
1. Geben Sie die folgenden Details in die **Prozess** Registerkarte des Dialogfelds und klicken Sie auf OK:
   - Auswählen **Dokumentstatus für jedes DAM-Asset festlegen** aus der Dropdown-Liste Prozess aus.
   - Aktivieren Sie das Kontrollkästchen Handler-Modus .
   - Geben Sie den Namen des Dokumentstatus im **Argumente** Textfeld.

     >[!NOTE]
     >
     > Vergewissern Sie sich, dass Sie den richtigen Dokumentstatus in das Textfeld Argument eingeben. Wenn Sie einen falschen Namen eingeben, wird für das Dokument der falsche Dokumentstatus festgelegt.

1. Klicks **Speichern** , um den Workflow zu speichern.

## Genehmigungs-Workflow aktivieren

AEM Guides bieten einen Arbeitsablauf für die Dokumentgenehmigung, mit dem Sie den Lebenszyklus Ihres Dokumententwicklungsprozesses steuern können. Führen Sie die folgenden Schritte aus, um den Genehmigungs-Workflow zu aktivieren:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zur Standardkonfigurationsdatei, die unter folgendem Speicherort verfügbar ist:

   `/libs/fmdita/clientlibs/clientlibs/xmleditor/ui_config.json`

1. Erstellen Sie eine Kopie der Standardkonfigurationsdatei an folgendem Speicherort:

   `/apps/fmdita/xmleditor/ui_config.json`

1. Navigieren Sie zu und öffnen Sie die `ui_config.json` in der Datei `apps` Knoten zur Bearbeitung.

1. Im `ui_config.json` Datei, aktivieren Sie die Validierungs-Workflow-Funktion, indem Sie die *Funktionen* wie unten gezeigt:

   ```json
   "features":  
   { 
      "approvalWorkflow":  true 
   }
   ```
