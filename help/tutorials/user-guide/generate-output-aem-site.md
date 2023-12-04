---
title: AEM Site
description: Erstellen und konfigurieren Sie AEM in AEM Handbüchern. Verwenden Sie AEM Site-Unterstützung, um eine artikelbasierte Ausgabe zu generieren, Themen zur Ausgabenverknüpfung zu erstellen, Conref zu veröffentlichen und eine Zeichenfolge innerhalb des Inhalts zu suchen.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '2570'
ht-degree: 0%

---

# AEM Site {#id205BE3008SW}

Die folgenden Optionen sind für die Ausgabe der AEM Site verfügbar:

Sie können die Vorgabe für die AEM Website auf zwei Arten erstellen:

**Im Web-Editor:** Öffnen Sie im Bereich &quot;Repository&quot;die DITA-Zuordnungsdatei in der Zuordnungsansicht, wählen Sie dann auf der Registerkarte &quot;Ausgabe&quot;das Symbol + aus, um eine Ausgabevorgabe zu erstellen, und wählen Sie dann AEM Site aus der Dropdown-Liste Typ im Dialogfeld Vorgabe hinzufügen aus. Im Web-Editor wurden die Konfigurationen auf den Registerkarten Allgemein und Erweitert organisiert:

**Allgemein**

Die **Allgemein** tab enthält die folgenden Konfigurationen:

- Site-Name
- Ausgabepfad
- Vorhandene Ausgabeseiten
- Löschen von verwaisten Site-Seiten
- Bedingungen anwenden mit \(Wenn die Bedingungen für eine Zuordnung definiert sind\)
- Grundlinie verwenden \(Wenn eine Grundlinie für eine Zuordnung erstellt wird\)
- Arbeitsablauf nach der Erstellung

**Erweitert**

Die Registerkarte Erweitert enthält die folgenden Konfigurationen:

- Temporäre DITA-OT-Dateien bereinigen
- Separate PDF für jedes Thema generieren
- Verwenden von Zuordnungseigenschaften als Standard

