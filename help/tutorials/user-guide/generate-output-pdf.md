---
title: Generate PDF
description: Erfahren Sie, wie Sie eine PDF-Vorgabe aus dem Web-Editor und dem Map-Dashboard erstellen. Konfigurieren Sie die PDF-Ausgabevorgabe in AEM Guides.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 1%

---

# PDF {#id205BE600HAH}

Sie können die PDF-Vorgabe auf zwei Arten erstellen:

**Im Web-Editor:** Öffnen Sie im Bedienfeld &quot;Repository&quot;die DITA-Zuordnungsdatei in der Zuordnungsansicht, wählen Sie dann auf der Registerkarte &quot;Ausgabe&quot;das Symbol + aus, um eine Ausgabevorgabe zu erstellen, und wählen Sie dann PDF aus der Dropdown-Liste Typ im Dialogfeld Vorgabe hinzufügen aus.

>[!NOTE]
>
> Sie können die Methode zum Generieren von PDF mit DITA-OT, nativer PDF oder FMPS auswählen \(sofern Ihr Systemadministrator sie konfiguriert hat\).

Im Web-Editor wurden die Konfigurationen unter den Registerkarten Allgemein und Erweitert organisiert:

**Allgemein**

Die **Allgemein** tab enthält die folgenden Konfigurationen:

- Ausgabepfad
- DITA-OT-Befehlszeilenargumente
- Name der Umwandlung
- PDF Filename
- Bedingungen anwenden mit \(Wenn die Bedingungen für eine Zuordnung definiert sind\)
- Grundlinie verwenden \(Wenn eine Grundlinie für eine Zuordnung erstellt wird\)
- Arbeitsablauf nach der Erstellung

**Erweitert**

Die Registerkarte Erweitert enthält die folgenden Konfigurationen:

- Versionierung aktivieren
- Temporäre DITA-OT-Dateien bereinigen

