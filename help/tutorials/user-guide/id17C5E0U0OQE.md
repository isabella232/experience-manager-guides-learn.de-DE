---
title: DITAVAL-Editor
description: Erfahren Sie, wie Sie den DITAVAL-Editor
source-git-commit: 9d0f5e7958f3b57a89abfb053bb40a4e84348e03
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---


# DITAVAL-Editor {#id17C5E0U0OQE}

DITAVAL-Dateien werden verwendet, um eine bedingte Ausgabe zu generieren. In einem einzelnen Thema können Sie Bedingungen mithilfe von Elementattributen hinzufügen, um Inhalte an Bedingungen zu knüpfen. Anschließend erstellen Sie eine DITAVAL-Datei, in der Sie die Bedingungen angeben, die aufgenommen werden sollen, um Inhalte zu generieren, und welche Bedingung aus der endgültigen Ausgabe ausgeschlossen werden soll.

Mit AEM Guides können Sie DITAVAL-Dateien einfach mit dem DITAVAL-Editor erstellen und bearbeiten. Der DITAVAL-Editor ruft die in Ihrem System definierten Attribute \(oder Tags\) ab und Sie können sie zum Erstellen oder Bearbeiten von DITAVAL-Dateien verwenden. Weitere Informationen zum Erstellen und Verwalten von Tags in AEM finden Sie unter [Verwalten von Tags](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) in AEM Dokumentation.

## DITAVAL-Datei erstellen

Führen Sie die folgenden Schritte aus, um eine DITAVAL-Datei zu erstellen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zu dem Speicherort, an dem Sie die DITAVAL-Datei erstellen möchten.

1. Klicken **Erstellen** \> **DITA-Thema**.

1. Wählen Sie auf der Blueprint-Seite die DITAVAL-Dateivorlage aus und klicken Sie auf **Nächste**.

1. Geben Sie auf der Seite Eigenschaften die **Titel** und **Name** für die DITAVAL-Datei.

   >[!NOTE]
   >
   > Der Name wird basierend auf dem Titel Ihrer Datei automatisch vorgeschlagen. Wenn Sie den Dateinamen manuell angeben möchten, stellen Sie sicher, dass der Name keine Leerzeichen, Apostroph oder Klammern enthält und mit `.ditaval`.

1. Klicken Sie auf **Erstellen**. Die Meldung Thema erstellt wird angezeigt.

   Sie können die DITAVAL-Datei zur Bearbeitung im DITAVAL-Editor öffnen oder die Themendatei im AEM Repository speichern.


## DITAVAL-Datei bearbeiten

Führen Sie die folgenden Schritte aus, um eine DITAVAL-Datei zu bearbeiten:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITAVAL-Datei, die Sie bearbeiten möchten.
1. Um eine exklusive Sperre für die Datei zu erhalten, wählen Sie die Datei aus und klicken Sie auf **Auschecken**.
1. Wählen Sie die Datei aus und klicken Sie auf **Bearbeiten** , um die Datei im DITAVAL-Editor AEM Guides zu öffnen.

   Mit dem DITAVAL-Editor können Sie die folgenden Aufgaben ausführen:

   **A: Linkes Bedienfeld ein/aus**

   Wechsel zur linken Bereichsansicht. Wenn Sie die DITAVAL-Datei über die DITA-Zuordnung geöffnet haben, werden die Zuordnung und das Repository in diesem Bedienfeld angezeigt. Weitere Informationen zum Öffnen einer Datei über eine DITA-Zuordnung finden Sie unter [Themen über DITA-Map bearbeiten](map-editor-advanced-map-editor.md#id17ACJ0F0FHS).

   **B: Speichern**

   Speichert die Änderungen, die Sie in der Datei vorgenommen haben. Alle Ihre Änderungen werden in der aktuellen Version Ihrer Datei gespeichert.

   **C: Eigenschaft hinzufügen**

   Fügen Sie eine einzelne Eigenschaft in Ihrer DITAVAL-Datei hinzu.

   ![](images/ditaval-editor-props.png)

   In der ersten Dropdown-Liste werden die zulässigen DITA-Attribute aufgelistet, die Sie in der DITAVAL-Datei verwenden können. Es werden fünf Attribute unterstützt - `audience`, `platform`, `product`, `props`und `otherprops`.

   Die zweite Dropdown-Liste zeigt die für das ausgewählte Attribut konfigurierten Werte an. In der nächsten Dropdownliste werden die Aktionen angezeigt, die Sie für das ausgewählte Attribut konfigurieren können. Zulässige Werte in der Dropdown-Liste Aktion sind: `include`, `exclude`, `passthrough`und `flag`. Weitere Informationen zu diesen Werten finden Sie in der Definition von [prop](http://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/ditaval/ditaval-prop.html#ditaval-prop) Element in der OASIS DITA-Dokumentation

   **D: Alle Eigenschaften hinzufügen**

   Wenn Sie alle in Ihrem System definierten bedingten Eigenschaften oder Attribute mit einem Klick hinzufügen möchten, verwenden Sie die Funktion Alle Eigenschaften hinzufügen .

   >[!NOTE]
   >
   > Wenn alle definierten bedingten Eigenschaften bereits in der DITAVAL-Datei vorhanden sind, können Sie keine weiteren Eigenschaften hinzufügen. In diesem Szenario erhalten Sie eine Fehlermeldung.

   ![](images/ditaval-all-props.png)

1. Nachdem Sie die Bearbeitung der DITAVAL-Datei abgeschlossen haben, klicken Sie auf **Speichern**.

   >[!NOTE]
   >
   > Wenn Sie die Datei ohne Speichern schließen, gehen die Änderungen verloren. Wenn Sie keine Änderungen in AEM Repository übertragen möchten, klicken Sie auf **Schließen** und klicken Sie anschließend auf **Ohne Speichern schließen** im **Nicht gespeicherte Änderungen** angezeigt.


## DITAVAL-Editor-Ansichten

Der DITAVAL-Editor von AEM Guides unterstützt die Anzeige von DITAVAL-Dateien in zwei verschiedenen Modi oder Ansichten:

**Autor** - Dies ist eine typische Ansicht des DITAVAL-Editors, was Sie sehen, was Sie \(WYSISYG\) erhalten. Sie können Eigenschaften über die einfache Benutzeroberfläche hinzufügen oder entfernen, in der die Eigenschaften, Werte und Aktionen in einer Dropdown-Liste angezeigt werden. In der Autorenansicht haben Sie die Möglichkeit, eine einzelne Eigenschaft einzufügen und alle Eigenschaften mit einem Klick einzufügen.

Sie können auch die Version der DITAVAL-Datei finden, an der Sie derzeit arbeiten, indem Sie den Mauszeiger über den Dateinamen bewegen.

**Quelle** - In der Quellansicht wird die zugrunde liegende XML-Datei angezeigt, aus der sich die DITAVAL-Datei zusammensetzt. In dieser Ansicht können Autoren nicht nur reguläre Textänderungen vornehmen, sondern auch Eigenschaften mithilfe des Smart-Katalogs hinzufügen oder bearbeiten.

Um den Smart-Katalog aufzurufen, platzieren Sie den Cursor am Ende einer beliebigen Eigenschaftsdefinition und geben Sie &quot;&lt;&quot;ein. Der Editor zeigt eine Liste aller gültigen XML-Elemente an, die Sie an dieser Stelle einfügen können.

![](images/ditaval-source-view.png)

**Übergeordnetes Thema:**[ Verfassen von Inhalten mithilfe AEM Handbüchern](authoring-content-xml-doc.md)

