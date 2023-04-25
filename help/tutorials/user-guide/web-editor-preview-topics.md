---
title: Vorschau eines Themas
description: Erfahren Sie, wie Sie eine Vorschau eines Themas anzeigen
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '1815'
ht-degree: 0%

---


# Vorschau eines Themas {#id1696II000QR}

Nachdem ein Thema erstellt wurde, generiert AEM Guides eine Vorschau des Themas. Der Vorschaumodus bietet verschiedene Funktionen, mit denen Sie Ihr Dokument bearbeiten können.

Führen Sie die folgenden Schritte aus, um eine Vorschau eines Themas anzuzeigen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zu dem Thema, das Sie anzeigen möchten.
1. Klicken Sie auf das Thema, das Sie anzeigen möchten.

   Eine Vorschau des Themas wird in der Assets-Benutzeroberfläche angezeigt.

   >[!NOTE]
   >
   > Sie können die Version des aktiven Themas oder der DITA-Zuordnung oben rechts auf der Registerkarte &quot;Datei&quot;des Themas sehen.

   >[!IMPORTANT]
   >
   > Die Positionierung der folgenden Funktionen in der Vorschau-Symbolleiste kann je nach Einrichtung des AEM-Servers unterschiedlich sein. Einige der Funktionen sind möglicherweise in der Hauptsymbolleiste verfügbar, während andere im Menü Mehr verfügbar sein könnten.

## Im Vorschaumodus verfügbare Funktionen

![](images/preview-screen.png){width="800" align="left"}

Sie können die folgenden Vorgänge über die Symbolleiste im Vorschaumodus ausführen:

**Eigenschaften**

Zeigen Sie die Eigenschaften des ausgewählten Themas an. Basierend auf Ihrer AEM können Sie Eigenschaften wie Metadaten, Aktivierung planen \(de\), Verweise, Dokumentstatus und mehr sehen.

>[!NOTE]
>
> Die Titeleigenschaft eines Themas wird automatisch aus dem `title` -Tag des DITA-Themas oder -Map. Wenn Sie im Eigenschaftenfenster Änderungen am Titel vornehmen, geht diese Änderung verloren. Wenn Sie die Eigenschaft title aktualisieren möchten, sollten Sie dies mit dem Web-Editor tun.

Die Eigenschaftenseite enthält nützliche Informationen zu den Verweisen, z. B. wo eine Zuordnung oder ein Thema verwendet wird oder welche Verweise in einem Dokument enthalten sind. Auf der Seite &quot;Eigenschaften&quot;werden zwei Arten von Verweisen für ein Dokument aufgelistet: **Verwendet in** und **Ausgehende Verweise**.

Die **Verwendet in** referenziert die Dokumente, in denen die aktuelle Datei referenziert oder verwendet wird. Die **Ausgehende Verweise** listet die Dokumente auf, auf die im aktuellen Dokument verwiesen wird.

Das Symbol \(+\) im **Verwendet in** Im Abschnitt Verweise können Sie weiter nach oben navigieren, um zu ermitteln, wo dieses Thema verwendet oder referenziert wird.

![](images/used-in-dialog_cs.png){width="800" align="left"}

Klicken Sie auf ![](images/right-arrow-used-in-dialog.svg)-Symbol neben einem Dokument zeigt die Zuordnungs- oder Themendateien an, auf die dieses Dokument weitergeleitet wird.

**Bedingte Filterung \(A/B\)**

Wenn Ihr Thema bedingte Inhalte enthält, wird das A/B-Symbol in der Symbolleiste angezeigt. Wenn Sie auf dieses Symbol klicken, wird ein Popup geöffnet, in dem Sie den Inhalt gemäß den verfügbaren Bedingungen im Thema filtern können.

>[!NOTE]
>
> Der bedingte Inhalt wird im Web Editor mit einer hellen Hintergrundfarbe hervorgehoben.

![](images/conditional-popup_cs.png){width="300" align="left"}

**Bearbeiten**

- Öffnen Sie das Thema zur Bearbeitung im Web-Editor. Die **Bearbeiten** ist nicht verfügbar, wenn Ihr Administrator die Option **Bearbeitung ohne Checkout deaktivieren** -Option. Wenn die Option aktiviert ist, wird die **Bearbeiten** nur nach dem Auschecken einer Themendatei.

