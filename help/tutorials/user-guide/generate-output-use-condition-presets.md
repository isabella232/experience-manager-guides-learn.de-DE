---
title: Verwenden von Bedingungsvorgaben
description: Erfahren Sie, wie Sie Bedingungsvorgaben verwenden
source-git-commit: 6eb8d29e71301581e8dbb5b6a4252194c5a89f96
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---


# Verwenden von Bedingungsvorgaben {#id1825FL004PN}

Sie können Attribute in Ihren DITA-Themen definieren und mithilfe der Bedingungsvoreinstellung festlegen, was mit dem -Attribut in der endgültigen Ausgabe geschieht. Beispielsweise können Sie Ihrem Inhalt Attribute wie Version 1.0 und Version 2.0 hinzufügen und eine Bedingungsvoreinstellung verwenden, um Version 1.0 für Version 1.0 einzubeziehen und Version 2.0 auszuschließen. Ebenso können Sie Ihrem Inhalt Attribute wie Windows und Linux des Betriebssystems hinzufügen und dann den relevanten Inhalt für Ihre endgültige Ausgabe entsprechend dem Betriebssystem ein- oder ausschließen.

## Bedingungsvorgabe erstellen

Führen Sie die folgenden Schritte aus, um eine Bedingungsvorgabe zu erstellen:

1. Klicken **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Klicken **Erstellen** Schaltfläche.
1. Geben Sie einen Namen für die Vorgabe in ein. **Namensbedingung**.
1. Wählen Sie eine der folgenden Standardaktionen aus **Legen Sie die Standardaktion auf** Dropdown-Liste:

   - Einschließen
   - Ausschließen
   - Durchgang
   - Flag Die Aktion wird als Standardaktion für alle Attribute festgelegt, unabhängig davon, ob sie zur Bedingungsvorgabe hinzugefügt werden oder nicht.

   Sie haben beispielsweise 15 Bedingungsattribute in Ihrem Dokument und vier davon wurden in die Bedingungsvorgabe aufgenommen. Wenn Sie **exclude** als Standardaktion festgelegt ist, wird sie auf alle 15 Attribute angewendet.

1. Führen Sie einen der folgenden Schritte aus, um die Attribute hinzuzufügen:
   - Klicken **Hinzufügen** auf ein Attribut zur Bedingungsvoreinstellung. Sie können diesen Schritt wiederholen, um weitere Attribute hinzuzufügen.
   - Klicken **Alle hinzufügen** , um alle Attribute zur Bedingungsvorgabe hinzuzufügen.
1. \(Optional\) Bei Bedarf können Sie die Standardaktion überschreiben, die auf die Attribute in Schritt 4 angewendet wird. Führen Sie einen der folgenden Schritte aus:
   - Auswählen mehrerer Attribute, Auswählen einer Aktion aus **Setzen Sie die Aktion für ausgewählte Bedingungen auf** und klicken Sie auf **Anwenden**.
   - Wählen Sie eine Aktion für ein Attribut aus dem **Aktion** Dropdown-Liste.
1. Klicken Sie auf **Speichern**.

## Bedingungsvorgabe bearbeiten

Sie können Änderungen an einer vorhandenen Bedingungsvorgabe vornehmen, um die Aktionen zu ändern, die auf die Attribute in der Bedingungsvorgabe angewendet werden. Führen Sie die folgenden Schritte aus, um eine Bedingungsvorgabe zu bearbeiten:

1. Klicken **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Klicken **Bearbeiten** Schaltfläche.
1. Nehmen Sie die erforderlichen Änderungen für alle Attribute in der Bedingungsvorgabe vor.
1. Klicken Sie auf **Speichern**.

## Erstellen Sie eine Kopie einer Bedingungsvorgabe

Sie können eine Kopie einer Bedingungsvorgabe erstellen und diese dann entsprechend Ihren Anforderungen ändern. Führen Sie die folgenden Schritte aus, um eine Kopie einer Bedingungsvorgabe zu erstellen:

1. Klicken **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Klicken **Duplizieren** Schaltfläche.

   >[!NOTE]
   >
   > Der Standardname der Vorgabe lautet `<selected condition preset name>_Duplicate`

   Sie können den Namen nach Bedarf ändern.

1. \(Optional\) Nehmen Sie die erforderlichen Änderungen für alle Attribute in der Bedingungsvorgabe vor.
1. Klicken Sie auf **Speichern**.

## Bedingungsvorgabe löschen

Sie können eine oder mehrere Bedingungsvorgaben aus dem **Bedingungsvorgabe** Registerkarte der DITA-Map-Konsole. Führen Sie die folgenden Schritte aus, um Bedingungsvorgaben zu löschen:

1. Klicken **Bedingungsvorgaben** in der DITA-Map-Konsole.
1. Wählen Sie die zu löschenden Bedingungsvoreinstellungen aus.
1. Klicken **Entfernen** Schaltfläche.
1. Klicken **Entfernen** , um die Aktion zu bestätigen.

**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)

