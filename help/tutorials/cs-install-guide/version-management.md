---
title: Versionsverwaltung
description: Erfahren Sie, wie Sie Versionen verwalten
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1502'
ht-degree: 0%

---

# Versionsverwaltung {#id181GB000XY4}

Die Versionierung ist ein wichtiger Aspekt jedes Content Management-Systems. Damit können Sie zu einem bestimmten Zeitpunkt eine Momentaufnahme Ihres digitalen Assets erstellen. Wenn eine Version eines digitalen Assets vorhanden ist, können Sie die erforderliche Version des Assets wiederherstellen und aktualisieren. In der Regel würden Sie zum Erstellen einer Version eines Assets das erforderliche Asset auschecken und einchecken.

Als Administrator können Sie Regeln durchsetzen, die Benutzer daran hindern, eine Datei zu bearbeiten, ohne sie auszuchecken. Ebenso können Sie sicherstellen, dass alle ausgecheckten Dateien wieder eingecheckt werden, um Datenverlust zu vermeiden.

In einer Umgebung mit mehreren Anwendungen ist es auch wichtig sicherzustellen, dass Benutzer keine Dateien aus dem System löschen. Diese Anforderung ist für Dateien, die von anderen Benutzern ausgecheckt werden, wichtiger. Um zu verhindern, dass Benutzer versehentlich ausgecheckte Dateien aus dem System löschen, bietet AEM Guides eine Konfiguration, die Sie verwenden können. Zusätzlich zu ausgecheckten Dateien können Sie auch das Löschen von Dateien steuern, die Verweise enthalten oder aus anderen Dateien referenziert werden.

## Neue Version für hochgeladene Datei erstellen

>[!NOTE]
>
> Diese Konfiguration gilt nur beim Hochladen von Dateien.

So aktivieren Sie die **Neue Version für hochgeladene Datei erstellen** -Option, führen Sie die folgenden Schritte aus:

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die **Neue Version für hochgeladene Datei erstellen** Option:


   | PID | Eigenschaftenschlüssel | Eigenschaftswert |
   |---|------------|--------------|
   | `com.adobe.fmdita.confi g.ConfigManager` | `create.ver.new.content` | Boolesch \(true/false\).<br> **Standardwert**: `true` |

>[!NOTE]
>
> Wenn die Option ausgewählt ist, wird ein neuer Versionsverwaltungsmechanismus eingesetzt, der das standardmäßige Upload-Verhalten außer Kraft setzt, das bei jedem nachfolgenden Upload gilt. Dadurch wird der Inhalt der hochgeladenen Datei als neue Version gespeichert. Wenn die Option deaktiviert ist, verwendet AEM Guides den standardmäßigen Versionsverwaltungsmechanismus AEM.

## Einstellungen konfigurieren, um die Bearbeitung ausgecheckter Dateien zu ermöglichen

Mit dem Web Editor für AEM Guides können Sie DITA-Themen erstellen und aktualisieren. Sie können den Web Editor so konfigurieren, dass nur die Dokumente bearbeitet werden können, die aus dem Repository ausgecheckt wurden. Dadurch wird sichergestellt, dass kein anderer Autor versehentlich ein Thema überschreibt, das von einem anderen Autor zur Bearbeitung geöffnet wird. Sobald ein Thema zur Bearbeitung geöffnet ist, kann ein Autor die Datei zum Zeitpunkt des Schließens der Datei einchecken.

Eine weitere wichtige Regel besteht darin sicherzustellen, dass ausgecheckte Dateien wieder in das System eingecheckt werden. Dadurch wird verhindert, dass Benutzer die Dateien versehentlich schließen, ohne sie erneut einzuchecken.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die Bearbeitung ausgecheckter Dateien zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.autocheckout` | Boolesch \(true/false\).<br> **Standardwert**: `false` |

Darüber hinaus können Sie konfigurieren, dass eine Warnmeldung angezeigt wird, wenn eine ausgecheckte Datei geschlossen wird, ohne sie zu speichern oder erneut im Repository zu überprüfen.

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.checkin` | Boolesch \(true/false\).<br> **Standardwert**: `false` |