**Schlüsselauflösung**

- Wenn Sie eine Schlüsselspeicherdatei für das Thema verwenden möchten, klicken Sie auf das Symbol Schlüsselauflösung . Sie können dann im Popup Schlüsselauflösung einen Schlüsselraum auswählen.

**Quelle**

- Öffnen Sie den XML-Quellcode einer Datei. Sie können den zugrunde liegenden XML-Code einer Zuordnung, eines Themas oder einer DITAVAL-Datei anzeigen, indem Sie die Datei im Vorschaumodus öffnen und auf das Symbol Quelle klicken. Das Popup &quot;XML-Quelle&quot;zeigt den XML-Quellcode an. Sie können einen bestimmten Code aus der Datei auswählen oder `Ctrl`+`a` , um den gesamten Inhalt auszuwählen.

   >[!NOTE]
   >
   > Um die Quellcodeansicht einer DITA-Map-Datei zu erhalten, wählen Sie die Datei in der Assets-Benutzeroberfläche aus und klicken Sie auf Quelle .

   ![](images/xml-source-code-view-from-preview_cs.png){width="800" align="left"}

**UUID-Link freigeben**

- Mit AEM Guides können Sie die UUID-basierten Links für DITA-Maps, -Themen und -Bilddateien von den folgenden Orten freigeben:

   - Assets-Benutzeroberfläche
   - DITA-Map-Konsole
   - Themen- oder Bildvorschau

Eine neue Option **UUID-Link freigeben** wird in der Symbolleiste der oben genannten Bereiche angezeigt. Der folgende Screenshot zeigt die **UUID-Link freigeben** im Vorschaumodus eines Themas:

![](images/share-uuid-link_cs.png){width="800" align="left"}

In der Asset-Benutzeroberfläche ist diese Option bei der Auswahl einer Datei sichtbar. Im Vorschaumodus ist diese Option standardmäßig in der Hauptsymbolleiste verfügbar. In einer DITA-Map-Konsole ist diese Option im Abschnitt Ausgabevorgaben sichtbar.

Nachdem Sie die URL kopiert haben, können Sie sie auch für andere Benutzer freigeben, um ihnen direkten Zugriff auf die Datei zu gewähren. Dieser Link bleibt auch dann gültig, wenn die Datei an einen anderen Speicherort im Repository verschoben wird. Der Link schlägt nur dann fehl, wenn die Datei aus dem Repository gelöscht wird.

Wenn Sie den Link über die DITA-Map-Konsole oder den Vorschaumodus einer Datei freigeben, hat der Benutzer dieselbe Ansicht der Datei aufgerufen. Wenn Sie jedoch den Link einer Zuordnungsdatei über die Assets-Benutzeroberfläche freigeben, wird der Benutzer zur Konsole der Zuordnung geleitet. Gleichermaßen wird bei Themen oder Bilddateien die Vorschau der Datei angezeigt.

>[!IMPORTANT]
>
> Der Link kann nicht als Referenz-Link in einem anderen Thema verwendet werden. Er bietet nur direkten Zugriff auf die Datei im Repository. Außerdem bleibt der Link gültig, solange die Datei im Repository verfügbar ist. Selbst wenn die Datei an einen anderen Speicherort im Repository verschoben wird, bleibt der Link gültig. Der Link schlägt nur fehl, wenn die Datei aus dem Repository gelöscht wird.

**Auschecken/Einchecken**

- Blendet die Funktionen &quot;Auschecken und Einchecken&quot;ein bzw. aus. Wenn eine Datei ausgecheckt ist, erhält der aktuelle Benutzer eine exklusive Schreibberechtigung für die Datei. Eine ausgecheckte Datei kann im Web Editor zur Bearbeitung geöffnet werden. Nachdem Sie die erforderlichen Änderungen vorgenommen haben, klicken Sie auf das Symbol Einchecken , um die Datei in DAM zu speichern.

Wenn Sie ein Thema auschecken, wird der Dateistatus in der Kartenansicht und in der Listenansicht als ausgecheckt angezeigt.

Ausgecheckte Datei in der Kartenansicht:

![](images/checkout-card-62.png){width="300" align="left"}

Ausgecheckte Datei in der Listenansicht:

![](images/checkout-list-62.png){width="550" align="left"}

Wenn die Spalte &quot;Ausgecheckt&quot;nicht angezeigt wird, wählen Sie **Anzeigeeinstellungen** under **Listenansicht** und wählen Sie die **Ausgecheckt** -Status in **Spalten konfigurieren** angezeigt.

![](images/list-view-settings-check-out_cs.png){width="800" align="left"}

>[!TIP]
>
> Best Practices für die Arbeit mit dem Auschecken und Einchecken von Dateien finden Sie im Abschnitt Versionierung von Inhalten im Handbuch Best Practices .

**Unterschied der webbasierten Version**

- Wenn Ihr Thema einige Änderungen erfahren hat, können Sie die Änderungen, die in verschiedenen Versionen dieses Themas vorgenommen wurden, einfach herausfinden. So finden Sie Änderungen in verschiedenen Versionen eines Themas:

   >[!IMPORTANT]
   >
   > Die im folgenden Verfahren beschriebene Methode gilt nur für DITA-Dateien. Verwenden Sie bei Nicht-DITA-Dateien die Timeline-Ansicht, um Versionen zu erstellen oder eine vorhandene Version einer Datei wiederherzustellen.

   1. Öffnen Sie das Thema im Vorschaumodus.

   1. Klicken Sie in der linken Leiste auf **Versionsverlauf** und wählen Sie eine Version aus.

      ![](images/timeline-versions62_cs.png){width="800" align="left"}

   1. Wählen Sie in den aufgeführten Versionen die Version aus, die Sie als Basisversion verwenden möchten, und klicken Sie auf **Vorschau der Version**. Die Vorschau der ausgewählten Version wird im Fenster Versionsvorschau angezeigt.

   1. Aus dem **Diff anzeigen** auswählen, wählen Sie die Version aus, mit der Sie die Basisversion vergleichen möchten.

      ![](images/show-diff-list-cropped.png){width="800" align="left"}

      Der geänderte Inhalt wird in der Themenvorschau hervorgehoben. Der grün hervorgehobene Inhalt kennzeichnet den neu hinzugefügten Inhalt und der Inhalt in Rot ist der gelöschte Inhalt.

      ![](images/version-difference.png){width="800" align="left"}


### Verzweigung, Wiederherstellung und nachfolgende Versionierung {#id193PG0Y051X}

