---
title: Erstellen und Verwalten von Grundlinien im Web-Editor
description: Erfahren Sie, wie Sie Grundlinien im Web Editor erstellen und verwalten
source-git-commit: 873111892d5b479f80a40c0b18cda9b538f5a1de
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---


# Erstellen und Verwalten von Grundlinien im Web-Editor {#id223MB0ZF043}

>[!TIP]
>
> Es wird empfohlen, diese Grundlinie-Funktion aus dem Web Editor zu verwenden, wenn Sie ein Upgrade auf AEM Guides-Version vom as a Cloud Service März oder höher durchgeführt haben.

AEM Handbücher bietet die Funktion &quot;Grundlinie&quot;im Web Editor, mit der Benutzer Grundlinien erstellen und Themen aus verschiedenen Versionen veröffentlichen oder übersetzen können.

## Erstellen einer Grundlinie

Sie können eine Grundlinie im Web Editor erstellen, indem Sie die folgenden Schritte ausführen:

1. Öffnen Sie im Bereich &quot;Repository&quot;die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte. Die **Grundlinie** zeigt die Grundlinien der DITA-Zuordnung an.

   ![](images/baseline-manage.png)

1. Im **Grundlinie** klicken Sie oben rechts auf das Symbol + . Sie können eine Grundlinie mit einer bestimmten Version der Themen und referenzierten Inhalten erstellen, die an einem bestimmten Datum und zu einer bestimmten Uhrzeit verfügbar sind, oder mit einer für eine Version der Themen definierten Bezeichnung.
1. Geben Sie einen Namen für die Grundlinie in **Baseline Name**.
1. In **Grundlinien-Option** können Sie entweder **Dateiversion verwenden** Option oder **Verwenden von Bezeichnungen** Option:

   **Dateiversion verwenden**: Sie können eine statische Grundlinie mit einer bestimmten Version der Themen und des referenzierten Inhalts erstellen, die zu einem bestimmten Datum und zu einer bestimmten Uhrzeit verfügbar ist, oder mit einer für eine Version der Themen definierten Beschriftung:

   - In **Legen Sie die neueste Version auf Grundlage von fest.** Wählen Sie eine der folgenden Optionen aus:


      1. **Datum** &lt;time stamp=&quot;&quot;>: Wählt die Version des Themas als Datum und Uhrzeit aus.
      1. **Titel**: Wählen Sie diese Option aus, um die Themen entsprechend dem Titel auszuwählen, der auf sie angewendet wird. Wenn für die Themen Beschriftungen angegeben sind, werden die Beschriftungen im Dropdown-Menü aufgeführt. Sie können einen Titel aus der Liste auswählen. Sie können auch eine Beschriftung in das Textfeld einfügen.\
         Wenn Sie **Titel,** Sie können die direkten und indirekten Verweise auswählen.
      - Bei direkten Verweisen innerhalb der DITA-Zuordnung erhalten Sie die Möglichkeit, die neueste Version von Themen zu verwenden, auf die die angegebene Bezeichnung nicht angewendet wurde.

      >[!NOTE]
      >
      > Wenn Sie einen nicht vorhandenen Titel eingeben, wählen Sie die Option **Erstellen Sie keine Grundlinie** dann schlägt die Grundlinien-Erstellung fehl und zeigt eine Fehlermeldung in der Nähe des Grundlinien-Namens im Bedienfeld Grundlinie an.

      - Bei indirekten Verweisen innerhalb der DITA-Zuordnung erhalten Sie eine zusätzliche Option, die neueste Version von Themen zu verwenden, auf die die angegebene Bezeichnung nicht angewendet wurde. Sie können auch **Automatisch auswählen** für den referenzierten Inhalt, und das System wählt automatisch die Version des referenzierten Inhalts aus, die der Version des Inhalts entspricht, in dem er referenziert wird.

   Nachdem Sie eine Bezeichnung oder Version als Datum ausgewählt haben, werden alle referenzierten Themen und Mediendateien in der Zuordnung entsprechend ausgewählt. Diese Themenauswahl wird nicht auf der Benutzeroberfläche angezeigt, sondern im Backend gespeichert.

   **Beschriftungen verwenden**: Wählen Sie diese Option für die Grundlagenerstellung aus, um die Themen entsprechend der auf sie angewendeten Bezeichnung auszuwählen.

   Grundlinien, die auf Bezeichnungen basieren, werden dynamisch aktualisiert. Wenn Sie eine Grundlinie erstellen, eine Grundlinie herunterladen oder ein Übersetzungsprojekt mit einer Grundlinie erstellen, werden die Dateien dynamisch anhand der aktualisierten Beschriftungen ausgewählt. Wenn Sie beispielsweise Version 1.2 eines Themas mit Label Release 1.0 für die Grundlinie und später aktualisierte Version 1.5 mit Label Release 1.0 verwendet haben, wird die Grundlinie dynamisch aktualisiert und Version 1.5 wird verwendet.

   ![](images/dynamic-baseline.png)

   - **Beschriftungen auswählen**: Wenn für die Themen Beschriftungen angegeben sind, werden die Beschriftungen im **Beschriftungen auswählen** Dropdown-Liste. Sie können die Titel\(s\) aus der Liste auswählen. Die zuerst ausgewählten Titel erhalten höhere Priorität als die späteren.
