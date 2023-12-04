---
title: DITA-Zuordnungsbericht aus dem Web-Editor
description: Generieren Sie DITA-Map-Berichte aus dem Webeditor in AEM Handbüchern. Erfahren Sie, wie Sie eine CSV-Datei für Themenlisten, Multimedia-, Metadaten- und Berichte zu fehlerhaften Links erstellen.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '2366'
ht-degree: 0%

---

# DITA-Zuordnungsbericht aus dem Web-Editor {#id231HF0Z0NXA}

AEM Guides verfügen über eine Funktion im Web Editor, mit der Sie die Gesamtintegrität Ihrer Verweise überprüfen und Berichte für diese generieren können.

Sie können die Themenliste anzeigen, die Metadaten aller Verweise verwalten und die Multimedia-Liste für die aktuelle Karte über die **Berichte** im Web Editor.

## Erstellen einer CSV-Datei aus der Themenlistenansicht

Die **Themenliste** -Ansicht enthält detaillierte Informationen zu Ihren Themen, wie z. B. den Referenztyp, den Dokumentstatus und den Autor.

Sie können einen Bericht zu den Themen erstellen, indem Sie die folgenden Schritte ausführen:

1. Im **Repository** öffnen Sie die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte.
1. Doppelklicken **Themenliste** auf der linken Seite. Die Liste der in der DITA-Map vorhandenen Themen wird angezeigt.

   ![](images/web-editor-topiclist-panel.png){width="800" align="left"}

1. Aus dem **Filter** Bedienfeld Sie können Ihre Themen nach **Referenztyp** \(direkt oder indirekt\), **Dokumentstatus** \(der aktuelle Status Ihrer Themen. Wenn sich Ihre Themen beispielsweise im Status &quot;Bearbeiten&quot;, &quot;In Überprüfung&quot;oder &quot;Überprüfen&quot;befinden, werden sie aufgelistet\) oder die **Autor** des Themas.

1. Sie können auch die folgenden Themenfilteroptionen verwenden, um die folgenden Spalten in der Liste anzuzeigen:

   - **Thema** Der Titel des Themas wird in der DITA-Zuordnung angegeben. Sie können auf das Thema klicken, um es zu bearbeiten.
   - **Dateiname** Name der Datei.
   - **UUID** Die universelle eindeutige Kennung \(UUID\) der Datei.
   - **Dateispeicherort** Der vollständige Pfad des Themas.
   - **Referenztyp** Die Art der Referenz - direkt oder indirekt.
   - **Dokumentstatus** Der aktuelle Status des Themas.
   - **Autor** Der Benutzer, der zuletzt an dem Thema gearbeitet hat.
   - **Übergeordnete Zuordnung** Die Liste aller Maps, auf die direkt auf das Thema verwiesen wird.
   >[!NOTE]
   >
   > Klicks **Aktualisieren** , um eine neue Liste von Themen zu erhalten und alle Änderungen in Ihrer Zuordnungsdatei anzuzeigen oder ob ein Verweis in Ihrer Themendatei aktualisiert wird.

1. Klicks **CSV herunterladen** um den aktuellen Schnappschuss der Themen in der DITA-Map herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die in der **Themenliste** anzeigen. Anschließend können Sie diese CSV-Datei mit der Themenliste in einem beliebigen CSV-Editor öffnen.

**Metadaten stapelweise aus dem Metadatenbericht verwalten**

Mit AEM Guides können Sie DITA-Inhalte aus dem Web-Editor taggen. Sie können Tags auf ein einzelnes Thema anwenden oder die Bulk-Tagging-Funktion verwenden, um mehrere Tags auf mehrere Themen, eine DITA-Map oder eine Unterzuordnung anzuwenden. Sie können auch den Dokumentstatus aller ausgewählten Themen in den nächsten möglichen allgemeinen Dokumentstatus ändern.

## Anzeigen von Metadaten

Führen Sie die folgenden Schritte aus, um die Metadaten Ihrer Referenzen in der aktuellen DITA-Zuordnung anzuzeigen:

