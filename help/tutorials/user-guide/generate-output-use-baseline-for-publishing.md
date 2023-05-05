---
title: Arbeiten mit Grundlinien
description: Erfahren Sie, wie Sie mit Grundlinie arbeiten
exl-id: dcafab53-c388-48c3-9455-e4251cdda17d
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1917'
ht-degree: 0%

---

# Arbeiten mit Grundlinien {#id1825FI0J0PF}

Mit der Grundlinien-Funktion können Sie eine Version Ihrer Themen und Assets erstellen, die dann für die Veröffentlichung oder Übersetzung verwendet werden kann. Wenn Ihre DITA-Zuordnung beispielsweise `topicA` und `imageA`können Sie eine Grundlinie erstellen, um die dritte Version von `topicA`, aber die 4. Version von `ImageA`. Sobald Sie eine Grundlinie eingerichtet haben, können Sie Themen verschiedener Versionen mit einem einzigen Klick veröffentlichen oder übersetzen.

Die Auswahl einer Grundlinie ist für Ausgabevorgaben optional und eine DITA-Zuordnung kann mehrere Grundlinien aufweisen. Jede Ausgabevorgabe innerhalb einer DITA-Zuordnung kann jedoch nur einer einzelnen Baseline zugeordnet werden. Wenn zum Zeitpunkt der Veröffentlichung keine Grundlinie angegeben ist, wird die Ausgabe mit der neuesten Version des Inhalts veröffentlicht.

