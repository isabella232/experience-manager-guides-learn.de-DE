---
title: DITA-Zuordnungsbericht aus dem Web-Editor
description: Erfahren Sie, wie Sie im Web Editor einen DITA-Zuordnungsbericht erstellen
source-git-commit: 895d9bd3587c871d5223df5b71403d10bdc3d762
workflow-type: tm+mt
source-wordcount: '1608'
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

   ![](images/web-editor-topiclist-panel.png)

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
   > Klicken **Aktualisieren** um eine neue Liste von Themen zu erhalten und alle Änderungen in Ihrer Zuordnungsdatei zu sehen oder ob ein Verweis in Ihrer Themendatei aktualisiert wird.

1. Klicken **CSV herunterladen** um den aktuellen Schnappschuss der Themen in der DITA-Map herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die in der **Themenliste** anzeigen. Anschließend können Sie diese CSV-Datei mit der Themenliste in einem beliebigen CSV-Editor öffnen.

**Metadaten stapelweise aus dem Metadatenbericht verwalten**

Mit AEM Guides können Sie DITA-Inhalte aus dem Web-Editor taggen. Sie können Tags auf ein einzelnes Thema anwenden oder die Bulk-Tagging-Funktion verwenden, um mehrere Tags auf mehrere Themen, eine DITA-Map oder eine Unterzuordnung anzuwenden. Sie können auch den Dokumentstatus aller ausgewählten Themen in den nächsten möglichen allgemeinen Dokumentstatus ändern.

## Anzeigen von Metadaten

Führen Sie die folgenden Schritte aus, um die Metadaten Ihrer Referenzen in der aktuellen DITA-Zuordnung anzuzeigen:

1. Öffnen Sie im Bereich &quot;Repository&quot;die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte.
1. Doppelklicken **Metadaten** auf der linken Seite. Die Metadatenliste aller Verweise in der DITA-Zuordnung wird angezeigt. Dazu gehören auch die Medienreferenzen.

   ![](images/web-editor-metadata-panel.png)

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
         > Standardmäßig werden zwei Tags für eine Datei angezeigt. Um weitere Tags anzuzeigen, klicken Sie auf **Mehr anzeigen**. Klicken **Weniger anzeigen** um die Liste erneut zu verzeichnen.

      - **Referenztyp** Art der Referenz - direkt oder indirekt
      - **Dokumentstatus** \(standardmäßig ausgewählt\) Der aktuelle Status der Referenzdatei.
      - **Dateityp** \(standardmäßig ausgewählt\) Typ der Quelldatei. Die verfügbaren Optionen sind &quot;Zuordnung&quot;, &quot;Thema&quot;und &quot;Bild&quot;.
      - **Ausgecheckt von** Der Benutzer, der die Datei ausgecheckt hat.
1. Klicken **CSV herunterladen** , um die aktuelle Momentaufnahme der Verweise in der DITA-Map herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die in der Ansicht &quot;Themenliste&quot;gefilterten Referenzen. Sie können diese Metadaten-CSV-Datei dann in einem beliebigen CSV-Editor öffnen.

**Aktualisieren von Metadaten**

1. Um Metadaten zu aktualisieren, wählen Sie die Dateien aus, für die Sie aktualisieren möchten.

   >[!NOTE]
   >
   > Es ist nicht möglich, ausgecheckte Dateien auszuwählen. Neben dem Titel einer ausgecheckten Datei wird auch ein Symbol zum Auschecken angezeigt. Sie können den Mauszeiger über das Symbol bewegen, um den Namen des Benutzers anzuzeigen.

1. Auswählen **Verwalten** von oben aus.

   ![](images/web-editor-manage-metadata.png)

1. Wenn Sie neue Tags hinzufügen möchten, wählen Sie neue Tags aus der Dropdown-Liste aus, um sie auf alle ausgewählten Themen anzuwenden. Sie können auch ein beliebiges Tag löschen, indem Sie auf das Kreuzsymbol neben dem Tag klicken.

   >[!NOTE]
   >
   > Die allgemeinen Tags, die auf alle ausgewählten Themen angewendet werden, werden aufgelistet.

1. Wählen Sie einen neuen Dokumentstatus aus, wenn Sie den Dokumentstatus aller ausgewählten Verweise ändern möchten. Das Dopdown zeigt den gemeinsamen möglichen Status für alle ausgewählten Themen an. Wenn der aktuelle Status Ihrer Themen beispielsweise In-Review lautet, können Sie den Status &quot;Entwurf&quot;, &quot;Genehmigt&quot;oder &quot;Überprüfen&quot;anzeigen.
1. Klicken **Aktualisieren** , um die Metadaten zu aktualisieren. Eine Bestätigungsmeldung wird für die Metadaten angezeigt, unabhängig davon, ob sie erfolgreich aktualisiert wurden oder fehlgeschlagene Aktualisierungen aufweisen. Sie können auch auf **Bericht herunterladen** , um die Metadaten-CSV-Datei aus dem Bestätigungsdialogfeld herunterzuladen. Diese CSV-Datei enthält Details zum Aktualisierungsstatus für die ausgewählten Verweise.