- In einer typischen Authoring-Umgebung müssten Sie einen neuen Zweig eines Themas erstellen, um einer bestimmten Version gerecht zu werden. Wie jedes andere Versionsverwaltungssystem können Sie mit AEM Guides eine Verzweigung aus einer vorhandenen Version eines Themas erstellen oder zu einer älteren Version eines Themas zurückkehren. Mithilfe der in AEM Handbüchern bereitgestellten Funktionen zur Versionsverwaltung können Sie die folgenden Aufgaben ausführen:

   - Erstellen einer Verzweigung aus einer vorhandenen Version eines Themas
   - Nachfolgende Versionen in einem neuen Zweig erstellen
   - Auf eine bestimmte Version eines Themas zurücksetzen

   Die folgende Abbildung zeigt die typische Verzweigung und das nachfolgende Versionierungssystem:

   ![](images/branching_illustration.png){width="550" align="center"}

   Für jedes neue Thema wird die erste Version als 1.0 nummeriert. Danach wird jede neue Version des Themas mit einer inkrementellen Zahl wie 1.1, 1.2 usw. gespeichert. Nachdem Sie eine Verzweigung eines Themas erstellt haben, wird eine neue Verzweigung erstellt, die die Versionsnummer enthält, von der aus die Verzweigung erstellt wird, und am Ende der Version eine 0 hinzufügt. Wie in der Abbildung gezeigt, wird eine neue Verzweigung aus Version 1.1 eines Themas erstellt. Der neue Zweig wird mit Version 1.1.0 versioniert. Jedes Mal, wenn Sie eine neue Version des Themas in diesem Zweig speichern, erhält dieser eine inkrementelle Versionsnummer wie 1.1.1, 1.1.2 usw.

   Ähnlich wie beim Verzweigen können Sie auch Ihre funktionierende oder aktuelle Version auf eine beliebige Version zurücksetzen, die im Repository vorhanden ist. Um zu einer Version zurückzukehren, wählen Sie einfach die gewünschte Version des Themas aus und klicken Sie auf **Auf diese Version zurücksetzen** im **Versionsverlauf** Bereich.

   Führen Sie die folgenden Schritte aus, um einen Zweig zu erstellen, zu einer Version zurückzukehren und nachfolgende Versionen eines Themas zu verwalten:

   >[!IMPORTANT]
   >
   > Die im folgenden Verfahren beschriebene Methode gilt nur für DITA-Dateien. Verwenden Sie bei Nicht-DITA-Dateien die Timeline-Ansicht, um Versionen zu erstellen oder eine vorhandene Version einer Datei wiederherzustellen.

   1. Rufen Sie das Thema in der Assets-Benutzeroberfläche auf.

      >[!NOTE]
      >
      > Sie können das Thema auch im Vorschaumodus öffnen und mit Schritt 3 fortfahren.

   1. Wählen Sie das Thema aus, für das Sie eine Verzweigung erstellen möchten.

   1. Klicken Sie in der linken Leiste auf **Versionsverlauf**.

      >[!NOTE]
      >
      > Eine Liste der für das ausgewählte Thema verfügbaren Versionen wird angezeigt. Jede Version enthält den Zeitstempel, den Benutzernamen, den Versionskommentar und [label](web-editor-use-label.md#) Informationen.

   1. Wählen Sie eine Version aus, aus der Sie eine Verzweigung erstellen möchten. Im folgenden Screenshot wird Version 1.2 zum Erstellen einer Verzweigung ausgewählt.

      ![](images/branching.png){width="300" align="left"}

      >[!NOTE]
      >
      > Die aktuelle Version eines Themas enthält *\(Aktuell\)* neben der Versionsnummer angegeben.

   1. Klicken **Auf diese Version zurücksetzen**.

      Es wird eine Meldung angezeigt, in der Sie aufgefordert werden, die Erstellung einer neuen Verzweigung zu bestätigen.

   1. *\(Optional\)* In der Eingabeaufforderung erhalten Sie eine Option, die **Aktuelle Arbeitskopie als neue Version speichern**. Je nach Auswahl dieser Option sind die beiden folgenden Aktionen möglich:

      - Wenn Sie diese Option auswählen, wird eine Verzweigung aus Version 1.1 erstellt. Außerdem wird eine neue Version des Themas auch aus der aktuellen Arbeitskopie des Themas erstellt und als nächste Version - 1.4 - gespeichert.

         ![](images/next_version_created_over_working_copy.png){width="300" align="left"}

         Version 1.2 wird zur aktuellen Arbeitskopie des Themas. Jede anschließend gespeicherte Version wird unter dem neuen Zweig 1.1 erstellt. Die nachfolgende Version eines neuen Themas in diesem Zweig wird beispielsweise als 1.2.0 gespeichert.

         ![](images/new_version_in_branch.png){width="300" align="left"}

      - Wenn Sie diese Option nicht auswählen, wird keine neue Version aus der aktuellen Arbeitskopie des Themas erstellt. Eine neue Verzweigung wird aus Version 1.2 des Themas erstellt. Jede nachfolgende Version des Themas wird unter der Verzweigung 1.2.0, 1.2.1 usw. gespeichert.

         ![](images/new_version_without_working_copy.png){width="300" align="left"}
   1. Klicken Sie auf **OK**.
   Eine neue Verzweigung wird aus der ausgewählten Version des Themas erstellt. Der obige Prozess kann auch angewendet werden, um zu einer bestimmten Version eines Themas zurückzukehren. Technisch gesehen bedeutet das Zurücksetzen auf eine bestimmte Version, dass Sie eine neue Verzweigung aus der ausgewählten Version erstellen und diese Version zur aktuellen Arbeitskopie des Themas machen. Sie können auch den Verlauf der Dateien anzeigen, die im Bericht Versionsverlauf zurückgesetzt wurden. Weitere Informationen zu diesem Bericht finden Sie unter [Versionsverlauf wiederhergestellter Dateien - Bericht](reports-reverted-file-version-history.md#).

**Übergeordnetes Thema:**[ Erstellen und Anzeigen einer Vorschau von Themen](create-preview-topics.md)

