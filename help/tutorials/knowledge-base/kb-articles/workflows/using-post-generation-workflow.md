---
title: Arbeitsablauf nach der Erstellung
description: Eine Übersicht über den Nachbearbeitungs-Workflow mit einem Beispiel
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 2%

---

# Veröffentlichung von AEM-Handbüchern - Workflow nach der Erstellung

AEM Handbücher bieten Ihnen die Flexibilität, einen Workflow zur Erstellung nach der Ausgabe festzulegen. Sie können einige Nachbearbeitungsaufgaben für die Ausgabe ausführen, die mithilfe von AEM-Handbüchern generiert wird.
Sie können beispielsweise bestimmte Eigenschaften für die PDF-Ausgabe festlegen oder eine E-Mail an eine Benutzergruppe senden, sobald die Ausgabe generiert wurde.


## Welche Schritte sind erforderlich, um Workflows nach der Generierung zu nutzen?

### Workflow-Prozess erstellen

Erstellen Sie einen Java- oder ECMA-basierten Workflow-Prozess, der den Vorgang für die generierte Ausgabe ausführt. Beispiel: Kopieren einiger Metadaten aus der Quelle in den generierten Inhalt oder Bearbeiten von Metadaten der generierten Ausgabe.
- Wir werden ein Beispiel für die Erstellung eines solchen Prozesses mit ECMA-Skript verwenden (siehe angehängtes Paket).
- Informationen zum Java-basierten Workflow-Prozess finden Sie im Abschnitt &quot;*Arbeitsablauf für die Generierung nach der Ausgabe anpassen*&quot; [Handbuch zur Installation und Konfiguration](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/install-guide/on-prem-ig/custom-workflow/customize-workflows.html?lang=en#id17A6GI004Y4)


### Erstellen Sie ein Workflow-Modell

Erstellen Sie mit dem benutzerdefinierten Workflow-Prozess, den Sie im vorherigen Schritt erstellt haben, ein Workflow-Modell und fügen Sie diesen Prozessschritt hinzu.
- Sie müssen auch einen obligatorischen Prozessschritt hinzufügen &quot;*Post-Generierung abschließen*&quot; als letzten Schritt des Workflows.

Siehe Beispiel-Workflow-Modell unten:

![Workflow-Modell nach der Generierung](../assets/workflows/pgwf-workflow-model.png)


### Verwenden Sie diesen Nachbearbeitungs-Workflow auf einer Karte

Der Arbeitsablauf nach der Generierung ist eine Eigenschaft, die für jede Ausgabevorgabe im Veröffentlichungsmechanismus AEM Guides konfiguriert werden kann. Beispiel:

![Arbeitsablauf nach der Generierung in der Ausgabevorgabe](../assets/workflows/pgwf-preset-settings.png)


Vorausgesetzt, das ausgewählte Modell wurde bereits erstellt.


### Testen

Jetzt können Sie die Veröffentlichung mit dieser Vorgabe ausführen und die Ausgabe des Prozessschritts überprüfen


## Beispiel

Als Referenz können Sie das folgende Paket verwenden und es über den Paketmanager installieren, um den Beispielnachbearbeitungs-Workflow zu testen (*wie oben in den Screenshots angegeben*)

[Beispiel für ein ECMA-basiertes Workflow-Modell nach der Generierung](../assets/workflows/sample-pgwf-ecma-test-wfmetadata.zip)