## Multimedia-Bericht erstellen

Die **Multimedia** enthält detaillierte Informationen zu den in Ihrer Zuordnung verwendeten Multimedia-Dateien, wie Titel, Typ \(Audio, Video und Bilder\), Dateien, in denen Multimedia verwendet wird, und Referenztyp der Dateien, in denen sie verwendet wurden. Sie können auch die UUID und den Speicherort der Multimedia-Dateien im Repository anzeigen. Sie können einen Multimedia-Bericht erstellen, indem Sie die folgenden Schritte ausführen:

1. Im **Repository** öffnen Sie die DITA-Map-Datei in der Kartenansicht.
1. Klicken Sie auf **Verwalten** Registerkarte.
1. Doppelklicken **Multimedia** auf der linken Seite. Die Liste der in der DITA-Karte vorhandenen Multimedia-Dateien wird angezeigt.
1. Aus dem **Filter** -Bedienfeld können Sie die Liste nach Multimedia oder nach den Namen von sortieren, die in Referenzen verwendet werden.

   - Wenn Sie nach **Multimedia**, wird der Name des Multimediums in der ersten Spalte angezeigt und dann werden die Namen aller Verweise, in denen es verwendet wurde, in einer anderen Spalte in derselben Zeile angezeigt. Der folgende Screenshot zeigt beispielsweise die Multimedia-Datei WarmCoolForC.gif in der ersten Spalte und drei Referenzen, in denen sie verwendet wird, werden in der dritten Spalte in derselben Zeile angezeigt.

      ![](images/multimedia-report-file-order.png)

   - Wenn Sie nach **Verwendet in** -Spalte, sehen Sie die verschobene Ansicht, in der die Namen der Verweise, in denen Multimedia verwendet wurde, in der ersten Spalte aufgeführt sind, während die Multimedia-Namen in einer anderen Spalte in separaten Zeilen aufgeführt sind. Der folgende Screenshot zeigt beispielsweise die Namen der drei Verweise \(Sitztemperatur anpassen, Sitztemperatur ändern und Besatzfläche ändern\) in der ersten Spalte und das Multimedia WarmCoolForC.gif wird in der dritten Spalte in drei separaten Zeilen angezeigt.

      ![](images/multimedia-report-used-in-order.png)

1. Sie können Ihre Multimedia-Daten nach **Multimedia-Typ** und **Referenztyp**. Die Liste der Multimedia-Dateien wird je nach Auswahl in der Dropdown-Liste angezeigt. Sie können beispielsweise festlegen, dass nur die Audioverweise in Ihrer DITA-Zuordnung angezeigt werden und eine Datei nur die darin verwendeten Audioverweise anzeigt.

   >[!NOTE]
   >
   > Je nach Multimedia-Typ, der auf Ihrer Karte verwendet wird, sind Bild, Video und Audio in der **Multimedia-Typ** Dropdown-Liste und Direkt oder Indirect werden im **Referenztyp** Dropdown-Liste.

1. Sie können auch die folgenden Filteroptionen verwenden, um die folgenden Spalten in der Liste anzuzeigen:

   - **Multimedia** \(standardmäßig ausgewählt\) Der Titel des Multimediums wird in der DITA-Zuordnung angegeben. Sie können auf das Multimedia klicken, um es zu bearbeiten.
   - **Multimedia-Speicherort** Der vollständige Pfad des Multimediums.
   - **Multimedia-UUID** Die universelle eindeutige Kennung \(UUID\) der Datei.
   - **Multimedia-Typ** \(standardmäßig ausgewählt\) Typ des Multimediums. Die verfügbaren Optionen sind Audio, Video oder Bild.
   - **Verwendet in** \(standardmäßig ausgewählt\) Die Referenzen, in denen das Multimedia verwendet wurde. Sie können auf die Referenz klicken, um sie zu bearbeiten.
   - **Referenztyp** \(standardmäßig ausgewählt\) Der Verweistyp - direkt oder indirekt.

   >[!NOTE]
   >
   > Klicken **Aktualisieren** um eine neue Liste von Multimedia zu erhalten und alle Änderungen in Ihrer Map-Datei zu sehen oder ob Multimedia in Ihrer DITA-Karte aktualisiert wird.
1. Sie können auch im Web Editor auf eine Audio- oder Videodatei klicken und diese wiedergeben. Sie können die Lautstärke oder die Ansicht des Videos ändern. Im Kontextmenü haben Sie auch die Möglichkeit, Bilder herunterzuladen, die Wiedergabegeschwindigkeit zu ändern oder Bilder im Bild anzuzeigen.
   ![](images/video-web-editor.png)

1. Klicken **CSV herunterladen** um den aktuellen Schnappschuss des Multimedia-Programms in die DITA-Karte herunterzuladen. Die CSV-Datei enthält die ausgewählten Spalten und die Multimedia-Datei, die im **Multimedia** anzeigen. Sie können diese Multimedia-CSV-Datei dann in einem beliebigen CSV-Editor öffnen.

**Übergeordnetes Thema:**[ Berichte](reports-intro.md)