1. **Indirekte Verweise**: Für indirekte Verweise innerhalb der DITA-Zuordnung erhalten Sie die folgenden Optionen:

   - **Automatisch auswählen**: Sie können zwischen **Automatisch auswählen** für den referenzierten Inhalt, und das System wählt automatisch die Version des referenzierten Inhalts aus, die der Version des Inhalts entspricht, in dem er referenziert wird.

   - **Ausgewählte Bezeichnung verwenden**: Sie können eine Grundlinie mit der ausgewählten Bezeichnung erstellen, die für eine Version von Themen definiert ist.
   - **Verwenden Sie die neueste Version oder die Arbeitskopie**: Verwenden Sie die neueste Version der Themen, auf die nicht die angegebene Beschriftung angewendet wurde, oder wenn keine Version erstellt wurde, verwenden Sie die Arbeitskopie der Themen, um die Grundlinie zu erstellen.
1. Klicken Sie auf **Übernehmen**.

Die Grundlinie wird erstellt. Die Grundlinien-Erstellung erfolgt asynchron, sodass Sie im Web Editor weiterhin an anderen Dateien arbeiten können. Nachdem die Grundlinie erstellt wurde, wird eine Popup-Meldung angezeigt, die bestätigt, dass die Grundlinie erstellt wurde, und Sie erhalten auch eine Inbox-Benachrichtigung für dieselbe Grundlinie.

## Grundlinien verwalten

Sie können Ihre vorhandenen Grundlinien mithilfe der verschiedenen Funktionen im Dashboard Grundlinie verwalten.

- Sie können über das Textfeld im Bedienfeld &quot;Grundlinie&quot;nach einer vorhandenen Grundlinie suchen. Verwenden Sie die **Filter anwenden** -Symbol, um alle Grundlinien anzuzeigen oder die Grundlinien mit dem Erstellungsstatus als &quot;Erfolgreich&quot;, &quot;In Bearbeitung&quot;oder &quot;Fehlgeschlagen&quot;aufzulisten.
- Verwenden Sie die **Aktualisieren** im Bedienfeld &quot;Grundlinie&quot;ein, um alle Grundlinien erneut zu überprüfen und eine neue Liste der Grundlinien für die DITA-Karte anzuzeigen, die in der Kartenansicht geöffnet ist.
- Sie können den Inhalt einer vorhandenen Grundlinie anzeigen oder bearbeiten, indem Sie im Bedienfeld Grundlinie auf die Grundlinie doppelklicken. Das Grundlinien-Bearbeitungsfenster in der Mitte zeigt die DITA-Map-Datei, den Inhalt oder die Themen der Zuordnung und den referenzierten Inhalt an.


![](images/baseline-options.png)

Sie können auch die folgenden Vorgänge auf der Grundlinie im Menü Optionen ausführen:

- **Bearbeiten**, **Duplizieren,** oder **Löschen** eine bestehende Grundlinie.
- Hinzufügen, Entfernen oder Ändern vorhandener Bezeichnungen aus dem **Verwalten von Bezeichnungen** -Option. Wenn Ihr Administrator vordefinierte Beschriftungen konfiguriert hat, werden diese Beschriftungen in der Dropdownliste Titel hinzufügen angezeigt. Weitere Informationen zum Hinzufügen von Bezeichnungen finden Sie unter [Verwenden von Bezeichnungen](web-editor-use-label.md#).

   >[!NOTE]
   >
   > Der Prozess zum Hinzufügen oder Entfernen von Bezeichnungen erfolgt asynchron, sodass Sie im Web Editor weiterhin an anderen Dateien arbeiten können. Nachdem der Titel hinzugefügt oder entfernt wurde, wird eine Popup-Meldung angezeigt, in der bestätigt wird, dass der Titel hinzugefügt oder entfernt wurde, und Sie erhalten auch eine Inbox-Benachrichtigung.

- **Eigenschaften bearbeiten** einer vorhandenen Grundlinie, die Sie beim Erstellen der Grundlinie festgelegt haben.
- Exportieren Sie die Momentaufnahme einer Grundlinie in eine CSV-Datei mit dem **Exportgrundlinie** -Option.

**Standardfilter**

Verwenden des Symbols Filter im **Standardfilter** -Bedienfeld können Sie Filter auf die Grundlinie anwenden, die im Fenster der Grundlinienbearbeitung geöffnet wurde:

![](images/baseline-filter.png)

- Filtern Sie die Dateien nach Dateinamen oder Dateispeicherort.
- Filtern Sie die Dateien anhand der Werte für verschiedene Spalten wie Dateityp, Referenztyp usw.
- Wählen Sie die Spalten aus, die im Bearbeitungsfenster für die Grundlinie angezeigt werden sollen.

>[!NOTE]
>
> Sie können auf eine Spaltenüberschrift klicken und die Dateien nach den Spalten im Bearbeitungsfenster für die Grundlinie sortieren.

**Speichern oder Zurücksetzen einer Grundlinie**

Nachdem Sie die Grundlinie bearbeitet haben, können Sie auf die **Speichern** oben auf die Schaltfläche klicken, um die Änderungen an der Grundlinie zu speichern. Sie können auf die **Zurücksetzen** , wenn Sie die Änderung nicht speichern und die Grundlinie zurücksetzen möchten. Wenn Sie auf die **Zurücksetzen** -Schaltfläche ein Warnhinweis angezeigt, dass nicht gespeicherte Änderungen verloren gehen.

**Übergeordnetes Thema:**[ Arbeiten mit dem Web-Editor](web-editor.md)

