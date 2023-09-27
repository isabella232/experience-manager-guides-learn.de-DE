---
title: Bearbeiten von Themen im Web-Editor
description: Erfahren Sie, wie Sie Themen im Web-Editor bearbeiten können. Erfahren Sie mehr über verschiedene Bearbeitungsfunktionen, um Ihre Themendateien in AEM Handbüchern zu ändern.
exl-id: 9950df78-09bd-433a-891d-0d689bb0c2e4
source-git-commit: 3cc7a9bf91881ed09173077be7d7fc7705295e4b
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Bearbeiten von Themen im Web-Editor {#id2056B040VUI}

Der Web Editor verfügt über eine Reihe von Bearbeitungsfunktionen, mit denen Sie Themendateien einfach erstellen oder ändern können. Im Großen und Ganzen führen Sie die folgenden Schritte aus, um ein Thema im Web Editor zu bearbeiten.

>[!IMPORTANT]
>
> Wenn bei der Arbeit mit dem Web Editor ein Anwendungsfehler auftritt, aktualisieren Sie die Seite, damit sie weiterhin funktioniert.

1. Um Änderungen an Ihrem Thema vorzunehmen, klicken Sie auf den Textbereich des erforderlichen Elements und nehmen Sie Änderungen vor.

1. Um ein bestimmtes Element einzufügen, klicken Sie auf das Ende des Elements, nach dem Sie das neue Element einfügen möchten, und klicken Sie in der Symbolleiste auf das Symbol für das gewünschte Element. Sie können auch den Tastaturbefehl `Alt+Enter` , um die **Element einfügen** Popup.

   Es wird eine Liste mit Elementen angezeigt, die im Thema verwendet werden können. AEM Guides führen eine intelligente Platzierung von Elementen gemäß ihrer gültigen Position im Thema durch.

   >[!NOTE]
   >
   > Sie können auch auswählen, welches Symbol in der Symbolleiste angezeigt werden soll, indem Sie die `ui_config.json` Datei unter - `/etc/designs/fmdita/clientlibs/xmleditor/`. Weitere Informationen zum Anpassen von Funktionen erhalten Sie von Ihrem Systemadministrator.

1. Nachdem Sie die Bearbeitung des Dokuments abgeschlossen haben, klicken Sie auf **Speichern**.

   >[!NOTE]
   >
   > Wenn Sie keine Änderungen in AEM Repository übertragen möchten, klicken Sie auf **Schließen** und klicken Sie anschließend auf **Ohne Speichern schließen** im Dialogfeld Nicht gespeicherte Änderungen .

   **Aktualisieren des Browsers beim Bearbeiten der Dateien**
AEM Handbücher bieten die Möglichkeit, den Browser zu aktualisieren, während Sie Ihre Inhalte im Web Editor bearbeiten. Mit dieser Funktion können Sie die Bearbeitung von Inhalten fortsetzen, falls bei der Arbeit ein Anwendungsfehler auftritt. Wenn Sie auf die Browseraktualisierung klicken, während eine oder mehrere Dateien mit nicht gespeicherten Änderungen zur Bearbeitung geöffnet sind, werden Sie gewarnt, dass die nicht gespeicherten Änderungen möglicherweise verloren gehen. Sie erhalten die Möglichkeit, den Aktualisierungsvorgang abzubrechen und Ihre Dateien zu speichern, um Ihre Änderungen beizubehalten.

   Selbst beim Aktualisieren des Browsers werden die Ansichten des linken und des rechten Bereichs im Web Editor beibehalten. Beispielsweise wird das aktive Thema im Bereich &quot;Repository&quot;erneut geöffnet. Das Zuordnungsbedienfeld wird zusammen mit der zuvor geöffneten Karte beibehalten.

   Das aktive Thema oder die DITA-Zuordnung wird im Inhaltsbearbeitungsbereich erneut geöffnet.

   Das rechte Bedienfeld wird ebenfalls neu geöffnet und zeigt dieselbe Ansicht an wie vor der Aktualisierung.

   **Arbeitskopierer**
AEM Handbücher bieten einen Arbeitskopie-Indikator, der anzeigt, ob die aktuelle \(Arbeitskopie\) der Datei mit der gespeicherten Version synchronisiert ist oder nicht. Wenn Sie Änderungen an Ihrer aktuellen Kopie vorgenommen und Ihre Datei nicht gespeichert haben, wird auf der Registerkarte &quot;Datei&quot;des Themas ein \*-Zeichen mit dem Titel angezeigt. Dieser Indikator dient als Erinnerung, um Ihre Änderungen zu speichern, und verschwindet, wenn Sie Ihre Datei speichern.

   ![](images/working-copy-text-update-indicator.png){width="550" align="left"}

   AEM Guides zeigen auch an, ob die letzte gespeicherte \(Work\) Kopie der Datei mit der gespeicherten Version synchronisiert ist oder nicht. Wenn Sie einige nicht gespeicherte Änderungen zwischen der Arbeitskopie und der zuletzt gespeicherten Version haben, wird ein \*-Zeichen zusammen mit den Versionsinformationen angezeigt, die in der rechten oberen Ecke der Registerkarte &quot;Datei&quot;des Themas angezeigt werden. Dieser Indikator dient als Erinnerung zum Speichern und Erstellen einer Version aus Ihrer aktuellen \(funktionierenden\) Kopie der Datei.

   ![](images/version-update-indicator.png){width="550" align="left"}


**Übergeordnetes Thema:**[ Arbeiten mit dem Web-Editor](web-editor.md)
