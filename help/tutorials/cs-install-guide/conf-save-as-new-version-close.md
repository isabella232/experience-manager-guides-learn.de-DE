---
title: Eingabeaufforderung zum Speichern als neue Version beim Schließen konfigurieren
description: Erfahren Sie, wie Sie die Eingabeaufforderung zum Speichern als neue Version beim Schließen konfigurieren
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# Eingabeaufforderung zum Speichern als neue Version beim Schließen konfigurieren {#id222HBI00XXA}

Wenn der Benutzer versucht, eine Datei zu schließen, die im Web-Editor mit dem **Schließen** auf der Registerkarte der Datei oder **Schließen** im Menü Optionen wird ein Dialogfeld angezeigt, wenn die Datei nicht gespeicherte Daten oder eine nicht gespeicherte Version aufweist. Der Benutzer wird aufgefordert, die Datei als neue Version zu speichern, wenn die Version nicht gespeichert wird.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um eine Eingabeaufforderung zum Speichern beim Schließen als neue Version zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.savenewversion` | Boolesch \( true/false\). <br>  **Standardwert**: true |

Wenn diese Konfiguration aktiviert ist, wird die **Als neue Version speichern** ist im Dialogfeld standardmäßig aktiviert.

Weitere Informationen finden Sie unter *Szenarien zum Schließen und Speichern von Dateien* im as a Cloud Service Handbuch Verwenden von Adobe Experience Manager-Handbüchern beschrieben.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)

