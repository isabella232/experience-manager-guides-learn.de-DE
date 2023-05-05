---
title: JSON
description: Erfahren Sie, wie Sie JSON verwenden
exl-id: 0a938cc2-1a6f-4ee4-ad7e-f94ad2a0cf94
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# JSON {#id231KK0180T4}

Sie können die JSON-Vorgabe im Web Editor erstellen:

Öffnen Sie im Bereich &quot;Repository&quot;die DITA-Zuordnungsdatei in der Zuordnungsansicht, wählen Sie dann auf der Registerkarte &quot;Ausgabe&quot;das Symbol + aus, um eine Ausgabevorgabe zu erstellen, und wählen Sie dann JSON aus der Dropdown-Liste Typ im Dialogfeld Vorgabe hinzufügen aus.

Im Web-Editor wurden die folgenden Konfigurationen unter dem **Allgemein** tab:

- Ausgabepfad
- Indexdatei
- Bedingungen anwenden mit \(Wenn die Bedingungen für eine Zuordnung definiert sind\)
- Grundlinie verwenden \(Wenn eine Grundlinie für eine Zuordnung erstellt wird\)
- Eigenschaften, die in der Ausgabe propagiert werden sollen
- Arbeitsablauf nach der Erstellung

Weitere Informationen finden Sie unter [JSON-Konfiguration](#id231KJA00REJ).

**Über das Zuordnungs-Dashboard**

Um Ausgabevorgaben für das PDF zu öffnen, klicken Sie in der Assets-Benutzeroberfläche auf eine DITA-Zuordnungsdatei, klicken Sie dann auf Ausgabevorgaben und dann auf die Option HTML5 . Klicken Sie im Dashboard Map auf **Bearbeiten** Klicken Sie oben auf , um die verschiedenen Konfigurationen zu aktualisieren, und klicken Sie dann auf **Speichern**.

**JSON-Konfiguration**

Die folgenden Optionen sind für die JSON-Vorgabe verfügbar:

>[!NOTE]
>
> Sie können die JSON-Datei auch im Web Editor bearbeiten.

| JSON-Optionen | Beschreibung |
| --- | --- |
| Ausgabepfad | Der Pfad in Ihrem AEM-Repository, in dem die JSON-Ausgabe gespeichert wird. |
| Indexdatei | Sie können einen Namen für die Indexdatei angeben, die Sie für die JSON-Ausgabe erstellen. Standardmäßig wird der Dateiname der DITA-Map ausgewählt und ein Suffix hinzugefügt (wie `map_filename_index.json`).<br><br>Sie können auch Variablen beim Festlegen der Indexdatei verwenden. Weitere Informationen zur Verwendung von Variablen finden Sie unter [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](generate-output-use-variables.md#id18BUG70K05Z). |
| Bedingungen anwenden mit | Wählen Sie eine der folgenden Optionen aus:<br><br>* **Keine Anwendung**: Wählen Sie diese Option aus, wenn Sie keine Bedingung auf die veröffentlichte Ausgabe anwenden möchten.<br>* **DITAVAL-Datei**: Wählen Sie DITAVAL-Dateien aus, um personalisierten Inhalt zu generieren. Sie können mehrere DITAVAL-Dateien über das Dialogfeld &quot;Durchsuchen&quot;oder durch Eingabe des Dateipfads auswählen. Verwenden Sie das Kreuzsymbol neben dem Dateinamen, um ihn zu entfernen. DITAVAL-Dateien werden in der angegebenen Reihenfolge ausgewertet, sodass die in der ersten Datei angegebenen Bedingungen Vorrang vor den in späteren Dateien angegebenen Bedingungen haben. Sie können die Dateireihenfolge beibehalten, indem Sie Dateien hinzufügen oder löschen. Wenn die DITAVAL-Datei an einen anderen Speicherort verschoben oder gelöscht wird, wird sie nicht automatisch aus dem Mapping-Dashboard gelöscht. Sie müssen den Speicherort aktualisieren, falls Dateien verschoben oder gelöscht werden. Sie können den Mauszeiger über den Dateinamen bewegen, um den Pfad im AEM Repository anzuzeigen, in dem die Datei gespeichert ist. Sie können nur DITAVAL-Dateien auswählen. Wenn Sie einen anderen Dateityp ausgewählt haben, wird ein Fehler angezeigt.<br>* **Bedingungsvoreinstellung**: Wählen Sie eine Bedingungsvorgabe aus der Dropdown-Liste aus, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Die Option ist sichtbar, wenn Sie eine Bedingung auf der Registerkarte Bedingungsvorgaben der DITA-Zuordnungskonsole hinzugefügt haben. Weitere Informationen zur Bedingungsvorgabe finden Sie unter [Verwenden von Bedingungsvorgaben](generate-output-use-condition-presets.md#id1825FL004PN). |
| Grundlinie verwenden | Wenn Sie eine Grundlinie für die ausgewählte DITA-Zuordnung erstellt haben, wählen Sie diese Option, um die Version anzugeben, die Sie veröffentlichen möchten.<br><br>Siehe [Arbeiten mit Grundlinien](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) für weitere Details. |
| Eigenschaften, die in der Ausgabe propagiert werden sollen | Wählen Sie die Eigenschaften aus, die Sie als Metadaten verarbeiten möchten. Diese Eigenschaften werden auf der Seite &quot;Eigenschaften&quot;der DITA-Map- oder Bookmap-Datei festgelegt. Die Eigenschaften, die Sie aus der Dropdown-Liste auswählen, sind unter dem Feld Eigenschaften aufgeführt.<br><br>**Hinweis**: Sie können auch benutzerdefinierte Eigenschaften definieren und die Metadaten mithilfe der DITA-OT-Veröffentlichung an die Ausgabe übergeben. Weitere Informationen finden Sie unter [Arbeiten mit Metadaten](metadata-dita.md#id21BJ00QD0XA). |
| Arbeitsablauf nach der Erstellung | Wenn Sie diese Option wählen, wird eine neue Dropdownliste mit dem Workflow nach der Generierung angezeigt, die alle in AEM konfigurierten Workflows enthält. Sie müssen einen Workflow auswählen, der nach Abschluss des Workflows zur Generierung der Ausgabe ausgeführt werden soll.<br><br>**Hinweis**: Weitere Informationen zum Erstellen eines benutzerdefinierten Workflows für die Generierung nach der Ausgabe finden Sie unter _Arbeitsablauf für die Generierung nach der Ausgabe anpassen_ im as a Cloud Service Handbuch zum Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern. |

**Übergeordnetes Thema:**[ Grundlegendes zu den Ausgabevorgaben](generate-output-understand-presets.md)
