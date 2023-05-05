---
title: Verwalten von Veröffentlichungsaufgaben mit dem Veröffentlichungs-Dashboard
description: Erfahren Sie, wie Sie Veröffentlichungsaufgaben mit dem Veröffentlichungs-Dashboard verwalten
exl-id: 5ede608d-f905-44b7-9147-ab678ad68ee7
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Verwalten von Veröffentlichungsaufgaben mit dem Veröffentlichungs-Dashboard {#id205CC08305Z}

Wenn Sie eine große Anzahl von Veröffentlichungsaufgaben auf Ihrem System ausführen, ist es praktisch unmöglich, jede DITA-Karte einzeln zu überprüfen, um ihre Veröffentlichungsaufgabe zu überwachen. AEM Guides bieten Administratoren und Herausgebern eine einheitliche Ansicht aller Veröffentlichungsaufgaben, die im System ausgeführt werden. Eine Liste aller aktiven Veröffentlichungsaufgaben ist im Dashboard veröffentlichen verfügbar.

Das Dashboard &quot;Veröffentlichen&quot;bietet einen vollständigen Überblick über alle Veröffentlichungsaufgaben, die derzeit im System ausgeführt werden.

![](images/publish-dashboard.png){width="800" align="left"}

Das Dashboard &quot;Veröffentlichen&quot;enthält die folgenden Details:

- **Map Title** - Der Titel einer Map-Datei, die derzeit veröffentlicht wird oder sich in der Veröffentlichungswarteschlange befindet.

- **Dateiname** - Der Dateiname der DITA-Zuordnung.

- **Ausgabevorgabe** - Name der Ausgabevorgabe, die zum Generieren der Ausgabe verwendet wird.

- **Initiiert von** - Benutzername des Benutzers, der die Veröffentlichungsaufgabe initiiert hat.

- **Started On** - Datum und Uhrzeit des Beginns der Veröffentlichungsaufgabe.

- **Verstrichene Zeit** - Zeit seit der Ausführung der Veröffentlichungsaufgabe im System.

- **Löschsymbol** - Abbrechen oder Beenden einer Veröffentlichungsaufgabe.

Das linke Bedienfeld im Dashboard &quot;Veröffentlichen&quot;bietet die folgenden Filteroptionen:

- **Ausgabevorgabe** - Wählen Sie eine oder mehrere Ausgabevorgaben aus, für die Sie die derzeit aktiven Veröffentlichungsaufgaben anzeigen möchten. Im folgenden Screenshot werden die Veröffentlichungsaufgaben gefiltert, um nur die Aufgaben anzuzeigen, die die AEM Site-Ausgabevorgabe verwenden:

   ![](images/publish-dashboard-preset-filter.png){width="800" align="left"}

- **Initiiert von** - Wählen Sie einen Benutzernamen aus der Liste aus, um die vom ausgewählten Benutzer initiierten Veröffentlichungsaufgaben anzuzeigen.

- **Zuordnung** - Wählen Sie eine Zuordnungsdatei aus der Liste aus, um die Veröffentlichungsaufgaben anzuzeigen, die für die ausgewählte Zuordnung ausgeführt werden.

## Zugriff auf das Veröffentlichungs-Dashboard {#id205CC100DY4}

Führen Sie die folgenden Schritte aus, um auf das Veröffentlichungs-Dashboard zuzugreifen:

>[!NOTE]
>
> Nur ein Administrator oder Herausgeber kann auf das Dashboard &quot;Veröffentlichen&quot;zugreifen.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools.

1. Klicken Sie auf **Dashboard veröffentlichen** Kachel.

   Das Dashboard &quot;Veröffentlichen&quot;wird mit einer Liste aller aktiven Veröffentlichungsaufgaben im System geöffnet.

   Wenn Sie auf den Link Dateiname klicken, wird die DITA-Zuordnungskonsole der ausgewählten Zuordnung angezeigt.

   ![](images/publish-dashboard-click-filename-link.png){width="800" align="left"}


>[!NOTE]
>
> Sie können auch über die Registerkarte &quot;Ausgaben&quot;auf das Dashboard &quot;Veröffentlichen&quot;zugreifen, während Sie die Ausgabe über das Mapping-Dashboard generieren. Weitere Informationen finden Sie unter [Status der Ausgabegenerierungsaufgabe anzeigen](generate-output-for-a-dita-map.md#viewing_output_history).

## Abbrechen einer Veröffentlichungsaufgabe

Führen Sie die folgenden Schritte aus, um eine Ausgabegenerierungsaufgabe im Veröffentlichungs-Dashboard abzubrechen:

1. [Zugriff auf das Veröffentlichungs-Dashboard](#id205CC100DY4).

1. Klicken Sie in der Liste der aktiven Veröffentlichungsaufgaben auf das Löschsymbol einer Aufgabe, die Sie abbrechen möchten.

   ![](images/publish-dashboard-cancel-task.png){width="800" align="left"}

1. Klicken **Ja** auf der Meldung Abbruch bestätigen angezeigt.

   Der Befehl &quot;Abbrechen&quot;wird akzeptiert und der Abbruch wird versucht, solange die Aufgabe aktiv bleibt. Nachdem die Aufgabe erfolgreich beendet wurde, wird sie aus der Liste der derzeit aktiven Aufgaben entfernt. Der Status der Aufgabe wird auch in der DITA-Zuordnungskonsole als Abgebrochen aktualisiert. Im folgenden Screenshot wird die *HTML5* Aufgabe wird über das Dashboard &quot;Veröffentlichen&quot;abgebrochen und ihr Status wird auch in der DITA-Zuordnungskonsole geändert.

   ![](images/cancelled-output-task.png){width="800" align="left"}


**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)