Weitere Informationen finden Sie unter [PDF-Konfiguration](#id231KIM004X1).

**Über das Zuordnungs-Dashboard**

Um Ausgabevorgaben für das PDF zu öffnen, klicken Sie in der Assets-Benutzeroberfläche auf eine DITA-Zuordnungsdatei, klicken Sie auf Ausgabevorgaben und dann auf die Option PDF . Klicken Sie im Dashboard Map auf **Bearbeiten** Klicken Sie oben auf , um die verschiedenen Konfigurationen zu aktualisieren, und klicken Sie dann auf **Speichern**.

**PDF-Konfiguration**

Die folgenden Optionen sind für die PDF-Ausgabe verfügbar:

| PDF-Optionen | Beschreibung |
| --- | --- |
| Ausgabetyp | Der Typ der Ausgabe, die Sie generieren möchten. Um eine PDF-Ausgabe zu generieren, wählen Sie die Option PDF . |
| Einstellungsname | Geben Sie einen beschreibenden Namen für die PDF-Ausgabeeinstellungen ein, die Sie erstellen. Sie können beispielsweise _Interne Kundenausgabe_ oder _Ausgabe der Endbenutzer_. |
| DITA-OT-Befehlszeilenargumente | Geben Sie die zusätzlichen Argumente an, die DITA-OT beim Generieren der Ausgabe verarbeiten soll. Weitere Informationen zu den in DITA-OT unterstützten Befehlszeilenargumenten finden Sie unter [DITA-OT-Dokumentation](https://www.dita-ot.org/). |
| Bedingungen anwenden mit | Wählen Sie eine der folgenden Optionen aus:<br><br>* **Keine Anwendung**: Wählen Sie diese Option, wenn Sie keine Bedingung auf die veröffentlichte Ausgabe anwenden möchten.<br>* **DITAVal-Datei**: Wählen Sie DITAVal-Dateien aus, um personalisierten Inhalt zu generieren. Sie können mehrere DITAVal-Dateien über das Dialogfeld &quot;Durchsuchen&quot;oder durch Eingabe des Dateipfads auswählen. Verwenden Sie das Kreuzsymbol neben dem Dateinamen, um ihn zu entfernen. DITAVal-Dateien werden in der angegebenen Reihenfolge ausgewertet, sodass die in der ersten Datei angegebenen Bedingungen Vorrang vor den in späteren Dateien angegebenen Bedingungen haben. Sie können die Dateireihenfolge beibehalten, indem Sie Dateien hinzufügen oder löschen. Wenn die DITAVal-Datei an einen anderen Speicherort verschoben oder gelöscht wird, wird sie nicht automatisch aus dem Mapping-Dashboard gelöscht. Sie müssen den Speicherort aktualisieren, falls Dateien verschoben oder gelöscht werden. Sie können den Mauszeiger über den Dateinamen bewegen, um den Pfad im AEM Repository anzuzeigen, in dem die Datei gespeichert ist. Sie können nur DITAVal-Dateien auswählen. Wenn Sie einen anderen Dateityp ausgewählt haben, wird ein Fehler angezeigt. FrameMaker Publishing Server unterstützt nicht mehrere DITAVAL-Dateien.<br>* **Bedingungsvoreinstellung**: Wählen Sie eine Bedingungsvorgabe aus der Dropdown-Liste aus, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Die Option ist sichtbar, wenn Sie eine Bedingung auf der Registerkarte Bedingungsvorgaben der DITA-Zuordnungskonsole hinzugefügt haben. Weitere Informationen zur Bedingungsvorgabe finden Sie unter [Verwenden von Bedingungsvorgaben](generate-output-use-condition-presets.md#id1825FL004PN). |
| Generieren von PDF mithilfe von | Wählen Sie DITA-OT aus, um die PDF zu generieren. |
| Workflow &quot;Nach der Erstellung ausführen&quot; | Wenn Sie diese Option wählen, wird eine neue Dropdownliste mit dem Workflow nach der Generierung angezeigt, die alle in AEM konfigurierten Workflows enthält. Sie müssen einen Workflow auswählen, der nach Abschluss des Workflows zur Generierung der Ausgabe ausgeführt werden soll.<br><br>**Hinweis**: Weitere Informationen zum Erstellen eines benutzerdefinierten Workflows für die Generierung nach der Ausgabe finden Sie unter Workflow für die Generierung nach der Ausgabe anpassen im Abschnitt as a Cloud Service Adobe Experience Manager-Handbücher installieren und konfigurieren . |
| Name der Umwandlung | Geben Sie den Typ der Ausgabe an, die Sie generieren möchten. Dies ist erforderlich, wenn Sie die Ausgabe mithilfe Ihres eigenen benutzerdefinierten Plug-ins generieren möchten, das in das DITA-OT-Plug-in integriert ist. Wenn Sie beispielsweise eine XHTML-Ausgabe generieren möchten, geben Sie `xhtml`. Eine Liste der in DITA-OT verfügbaren Umwandlungen finden Sie unter [DITA-OT-Transformationen (Ausgabeformate)](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) im OASIS DITA-OT-Benutzerhandbuch. |
| Dateiname | Geben Sie den Dateinamen an, mit dem Sie die PDF speichern möchten.<br><br>Sie können auch Variablen beim Festlegen des PDF-Dateinamens verwenden. Weitere Informationen zur Verwendung von Variablen finden Sie unter [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](generate-output-use-variables.md#id18BUG70K05Z).<br><br>**Hinweis**: Wenn Sie keinen Dateinamen angeben, wird der Titel der DITA-Zuordnung verwendet, um den endgültigen PDF-Dateinamen zu generieren. Wenn die Zuordnung keinen Titel hat, wird der Dateiname der DITA-Zuordnung verwendet, um die endgültige PDF zu benennen. Der Dateiname wird mithilfe der im System konfigurierten Regeln bereinigt, um ungültige Zeichen zu verarbeiten. |
| Zielpfad | Der Pfad in Ihrem AEM-Repository, in dem die PDF gespeichert ist.<br><br>Sie können auch Variablen beim Festlegen des Zielpfads verwenden. Weitere Informationen zur Verwendung von Variablen finden Sie unter [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](generate-output-use-variables.md#id18BUG70K05Z). |
| Temporäre DITA-OT-Dateien bereinigen | Wählen Sie diese Option, um die von DITA-OT generierten temporären Dateien zu bereinigen. Der Speicherort, an dem DITA-OT temporäre Dateien speichert, finden Sie im Ausgabegenerierungsprotokoll.<br><br>Wenn beim Generieren der Ausgabe über DITA-OT Fehler auftreten, können Sie diese Option deaktivieren, um die temporären Dateien beizubehalten. Anschließend können Sie diese Dateien zur Fehlerbehebung bei Fehlern bei der Ausgabe-Generierung verwenden. |
| Grundlinie verwenden | Wenn Sie eine Grundlinie für die ausgewählte DITA-Zuordnung erstellt haben, wählen Sie diese Option, um die Version anzugeben, die Sie veröffentlichen möchten.<br><br>Siehe [Arbeiten mit Grundlinien](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) für weitere Details. |
| Eigenschaften | Wählen Sie die Eigenschaften aus, die Sie als Metadaten verarbeiten möchten. Diese Eigenschaften werden auf der Seite &quot;Eigenschaften&quot;der DITA-Map- oder Bookmap-Datei festgelegt. Die Eigenschaften, die Sie aus der Dropdownliste auswählen, sind unter der **Eigenschaften** und werden aus der Dropdown-Liste entfernt. Nach dem Festlegen werden diese Eigenschaften auch in die Themen in der Zuordnung kopiert.<br><br>Hinweis: Sie können die Metadaten auch mithilfe der DITA-OT-Veröffentlichung an die Ausgabe übergeben. Weitere Informationen finden Sie unter [Übergeben der Metadaten an die Ausgabe mithilfe von DITA-OT](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Übergeordnetes Thema:**[ Grundlegendes zu den Ausgabevorgaben](generate-output-understand-presets.md)