>[!NOTE]
>
> Unabhängig davon, ob Sie diese Funktion aktivieren oder deaktivieren, sind die Optionen &quot;Auschecken&quot;und &quot;Einchecken&quot;immer in einer Themenvorschau verfügbar.

## Ausgecheckte Datei beim Hochladen überschreiben

>[!NOTE]
>
> *Diese Konfiguration ist nur anwendbar, wenn Sie Dateien über die Assets-Benutzeroberfläche erstellen und nicht, wenn Sie Dateien mit dem WebDAV-Tool hochladen.*

So können Benutzer die Datei beim Hochladen überschreiben, die von ihnen oder einem anderen Benutzer ausgecheckt wurde:

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die **Auscheckte Datei beim Hochladen überschreiben** Option:


| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.confi g.ConfigManager` | `overwrite.checkout.onupload` | Boolesch \(true/false\).<br> **Standardwert**: `false` |

>[!NOTE]
>
> Standardmäßig ist diese Option deaktiviert. Wenn diese Option aktiviert ist, können Benutzer ausgecheckte Dateien überschreiben. Wenn die Option nicht ausgewählt ist, kann die Datei nicht überschrieben werden, wenn sie von ihnen oder einem anderen Benutzer ausgecheckt wurde.

## Löschen ausgecheckter Dateien verhindern

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um zu verhindern, dass Benutzer versehentlich ausgecheckte Dateien löschen:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.preventcheckedoutcontentdeletion` | Boolesch \(true/false\). <br> **Standardwert**: `true` |

## Löschen referenzierter Dateien verhindern

Als Administrator können Sie steuern, wer Dateien aus dem AEM-Repository löschen kann. Wenn eine Datei Verweise enthält oder von einer anderen Datei referenziert wird, können Sie definieren, wer diese Dateien löschen kann.

Mit dieser Konfiguration können Sie das Löschen von Dateien durch alle Benutzer zulassen oder verweigern oder zulassen, dass nur eine bestimmte Benutzergruppe Dateien löscht. Wenn das Löschen von Dateien zulässig ist, wird der folgende Prozess ausgeführt:

- Wenn Sie einen Ordner löschen, der alle referenzierten und referenzierenden Dateien enthält, werden alle Dateien gelöscht. Der Prozess löscht zunächst alle Dateien, die keine Verweise enthalten, gefolgt von Dateien, die Verweise enthalten oder darauf verwiesen wird.

- Wenn Sie einen Ordner löschen und eine beliebige Datei im Ordner von einer Datei außerhalb dieses Ordners referenziert wird, werden Sie aufgefordert, den Verweis zu entfernen, bevor Sie die Datei löschen.


Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um festzulegen, wer eine Datei löschen kann, die Verweise enthält oder von anderen Dateien referenziert wird:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `block.unsafe.delete` | Mögliche Werte sind: <br> - allow\_unsafe\_delete\_for\_all <br> - allow\_unsafe\_delete\_for\_delete\_assets\_group <br> - block\_unsafe\_delete\_for\_all <br> **Standardwert**: `allow_unsafe_delete_for_delete_assets_group` <br> Die Details zu diesen Konstanten sind unten aufgeführt. |

Je nachdem, wem Sie Zugriff auf das Löschen gewähren möchten, geben Sie eine der folgenden Konstanten an:

- allow\_unsafe\_delete\_for\_all: Erteilen Sie allen Benutzern die Berechtigung zum Löschen von Dateien. Wenn in diesem Fall die Datei\(en\) Verweise enthält oder von anderen Dateien referenziert wird, können Sie diese Dateien auch erzwungen löschen\(en\). Vor dem Löschen der Datei wird Ihnen eine Eingabeaufforderung mit den Verweisen angezeigt. Sie können den Löschvorgang abbrechen, die Verweise entfernen und schließlich die Datei löschen\(en\). Alternativ können Sie die Datei\(en\) erzwungen löschen, ohne die Verweise zu entfernen.

  ![](assets/allow_unsafe_delete-force-delete.PNG)

- allow\_unsafe\_delete\_for\_delete\_assets\_group: Ein Administrator oder ein Benutzer, der zum *delete-assets* -Gruppe Dateien löschen kann. Wenn ein anderer Benutzer versucht, Dateien mit Verweisen zu löschen, kann er diese Dateien erst löschen, wenn alle Verweise entfernt wurden. Der folgende Screenshot wird angezeigt, wenn ein Benutzer, der keine Berechtigungen hat, versucht, Dateien zu löschen.

  ![](assets/allow_unsafe_delete_for_delete_assets_group.PNG)

