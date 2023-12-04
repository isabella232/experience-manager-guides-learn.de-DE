---
title: Verwenden von Bedingungsvorgaben
description: Erfahren Sie mehr über die Verwendung von Bedingungsvorgaben in AEM Guides. Erfahren Sie, wie Sie in AEM Bedingungsvorgaben erstellen, bearbeiten, kopieren und löschen.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 1%

---

# Verwenden von Bedingungsvorgaben {#id1825FL004PN}

Sie können Attribute in Ihren DITA-Themen definieren und mithilfe der Bedingungsvoreinstellung festlegen, was mit dem -Attribut in der endgültigen Ausgabe geschieht. Sie können beispielsweise Attribute als Version 1.0 und Version 2.0 in Ihren Inhalt einfügen und eine Bedingungsvoreinstellung verwenden, um Version 1.0 für Version 1.0 einzubeziehen und Version 2.0 auszuschließen. Auf ähnliche Weise können Sie Ihrem Inhalt Attribute wie Windows und OS Linux hinzufügen und dann den relevanten Inhalt für Ihre endgültige Ausgabe gemäß dem Betriebssystem einschließen oder ausschließen.

Sie können Bedingungsvorgaben auf zwei Arten erstellen:

* Im Web-Editor: Ermöglicht die Erstellung und Verwaltung der Bedingungsvorgaben für eine DITA-Zuordnung im Web Editor.
* Über das Mapping-Dashboard: Ermöglicht die Erstellung und Verwaltung der Bedingungsvorgaben für eine DITA-Map über das Mapping-Dashboard.


## Bedingungsvorgaben aus dem Web-Editor

In Experience Manager-Handbüchern können Sie Bedingungsvorgaben im Web-Editor verwalten und in den Ausgabevorgaben verwenden, um die endgültige Ausgabe zu generieren.
Sie können die Bedingungsvorgaben erstellen und anzeigen, die Attribute anzeigen und die Aktionen für die aktuelle Zuordnung über die **Bedingungsvorgaben** im Web Editor angezeigt.

<img src="images//manage-condtions-presets.png" alt= "Bedingungsvorgaben im Web-Editor" width="800" border="1px">



### Bedingungsvorgabe erstellen

Die **Bedingungsvorgaben** -Ansicht enthält detaillierte Informationen zu den Bedingungsvorgaben, z. B. deren Attributen, Werten und Aktionen.
Sie können eine Bedingungsvoreinstellung für die Themen erstellen, indem Sie die folgenden Schritte ausführen:

1. Im **Repository** öffnen Sie die DITA-Map-Datei in der Kartenansicht.
1. Wählen Sie die **Verwalten** Registerkarte.
1. Auswählen **Bedingungsvorgaben** auf der linken Seite. Die Liste der für die DITA-Zuordnung definierten Bedingungsvorgaben wird angezeigt.
1. Wählen Sie das Symbol + neben **Bedingungsvorgaben** , um die **Neue Bedingungsvorgabe** angezeigt.
1. Geben Sie einen eindeutigen Namen für die Vorgabe ein.

   >[!NOTE]
   >
   > Wenn das Namensfeld leer ist oder Sie ein ungültiges Zeichen oder einen Namen eingeben, der mit einer vorhandenen Bedingungsvorgabe übereinstimmt, wird ein Fehler angezeigt. Sie können einen Bindestrich &quot;-&quot;oder einen Unterstrich &quot;_&quot;als Trennzeichen verwenden.