Ebenso ist die Auswahl einer Grundlinie zur Übersetzung von Inhalten optional. Wenn Sie sich jedoch dafür entscheiden, Inhalte mithilfe einer Grundlinie zu übersetzen, werden die Inhalte der Grundlinie zusammen mit den übersetzten Kopien gespeichert. Sie können dann die übersetzte Grundlinie verwenden, um weitere Vorgänge auszuführen, z. B. die Freigabe für externe Herausgeber oder die Archivierung. Weitere Informationen zum Exportieren einer übersetzten Grundlinie finden Sie unter [Exportieren der übersetzten Grundlinie](#id196SE600GHS).

>[!TIP]
>
> Siehe *Grundlinie* im Leitfaden zu Best Practices Best Practices für die Arbeit mit Grundlinien beschrieben.

Ihr Administrator kann die Registerkarte &quot;Grundlinie&quot;im Dashboard der Karte konfigurieren. Weitere Informationen finden Sie unter *Konfigurieren der Registerkarte &quot;Grundlinie&quot;im DITA-Map-Dashboard* im Installations- und Konfigurationshandbuch.

Sie können auf die Funktion &quot;Grundlinie&quot;zugreifen, indem Sie die folgenden Schritte ausführen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnungsdatei und klicken Sie darauf.
1. Navigieren Sie zu **Grundlinien** Registerkarte.

Auf der Registerkarte &quot;Grundlinien&quot;können Sie die folgenden Aktionen durchführen:

- [Erstellen einer Grundlinie](#id195FI0I0MUQ)
- [Inhalt einer Grundlinie anzeigen](#id195FI0I0TLN)
- [Grundlinien bearbeiten, duplizieren oder entfernen](#id195FI0I0YJL)
- [Hinzufügen von Bezeichnungen zu einer Grundlinie](#id184KD0T305Z)

## Erstellen einer Grundlinie {#id195FI0I0MUQ}

Sie können eine Baseline mit einer bestimmten Version der Themen und referenzierten Inhalten erstellen, die an einem bestimmten Datum und zu einer bestimmten Uhrzeit verfügbar sind, oder mit einer für eine Version der Themen definierten Bezeichnung. Sie können die Versionen der ausgewählten Themen in einer Grundlinie individuell festlegen, sodass jedes Mal, wenn Sie die Grundlinie im Veröffentlichungs- oder Übersetzungs-Workflow anwenden, die ausgewählten Themen und die zugehörigen Versionen zur Generierung oder Übersetzung der Ausgabe hinzugefügt werden.

Führen Sie die folgenden Schritte aus, um eine Grundlinie zu erstellen:

1. Klicken Sie auf der Seite &quot;Grundlinien&quot;auf **Erstellen**.
1. Geben Sie einen Namen für die Grundlinie in **Baseline Name**.
1. In **Version basierend auf festlegen** wählen Sie eine der folgenden Optionen aus:

   - **Titel**: Wählen Sie diese Option aus, um die Themen entsprechend dem Titel auszuwählen, der auf sie angewendet wird. Geben Sie einen Titel ein, um die Liste nach der eingegebenen Zeichenfolge zu filtern. Aus der gefilterten Liste können Sie eine Bezeichnung auswählen, um Themen und andere Assets mit der angegebenen Bezeichnung auszuwählen.
   Wenn Sie **Titel** erhalten Sie außerdem eine zusätzliche Option, um die neueste Version der Themen zu verwenden, auf die die angegebene Bezeichnung nicht angewendet wurde. Wenn Sie diese Option nicht auswählen und eine Themen- oder Mediendatei nicht mit der angegebenen Beschriftung versehen ist, schlägt der Prozess der Grundlinienerstellung fehl. Weitere Informationen zum Hinzufügen von Bezeichnungen finden Sie unter [Verwenden von Bezeichnungen](web-editor-use-label.md#).

   - **Version auf** &lt;*Zeitstempel*\>: Wählt die Version des Themas als Datum und Uhrzeit aus. Beachten Sie, dass die hier angegebene Uhrzeit der Zeitzone Ihres AEM-Servers entspricht. Wenn sich Ihr Server in einer anderen Zeitzone befindet, werden die Themen gemäß der Zeitzone Ihres Servers und nicht Ihrer lokalen Zeitzone abgerufen.

   Nachdem Sie eine Bezeichnung oder Version als Datum ausgewählt haben, werden alle referenzierten Themen und Mediendateien in der Zuordnung entsprechend ausgewählt. Diese Themenauswahl wird nicht auf der Benutzeroberfläche angezeigt, sondern im Backend gespeichert.

1. Wenn Sie eine andere Version für ein oder mehrere Themen verwenden möchten, können Sie dies tun, indem Sie diese Themen manuell auswählen. Klicken **Thema durchsuchen**, wählen Sie das Thema aus, für das Sie eine andere Version verwenden möchten. Wählen Sie aus der Dropdownliste Version für das ausgewählte Thema auswählen eine Version des Themas aus, das Sie in der Grundlinie verwenden möchten, und klicken Sie auf **OK**.

   ![](images/baseline-select-version-drop-down.png){width="800" align="left"}

   Die Informationen zum Thema und zur ausgewählten Version werden im Backend gespeichert. Sie können diesen Schritt wiederholen, um die ausgewählte Version für mehrere Themen zu ändern.

1. Klicken Sie auf **Alle Themen durchsuchen** Link zum Laden aller Themen und Mediendateien, auf die in der DITA-Zuordnung verwiesen wird. Die UUID der Themen und Mediendateien wird auch unter dem Thementitel oder dem Dateinamen \(media\) angezeigt.

   >[!NOTE]
   >
   > Wenn Ihre DITA-Map sehr große Dateien mit verschachtelten Karten und Themen enthält, kann es etwas dauern, bis alle Dateien geladen werden, wenn Sie auf Alle Themen durchsuchen klicken.

   Der Inhalt Ihrer Karte wird in den drei Abschnitten dargestellt: Zuordnungsdatei, Inhalt \(Themenverweise\) und Referred Content \(verschachtelte Themen, Zuordnungen und andere Assets\). Sobald der gesamte referenzierte Inhalt verfügbar ist, können Sie einzeln die Version des Themas auswählen, das Sie in Ihrer Grundlinie verwenden möchten.

   Die **Version** in der Dropdown-Liste werden die verfügbaren Versionen der Themen oder des referenzierten Inhalts angezeigt. Für den referenzierten Inhalt haben Sie die Möglichkeit, automatisch eine Version auszuwählen.

   Wenn Sie **Automatisch auswählen** für den referenzierten Inhalt wählt das System automatisch die Version des referenzierten Inhalts aus, die der Version des Inhalts entspricht, in dem er referenziert wird. Nehmen wir beispielsweise an, ein Thema A verweist auf ein Bild B. Bei der Erstellung von Version 1.5 von Thema A war die Version von Bild B 1.2 im Repository. Wenn jetzt eine Grundlinie mit Version 1.5 des Themas A erstellt wird, wobei Bild B auf **Automatisch auswählen**, wählt das System automatisch Version 1.2 von Bild B aus.

   Wenn Sie eine Grundlinie mithilfe der Beschriftungen erstellen, **Automatisch auswählen** wird auf die Version aller referenzierten Inhalte angewendet.

   Wenn der referenzierte Inhalt oder die Assets \(Thema, Unter-Maps, Bilder oder Videos\) nicht versioniert werden \(z. B. neu hochgeladene Inhalte\), erstellt die Erstellung einer Grundlinie eine Version für diese Dateien. Wenn Ihre Dateien jedoch versioniert sind, wird für diese Dateien keine inkrementelle Version erstellt. Dieses Verhalten wird durch die Einstellung zur automatischen Versionserstellung gesteuert, die standardmäßig aktiviert ist. Dies ist auch für die Übersetzung von Inhalten erforderlich, wobei der Übersetzungsprozess erwartet, dass alle Dateien über eine Version verfügen.

   >[!NOTE]
   >
   > Wenn Sie für eine Ressource eine andere Version festlegen möchten, wählen Sie dazu die gewünschte Version aus dem **Version** Dropdown-Liste.

1. Klicken Sie auf **Speichern**.

## Inhalt einer Grundlinie anzeigen {#id195FI0I0TLN}

Sie können den Inhalt einer vorhandenen Grundlinie anzeigen, indem Sie auf die Registerkarte Grundlinien klicken und die gewünschte Grundlinienversion aus der Liste auswählen. Die Seite &quot;Grundlinien&quot;ist in drei Teile unterteilt: DITA-Zuordnungsdatei, Inhalt oder Themen der Zuordnung und der referenzierte Inhalt. Wenn Ihre Zuordnung Unterkarten enthält, werden die in der Unterzuordnung referenzierten Themen auch im Abschnitt Inhalt angezeigt. Die verschiedenen Spalten auf der Seite &quot;Grundlinie&quot;werden nachfolgend beschrieben:

- **Name**: Listet die DITA-Zuordnung oder den Titel des Themas oder den Namen des Assets auf, z. B. den Dateinamen eines Bildes.

- **Kind**: Listet die Art oder den Typ des Assets in der Zuordnung auf, z. B. DITA-Zuordnung, DITA-Thema oder Bildformat.

- **Version**: Listet die Version des Assets auf, die in der Grundlinie verfügbar ist.

- **Versionsdatum und -zeit**: Listet das Erstellungsdatum und die Erstellungszeit des Assets für die ausgewählte Version auf.

- **Neueste**: Listet auf, ob die neueste Version des Assets in der Grundlinie verwendet wird.

- **Übergeordnete Zuordnung**: Wenn Ihre Zuordnungsdatei Unterkarten enthält, enthält diese Spalte den Namen der Zuordnung, auf die ein Thema verwiesen wird.

- **Titel**: Listet die Beschriftung\(n\) auf, die auf die Version des Themas angewendet wird.

- **Referenziert von**: Diese Spalte ist nur für den referenzierten Inhalt verfügbar. Es zeigt das übergeordnete Thema des referenzierten Assets an. Wenn ein Asset durch mehrere Themen referenziert wird, werden die Themen durch Kommas getrennt.

## Grundlinien bearbeiten, duplizieren oder entfernen {#id195FI0I0YJL}

**Grundlinien bearbeiten**

Führen Sie die folgenden Schritte aus, um eine vorhandene Grundlinie zu bearbeiten:

1. Wählen Sie die Grundlinie aus und klicken Sie auf **Bearbeiten**.
1. Nehmen Sie die erforderlichen Änderungen an der Grundlinie vor. Sie können den Namen und die Version des Themas oder des referenzierten Inhalts ändern.
1. Klicken Sie auf **Speichern**.

**Grundlinien duplizieren**

Wählen Sie die Grundlinie aus und klicken Sie auf **Duplizieren** , um eine Kopie einer vorhandenen Grundlinie zu erstellen. Geben Sie einen anderen Namen für die Grundlinie an, wählen Sie die Versionsnummer für die Themen und den referenzierten Inhalt aus und klicken Sie auf **Speichern**.

**Grundlinien entfernen**

Wählen Sie die Grundlinien-Version aus und klicken Sie auf **Entfernen** , um eine Grundlinie zu entfernen.

## Hinzufügen von Bezeichnungen zu einer Grundlinie {#id184KD0T305Z}

Das Hinzufügen von Bezeichnungen zu jedem einzelnen Thema kann zeitaufwendig sein. AEM Guides bieten einen einmaligen Mechanismus zum Hinzufügen von Bezeichnungen zu mehreren Themen und referenzierten Inhalten in einer DITA-Map.

Führen Sie die folgenden Schritte aus, um eine Bezeichnung zu mehreren Themen und referenzierten Inhalten in einer DITA Map hinzuzufügen:

1. Wählen Sie auf der Seite Grundlinien eine Grundlinie aus, die die Themen und referenzierten Inhalte enthält, zu denen Sie eine Beschriftung hinzufügen möchten.

   >[!NOTE]
   >
   > Stellen Sie sicher, dass Ihre Grundlinie nicht über die neueste Version eines Themas oder Assets verfügt. Eine Bezeichnung kann nur zu einem Thema oder einem Asset mit Versionsangabe hinzugefügt werden.

1. Klicken **Hinzufügen von Bezeichnungen**.

   ![](images/add-label-baseline-uuid.png){width="800" align="left"}

1. Im **Titel hinzufügen** angeben, geben Sie eine eindeutige Beschriftung an, die dieser Grundlinie zugeordnet werden soll.

   Wenn Ihr Administrator vordefinierte Beschriftungen konfiguriert hat, werden diese Beschriftungen in einer Dropdown-Liste angezeigt. Sie müssen einen Titel aus der Liste auswählen.

1. Wenn Sie die Bezeichnung auf Themen anwenden möchten, die in den Unterkarten referenziert werden, wählen Sie **Beschriftung auf untergeordnete Maps und abhängige Elemente anwenden** -Option.

   - Klicken Sie auf **Hinzufügen**.
Die angegebene Bezeichnung wird der DITA-Zuordnung sowie den referenzierten Themen und Inhalten hinzugefügt.

      ![](images/label-added-baseline-uuid.png){width="650" align="left"}


## Exportieren der übersetzten Grundlinie {#id196SE600GHS}

Sie können Grundlinien für die Übersetzung von Inhalten verwenden. Sie können beispielsweise eine Grundlinie für Version 1.1 erstellen, die für die Übersetzung auf Französisch bereit ist. Auf der Registerkarte Übersetzung müssen Sie Grundlinien verwenden, um Ihren Inhalt zu filtern, und dann die Grundlinie für Version 1.1 Ihres Inhalts auswählen. Die Verwendung von Grundlinien zur Übersetzung von Inhalten erleichtert die Verwaltung Ihrer Inhalte.

Sobald der Inhalt übersetzt wurde, können Sie die übersetzte Grundlinie zur Archivierung exportieren oder für verschiedene Teams in Ihrer Organisation freigeben. Beachten Sie die folgenden Punkte, bevor Sie eine übersetzte Grundlinie exportieren:

- Das Exportieren einer Grundlinie ist erst möglich, nachdem der Inhalt in der Grundlinie übersetzt wurde. Wenn Sie versuchen, eine Grundlinie zu exportieren, für die die Übersetzung nicht gestartet oder nicht abgeschlossen ist, wird ein Fehler ausgegeben.
- Sie können Baseline nur für eine bereits übersetzte Version übertragen. Wenn Sie beispielsweise eine Grundlinie für Version 1.1 Ihres Inhalts erstellt haben und derselbe übersetzt wird, können Sie diese Grundlinie exportieren. Wenn Sie jedoch eine Grundlinie für Version 1.2 erstellt haben, die nicht übersetzt ist, können Sie diese Grundlinie nicht exportieren.
- Wenn eine Grundlinie bereits exportiert wurde, können Sie die vorhandene Grundlinie überschreiben, indem Sie die *Vorhandene Grundlinie überschreiben* -Option beim Exportieren.

Führen Sie die folgenden Schritte aus, um eine übersetzte Grundlinie zu exportieren:

1. Öffnen Sie die DITA-Zuordnung, die die übersetzte Grundlinie enthält.

1. Im **Übersetzung** Registerkarte, erweitern Sie die **Grundlinie** in der linken Leiste verfügbar.

   ![](images/export-baseline.png){width="800" align="left"}

1. Wählen Sie die **Grundlinie verwenden** und wählen Sie die Grundlinie aus, die Sie exportieren möchten.

1. Klicken **Exportgrundlinie**.

   Der Exportstatus wird angezeigt. Wenn der Prozess erfolgreich war, wird Ihnen eine Meldung angezeigt, in der die Sprache erwähnt wird, für die die Grundlinie exportiert wird. Im Fall eines Fehlers wird die Fehlerursache angezeigt.

   Wenn Sie versuchen, die bereits exportierte Baseline zu exportieren, wird Ihnen auch die Fehlermeldung Baseline-Erstellung angezeigt.

1. \(Optional\) Um eine bereits exportierte Grundlinie zu exportieren, wählen Sie **Vorhandene Grundlinie überschreiben** und klicken Sie anschließend auf **Exportgrundlinie**.


**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)
