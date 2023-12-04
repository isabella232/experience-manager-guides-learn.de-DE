---
title: Verwalten von Prüfungsaufgaben mithilfe des Überprüfungs-Dashboards
description: Verwalten Sie Prüfungsaufgaben über das Dashboard "Überprüfen"in AEM Handbüchern. Erfahren Sie mehr über die durchgeführten Aktionen auf der Registerkarte "Aufgabe", "Inhalt", "Überprüfer"und überprüfen Sie den Status einer Prüfungsaufgabe.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 0%

---

# Verwalten von Prüfungsaufgaben mithilfe des Überprüfungs-Dashboards {#id2056B0Y70X4}

Der Workflow zur Verwaltung von Überprüfungen kann eine Vielzahl von Aufgaben umfassen. Sie können beispielsweise Prüfer für ein bestimmtes Thema hinzufügen oder die Frist für eine Überprüfung verlängern. Sie können die Prüfungsaufgabe auch als abgeschlossen kennzeichnen, wenn Sie der Meinung sind, dass alle Beteiligten ihre Meinung dazu geäußert haben. Diese Aufgaben können über das Dashboard &quot;Überprüfen&quot;verwaltet werden.

Führen Sie die folgenden Schritte aus, um auf das Überprüfungs-Dashboard zuzugreifen und es zu verwenden:

>[!NOTE]
>
> Sie können Prüfungsaufgaben nur für die Projekte verwalten, für die Sie der Autor sind \(oder Initiator\). Selbst wenn Sie Überprüfer oder Herausgeber sind \(Benutzer\), haben Sie keinen Zugriff auf eine der Projektaufgaben.

1. Im **Projekte** klicken Sie auf das Überprüfungsprojekt, das Sie verwalten möchten.

   Ein Projektbereich mit Aufgabenkacheln wird angezeigt.

   ![](images/review-management.png){width="800" align="left"}

1. Klicken Sie auf die drei Punkte im **Überprüfungen** Kachel.

   Das Überprüfungs-Dashboard wird angezeigt. Im Dashboard werden alle von Ihnen erstellten Prüfungsaufgaben aufgelistet.

   ![](images/review-dashboard.png){width="800" align="left"}

   Im Dashboard &quot;Überprüfen&quot;werden die Details zur Prüfungsaufgabe angezeigt, z. B. der Aufgabenname, der Benutzer, der die Überprüfung gestartet hat, das Datum, an dem die Überprüfung gestartet wurde, das Fälligkeitsdatum, der Status, die Anzahl neuer Kommentare, die vom Autor nicht akzeptiert oder abgelehnt wurden, und der Name der Überprüfer. Die Aufgaben werden in der Reihenfolge der neu erstellten Aufgaben zu älteren Aufgaben aufgelistet.

   >[!NOTE]
   >
   > Wenn Sie auf den Link Prüfungsaufgabe klicken, wird das Thema oder die Zuordnungsdatei, die zur Überprüfung gesendet wird, geöffnet.