1. Öffnen Sie im Bereich &quot;Repository&quot;die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte.
1. Doppelklicken **Metadaten** auf der linken Seite. Die Metadatenliste aller Verweise in der DITA-Zuordnung wird angezeigt. Dazu gehören auch die Medienreferenzen.

   ![](images/web-editor-metadata-panel.png){width="800" align="left"}

1. Aus dem **Filter** Bereich können Sie Ihre Themen nach **Dokumentstatus** \(der aktuelle Status Ihrer Themen. Wenn sich Ihre Themen beispielsweise im Status &quot;Bearbeiten&quot;, &quot;In Überprüfung&quot;oder &quot;Überprüfen&quot;befinden, werden sie aufgelistet\), **Verweise** \(direkt oder indirekt\), **Dateityp** \(Zuordnung, Thema und Bild\) der Referenz.
1. Sie können auch festlegen, dass nur die **Dateien ohne Tags** oder wählen Sie bestimmte Tags aus der **Tags** filtern, um die mit ihnen verknüpften Dateien anzuzeigen.
   1. Sie können auch die folgenden Themenfilteroptionen verwenden, um die folgenden Spalten in der Metadatenliste anzuzeigen:
      - **Titel** \(standardmäßig ausgewählt\) Der Titel der referenzierten Datei wird in der DITA-Zuordnung angegeben. Sie können auf die Datei klicken, um sie zu bearbeiten. Sie können auch im Web Editor auf eine Audio- oder Videodatei klicken und diese wiedergeben. Sie können die Lautstärke oder die Ansicht des Videos ändern. Im Kontextmenü haben Sie auch die Möglichkeit, Bilder herunterzuladen, die Wiedergabegeschwindigkeit zu ändern oder Bilder im Bild anzuzeigen.

        >[!NOTE]
        >
        > Neben dem Titel einer ausgecheckten Datei wird auch ein Symbol zum Auschecken angezeigt. Sie können den Mauszeiger über das Symbol bewegen, um den Namen des Benutzers anzuzeigen.

      - **Dateiname** Der Name der Datei.
      - **Dateispeicherort** Der vollständige Pfad der Datei.
      - **Tags** \(standardmäßig ausgewählt\) Auf die Datei angewendete Tags.

        >[!NOTE]
        >
        > Standardmäßig können Sie zwei Tags für eine Datei anzeigen. Um weitere Tags anzuzeigen, klicken Sie auf **Mehr anzeigen**. Klicks **Weniger anzeigen** , um die Liste erneut zu verzeichnen.

      - **Referenztyp** Art der Referenz - direkt oder indirekt
      - **Dokumentstatus** \(standardmäßig ausgewählt\) Der aktuelle Status der Referenzdatei.
      - **Dateityp** \(standardmäßig ausgewählt\) Typ der Quelldatei. Die verfügbaren Optionen sind &quot;Zuordnung&quot;, &quot;Thema&quot;und &quot;Bild&quot;.
      - **Ausgecheckt von** Der Benutzer, der die Datei ausgecheckt hat.
1. Klicks **CSV herunterladen** , um die aktuelle Momentaufnahme der Verweise in der DITA-Map herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die in der Ansicht &quot;Themenliste&quot;gefilterten Referenzen. Sie können diese Metadaten-CSV-Datei dann in einem beliebigen CSV-Editor öffnen.

**Aktualisieren von Metadaten**

1. Um Metadaten zu aktualisieren, wählen Sie die Dateien aus, für die Sie aktualisieren möchten.

   >[!NOTE]
   >
   > Es ist nicht möglich, ausgecheckte Dateien auszuwählen. Neben dem Titel einer ausgecheckten Datei wird auch ein Symbol zum Auschecken angezeigt. Sie können den Mauszeiger über das Symbol bewegen, um den Namen des Benutzers anzuzeigen.

1. Auswählen **Verwalten** von oben aus.

   ![](images/web-editor-manage-metadata.png){width="350" align="left"}

1. Wenn Sie neue Tags hinzufügen möchten, wählen Sie neue Tags aus der Dropdown-Liste aus, um sie auf alle ausgewählten Themen anzuwenden. Sie können auch ein beliebiges Tag löschen, indem Sie auf das Kreuzsymbol neben dem Tag klicken.

   >[!NOTE]
   >
   > Die allgemeinen Tags, die auf alle ausgewählten Themen angewendet werden, werden aufgelistet.