1. Auswählen **Erstellen**.
Die neue Bedingungsvoreinstellung wird der Liste hinzugefügt.
1. Doppelklicken Sie auf eine Bedingungsvorgabe, um die Attribute und Aktionen anzuzeigen.
Die **Attribute** zeigt alle Attribute an, die zu allen Verweisen hinzugefügt wurden, die in der Zuordnung vorhanden sind. Im rechten Bereich werden nur die Bedingungen angezeigt, die Sie den Bedingungsvorgaben hinzugefügt haben.
1. Führen Sie einen der folgenden Schritte aus, um die Attribute hinzuzufügen:
   * Wählen Sie ein oder mehrere Attribute aus, um alle darunter stehenden Werte zur Bedingungsvorgabe hinzuzufügen. Sie können beispielsweise die `platform` -Attribut, um alle zugehörigen Werte hinzuzufügen.
   * Wählen Sie einen oder mehrere Attributwerte aus, um sie der Bedingungsvorgabe hinzuzufügen. Sie können beispielsweise die `Unix` und `Win` Plattformattribute-Werte
   * Wählen Sie ein beliebiges Attribut- und Wertpaar aus und ziehen Sie es in das mittlere Bedienfeld. Sie können beispielsweise die `Unix` des Plattformattributs und ziehen Sie es.
   * **Alle auswählen** , um alle Attribute und deren Werte zur Bedingungsvoreinstellung hinzuzufügen.
Standardmäßig ist die Aktion für ein Attribut `Include`.

1. Auswählen **Hinzufügen**. Sie können diesen Schritt wiederholen, um weitere Attribute hinzuzufügen. Die von Ihnen hinzugefügten Attribute werden von der Mitte zum rechten Bereich verschoben.
1. Wählen Sie oben in der Aktionsleiste Entfernen aus, um die ausgewählten Attribute im rechten Bereich zu entfernen.
1. (Optional) Bei Bedarf können Sie die auf die Attribute angewendete Aktion überschreiben.
Führen Sie einen der folgenden Schritte aus:
   * Wählen Sie für jedes Attribut eine der folgenden Aktionen aus der Dropdown-Liste Aktion aus.
      * Einschließen
      * Ausschließen
      * Durchgang
      * Kennzeichnung
   * Wählen Sie im rechten Bereich mehrere Attributzeilen aus und wählen Sie in der Aktionsleiste oben eine Aktion aus. Beispielsweise können Sie die Aktion Ausschließen für die ausgewählten Attribute auswählen.
1. Auswählen **Speichern** , um die Bedingungsvorgabe zu speichern.

   >[!NOTE]
   >
   > Sie sehen eine Warnung, wenn Sie eine andere Vorgabe auswählen oder die Vorgabe schließen, ohne sie zu speichern.

Nachdem Sie eine Bedingungsvorgabe erstellt haben, wird sie unter der **Bedingungsvorgaben** Dropdown-Liste der Ausgabevorgaben. Erfahren Sie mehr über das [PDF-Ausgabe veröffentlichen](../web-editor/native-pdf-web-editor.md).

### Umbenennen einer Bedingungsvorgabe

Führen Sie die folgenden Schritte aus, um eine Bedingungsvorgabe umzubenennen:

1. Bewegen Sie den Mauszeiger über eine Bedingungsvorgabe aus der **Bedingungsvorgaben** Bedienfeld.
1. Auswählen **Umbenennen** über das Menü Optionen , um die **Vorgabe für Bedingungen umbenennen** angezeigt.
1. Bearbeiten Sie den Namen der Bedingungsvorgabe.
1. Klicks **Umbenennen**.

### Bedingungsvorgabe duplizieren

Führen Sie die folgenden Schritte aus, um eine Bedingungsvorgabe zu duplizieren:

1. Bewegen Sie den Mauszeiger über eine Bedingungsvorgabe aus der **Bedingungsvorgaben** Bedienfeld.
1. Auswählen **Duplizieren** über das Menü Optionen , um die **Vorgabe für doppelte Bedingung** angezeigt.
   >[!NOTE]
   >
   > Der Standardname der Vorgabe lautet `<selected condition preset name>_1`. Sie können den Namen entsprechend Ihren Anforderungen ändern.

1. Klicks **Duplizieren**.

### Bedingungsvorgabe löschen

Führen Sie die folgenden Schritte aus, um Bedingungsvorgaben zu löschen:

1. Bewegen Sie den Mauszeiger über eine Bedingungsvorgabe aus der **Bedingungsvorgaben** Bedienfeld.
1. Auswählen **Löschen** über das Menü Optionen , um die **Bedingungsvorgabe löschen** angezeigt.
1. Klicken Sie auf **Löschen**.



## Bedingungsvorgaben aus dem Mapping-Dashboard


### Bedingungsvorgabe erstellen

Führen Sie die folgenden Schritte aus, um eine Bedingungsvorgabe zu erstellen:

1. Auswählen **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Klicks **Erstellen** Schaltfläche.
1. Geben Sie einen Namen für die Vorgabe in ein **Namensbedingung**.
1. Wählen Sie eine der folgenden Standardaktionen aus **Legen Sie die Standardaktion auf** Dropdownliste:

   * Einschließen
   * Ausschließen
   * Durchgang
   * Flag Die Aktion wird als Standardaktion für alle Attribute festgelegt, unabhängig davon, ob sie zur Bedingungsvorgabe hinzugefügt werden oder nicht.

   Sie haben beispielsweise 15 Bedingungsattribute in Ihrem Dokument und vier davon wurden in die Bedingungsvorgabe aufgenommen. Wenn Sie **exclude** als Standardaktion festgelegt ist, wird sie auf alle 15 Attribute angewendet.

1. Führen Sie einen der folgenden Schritte aus, um die Attribute hinzuzufügen:
   * Klicks **Hinzufügen** auf ein Attribut zur Bedingungsvorgabe. Sie können diesen Schritt wiederholen, um weitere Attribute hinzuzufügen.
   * Klicks **Alle hinzufügen** , um alle Attribute zur Bedingungsvorgabe hinzuzufügen.
1. \(Optional\) Bei Bedarf können Sie die Standardaktion überschreiben, die auf die Attribute in Schritt 4 angewendet wird. Führen Sie einen der folgenden Schritte aus:
   * Auswählen mehrerer Attribute, Auswählen einer Aktion aus **Setzen Sie die Aktion für ausgewählte Bedingungen auf** und klicken Sie auf **Anwenden**.
   * Wählen Sie eine Aktion für ein Attribut aus dem **Aktion** angezeigt.
1. Klicken Sie auf **Speichern**.

### Bedingungsvorgabe bearbeiten

Sie können Änderungen an einer vorhandenen Bedingungsvorgabe vornehmen, um die Aktionen zu ändern, die auf die Attribute in der Bedingungsvorgabe angewendet werden. Führen Sie die folgenden Schritte aus, um eine Bedingungsvorgabe zu bearbeiten:

1. Auswählen **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Klicks **Bearbeiten** Schaltfläche.
1. Nehmen Sie die erforderlichen Änderungen für alle Attribute in der Bedingungsvorgabe vor.
1. Klicken Sie auf **Speichern**.

### Erstellen einer Kopie einer Bedingungsvorgabe

Sie können eine Kopie einer Bedingungsvorgabe erstellen und diese dann entsprechend Ihren Anforderungen ändern. Führen Sie die folgenden Schritte aus, um eine Kopie einer Bedingungsvorgabe zu erstellen:

1. Auswählen **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Klicks **Duplizieren** Schaltfläche.

   >[!NOTE]
   >
   > Der Standardname der Vorgabe lautet `<selected condition preset name>_Duplicate`

   Sie können den Namen nach Bedarf ändern.

1. \(Optional\) Nehmen Sie die erforderlichen Änderungen für alle Attribute in der Bedingungsvorgabe vor.
1. Klicken Sie auf **Speichern**.

### Bedingungsvorgabe löschen

Sie können eine oder mehrere Bedingungsvorgaben aus dem **Bedingungsvorgabe** Registerkarte der DITA-Map-Konsole. Führen Sie die folgenden Schritte aus, um Bedingungsvorgaben zu löschen:

1. Auswählen **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Wählen Sie die zu löschenden Bedingungsvorgaben aus.
1. Klicks **Entfernen** Schaltfläche.
1. Klicks **Entfernen** , um die Aktion zu bestätigen.

**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)