1. Wählen Sie eine Prüfungsaufgabe aus.

   Ihnen wird die Option Eigenschaften bearbeiten angezeigt und [Status](#check-review-status-id199RF0A0UHS) Optionen in der Symbolleiste.

1. Wenn Sie auf **Eigenschaften bearbeiten**, wird die Seite &quot;Aufgabendetails&quot;angezeigt.

   Auf der Seite &quot;Aufgabendetails&quot;gibt es drei Registerkarten: &quot;Aufgabe&quot;, &quot;Inhalt&quot;und &quot;Prüfer&quot;. In den folgenden Abschnitten werden die verschiedenen Funktionen beschrieben, die auf den einzelnen Registerkarten verfügbar sind.


## Registerkarte &quot;Aufgabe&quot;

![](images/review-task-page.png){width="800" align="left"}

Sie können die folgenden Aktionen im **Aufgabe** tab:

- Ändern Sie den Titel der Aufgabe im **Titel** -Feld.
- Hinzufügen von Standardverantwortlichen im **Zuweisen zu** Dropdown-Liste. Die von Ihnen hinzugefügten validierungsverantwortlichen Benutzer erhalten Zugriff auf die Überprüfung aller Themen, die Teil dieser Prüfungsaufgabe sind. Sie können festlegen, ob weitere Validierer für bestimmte Themen aus dem [Registerkarte &quot;Validierer&quot;](#reviewer-tab-id199RF0N0MUI).
- Aktualisieren Sie die Beschreibung der Aufgabe im **Beschreibung** -Feld.
- Ändern Sie die **Fälligkeitsdatum**. Sie können den Termin für den Abschluss der Aufgabe vorbereiten oder verschieben.
- Wählen Sie die Option aus, um Benutzer auf die Themen zu beschränken, die ihnen zugewiesen sind.
- Klicks **Aktualisieren** , um die geänderten Details zu aktualisieren.
- Klicks **Fertig** , um die Prüfungsaufgabe vor dem Fälligkeitsdatum als abgeschlossen zu markieren. Wenn die Aufgabe eines einzelnen Themas als abgeschlossen markiert ist, wird die Überprüfung des ausgewählten Themas geschlossen. Bei Themen, die über eine DITA-Zuordnung zur Überprüfung freigegeben werden, schließt die Kennzeichnung der DITA-Map-Aufgabe als &quot;Complete&quot;jedoch die Überprüfung aller Themen in der Map, die zur Überprüfung freigegeben wurden.
- Klicks **Duplizieren** , um eine Kopie der Prüfungsaufgabe zu erstellen. Das Erstellen einer doppelten Prüfungsaufgabe verläuft ähnlich wie das Erstellen einer neuen Prüfungsaufgabe. Nachdem Sie den Workflow für die doppelte Aufgabe gestartet haben, wird Ihnen die Seite Prüfungsaufgabe erstellen angezeigt. Sie müssen die neuen Aufgabendetails wie unter [Senden von Themen zur Überprüfung](review-send-topics-for-review.md#).

  Wenn Sie eine Prüfungsaufgabe ausgewählt haben, die aus einer DITA-Zuordnung erstellt wurde, werden Ihnen die Themen angezeigt, die Teil der Zuordnung sind. Anschließend können Sie die Themen auswählen, die Sie in die neue Prüfungsaufgabe aufnehmen möchten.

  Wenn eine Prüfungsaufgabe aus einer oder mehreren Themenüberprüfungen dupliziert wird, werden nur diese Themen in der Liste der Prüfungsaufgaben angezeigt. Sie können diese Themen für eine Überprüfung mit einer anderen Gruppe von Validierern freigeben.

- Klicks **Schließen** , um zur Seite &quot;Posteingang&quot;zu wechseln.

## Registerkarte &quot;Inhalt&quot;

![](images/review-content-page.png){width="800" align="left"}

Sie können die folgenden Aktionen im **Inhalt** tab:

- Ändern Sie die Version des Themas, das zur Überprüfung gesendet wird. Sie können die neueste Version des Themas, Version als Datum, Version mit einer bestimmten Bezeichnung oder Version mit einer bestimmten Grundlinie auswählen \(für eine DITA-Zuordnung\).

- Klicks **Aktualisieren** , um die aktualisierte Version des Themas für die Prüfer freizugeben. Die validierungsverantwortlichen Benutzer erhalten eine E-Mail-Benachrichtigung, dass die neuere Version des Themas zur Überprüfung gesendet wurde. Wenn ein Prüfer das Thema das nächste Mal öffnet, wird ihm die aktualisierte Version des Themas angezeigt.

  >[!NOTE]
  >
  > Bei einer aktualisierten Version eines Themas werden die alten Kommentare auch in der neueren Version beibehalten. Überprüfer können auch die Unterschiede zwischen den beiden Versionen sehen.

- Klicks **Fertig** , um die Prüfungsaufgabe vor dem Fälligkeitsdatum als abgeschlossen zu markieren. Wenn die Aufgabe eines einzelnen Themas als abgeschlossen markiert ist, wird die Überprüfung des ausgewählten Themas geschlossen. Bei Themen, die über eine DITA-Zuordnung zur Überprüfung freigegeben werden, schließt die Kennzeichnung der DITA-Map-Aufgabe als &quot;Complete&quot;jedoch die Überprüfung aller Themen in der Map, die zur Überprüfung freigegeben wurden.

- Klicks **Duplizieren** , um eine neue Prüfungsaufgabe zu erstellen, die die aktuelle Aufgabe als Basis verwendet.


## Registerkarte &quot;Validierer&quot; {#reviewer-tab-id199RF0N0MUI}

![](images/reviewers-tab.png){width="800" align="left"}

Sie können die folgenden Aktionen im **Überprüfer** tab:

- **Alle auswählen**: Auswahl aller Themen in der Themenliste. Nach Auswahl aller Themen können Sie einfach einen Batch-Vorgang ausführen.
- **Auswahl löschen**: Hebt die Auswahl der in der Themenliste ausgewählten Themen auf.

  >[!NOTE]
  >
  > Sie können ein Thema auch einzeln auswählen oder deaktivieren, indem Sie auf das Kontrollkästchen neben dem Thema klicken.

- **Hinzufügen**: Zeigt das Dialogfeld &quot;Überprüfer hinzufügen&quot;an. Sie können den Namen eines Validierers oder einer Benutzerrolle \(oder Gruppe\) eingeben, den Sie als Validierer zu den ausgewählten Themen hinzufügen möchten.
- **Entfernen**: Zeigt das Dialogfeld &quot;Reviewer entfernen&quot;an. Sie können den Namen eines Validierers oder einer Benutzerrolle \(oder Gruppe\) eingeben, den Sie als Validierer aus den ausgewählten Themen entfernen möchten.
- **Neu zuweisen**: Zeigt das Dialogfeld Reviewer erneut zuweisen an. Sie können den Namen eines Validierers oder einer Benutzerrolle eingeben \(oder Gruppe\), dem Sie die Prüfungsaufgabe zuweisen möchten. Dadurch werden alle vorhandenen Prüfer aus den ausgewählten Themen entfernt und die neu ausgewählten Prüfer diesen Themen zugewiesen.
- **Export**: Ermöglicht den Export der Details der Prüfungsaufgabe in eine CSV-Datei. Die Datei enthält Details wie den Pfad und Titel des Themas, den Namen des Prüfers und die Version der Themen, die zur Überprüfung gesendet werden.
- **Validierungsverantwortliche bearbeiten**: Klicken Sie auf das ![](images/edit_pencil_icon.svg)-Symbol in der Themenliste wird das Dialogfeld &quot;Überprüfer bearbeiten&quot;angezeigt. Sie können Überprüfer für das ausgewählte Thema in diesem Dialogfeld hinzufügen oder entfernen.

## Überprüfen des Status einer Prüfungsaufgabe {#check-review-status-id199RF0A0UHS}

Wählen Sie auf der Hauptseite des Prüfungsdashboards eine Prüfungsaufgabe aus und klicken Sie auf **Status**, wird der Statusbericht der Prüfungsaufgabe angezeigt:

![](images/review-status-report.png){width="800" align="left"}

Der Statusbericht für die Prüfungsaufgabe enthält die folgenden Details:

- Name\(n\) des Validierers, dem die Prüfungsaufgabe zugewiesen ist.
- Die Spalte Status gibt den Prüfungsstatus an. Der Status kann einer der folgenden sein:
   - **Nicht gestartet**: Der Validierer hat den Review-Link noch nicht geöffnet.
   - **In Bearbeitung**: Der Validierer hat den Prüfungslink geöffnet und ist dabei, das Thema zu überprüfen.
   - **Fertig**: Der Validierer hat die Überprüfung abgeschlossen, indem er die ihm zugewiesene Überprüfungsaufgabe abgeschlossen hat. Die Überprüfungsaufgabe befindet sich für jeden Überprüfer im Posteingang für AEM Benachrichtigungen.
- Wenn ein Überprüfer einen Überprüfungslink öffnet und zu einem bestimmten Thema navigiert, wird dieses Thema zur Liste &quot;Geprüft&quot;hinzugefügt. Dies hilft Autoren dabei festzustellen, ob die validierungsverantwortlichen Benutzer ihre jeweiligen Abschnitte geöffnet haben oder nicht. Wenn Kommentare abgegeben werden, werden diese in Klammern angezeigt.
- Gesamtzahl der Kommentare zu allen Themen. Bei mehreren Themen, die geprüft werden, wird die Anzahl der Kommentare zu den einzelnen Themen \(in Klammern\) in Bezug auf den Themennamen angegeben.
- Das Datum, an dem der Validierer zuletzt auf ein Thema zugegriffen hat.

**Übergeordnetes Thema:**[ Themen oder Zuordnungen überprüfen](review.md)