Weitere Informationen finden Sie unter [AEM Site-Konfiguration](#id231KIM004X1).

**Über das Zuordnungs-Dashboard**

Um Ausgabevorgaben für AEM Site zu öffnen, klicken Sie in der Assets-Benutzeroberfläche auf eine DITA-Zuordnungsdatei, klicken Sie auf Ausgabevorgaben und dann auf die Ausgabeoption AEM Site . Klicken Sie im Zuordnungs-Dashboard auf **Bearbeiten** Klicken Sie oben auf , um die verschiedenen Konfigurationen zu aktualisieren, und klicken Sie dann auf **Speichern**.

>[!TIP]
>
> Siehe *AEM Site-Veröffentlichung* im Handbuch Best Practices für Best Practices zur Erstellung AEM Site-Ausgabe.

## AEM Site-Konfiguration {#id_aem_site_config}

Die folgenden Optionen sind für die Ausgabe der AEM Site verfügbar:

| AEM Site-Optionen | Beschreibung |
| --- | --- |
| Ausgabetyp | Der Typ der Ausgabe, die Sie generieren möchten. Wählen Sie die Option Website AEM , um eine responsive AEM-Site-Ausgabe zu generieren. |
| Einstellungsname | Geben Sie einen beschreibenden Namen für die AEM Site-Einstellungen ein, die Sie erstellen. Sie können beispielsweise *Interne Kundenausgabe* oder *Ausgabe der Endbenutzer*. |
| Site-Name | Ein Site-Name, in dem die Ausgabe in Ihrem AEM-Repository gespeichert wird.<br><br>Ein Knoten im AEM Repository wird mit dem hier angegebenen Namen erstellt. Wenn Sie den Site-Namen nicht angeben, wird der Site-Knoten mit dem DITA-Map-Dateinamen erstellt.<br><br>Der hier angegebene Site-Name wird auch als Titel auf der Registerkarte &quot;Browser&quot;verwendet.<br><br>Sie können auch Variablen beim Festlegen des Site-Namens verwenden. Weitere Informationen zur Verwendung von Variablen finden Sie unter [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](generate-output-use-variables.md#id18BUG70K05Z). |
| Design | Wählen Sie die Designvorlage aus, die Sie zum Generieren der Ausgabe verwenden möchten.<br><br>Weitere Informationen zur Verwendung von benutzerdefinierten Designvorlagen zum Generieren von Ausgaben erhalten Sie von Ihrem Publishing-Administrator. |
| Zielpfad | Der Pfad in Ihrem AEM-Repository, in dem die Ausgabe gespeichert wird. Beim Generieren der endgültigen Ausgabe werden der Site-Name und der Zielpfad kombiniert. Wenn Sie beispielsweise den Site-Namen als `user-guide` und der Zielpfad als `/content/output/aem-guides`, wird die endgültige Ausgabe unter der `/content/output/aem-guides/user-guide` Knoten.<br><br>Sie können auch Variablen beim Festlegen des Zielpfads verwenden. Weitere Informationen zur Verwendung von Variablen finden Sie unter [Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;](generate-output-use-variables.md#id18BUG70K05Z). |
| Bedingungen anwenden mithilfe von | Wählen Sie eine der folgenden Optionen aus:<br><br>**Keine angewendet**: Wählen Sie diese Option, wenn Sie keine Bedingung auf die veröffentlichte Ausgabe anwenden möchten.<br>**DITAVal-Datei**: Wählen Sie DITAVal-Dateien aus, um konditionalisierten Inhalt zu generieren. Sie können mehrere DITAVal-Dateien über das Dialogfeld &quot;Durchsuchen&quot;oder durch Eingabe des Dateipfads auswählen. Verwenden Sie das Kreuzsymbol neben dem Dateinamen, um ihn zu entfernen. DITAVal-Dateien werden in der angegebenen Reihenfolge ausgewertet, sodass die in der ersten Datei angegebenen Bedingungen Vorrang vor den in späteren Dateien angegebenen Bedingungen haben. Sie können die Dateireihenfolge beibehalten, indem Sie Dateien hinzufügen oder löschen. Wenn die DITAVal-Datei an einen anderen Speicherort verschoben oder gelöscht wird, wird sie nicht automatisch aus dem Mapping-Dashboard gelöscht. Sie müssen den Speicherort aktualisieren, falls Dateien verschoben oder gelöscht werden. Sie können den Mauszeiger über den Dateinamen bewegen, um den Pfad im AEM Repository anzuzeigen, in dem die Datei gespeichert ist. Sie können nur DITAVal-Dateien auswählen. Ein Fehler wird angezeigt, wenn Sie einen anderen Dateityp auswählen.<br>**Bedingungsvoreinstellung**: Wählen Sie eine Bedingungsvorgabe aus der Dropdown-Liste aus, um beim Veröffentlichen der Ausgabe eine Bedingung anzuwenden. Diese Option ist sichtbar, wenn Sie eine Bedingung für die DITA-Map-Datei hinzugefügt haben. Die bedingten Einstellungen sind auf der Registerkarte Bedingungsvorgaben der DITA-Zuordnungskonsole verfügbar. Weitere Informationen zur Bedingungsvorgabe finden Sie unter [Verwenden von Bedingungsvorgaben](generate-output-use-condition-presets.md#id1825FL004PN). |
| Vorhandene Ausgabeseiten | Wählen Sie die **Inhalt überschreiben** Option zum Überschreiben von Inhalten auf den vorhandenen Seiten. Diese Option überschreibt nur Inhalte, die unter den Inhalts- und Kopfknoten der Seite vorhanden sind. Diese Option ermöglicht die gemischte Veröffentlichung von Inhalten. Wenn Sie diese Option auswählen, können Sie das Löschen verwaister Seiten aus der veröffentlichten Ausgabe auswählen. Dies ist auch die *default* zur Erstellung der AEM Site-Ausgabe.<br><br>Wählen Sie die **Löschen und Erstellen** -Option zum erzwingen des Löschens vorhandener Seiten während der Veröffentlichung. Mit dieser Option wird der Seitenknoten zusammen mit seinem Inhalt und allen untergeordneten Seiten darunter gelöscht. Verwenden Sie diese Option, wenn Sie die Designvorlage Ihrer Ausgabevorgabe geändert haben oder möchten, dass alle zusätzlichen Seiten, die bereits im Ziel vorhanden sind, entfernt werden. |
| Löschen von verwaisten Site-Seiten | Auswählen der **Inhalt überschreiben** im **Vorhandene Ausgabeseiten** Diese Option wird angezeigt. Wenn Sie diese Option auswählen, werden alle verwaisten Seiten von der veröffentlichten AEM Site gelöscht. Damit diese Funktion erfolgreich ausgeführt werden kann, müssen Sie die gesamte DITA-Zuordnung veröffentlichen und nicht die inkrementelle Veröffentlichung verwenden.<br><br>Angenommen, Sie haben eine DITA-Karte veröffentlicht, die die Themen a.dita, b.dita und c.dita enthält. Bevor Sie die Zuordnung erneut veröffentlichen, haben Sie das Thema b.dita aus der Zuordnung entfernt. Wenn Sie jetzt diese Option ausgewählt haben, werden alle Inhalte, die sich auf b.dita beziehen, aus der AEM Site-Ausgabe entfernt und nur a.dita und c.dita werden veröffentlicht.<br><br>Mit dieser Funktion werden keine veröffentlichten untergeordneten Zuordnungen entfernt. Wenn Ihre übergeordnete Zuordnung beispielsweise eine untergeordnete Zuordnung enthält und Sie die gesamte untergeordnete Zuordnung entfernen, wird der Inhalt der untergeordneten Zuordnung nicht aus der veröffentlichten Ausgabe gelöscht. Wenn Sie jedoch ein Thema aus einer untergeordneten Zuordnung entfernen und erneut veröffentlichen, wird der Inhalt des entfernten Themas aus der Site-Ausgabe gelöscht.<br><br>Wenn referenzierter Inhalt vorhanden ist und dieser Inhalt vor der erneuten Veröffentlichung entfernt wird, werden die Daten des referenzierten Inhalts nicht entfernt.<br><br>**Hinweis**: Informationen zu gelöschten verwaisten Seiten werden ebenfalls in den Ausgabegenerierungslogs erfasst. Weitere Informationen zum Zugriff auf die Protokolldateien finden Sie unter [Protokolldatei anzeigen und überprüfen](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). |
| Temporäre DITA-OT-Dateien bereinigen | Wählen Sie diese Option, um die von DITA-OT generierten temporären Dateien zu bereinigen. Der Speicherort, an dem DITA-OT temporäre Dateien speichert, finden Sie im Ausgabegenerierungsprotokoll.<br><br>Wenn beim Generieren der Ausgabe über DITA-OT Fehler auftreten, können Sie diese Option deaktivieren, um die temporären Dateien beizubehalten. Anschließend können Sie diese Dateien zur Fehlerbehebung bei Fehlern bei der Ausgabe-Generierung verwenden. |
| Separate PDF für jedes Thema generieren | Wenn diese Option aktiviert ist, wird auch für jedes Thema in der DITA-Map eine PDF erstellt. Wenn Sie diese Option wählen, wird eine neue Option PDF-Pfad teilen angezeigt.<br><br>Geben Sie im Feld PDF-Pfad teilen den Pfad an, unter dem die für jedes Thema generierten PDF gespeichert werden sollen.<br><br>**Hinweis**: AEM Guides verwenden das DITA-OT-Plug-in namens pdfx , um PDF für jedes Thema zu generieren. Dieses Plug-in ist mit dem standardmäßig bereitgestellten DITA-OT-Paket integriert. Sie können dieses Plug-in anpassen, um PDF gemäß Ihren Anforderungen zu generieren. Wenn Sie ein benutzerdefiniertes DITA-OT-Plug-in verwenden, stellen Sie sicher, dass Sie das pdfx-Plug-in integrieren, um die PDF-Generierungsfunktion auf Themenebene zu nutzen. |
| Workflow &quot;Nach der Erstellung ausführen&quot; | Wenn Sie diese Option wählen, wird eine neue Dropdownliste mit dem Workflow nach der Generierung angezeigt, die alle in AEM konfigurierten Workflows enthält. Sie müssen einen Workflow auswählen, der nach Abschluss des Workflows zur Generierung der Ausgabe ausgeführt werden soll. |
| Grundlinie verwenden | Wenn Sie eine Grundlinie für die ausgewählte DITA-Zuordnung erstellt haben, wählen Sie diese Option, um die Version anzugeben, die Sie veröffentlichen möchten.<br><br>**Wichtig**: Wenn Sie eine inkrementelle Ausgabe für die AEM Site generieren, wird die Ausgabe mit der aktuellen Version der Dateien und nicht mit der angehängten Grundlinie erstellt.<br><br>Siehe [Arbeiten mit Grundlinien](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) für weitere Details. |
| Eigenschaften | Wählen Sie die Eigenschaften aus, die Sie als Metadaten verarbeiten möchten. Diese Eigenschaften werden auf der Seite &quot;Eigenschaften&quot;der DITA-Map- oder Bookmap-Datei festgelegt. Die Eigenschaften, die Sie aus der Dropdown-Liste auswählen, werden unter dem Feld Eigenschaften aufgelistet und aus der Dropdown-Liste entfernt.<br><br>**Hinweis**: Bei den Metadateneigenschaften wird zwischen Groß- und Kleinschreibung unterschieden.<br><br>*Wenn Sie eine Grundlinie ausgewählt haben, basieren die Werte für die Eigenschaften auf der Version der ausgewählten Grundlinie.<br>* Wenn Sie keine Grundlinie ausgewählt haben, basieren die Werte für die Eigenschaften auf der neuesten Version.<br><br>Sie können die Metadaten auch mithilfe der DITA-OT-Veröffentlichung an die Ausgabe übergeben. Weitere Informationen finden Sie unter [Übergeben der Metadaten an die Ausgabe mithilfe von DITA-OT](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Hinweis**: Wenn Sie die Variable `cq:tags` in der Option Eigenschaften und dann die Werte für `cq:tags` werden aus der aktuellen Arbeitskopie ausgewählt, selbst wenn Sie eine Grundlinie für die Veröffentlichung ausgewählt haben. |
| Verwenden Sie die Zuordnungseigenschaften, wenn das Thema fehlt. | Wenn diese Option aktiviert ist, werden die für die Zuordnungsdatei definierten Eigenschaften auch in die Themen kopiert, in denen solche Eigenschaften nicht definiert sind. Beachten Sie bei Verwendung dieser Option die folgenden Punkte:<br><br>*Es können nur Eigenschaften vom Typ Zeichenfolge, Datum oder Lang (einzelne und mehrere Werte) an die Seiten der AEM übergeben werden.<br>* Metadatenwerte für eine String-Typ-Eigenschaft unterstützen keine Sonderzeichen (z. B. `@, #, " "`).<br>* Diese Option sollte zusammen mit der `Properties` -Option. |

## Zusätzlicher Hinweis auf AEM Site

### Artikelbasierte Ausgabe aus dem Web-Editor generieren

Sie können die AEM Site-Ausgabe für ein oder mehrere Themen oder die gesamte DITA-Zuordnung aus dem Web Editor generieren. Sie müssen Ausgabevorgaben für Ihre DITA-Zuordnung erstellen und können dann einfach die AEM Site-Ausgabe für Ihre Karte generieren. Wenn Sie einige Themen in Ihrer Zuordnung aktualisiert haben, können Sie auch die AEM Site-Ausgabe nur für diese Themen aus dem Web Editor generieren. Weitere Informationen finden Sie unter [Artikelbasierte Veröffentlichung im Web Editor](web-editor-article-publishing.md#id218CK0U019I).

### Generieren von Themen für die Ausgabenverknüpfung aus anderen Maps

Es ist ein sehr häufiges Szenario, dass eine große Menge von Dokumentation über mehrere Ordner und DITA-Maps verteilt ist. Es wird äußerst komplex, Inhalte zu veröffentlichen, die von verschiedenen Orten aus verknüpft sind. Standardmäßig sind alle Links `<xref>` werden mit dem `local` `@scope`. Das Veröffentlichen solcher Themen stellt keine Herausforderung dar, da es einen direkten Link zum Thema verwendet. Wenn das Thema außerhalb der aktuellen DITA-Zuordnung liegt, zeigt der Link den verknüpften Inhalt nicht an.

Eine andere Möglichkeit, Inhalte zu verknüpfen, besteht darin, einen Link mithilfe der `peer` `@scope`. Für solche Inhalte wird der Link zur Laufzeit aufgelöst, indem der konfigurierte Kontext für das verknüpfte Thema aus dem Veröffentlichungskontext der DITA-Map ausgewählt wird. Der folgende Screenshot zeigt den Bereich &quot;Eigenschaften&quot;für einen Link mit der `peer` `@scope`:

![](images/peer-link-scope-link.png){width="800" align="left"}

Um die Veröffentlichung komplexer Karten und Themen zu vereinfachen, die mit anderen Themen in anderen Maps verknüpft sind, können Sie in AEM Handbüchern den Veröffentlichungskontext für jede Ausgabevorgabe festlegen.

Im Veröffentlichungskontext können Sie festlegen, welches Thema für die Veröffentlichung einer bestimmten Ausgabe verwendet werden soll. Nehmen wir an, Sie haben vier Ordner: Beispiel a, Beispiel b, Beispiel c und Beispiel d. Jeder Ordner enthält eine DITA-Zuordnung - DITA-Zuordnung A, DITA-Zuordnung B, DITA-Zuordnung C und DITA-Zuordnung D. Die Querzuordnungsverknüpfung erfolgt, wenn ein Thema in DITA Map A auf ein Thema in DITA Map B, C oder D verlinkt. Im folgenden Screenshot enthält ein Beispielkonzept-Thema Verknüpfungen \(oder Verweise\) zu Dateien, die Teil anderer DITA-Maps sind.

![](images/sample-concept-link-to-other.png){width="350" align="left"}

Wenn Sie jetzt die Veröffentlichungseinstellungen der AEM Site für die Zuordnungsdatei konfigurieren, die dieses Thema enthält, können Sie auswählen, welcher Veröffentlichungskontext für den verknüpften Inhalt beim Veröffentlichen verwendet wird. Ein Veröffentlichungskontext ist eine Kombination aus DITA Map und der zugehörigen Ausgabevorgabe. Die Ausgabevorgabe wiederum enthält eine bestimmte Version des Inhalts und bedingte Vorgaben. Diese gesamte Kombination aus DITA-Zuordnung, Ausgabevorgabe, \(Dateien\) Version und Bedingungen definiert den Veröffentlichungskontext für eine verknüpfte Zuordnung.

Führen Sie die folgenden Schritte aus, um den Veröffentlichungskontext für verknüpfte Dateien anzugeben:

1. Öffnen Sie die **Ausgabevorgaben** der DITA-Map, die Sie veröffentlichen möchten.

1. Wählen Sie die **AEM Site** Ausgabevorgabe.

   Sie erhalten die Registerkarten Einstellungen für AEM Vorgaben und Veröffentlichungskontext .

   ![](images/aem-site-publish-settings.png){width="800" align="left"}

1. Öffnen Sie die **Veröffentlichungskontext** Registerkarte.

   Ihnen wird eine Liste der abhängigen Themen angezeigt. Dies sind die Themen, die von einem Thema in der aktuellen Karte verknüpft sind, aber in einigen anderen DITA-Maps verfügbar sind.

   >[!NOTE]
   >
   > Auf der Registerkarte Veröffentlichungskontext werden Themen angezeigt, die mithilfe des `peer` `@scope` nur. Für Links mit `local` `@scope`, müssen Sie den Veröffentlichungskontext nicht angeben.

   Standardmäßig sind bei allen verknüpften Themen die aktuellen Ausgabevorgaben und Zuordnungen ausgewählt.

   ![](images/default-publish-context.png){width="800" align="left"}

1. Um die Standardauswahl der DITA-Zuordnung und -Vorgabe zu ändern, klicken Sie auf **Bearbeiten** \(in der Hauptsymbolleiste\).

1. Wenn Sie die zuletzt veröffentlichte Ausgabe jeder abhängigen Datei in der Zuordnung verwenden möchten, wählen Sie **Verwenden des zuletzt generierten Veröffentlichungskontexts für alle abhängigen Themen**.

1. Im **Übergeordnete Zuordnung** in der Dropdown-Liste die Map-Datei auswählen, mit deren Ausgabe Sie die aktuelle Map-Ausgabe verknüpfen möchten.

   Bei der Auswahl einer Zuordnungsdatei wird die UUID der Zuordnung in der Spalte &quot;Übergeordnete Map-UUID&quot;angezeigt. Die mit der ausgewählten Zuordnung verknüpften Ausgabevorgaben werden in der Liste &quot;Voreinstellungen&quot;der übergeordneten Zuordnung aufgeführt.

1. Im **Vorgabe der übergeordneten Zuordnung** in der Dropdown-Liste die Ausgabevorgabe auswählen, mit der Sie die Ausgabe der aktuellen Karte verknüpfen möchten.

1. Wählen Sie die erforderliche Zuordnung und die Ausgabevorgabe für alle abhängigen Themen aus und klicken Sie auf **Fertig**.

   Der Kontext für die abhängigen Themen ist jetzt festgelegt. Sie können die Ausgabe für die aktuelle Zuordnung generieren. Weitere Informationen zum Generieren der Ausgabe finden Sie unter [Generieren der Ausgabe für eine DITA-Zuordnung über die Zuordnungskonsole](generate-output-for-a-dita-map.md#).

### Überblendung Veröffentlichung

AEM-Handbücher unterstützen die Veröffentlichung von DITA-Inhalten innerhalb Ihrer bestehenden AEM Site. Wenn Sie beispielsweise über eine vorhandene Site verfügen, können Sie die Ausgabe der AEM Site verwenden, um nur den DITA-Inhalt auf dieser Site zu veröffentlichen. In diesem Prozess wird der vorhandene Nicht-DITA-Inhalt durch den Veröffentlichungsprozess nicht geändert. Weitere Informationen zum Einrichten Ihrer Site für die Veröffentlichung von DITA-Inhalten finden Sie bei Ihrem Publishing-Administrator.

### Veröffentlichung `conref`

Wenn Sie `conref` in Ihrem Inhalt veröffentlicht wird, wird er als normaler oder eingebetteter Inhalt zusammen mit dem Inhalt im Quellthema \(oder Referrer\) veröffentlicht. Die `conref` Inhalt wird zusammen mit dem Hauptinhalt gerendert und es wird keine separate Site-Seite für denselben erstellt. Wenn Sie nach dem Inhalt suchen, auf den im `conref`, dann nur das Hauptthema oder die Seite, die die `conref` Inhalte werden in den Suchergebnissen angezeigt.

>[!NOTE]
>
>Wenn Sie separate Seiten für die `conref` Inhalte mit AEM Guides-Version 3.5 oder früher verwenden, wird empfohlen, diese Seiten mithilfe der [Löschen von verwaisten Site-Seiten](#delete-orphan-page-aem-site) -Option.


### Suchen einer Zeichenfolge im Inhalt

Sie können in der Ausgabe der AEM Site nach einer Zeichenfolge suchen. Standardmäßig können Sie nur in den Titeln nach der Zeichenfolge suchen. Wenden Sie sich an Ihren Systemadministrator, um die Eigenschaft flattening.enabled zu aktivieren, um im Inhalt oder im Hauptteil der AEM-Site nach der Zeichenfolge zu suchen.

![AEM Site-Ausgabe durchsuchen](images/aem-output-search.png){width="650" align="left"}

Weitere Informationen finden Sie unter *Reduzieren AEM Site-Knotenstruktur konfigurieren* im Handbuch &quot;Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern&quot;.

**Übergeordnetes Thema:**[ Grundlegendes zu den Ausgabevorgaben](generate-output-understand-presets.md)