1. Wählen Sie einen neuen Dokumentstatus aus, wenn Sie den Dokumentstatus aller ausgewählten Verweise ändern möchten. Das Dopdown zeigt den gemeinsamen möglichen Status für alle ausgewählten Themen an. Wenn der aktuelle Status Ihrer Themen beispielsweise In-Review lautet, können Sie den Status &quot;Entwurf&quot;, &quot;Genehmigt&quot;oder &quot;Überprüfen&quot;anzeigen.
1. Klicks **Aktualisieren** , um die Metadaten zu aktualisieren. Eine Bestätigungsmeldung wird für die Metadaten angezeigt, unabhängig davon, ob sie erfolgreich aktualisiert wurden oder fehlgeschlagene Aktualisierungen aufweisen. Sie können auch auf **Bericht herunterladen** , um die Metadaten-CSV-Datei aus dem Bestätigungsdialogfeld herunterzuladen. Diese CSV-Datei enthält die Details zum Aktualisierungsstatus für die ausgewählten Verweise.

## Multimedia-Bericht erstellen

Die **Multimedia** enthält detaillierte Informationen zu den in Ihrer Zuordnung verwendeten Multimedia-Dateien, wie Titel, Typ \(Audio, Video und Bilder\), Dateien, in denen Multimedia verwendet wird, und Referenztyp der Dateien, in denen sie verwendet wurden. Sie können auch die UUID und den Speicherort der Multimedia-Dateien im Repository anzeigen. Sie können einen Multimedia-Bericht erstellen, indem Sie die folgenden Schritte ausführen:

1. Im **Repository** öffnen Sie die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte.
1. Doppelklicken **Multimedia** auf der linken Seite. Die Liste der in der DITA-Karte vorhandenen Multimedia-Dateien wird angezeigt.
1. Aus dem **Filter** -Bedienfeld können Sie die Liste nach Multimedia oder nach den Namen von sortieren, die in Referenzen verwendet werden.

   - Wenn Sie nach **Multimedia**, wird der Name des Multimediums in der ersten Spalte angezeigt und dann werden die Namen aller Verweise, in denen es verwendet wurde, in einer anderen Spalte in derselben Zeile angezeigt. Der folgende Screenshot zeigt beispielsweise die Multimedia-Datei WarmCoolForC.gif in der ersten Spalte und drei Referenzen, in denen sie verwendet wird, werden in der dritten Spalte in derselben Zeile angezeigt.

     ![](images/multimedia-report-file-order.png){width="650" align="left"}

   - Wenn Sie nach **Verwendet in** -Spalte, werden Sie die verschobene Ansicht anzeigen, wobei die Namen der Referenzen, in denen Multimedia verwendet wurde, in der ersten Spalte aufgeführt sind, während die Multimedia-Namen in einer anderen Spalte in separaten Zeilen aufgeführt sind. Der folgende Screenshot zeigt beispielsweise die Namen der drei Verweise \(Sitztemperatur anpassen, Sitztemperatur ändern und Besatzfläche ändern\) in der ersten Spalte und das Multimedia WarmCoolForC.gif wird in der dritten Spalte in drei separaten Zeilen angezeigt.

     ![](images/multimedia-report-used-in-order.png){width="650" align="left"}

1. Sie können Ihre Multimedia-Daten nach **Multimedia-Typ**, und **Referenztyp**. Die Liste der Multimedia-Dateien wird je nach Auswahl in der Dropdown-Liste angezeigt. Sie können beispielsweise festlegen, dass nur die Audioverweise in Ihrer DITA-Zuordnung angezeigt werden und eine Datei nur die darin verwendeten Audioverweise anzeigt.

   >[!NOTE]
   >
   > Je nach Multimedia-Typ, der auf Ihrer Karte verwendet wird, sind Bild, Video und Audio in der **Multimedia-Typ** Dropdown-Liste und Direkt oder Indirect werden im **Referenztyp** Dropdown.