- block\_unsafe\_delete\_for\_all: Deaktivieren Sie alle Benutzer \(einschließlich Administratoren\) vom Löschen von Dateien, bis die Verweise auf und aus der Datei\(en\) entfernt werden.


## Löschen älterer Versionen von DITA-Dateien

Wenn Sie Inhalte aktualisieren und neue Versionen erstellen, werden die vorherigen Versionen der DITA-Dateien im Repository verwaltet. Viele Versionen werden möglicherweise über einen bestimmten Zeitraum für Ihre DITA-Dateien erstellt und können gemeinsam eine große Menge an Speicherplatz in Ihrem Repository beanspruchen. Mit AEM Guides können Sie die älteren Versionen konfigurieren, die aus dem Repository gelöscht werden sollen.

Wenn Sie über Administratorrechte verfügen, können Sie über die angegebene URL auf dieses Dienstprogramm zugreifen:

`<server folder path> /libs/fmdita/clientlibs/xmleditor_version_purge/page.html`

Die Version einer DITA-Datei, die eines der angegebenen Kriterien erfüllt, wird beibehalten und nicht bereinigt:

- Ist die erste Version einer Datei
- Ist in eine Grundlinie eingeschlossen
- Ist in einem Übersetzungs- oder Überprüfungs-Workflow enthalten
- Hat eine Beschriftung darauf angewendet
- Erfüllt das definierte Alter oder die Anzahl der Versionskriterien

Führen Sie die folgenden Schritte aus, um die älteren Versionen zu bereinigen:

1. Geben Sie die folgenden Details zu den Dateien ein, die Sie bereinigen möchten:

   ![](assets/preview-purge-report.png)

1. 
   - **Anzahl der Versionen, die von der neuesten Version beibehalten werden sollen**: Geben Sie die Anzahl der Versionen an, die beibehalten und nicht bereinigt werden sollen. Wenn wir beispielsweise 5 eingeben, werden die letzten fünf Versionen beibehalten und die Versionen vor diesen werden für die Bereinigung qualifiziert, falls andere Bereinigungsbedingungen erfüllt sind.
- **Erstellte Versionen innerhalb des Zeitbereichs beibehalten \(in Tagen\)**: Geben Sie das Höchstalter einer Version in Tagen an. Die Versionen, die älter als die angegebene Anzahl von Tagen sind, sind für die Bereinigung qualifiziert, falls andere Bereinigungsbedingungen erfüllt sind. Wenn Sie beispielsweise 100 eingeben, werden alle Versionen, die vor 100 Tagen erstellt wurden, für die Bereinigung qualifiziert, falls andere Bereinigungsbedingungen erfüllt sind.
- **Pfad**: Wählen Sie den Pfad der Datei oder des Ordners aus, deren Dateien Sie bereinigen möchten.

  >[!NOTE]
  >
  > Sie können nur DITA-Dateien bereinigen.

1. Klicks **Bericht zur Bereinigung der Vorschau**.

   >[!NOTE]
   >
   > Es kann jeweils nur eine Bereinigungsaufgabe geben. Sie können keinen anderen Versionsbereinigungsvorgang starten, wenn einer gerade ausgeführt wird.

   Der Versionsbereinigungsbericht wird generiert.

1. Laden Sie den Versionsbereinigungsbericht herunter und überprüfen Sie die Dateien und Versionen, die bereinigt werden sollen.
1. Sie können zwischen **Bereinigung abbrechen** oder **Bereinigung starten**.

   ![](assets/download-purge-report.png)

   Der Bereinigungsstatus wird angezeigt.

   Klicks **Bericht zur Versionsbereinigung herunterladen** , um die bereinigten Versionen anzuzeigen. Dieser Bericht liefert den Bereinigungsstatus für alle Versionen zusammen mit den Gründen, warum eine bestimmte Version beibehalten wurde oder warum sie bereinigt wurde.


>[!NOTE]
>
> Der Bericht wird am folgenden Speicherort heruntergeladen: `/var/dxml/versionpurge`
