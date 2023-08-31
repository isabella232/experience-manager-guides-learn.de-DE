---
title: Veröffentlichen eines Themas in einem Inhaltsfragment
description: Erfahren Sie, wie Sie ein Thema in einem Inhaltsfragment veröffentlichen.
source-git-commit: dd677257d94015d888705e4b6a43ae877e58be4b
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 1%

---


# In einem Inhaltsfragment veröffentlichen

Inhaltsfragmente sind separate Inhaltsfragmente in AEM. Sie sind strukturierte Inhalte, die auf einem Inhaltsmodell basieren. Inhaltsfragmente sind reine Inhalte ohne Design- oder Layoutinformationen. Sie können unabhängig von den von AEM unterstützten Kanälen erstellt und verwaltet werden. Inhaltsfragmente sind modular, wobei Inhalte in kleinere Komponenten unterteilt werden.

Mit AEM Guides können Sie ein Thema oder die Elemente innerhalb eines Themas in einem Inhaltsfragment veröffentlichen. Sie können eine JSON-basierte Zuordnung zwischen einem Thema und einem Inhaltsfragmentmodell erstellen. Verwenden Sie diese Zuordnung, um ein Thema oder die Elemente innerhalb eines Themas in einem Inhaltsfragment zu veröffentlichen. Sie können dann Inhaltsfragmente in jeder beliebigen AEM-Site verwenden oder die Details über APIs extrahieren, die von Inhaltsfragmenten unterstützt werden.


Gehen Sie wie folgt vor, um ein Inhaltsfragment zu erstellen:

1. Erstellen Sie eine [Inhaltsfragmentmodell](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=de) in AEM Assets.
1. Erstellen Sie einen Ordner, in dem Sie die Inhaltsfragmente speichern möchten, die Sie basierend auf dem Inhaltsfragmentmodell erstellen. Beispiel: &quot;stock-content-fragments&quot;.
1. Bearbeiten Sie die Eigenschaften des Ordners (z. B. &quot;stock-content-fragments&quot;) und fügen Sie den Pfad des Ordners hinzu, der das Inhaltsfragmentmodell in der Cloud-Konfiguration enthält.
Fügen Sie beispielsweise `/conf/we-retail` in der Cloud-Konfiguration. Diese Konfiguration verbindet alle Inhaltsfragmentmodelle mit dem Ordner .\
   ![Cloud-Konfigurationsdetails in den Ordnereigenschaften hinzufügen](images/fragment-folder-cloud-configuration.png){width="650" align="left"}
   *Fügen Sie die Cloud-Konfiguration in den Ordnereigenschaften hinzu, um sie mit den Fragmentmodellen zu verbinden.*
1. Wählen Sie das Thema aus, das Sie im **Repository-Ansicht**.
1. Aus dem **Optionen** Menü auswählen **Veröffentlichen als** > **Inhaltsfragment**.
1. Im **Als Inhaltsfragment veröffentlichen** das folgende Dialogfeld ausfüllen:
   ![Fügen Sie das Fragmentmodell und die Zuordnungsdetails im Dialogfeld Als Inhaltsfragment veröffentlichen hinzu](images/content-fragment-publish.png){width="500" align="left"}
   *Fügen Sie die Pfad-, Modell- und Zuordnungsdetails hinzu, um ein Thema oder seine Elemente als Inhaltsfragment zu veröffentlichen. Sie können ein vorhandenes Inhaltsfragment überschreiben.*

   * **Pfad**: Durchsuchen und wählen Sie den Pfad des Ordners aus, in dem Sie das Inhaltsfragment veröffentlichen möchten. Sie können auch ein vorhandenes Inhaltsfragment auswählen und veröffentlichen.
   * **Titel**: Geben Sie den Titel des Inhaltsfragments ein.
   * **Name**: Geben Sie den Namen des Inhaltsfragments ein.
   * **Modell**: Wählen Sie das Inhaltsfragmentmodell aus, das Sie zum Erstellen Ihres Inhaltsfragments verwenden möchten. Die Modelle werden aus dem Ordner ausgewählt, den Sie in den Cloud-Services konfiguriert haben.
   * **Zuordnung**: Wählen Sie eine Zuordnung aus der Dropdown-Liste aus. Es wählt die Zuordnungen aus der *contentFragmentMapping.json* -Datei.



     Je nach Einrichtung kann Ihr Administrator die Zuordnungen im *contentFragmentMapping.json* -Datei.

     <details>
        <summary>Cloud Services</summary>

     Erfahren Sie mehr über das [Erstellen einer Zuordnung zwischen einem Thema und einem Inhaltsfragment](../cs-install-guide/conf-content-fragment-mapping-cs.md) im Cloud Service-Installations- und Konfigurationshandbuch.
     </details>

     <details>
        <summary> On-Premise Software</summary>

     Erfahren Sie mehr über das [Erstellen einer Zuordnung zwischen einem Thema und einem Inhaltsfragment](../install-guide/conf-content-fragment-mapping.md) im On-Premise-Installations- und Konfigurationshandbuch.

     </details>
   * Wählen Sie die **Überschreiben** aktivieren, wenn Ihr Inhaltsfragment bereits existiert und Sie es überschreiben möchten. AEM Guides zeigt einen Fehler an, wenn Sie das Kontrollkästchen nicht aktivieren und Ihr Inhaltsfragment bereits existiert.
1. Klicks **Erstellen** , um das Inhaltsfragment zu veröffentlichen.
1. Sie können die Inhaltsfragmente für ein Thema unter dem **Fragmente** im Abschnitt **Dateieigenschaften**.

   ![Inhaltsfragmente für ein Thema anzeigen](images/topic-content-fragments.png){width="300" align="left"}

   *Zeigen Sie die für ein Thema vorhandenen Inhaltsfragmente an und veröffentlichen Sie sie erneut.*

Sie können das Inhaltsfragment auch erneut veröffentlichen, um das Inhaltsfragment mit dem neuesten Inhalt aus dem DITA-Thema zu aktualisieren.



Nachdem Sie die Inhaltsfragmente veröffentlicht haben, können Sie sie auch auf jeder beliebigen AEM verwenden.

