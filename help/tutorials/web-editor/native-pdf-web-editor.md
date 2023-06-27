---
title: Native PDF | PDF-Ausgabegenerierung
description: Generieren einer PDF-Ausgabe in Adobe Experience Manager Guides as a Cloud Service
exl-id: ec3d59b7-1dda-4fd1-848e-21d8a36ff5e4
source-git-commit: d8bc9e2673ce08fe5f71154e9d009d1847b0274d
workflow-type: tm+mt
source-wordcount: '2903'
ht-degree: 1%

---

# PDF-Ausgabe veröffentlichen

Mit AEM Guides können Sie PDF einzelner Themen oder einer ganzen Map-Datei generieren. Sie können Ihre Inhalte mit einer der drei folgenden Methoden im PDF-Format veröffentlichen:

* **DITA-OT**

Verwenden Sie diese Methode, um eine PDF-Ausgabe für eine Zuordnung aus dem Mapping-Dashboard zu generieren. Sie können die Veröffentlichungseigenschaften festlegen, bevor Sie die PDF generieren, indem Sie eine Ausgabevorgabe für die Karte erstellen, die im Karten-Dashboard geöffnet ist. Um eine Ausgabevorgabe zu erstellen oder zu bearbeiten, muss die *Grundlegendes zu den Ausgabevorgaben* im Abschnitt [as a Cloud Service Benutzerhandbuch für AEM](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Weitere Informationen zum Generieren einer PDF mithilfe der DITA-OT-Methode finden Sie unter [Generieren von PDF mithilfe von DITA-OT](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-pdf.html).

* **FrameMaker Publishing Server (FMPS)**

Verwenden Sie diese Methode, um eine PDF-Ausgabe nicht nur aus dem DITA-Inhalt, sondern auch aus FrameMaker-Dokumenten (.book und .fm) zu generieren, die in Ihrem AEM-Repository verfügbar sind. Die PDF kann durch Konfigurieren einer Ausgabevorgabe erstellt und mithilfe von FrameMaker Publishing Server (FMPS) veröffentlicht werden. Sie können das Erscheinungsbild Ihrer Ausgabe für PDF und andere Formate entwerfen und konfigurieren und diese in einer Einstellungsdatei (.sts) speichern. Diese Einstellungsdatei wird dann von FMPS verwendet, um eine Ausgabe für eine DITA-Map- oder .book-Datei zu generieren. Informationen zum Erstellen oder Bearbeiten einer Ausgabevorgabe finden Sie im Abschnitt  *Grundlegendes zu den Ausgabevorgaben* im Abschnitt [as a Cloud Service Benutzerhandbuch für AEM](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Weitere Informationen zum Konfigurieren von FMPS finden Sie unter [Ausgabe aus FrameMaker-Dokumenten generieren](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Ffm-output-generatation.html).

* **Native PDF-Veröffentlichung**

Verwenden Sie diese Methode, um eine funktionsreiche PDF-Ausgabe zu generieren, die auf W3C CSS3- und CSS-Medienstandards basiert. Mit der nativen PDF-Veröffentlichung können Sie Vorlagen verwenden, um das Layout und die Formatierung für Ihre festzulegen und verschiedene Einstellungen zur Feinabstimmung Ihrer PDF anzuwenden. Darüber hinaus können Sie mit dem Vorlageneditor Ihre eigenen Vorlagen ändern und erstellen.

Weitere Informationen zum nativen PDF-Publishing finden Sie unter [Verwenden der nativen PDF-Veröffentlichung](#native-pdf-publishing).


## Verwenden der nativen PDF-Veröffentlichung {#native-pdf-publishing}

Beim Bearbeiten von Inhalten muss sichergestellt werden, dass der Inhalt für Anzeige, Bearbeitung und Druck optimiert ist. Mithilfe von Standards wie dem W3C CSS3 für Inhaltsstile und CSS-Standards für seitendefinierte Eigenschaften wie Größe, Ränder, Ausrichtung, Seitenumbrüche, Kopfzeilen, Fußzeilen und Seitennummerierung können Sie die Ansicht und das Layout für Ihr PDF-Dokument festlegen, um Konsistenz und Benutzerfreundlichkeit zu gewährleisten. Die native PDF-Veröffentlichungsfunktion verwendet diese Standards zum Generieren einer PDF.

Mit der nativen PDF-Veröffentlichung können Sie vordefinierte Vorlagen verwenden, um das Inhaltslayout und die Inhaltsstruktur konsistent zu gestalten, Stylesheets anwenden, um das Erscheinungsbild Ihrer Ausgabe zu ändern, PDF zu optimieren, Druckermarkierungen festzulegen, Unterstützung für Bildschirmlesehilfen zuzulassen, PDF-Konformität festzulegen, Schriftarten einzubetten und vieles mehr.

Die Erstellung einer PDF mit nativer PDF-Veröffentlichung hat zwei Aspekte:

* Verwenden Sie Vorlagen, um Stile auf Inhalte anzuwenden, Seitenlayouts festzulegen und verschiedene Einstellungen zur Feinabstimmung Ihres PDF vorzunehmen. Autoren können die bereitgestellten Beispielvorlagen verwenden/ändern oder benutzerdefinierte Vorlagen erstellen und erweiterte Konfigurationsoptionen festlegen, die von Herausgebern und Entwicklern verwendet werden.

* Erstellen oder konfigurieren Sie eine PDF-Ausgabevorgabe, um die PDF-Einstellungen zu steuern. Nachdem Sie eine PDF-Ausgabevorgabe erstellt haben, können Sie die PDF generieren.

Weitere Informationen finden Sie unter [Generieren einer PDF-Ausgabe](#generate-pdf-output).

## Erstellen einer PDF-Ausgabevorgabe {#create-output-preset}

Der erste Schritt beim Generieren einer PDF-Ausgabe besteht darin, eine PDF-Ausgabevorgabe zu erstellen, die aus einer Sammlung von Veröffentlichungseigenschaften besteht, die einer Zuordnung zugewiesen sind. Sie können eine Ausgabevorgabe für jede Karte erstellen, die im Bereich &quot;Map View&quot;geöffnet ist, oder eine vorhandene Vorgabe konfigurieren, um schnell eine PDF für dieselbe Karte zu generieren.

In der PDF-Ausgabevorgabe können Sie eine Vorlage auswählen, Bedingungen anwenden, Einschränkungen festlegen, um zu steuern, wie ein Benutzer mit Ihrer PDF interagiert, erweiterte Einstellungen wie Komprimierung, Konformität und mehr konfigurieren.

So erstellen oder konfigurieren Sie eine PDF-Ausgabevorgabe:

1. Klicken Sie auf der Registerkarte Ausgabe auf **Vorgaben** in der linken Seitenleiste.
Das Fenster &quot;Voreingestellt&quot;wird geöffnet. <br>
<img src="assets/preset-panel.png" alt="Vorgabenbedienfeld" width="600">

1. In der Ausgabe **Vorgaben** einen der folgenden Schritte ausführen:
   * Doppelklicken Sie auf eine vordefinierte PDF-Ausgabevorgabe, um sie anzuzeigen.
   * Klicken Sie auf das + -Symbol neben **Vorgaben** , um eine neue Ausgabevorgabe von **Typ: PDF**

1. So konfigurieren Sie die Einstellungen einer vorhandenen PDF-Vorgabe:
   * Klicken Sie auf  **Optionen** ![options](assets/options.svg) Symbol neben der gewünschten Ausgabevorgabe und wählen Sie **Bearbeiten**.
Sie können die folgenden Einstellungen in der **Allgemein**, **Metadaten**, **Layout**, **Sicherheit** und **Erweitert** Registerkarten zum Konfigurieren einer PDF-Ausgabevorgabe:

**Allgemein**

Verwenden Sie , um grundlegende Ausgabeeinstellungen anzugeben, z. B. Ausgabepfad, PDF-Dateiname und mehr.

| Einstellung | Beschreibung |
| --- | --- |
| **Ausgabepfad** | Der Pfad im AEM-Repository, in dem die PDF-Ausgabe gespeichert wird. Stellen Sie sicher, dass sich der Ausgabepfad nicht im Projektordner befindet. Wenn Sie das Feld leer lassen, wird die Ausgabe am standardmäßigen Speicherort der DITA-Zuordnung generiert.<br>Sie können auch die folgenden nativen Variablen verwenden, um den Ausgabepfad zu definieren. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um diese Option zu definieren. <br> `${map_filename}`: Verwendet den Namen der DITA-Map-Dateien, um den Zielpfad zu erstellen. <br> `${map_title}`: Verwendet den DITA-Map-Titel, um den Zielpfad zu erstellen. <br>`${preset_name}`: Verwendet den Namen der Ausgabevorgabe, um den Zielpfad zu erstellen. <br> `${language_code}`: Verwendet den Sprachcode, in dem sich die Map-Datei befindet, um den Zielpfad zu erstellen. <br> `${map_parentpath}`: Verwendet den vollständigen Pfad der Map-Datei, um den Zielpfad zu erstellen.  <br>`${path_after_langfolder}`: Verwendet den Pfad der Map-Datei nach dem Sprachordner, um den Zielpfad zu erstellen. |
| **PDF-Datei** | Geben Sie einen Dateinamen an, um die PDF zu speichern. Standardmäßig fügt der PDF-Dateiname den DITA-Map-Namen zusammen mit dem Vorgabennamen hinzu. Beispielsweise ist ditamap &#39;TestMap&#39; und der Name der Vorgabe &#39;preset1&#39;. Dann lautet der Standardname des PDF-Dokuments &#39;TestMap_preset1.pdf&#39;. <br>Sie können auch die folgenden nativen Variablen verwenden, um die PDF-Datei zu definieren. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um diese Option zu definieren. <br>`${map_filename}`<br>`${map_title}`<br>`${preset_name}` <br> `${language_code}`. |
| **Bedingungen anwenden mithilfe von** | Wählen Sie für konditionalisierten Inhalt aus den folgenden Optionen, um eine PDF-Ausgabe zu generieren, die auf diesen Bedingungen basiert: <br><ul> <li> **Keine angewendet** Wählen Sie diese Option aus, wenn Sie keine Bedingung auf die Zuordnung und den Quellinhalt anwenden möchten. <br><li> **Ditaval-Datei** Wählen Sie eine DITAVAL-Datei aus, um bedingte Inhalte zu generieren. Klicken Sie zur Auswahl auf unter &quot;Bedingungsvorgabe&quot;und suchen Sie die Datei. <br> <li> **Bedingungsvorgabe** Wählen Sie eine Bedingungsvorgabe aus der Dropdown-Liste aus, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Diese Option ist sichtbar, wenn Sie eine Bedingung für die DITA-Map-Datei hinzugefügt haben. Die bedingten Einstellungen sind auf der Registerkarte Bedingungsvorgaben der DITA-Zuordnungskonsole verfügbar. Weitere Informationen zur Bedingungsvorgabe finden Sie unter [Verwenden von Bedingungsvorgaben](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-condition-presets.html). <br> </ul> |
| **Grundlinie verwenden** | Wenn Sie eine Grundlinie für die ausgewählte DITA-Zuordnung erstellt haben, wählen Sie diese Option, um die Version anzugeben, die Sie veröffentlichen möchten. Siehe [Arbeiten mit Grundlinien](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-baseline-for-publishing.html) für weitere Details. |
| **PDF mit Änderungsleiste zwischen veröffentlichten Versionen erstellen** | Verwenden Sie die folgenden Optionen, um mithilfe von Änderungsleisten eine PDF zu erstellen, die die Inhaltsunterschiede zwischen zwei Versionen zeigt:   <br><ul><li> **Grundlinie der vorherigen Version** Wählen Sie die Grundlinienversion aus, die Sie mit der aktuellen Version oder einer anderen Grundlinie vergleichen möchten. Auf der PDF wird eine Änderungsleiste angezeigt, die den geänderten Inhalt angibt. Eine Änderungsleiste ist eine vertikale Linie, die neue oder überarbeitete Inhalte visuell identifiziert. Die Änderungsleiste wird links neben dem Inhalt angezeigt, der eingefügt, geändert oder gelöscht wurde. <br> **Hinweis**: Wenn Sie **Grundlinie verwenden** und eine Grundlinie für die Veröffentlichung auswählen, wird der Vergleich zwischen den beiden ausgewählten Grundversionen durchgeführt. Wenn Sie beispielsweise die Grundlinie Version 1.3 unter **Grundlinie verwenden** und Version 1.1 unter **Grundlinie der vorherigen Version**, wird der Vergleich zwischen Version 1.1 der Grundlinie und Version 1.3 durchgeführt. <br><li> **Hinzugefügten Text anzeigen** Wählen Sie diese Option aus, um den eingefügten Text in grüner Farbe und unterstrichen anzuzeigen. Standardmäßig ist diese Option aktiviert. <br> <li> **Gelöschten Text anzeigen** Wählen Sie diese Option, um den gelöschten Text in roter Farbe anzuzeigen und mit einer Durchstreichung zu markieren. Standardmäßig ist diese Option aktiviert. <br>**Hinweis** Sie können die Formatierung der Änderungsleiste, des eingefügten Inhalts oder des gelöschten Inhalts auch mithilfe des Stylesheets anpassen.<br></ul> |
| **Arbeitsablauf nach der Erstellung** | Wählen Sie diese Option, um eine Dropdownliste mit allen in AEM konfigurierten Workflows anzuzeigen. Sie können den Workflow auswählen, der nach Abschluss des Workflows zur PDF-Generierung ausgeführt werden soll. |

**Metadaten**

Metadaten sind die Beschreibung oder Definition Ihres Inhalts. Metadaten helfen beim Content Management und beim Durchsuchen von Dateien im Internet.

Legen Sie auf der Registerkarte Metadaten die Metadatenfelder wie den Namen des Autors, den Dokumenttitel, Schlüsselwörter, Copyright-Informationen und andere Datenfelder für die PDF-Ausgabe fest. Sie können auch benutzerdefinierte Metadaten für Ihre PDF-Ausgabe hinzufügen.

Diese Metadaten werden den Metadaten auf der Registerkarte &quot;Beschreibung&quot;in den Dokumenteigenschaften Ihrer Ausgabe-PDF zugeordnet.

**Hinweis**: Diese Metadaten setzen die auf Buchebene definierten Metadaten außer Kraft.

<img src="assets/pdf-metadata.png" alt="Metadaten-Registerkarte" width="600">

In den Ausgabevorgaben: **PDF auswählen** > **Metadaten** , um Metadatenoptionen hinzuzufügen und anzupassen.
* **XMP bereitstellen**

  Metadatenfelder können durch Importieren direkt ausgefüllt werden [XMP](https://www.adobe.com/products/xmp.html) (Extensible Metadata Platform). Hier können Sie eine XMP herunterladen.

[Herunterladen](assets/SampleXMP.xmp)

  Alternativ können Sie eine XMP mit Adobe Acrobat generieren.
   1. Klicken **Datei** > **Eigenschaften** in Acrobat.
   1. under **Beschreibung** klicken **Zusätzliche Metadaten**.
   1. Wählen Sie im linken Bereich die Option **Erweitert**.
   1. Klicken Sie auf **Speichern**.

  XMP Datei wird auf dem Gerät gespeichert.

* **Bereitstellen von Metadatennamen und -werten**

   1. Fügen Sie einen Namen hinzu, indem Sie aus der Dropdown-Liste auswählen, oder fügen Sie benutzerdefinierte Metadaten hinzu, indem Sie direkt in das Namensfeld eingeben.
   1. Geben Sie den Wert für die Metadaten ein und klicken Sie auf das Symbol &quot;+&quot;.
Die Metadaten werden der Metadatenliste für die PDF hinzugefügt.



**Layout**

Verwenden Sie , um Seitenlayouts festzulegen und Seitenansichtsoptionen für die PDF-Ausgabe wie Seitenanzeige festzulegen und Zoomstufen festzulegen.

| Einstellung | Beschreibung |
| --- | --- |
| **PDF-Vorlage** | PDF-Vorlagen bieten eine klare Struktur für die Definition von Seitenlayouts, Inhaltsstilen und die Anwendung verschiedener Einstellungen auf Ihre PDF-Ausgabe. Wählen Sie aus der Dropdown-Liste PDF-Vorlage die gewünschte Vorlage aus. |
| **Seitenanzeige** | Verwenden Sie die Seitenanzeige für die Seitenansicht, die anzeigt, wie die PDF beim Öffnen angezeigt wird. Wählen Sie aus den Dropdown-Optionen Seitenanzeige aus, um eine bevorzugte Ansicht auszuwählen. <br><ul><li> **Standard**  Wird gemäß der Standardeinstellung des PDF-Viewers auf dem Computer des Benutzers angezeigt.  <br> <li> **Einzelseitenansicht** Zeigt jeweils eine Seite an.   <br> <li> **Einzelseiten-Scrollen** Zeigt eine einzelne Seite in einer vertikalen Spalte mit fortlaufenden Werten an.  <br> <li> **Zwei Seitenansichten** Zeigt zwei Seiten gleichzeitig nebeneinander an. .<br> <li> **Scrollen auf zwei Seiten** Zeigt einen zweiseitigen, parallelen Scrollbereich mit kontinuierlichem Scrollen an. </ul> |
| **Zoom** | Wählen Sie diese Option aus, um die Seitenansicht zu ändern, die anzeigt, wie das PDF beim Öffnen angezeigt wird.  <br><ul><li> **Standard** Zeigt gemäß der Standardeinstellung des PDF-Viewers auf dem Computer eines Benutzers an    <br> <li> **100 %** Zeigt die tatsächliche Seitengröße an.     <br> <li> **Seite anpassen** Passt die Seitenbreite und -höhe in den Dokumentbereich ein. .<br> <li> **Seitenbreite anpassen** Legt die Breite der Seite so fest, dass sie die Breite des Dokumentbereichs ausfüllt.  <br> <li> **Seitenhöhe anpassen** Legt die Höhe der Seite als Füllhöhe für den Dokumentbereich fest. </ul> |

**Sicherheit**

Protect Sie Ihre PDF, indem Sie Einschränkungen zum Öffnen und Lesen der Datei hinzufügen. Verwenden Sie die folgenden Optionen, um unbefugten Zugriff zu vermeiden.

| Einstellung | Beschreibung |
| --- | --- |
| **Kennwort zum Öffnen des Dokuments festlegen** | Klicken Sie auf , um ein sicheres Kennwort hinzuzufügen, um Ihre PDF-Datei anzuzeigen. Geben Sie ein Kennwort im **Benutzerkennwort** -Feld. Die PDF kann nur durch Eingabe des in diesem Feld angegebenen Kennworts geöffnet werden. |
| **Dokumenteinschränkungen festlegen** | Wählen Sie diese Option aus, um die Interaktion der Benutzer mit Ihrer PDF zu beschränken. Geben Sie ein Kennwort im **Passwort des Eigentümers** für die folgenden Einschränkungseinstellungen verwenden.  <br><ul><li> **Drucken** Wählen Sie diese Option aus, damit ein Benutzer die PDF drucken kann. <br> <li> **EntwurfDrucken von Qualitätsdruckverfahren** Wählen Sie diese Option aus, damit ein Benutzer die PDF in einer niedrigeren Auflösung drucken kann.  <br> <li> **Inhaltskopie** Aktivieren Sie diese Option, damit Benutzer Inhalte von der PDF kopieren können.   <br> <li> **Anmerkungen** Wählen Sie diese Option aus, damit Benutzer Notizen oder Kommentare zum PDF hinzufügen können.  <br> <li> **Inhaltsänderungen** Wählen Sie diese Option aus, damit Benutzer den Inhalt im PDF ändern können.  <br> <li> **Inhaltskopierung für Barrierefreiheit** Wählen Sie diese Option aus, damit Bildschirmlesehilfen Inhalte im PDF lesen und navigieren können.  <br>  **Dokumentzusammenstellung** Wählen Sie diese Option aus, damit Benutzer Seiten in die PDF einfügen können.  <br> **Hinweis**: Die Benutzer müssen das Passwort des Eigentümers eingeben, um die Einschränkungen unter Datei > Eigenschaften in Adobe Acrobat zu ändern. |

**Erweitert**

Verwenden Sie die folgenden Optionen, um erweiterte Einstellungen zum Zusammenführen von PDF festzulegen, Komprimierung, Kompatibilitätsstandard usw. zu verwenden.

| Einstellung | Beschreibung |
| --- | --- |
| **Zugreifbare (getaggte) PDF erstellen** | Wählen Sie diese Option aus, um eine PDF mit Tags zu generieren. Eine getaggte PDF erleichtert Sprachausgaben das Lesen und Navigieren von Inhalten, Hyperlinks, Lesezeichen usw. Wenn beispielsweise eine Tabelle mit Tags versehen ist, weiß die Bildschirmlesehilfe, dass sie die Tabelle liest und nicht nur Zeilen und Text. |
| **Im Inhaltsverzeichnis enthaltene PDF zusammenführen** | Wählen Sie diese Option, um vorhandene PDF in Ihrer Ausgabe zusammenzuführen, indem Sie sie Ihrer DITA-Map als Ressourcendatei hinzufügen. Die PDF werden an der Stelle eingefügt, die in der Karte dargestellt wird, und die Seiten werden entsprechend inkrementiert. |
| **Einbetten verwendeter Schriftarten** | Aktivieren Sie diese Option bei der Verwendung von Schriftarten, die möglicherweise nicht auf dem Computer des Endbenutzers installiert sind. Wenn diese Option aktiviert ist, werden die verwendeten Schriftarten in die PDF eingebettet, sodass der Benutzer die PDF wie gewünscht sehen kann, selbst wenn die Schriftarten nicht auf seinem Computer installiert sind. <br> **Hinweis**: Eine Schrift kann nur eingebettet werden, wenn sie eine Einstellung des Schriftartenherstellers enthält, die die Einbettung ermöglicht. Stellen Sie sicher, dass Sie über die erforderliche Einstellung oder Lizenz verfügen, bevor Sie eine Schriftart einbetten. |
| **Automatische Silbentrennung verwenden** | Wenn die automatische Silbentrennung aktiviert ist, werden die Wörter am Zeilenende mit einem Bindestrich an grammatisch korrekten Stellen umbrochen. |
| **JavaScript aktivieren** | Aktivieren Sie diese Option, wenn Sie über einen JavaScript-Code verfügen, den Sie verwenden möchten, um Ihren Inhalt dynamisch umzuwandeln, bevor Sie eine PDF generieren. |
| **Multimedia-Dateien einbetten** | Wählen Sie diese Option aus, um Audio, Video und interaktive Inhalte in die PDF aufzunehmen. |
| **Verwenden Sie die vollständige Komprimierung, um die PDF-Größe zu optimieren.** | Wählen Sie diese Option aus, wenn Sie die Größe einer großen PDF komprimieren/verringern möchten. Beachten Sie, dass das Komprimieren des PDF die Dateiqualität beeinträchtigen kann. |
| **Verwenden Sie die Bildkomprimierung, um die PDF-Größe zu optimieren.** | Wählen Sie diese Option aus, wenn Sie die Größe der verwendeten Bilder in Ihrer PDF komprimieren/reduzieren möchten. Beachten Sie, dass das Komprimieren eines Bildes die Bildqualität beeinträchtigen kann. |
| **Verwenden Sie die benutzerdefinierte Auflösung (Pixel pro Zoll).** | Dies ist die Seitenanzeigeauflösung in Pixel pro Zoll. Geben Sie einen bevorzugten Wert in das Feld ein, das bei Auswahl dieser Option angezeigt wird. Der Standardwert ist 96 Pixel pro Zoll. Legen Sie einen höheren Wert fest, um mehr Inhalt in Zoll einzupassen, und umgekehrt, wenn Sie einen niedrigeren Wert festlegen. |
| **Wasserzeichen anzeigen** | Wählen Sie diese Option, um die in Ihrem Inhalt vorhandenen MathML-Gleichungen zu rendern. Andernfalls werden die Gleichungen ignoriert. |
| **Aktivieren von MathML-Gleichungen** | Wählen Sie diese Option, um die in Ihrem Inhalt vorhandenen MathML-Gleichungen zu rendern. Die Gleichungen werden standardmäßig ignoriert. |
| **PDF-Konformität** | Dies ist der Standard, den Sie speichern möchten, um sicherzustellen, dass Ihre PDF konform ist. Wählen Sie aus der Dropdown-Liste aus, um aus der Liste der verfügbaren PDF-Standards auszuwählen. Weitere Informationen zu den unterstützten Standards finden Sie unter [Über PDF-Standards](https://helpx.adobe.com/acrobat/using/pdf-conversion-settings.html#about_pdf_x_pdf_e_and_pdf_a_standards). |
| **Herunterladen temporärer Dateien** | Wählen Sie diese Option aus, wenn Sie die Zwischendatei-HTML herunterladen möchten, die beim Generieren der nativen PDF-Ausgabe erstellt wurde. Sie können die temporären Dateien später herunterladen, nachdem Sie die Ausgabe generiert haben. |

## Generieren einer PDF-Ausgabe {#generate-pdf-output}

Nachdem Sie die Ausgabevorgabe konfiguriert haben, können Sie die Ausgabe im Bereich &quot;Vorgaben&quot;mithilfe der **Vorgabe generieren** Funktion.

1. Unter dem **Autor** auswählen, wählen Sie die **Repository** Ansicht.\
   Dadurch wird das Repository-Bedienfeld geöffnet.

1. Öffnen Sie im Bereich &quot;Repository&quot;die DITA-Map-Datei in **Kartenansicht**.

1. Im **Ausgabe** Registerkarte, klicken Sie auf **Vorgaben** , um das Bedienfeld &quot;Voreingestellt&quot;anzuzeigen.
Informationen zum Erstellen oder Konfigurieren einer Ausgabevorgabe finden Sie unter [Erstellen einer PDF-Ausgabevorgabe](#create-output-preset).
1. Um Ihre Einstellungen zu speichern, klicken Sie auf das **Alle speichern** ![Alle speichern](assets/SaveFloppy_icon.svg) in der oberen linken Ecke der Standardsymbolleiste in der Ausgabeansicht.
1. Klicken Sie auf **Vorgabe generieren** ![Vorgabe generieren](assets/generate-output.svg) in der oberen Leiste angezeigt.
Sie können eine Fortschrittsleiste neben der ausgewählten Ausgabevorgabe im Bedienfeld Ausgabevorgaben anzeigen.
1. Sobald die Generierung der Ausgabe abgeschlossen ist, klicken Sie auf  **Ausgabe anzeigen** ![Anzeige der Ausgabe](assets/view-output.svg) in der oberen Leiste, um die Ausgabe anzuzeigen.\
   A **Erfolg** wird in der rechten unteren Ecke des Bildschirms angezeigt.
Wenn eine Ausgabe nicht erfolgreich ist, wird die folgende Fehlermeldung angezeigt.
<img src="assets/error-log.png" alt="Fehlerprotokoll" width="250">

Um das Fehlerprotokoll anzuzeigen, klicken Sie auf **Verwerfen**, bewegen Sie den Mauszeiger über die ausgewählte Vorgabe-Registerkarte und klicken Sie auf ![options](assets/options.svg) **Optionen** > **Protokoll anzeigen**.

### Laden Sie temporäre Dateien nach der Generierung der nativen PDF-Ausgabe herunter

Wenn Sie die **Herunterladen temporärer Dateien** in den erweiterten Einstellungen können Sie auch die Zwischendatei-HTML herunterladen, die beim Generieren der nativen PDF-Ausgabe erstellt wurde. Nachdem Sie die Ausgabe generiert haben, können Sie die temporären Dateien mit der **Herunterladen temporärer Dateien** ![Temporäre Dateien herunterladen](assets/native-pdf-download-temporary-files-icon.svg)in der oberen Leiste angezeigt. Diese Funktion hilft Ihnen beim Anzeigen Ihrer vorläufigen HTML-Stile und Layouts und hilft Ihnen, Ihre CSS-Stile gemäß Ihren Anforderungen zu korrigieren oder zu ändern.


>[!NOTE]
>
> Die **Herunterladen temporärer Dateien**  ![Temporäre Dateien herunterladen](assets/native-pdf-download-temporary-files-icon.svg) Das Symbol erscheint nur, wenn Sie die letzte PDF-Ausgabe mithilfe der Vorgabe generiert haben, wobei Sie die Option im **Erweitert** Registerkarte.
