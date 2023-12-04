---
title: Bericht zur Inhaltswiederverwendung
description: Erfahren Sie, wie Sie den Bericht zur Wiederverwendung von Inhalten in AEM Handbüchern anzeigen. Erstellen Sie den Bericht, um den Prozentsatz der Wiederverwendung des Inhalts zu ermitteln.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Bericht zur Inhaltswiederverwendung {#id205BB900OQD}

Ein weiterer nützlicher Bericht, den Sie generieren können, ist der Bericht zur Wiederverwendung von Inhalten. Dieser Bericht berechnet den durchschnittlichen Prozentsatz der Inhaltsnutzung, der für Projektmanager und Geschäftsinhaber sehr nützlich ist, um die Menge der wiederverwendeten Inhalte anzuzeigen.

>[!TIP]
>
> Um eine ordnungsgemäße Funktionsweise des Berichts zur Inhaltswiederverwendung sicherzustellen, müssen Sie den Nachbearbeitungs-Workflow aktivieren. Wenden Sie sich an Ihren Systemadministrator, um Nachbearbeitungs-Workflows zu aktivieren.

Führen Sie die folgenden Schritte aus, um den Bericht zur Wiederverwendung von Inhalten anzuzeigen:

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools.

1. Klicken Sie auf **Bericht zur Inhaltswiederverwendung** Kachel.

1. Klicks **Durchsuchen** um einen Pfad auszuwählen, in dem sich Ihre Themen befinden, oder den Pfad manuell eingeben.

   Der Bericht wird durch das Prüfen des Inhalts im übergeordneten Ordner und in allen untergeordneten Ordnern generiert.

1. Klicks **Bericht erstellen** , um den Bericht zur Inhaltswiederverwendung zu erhalten.

   ![](images/content-reuse-uuid.png){width="800" align="left"}

   Die Berichtsseite ist in zwei Teile unterteilt:

   - **Berichtszusammenfassung:**

     Listet die durchschnittliche Wiederverwendung von Inhalten auf, die als Wiederverwendungsinstanzen für Inhalte/Gesamtzahl der Themenanzahl berechnet wird. Dieser Bericht berücksichtigt bei der Berechnung alle direkten Inhaltsreferenzen und Themenreferenzen der ersten Ebene. Die Inhaltswiederverwendungsinstanzen werden als Summe der Werte im Feld Anzahl der wiederverwendeten Male berechnet. Das Thema, das am häufigsten wiederverwendet wird, ist auch in der Berichtszusammenfassung aufgeführt. Durch Klicken auf den Link des Themas im am häufigsten wiederverwendeten Thema wird die Vorschau des Themas geöffnet.

   - **Details:**

     Der Bereich Details enthält die folgenden Spalten:

      - **Titel**: Der Titel des Themas. Durch Klicken auf den Titel-Link des Themas wird die Themenvorschau geöffnet.

      - **UUID**: Die universelle eindeutige Kennung \(UUID\) der Datei.

      - **Größe**: Dateigröße in Byte.

      - **Status**: Der aktuelle Status des Dokuments - Entwurf, In-Review oder überprüft.

      - **Anzahl der wiederverwendeten Male**: Gibt an, wie oft das entsprechende Thema wiederverwendet wurde. Dies wird berechnet als Summe der Einträge in den Spalten &quot;Referenziert von&quot; minus 1.

      - **Referenziert von**: Die Themen, auf die das entsprechende Thema verwiesen wurde. Hier werden nur die direkten \(ersten\) Verweise berücksichtigt. Mehrere Themen werden durch Kommas getrennt. Die UUID der referenzierten Datei wird auch in Klammern erwähnt. Durch Klicken auf den Titel-Link des Themas wird die Themenvorschau geöffnet.


>[!NOTE]
>
> Sie können den Bericht zur Inhaltswiederverwendung auch im CSV-Format exportieren. Klicken Sie dazu oben links im Bildschirm auf den Link In CSV exportieren und wählen Sie einen Speicherort für die CSV-Datei aus. Sie können diese CSV-Datei dann in einem beliebigen CSV-Editor öffnen.

**Übergeordnetes Thema:**[ Berichte](reports-intro.md)