1. Sie können auch die folgenden Filteroptionen verwenden, um die folgenden Spalten in der Liste anzuzeigen:

   - **Multimedia** \(standardmäßig ausgewählt\) Der Titel des Multimediums wird in der DITA-Zuordnung angegeben. Sie können auf das Multimedia klicken, um es zu bearbeiten.
   - **Multimedia-Speicherort** Der vollständige Pfad des Multimediums.
   - **Multimedia-UUID** Die universelle eindeutige Kennung \(UUID\) der Datei.
   - **Multimedia-Typ** \(standardmäßig ausgewählt\) Typ des Multimediums. Die verfügbaren Optionen sind Audio, Video oder Bild.
   - **Verwendet in** \(standardmäßig ausgewählt\) Die Referenzen, in denen das Multimedia verwendet wurde. Sie können auf die Referenz klicken, um sie zu bearbeiten.
   - **Referenztyp** \(standardmäßig ausgewählt\) Der Verweistyp - direkt oder indirekt.
   >[!NOTE]
   >
   > Klicks **Aktualisieren** um eine neue Liste von Multimedia zu erhalten und alle Änderungen in Ihrer Map-Datei anzuzeigen oder ob Multimedia in Ihrer DITA-Karte aktualisiert wird.

1. Sie können auch im Web Editor auf eine Audio- oder Videodatei klicken und diese wiedergeben. Sie können die Lautstärke oder die Ansicht des Videos ändern. Im Kontextmenü haben Sie auch die Möglichkeit, Bilder herunterzuladen, die Wiedergabegeschwindigkeit zu ändern oder Bilder im Bild anzuzeigen.

   ![](images/video-web-editor.png){width="800" align="left"}

1. Klicks **CSV herunterladen** um den aktuellen Schnappschuss des Multimedia-Programms in die DITA-Karte herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die Multimedia-Datei, die im **Multimedia** anzeigen. Sie können diese Multimedia-CSV-Datei dann in einem beliebigen CSV-Editor öffnen.


## Fehlerbehebung bei fehlerhaften Links{#report-broken-links}

Die **Beschädigte Links** ist ein nützlicher Bericht, der Ihnen die Details der fehlerhaften Links auf Ihrer aktuellen Karte liefert. Sie können die fehlerhaften Links anzeigen, die für DITA-Themen, Multimedia-Dateiverweise, Content-Schlüssel-Verweise usw. sein können. Sie haben auch die Möglichkeit, diese hier selbst zu reparieren.
Der Bericht enthält detaillierte Informationen wie den fehlerhaften Link, den Link-Typ, die Dateien, in denen die Referenz verwendet wird, und den Typ der Dateien, in denen sie verwendet wurden.
Sie können den Bericht auf fehlerhafte Links anzeigen, indem Sie die folgenden Schritte ausführen:
1. Im **Repository** öffnen Sie die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte.
1. Doppelklicken **Beschädigte Links** auf der linken Seite. Die Liste der fehlerhaften Links oder Verweise, die in der DITA-Zuordnung vorhanden sind, wird angezeigt.
1. Aus dem **Filter** -Bedienfeld können Sie die Liste nach Links oder nach den Namen von sortieren, die in Referenzen verwendet werden.

   - Wenn Sie nach **Beschädigter Link**, werden die Pfade der fehlerhaften Links in der ersten Spalte angezeigt und die Namen aller Verweise, in denen sie verwendet wurden, werden dann in einer anderen Spalte in separaten Zeilen angezeigt. Wenn derselbe fehlerhafte Link in mehreren Dateien verwendet wird, werden sie in einer Zeile angezeigt und als gruppierte Zeilen oder Unterzeilen angezeigt. Der folgende Screenshot zeigt beispielsweise drei fehlerhafte Links in der ersten Spalte und die Referenz, in der sie verwendet werden. `TestMap.ditamap` wird in der dritten Spalte in drei separaten Zeilen angezeigt.
   ![](images/broken-link-report.png){width="800" align="left"}

   - Wenn Sie nach **Verwendet in** -Spalte, werden Sie die verschobene Ansicht anzeigen, wobei die Namen der Verweise, in denen die fehlerhaften Links verwendet wurden, in der ersten Spalte aufgeführt sind, während die fehlerhaften Links in einer anderen Spalte in derselben Zeile aufgeführt sind. Der folgende Screenshot zeigt beispielsweise die Referenz (in der der fehlerhafte Link verwendet wird) `TestMap.ditamap` in der ersten Spalte und die fehlerhaften Links werden in der dritten Spalte in derselben Zeile angezeigt.
   ![](images/broken-link-filter-usedin.png){width="800" align="left"}
1. Sie können Ihre fehlerhaften Links nach der **Dateityp** und **Link-Typ**. Die Liste der fehlerhaften Links wird basierend auf Ihrer Auswahl in der Dropdown-Liste angezeigt. Sie können beispielsweise festlegen, dass nur die Inhaltsreferenzen in Ihrer DITA-Zuordnung angezeigt werden und eine Datei nur die darin verwendeten Inhaltsreferenzen anzeigt.

   Je nach Typ der Referenzen, die in Ihrer Zuordnung verwendet werden, sind die Dateireferenz, die Schlüsselreferenz, die Inhaltsreferenz, die Inhaltsschlüsselreferenz, die Bildreferenz und die Multimedia-Dateireferenz in der **Link-Typ** Dropdown-Liste und **DITA-Thema** oder **DITA Map** sind in der **Dateityp** Dropdown.
1. Sie können auch die folgenden Filteroptionen verwenden, um die folgenden Spalten in der Liste anzuzeigen:

   - **Beschädigter Link** (standardmäßig ausgewählt) Der Pfad des fehlerhaften Links wird in der DITA-Zuordnung angegeben.

   - **Link-Typ** (standardmäßig ausgewählt) Der Typ der Links. Die verfügbaren Optionen sind Content Key Reference, Content Reference, DITA Topic, File Reference, Image Reference, Key reference, and Multimedia File Reference.

   - **Verwendet in** (standardmäßig ausgewählt) Die Verweise, in denen der fehlerhafte Link verwendet wurde. Sie können auf die Referenz klicken, um sie im Autorenmodus anzuzeigen.

   - **Dateityp** (standardmäßig ausgewählt) Der Verweistyp - DITA Map oder DITA-Thema.
Klicks **Aktualisieren** um eine neue Liste mit fehlerhaften Links zu erhalten und alle Änderungen in Ihrer Map-Datei anzuzeigen oder ob ein defekter Link in Ihrer DITA-Map aktualisiert wird.
1. Sie können auf die **Link reparieren** Symbol (![](images/fix-broken-link.svg)), um den fehlerhaften Link zu beheben.

   >[!NOTE]
   >
   > Bewegen Sie den Mauszeiger über den Pfad des fehlerhaften Links unter der Spalte &quot;Beschädigter Link&quot;, um den Link &quot;Fehlerbehebung&quot;anzuzeigen (![](images/fix-broken-link.svg)).

   Sie können einen Link in beiden Ansichten korrigieren, wenn Sie **Beschädigte Links** oder **Verwendet in**.

   >[!NOTE]
   >
   > Wenn Sie einen fehlerhaften Link korrigieren, während Sie nach fehlerhaften Links sortiert haben, wird der Link in allen Dateien behoben, in denen er verwendet wird (die in einer einzigen Zeile gruppiert sind).

1. Sie müssen die erforderlichen Referenzdetails im Abschnitt **Link aktualisieren** angezeigt. Die in **Link aktualisieren** würde vom Referenztyp abhängen.\
   Wenn Sie einen Link korrigieren, wird er nicht unter der Liste der fehlerhaften Links angezeigt. Stattdessen können Sie sie unter der Themenliste oder den Metadaten anzeigen.

1. Klicks **CSV herunterladen** , um die aktuelle Momentaufnahme der fehlerhaften Links in der DITA-Map herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die fehlerhaften Links, die in der Ansicht &quot;Broken Links&quot;gefiltert wurden. Sie können diese CSV-Datei dann in einem beliebigen CSV-Editor öffnen und anzeigen.


**Übergeordnetes Thema:**[ Berichte](reports-intro.md)
