---
title: Arbeiten mit dem erweiterten Map-Editor
description: Erfahren Sie, wie Sie mit dem erweiterten Map-Editor in AEM Guides arbeiten. Machen Sie sich mit den Funktionen des erweiterten Map-Editors vertraut. Bearbeiten Sie Themen über eine DITA-Zuordnung und verwenden Sie die Layoutansicht, die Autorenansicht und den Vorschaumodus.
exl-id: e58e3705-2c3b-48cc-b2c8-2596e9751c85
source-git-commit: e8a912b0f8bc690fceade0b54bb36057a727ab33
workflow-type: tm+mt
source-wordcount: '3707'
ht-degree: 0%

---

# Arbeiten mit dem erweiterten Map-Editor {#id1942D0S0IHS}

Der erweiterte Map-Editor verfügt über eine intuitive Benutzeroberfläche und ähnelt dem Web-Editor. Wenn Sie eine Zuordnungsdatei im Web-Editor öffnen, erhalten Sie eine Option, die Zuordnungsdatei mithilfe der Benutzeroberfläche des erweiterten Map-Editors zu bearbeiten. Der erweiterte Map-Editor ermöglicht das Hinzufügen von Themenverweisen, Schlüsselverweisen, die Strukturierung Ihres Inhalts und mehr.

Neben der direkten Bearbeitung von Zuordnungsdateien im Web-Editor können Sie auch Themendateien in einer Zuordnung zur Bearbeitung des Web-Editors öffnen. Dieses Thema führt Sie durch die Funktionen im erweiterten Map-Editor und wie Sie Dateien in einer DITA-Map im Web Editor öffnen und bearbeiten können.

## Hinzufügen von Themen zu einer Map-Datei

Führen Sie die folgenden Schritte aus, um Ihre Zuordnungsdatei mit dem erweiterten Zuordnungseditor zu erstellen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur Zuordnungsdatei, die Sie bearbeiten möchten.

   >[!NOTE]
   >
   > Vergewissern Sie sich, dass Sie den Asset-Auswahlmodus nicht aktiviert haben.

1. Um eine exklusive Sperre für die Zuordnungsdatei zu erhalten, wählen Sie die Zuordnungsdatei aus und klicken Sie auf **Auschecken**.

   >[!NOTE]
   >
   > Sobald Sie eine exklusive Sperre für eine Map-Datei haben, können andere Benutzer die Karte nicht mehr bearbeiten. Sie können jedoch an den Themen in der Map-Datei arbeiten. Wenn Ihr Administrator Ihren Web Editor so konfiguriert hat, dass Dateien vor der Bearbeitung ausgecheckt werden, können Sie eine Datei erst bearbeiten, wenn Sie sie auschecken. Ebenso werden Sie bei entsprechender Konfiguration aufgefordert, alle ausgecheckten Dateien einzuchecken, bevor Sie sie schließen

1. Klicken Sie bei ausgewählter Zuordnungsdatei auf **Themen bearbeiten**.

   ![](images/edit-map-main-menu.png){width="800" align="left"}

   Sie können auch die **Themen bearbeiten** Option im Aktionsmenü der Zuordnungsdatei:

   ![](images/edit-map-action-menu.png){width="800" align="left"}

   Die Zuordnungsdatei wird im Web Editor zur Bearbeitung geöffnet.

1. Klicken Sie auf das Symbol **Bearbeiten**.

   ![](images/edit-map-icon.png){width="550" align="left"}

   Die Karte wird in der Benutzeroberfläche des erweiterten Map-Editors geöffnet. Wenn Sie eine neue Zuordnungsdatei geöffnet haben, wird nur der Titel der Zuordnung im Editor angezeigt.

   ![](images/new-map-file-in-editor.png){width="800" align="left"}

   - **A** - \(*Hauptleiste*\): Dies ähnelt der Hauptsymbolleiste des Web-Editors. Siehe [Hauptleiste](web-editor-features.md#id2051EA0G05Z) im Web Editor für weitere Informationen.

   - **B** - \(*Sekundäre Symbolleiste*\) Dies ist die Sekundäre Symbolleiste, mit der Sie mit Zuordnungsdateien arbeiten können. Weitere Informationen zu den über die Sekundäre Symbolleiste verfügbaren Funktionen finden Sie unter [In der Symbolleiste des Erweiterten Map-Editors verfügbare Funktionen](#id205DEC0005Z).

   - **C** - \(*Zuordnungsansichten*\): Ermöglicht es Ihnen, den Map Editor zwischen Layout, Autor, Quelle und Vorschau zu wechseln. Die **Layout**-Ansicht ermöglicht es Ihnen, die Themen in einer DITA-Zuordnung zu organisieren. Dadurch erhält der Baum oder die hierarchische Ansicht der Karte. Die **Autor** -Ansicht können Sie die Themen im Map-Editor bearbeiten. Dies gibt auch die WYSIWYG-Ansicht der Map-Datei. Die **Quelle** -Ansicht können Sie mit der zugrunde liegenden XML der Map-Datei arbeiten. Die Vorschau bietet eine konsolidierte Ansicht aller Themen und Unterkarten innerhalb der Zuordnungsdatei. Die **Schließen** -Link schließt die Map-Datei.

   - **D** - \(*Linke Leiste*\): Bietet Zugriff auf das linke Bedienfeld, über das Sie auf die Funktionen Favoriten, Repository, Map, Gliederung und andere Funktionen zugreifen können. Sie können sie erweitern oder reduzieren, indem Sie auf das Symbol &quot;Seitenleiste erweitern&quot;\(![](images/sidebar-expand-icon.svg)\). Weitere Informationen zu den im linken Bereich verfügbaren Funktionen finden Sie unter [Linke Leiste](web-editor-features.md#id2051EA0M0HS) im Web-Editor.

   - **E** - \(*Mittlerer Bereich*\): Inhaltsbearbeitungsbereich zuordnen.

   - **F** - \(*Rechter Bereich*\): Gewährt Zugriff auf den Bereich Eigenschaften . Sie können die Inhaltseigenschaften und die Zuordnungseigenschaften des ausgewählten Themas oder der ausgewählten Zuordnung sehen. Weitere Informationen zu den in diesem Bedienfeld verfügbaren Funktionen finden Sie unter [Rechter Bereich](web-editor-features.md#id2051EB003YK) im Web-Editor.

1. Wechseln Sie in der linken Leiste zum **Repository-Ansicht**.

1. Navigieren Sie im AEM-Repository zu dem Ordner, der die Themen oder Unterkarten enthält, die Sie hinzufügen möchten.

1. Wählen Sie das Thema oder die Zuordnungsdatei im **Repository-Ansicht** und ziehen Sie sie per Drag-and-Drop in den Bearbeitungsbereich für Inhalte der \(mittleren\) Zuordnung.

   Das Thema wird der Karte hinzugefügt.

   ![Map Editor hinzufügen](images/map-editor-add-topic.png){width="800" align="left"}

1. Um nachfolgende Themen oder eine Unterzuordnung hinzuzufügen, ziehen Sie das Thema oder die Unterzuordnung per Drag-and-Drop an die gewünschte Position in der Zuordnung.

   Beachten Sie beim Erstellen Ihrer Zuordnungsdatei die folgenden Punkte:

   - Die Datei wird an einer Stelle hinzugefügt, an der die horizontale Leiste im Kartenbearbeitungsbereich angezeigt wird. Im folgenden Screenshot wird die *Übersicht* Das Thema wird zwischen den *Allgemeine Beschreibung* und *Launch- und Landingpage* Themen.

     ![](images/horizontal-line-in-adv-map-editor.png){width="350" align="left"}

   - Um ein Thema zu ersetzen, platzieren Sie das Thema oben, links oder rechts neben dem Thema, das Sie ersetzen möchten. Eine vertikale Leiste links oder rechts neben einem Thema zeigt an, dass es durch das Thema ersetzt wird, das darauf abgelegt wird.

     ![](images/vertical-bar-left-right.png){width="550" align="left"}

     Bevor Sie ein Thema ersetzen, erhalten Sie jedoch eine Bestätigungsaufforderung. Das Thema wird erst nach der Bestätigung ersetzt.

     ![](images/replace-topic-confirm.png){width="300" align="left"}

   - Wenn Sie Ihrer DITA-Zuordnung eine Unterzuordnung hinzufügen, wird die Unterzuordnung als Link in der DITA-Zuordnung angezeigt. Um alle Themen der Unterzuordnung anzuzeigen, klicken Sie bei gedrückter Strg-Taste auf den Unterzuordnungslink. Der Inhalt der Unterkarte wird in einem neuen Tab angezeigt. Um ein Thema aus der DITA-Zuordnung zu öffnen, klicken Sie bei gedrückter Strg-Taste auf den Themenlink und öffnen Sie es auf der neuen Registerkarte.

   - Sie können die Tastenkombinationen Strg+Z und Strg+Y oder ihre jeweiligen Symbole in der Symbolleiste verwenden, um jede Änderung in der Zuordnung rückgängig zu machen oder wiederherzustellen.

   - Um die Position eines Themas zu ändern, wählen Sie das Thema \(durch Klicken auf das Themensymbol\) aus und ziehen Sie es per Drag-and-Drop an die gewünschte Position in der Map-Datei. Stellen Sie sicher, dass die horizontale Leiste an der Stelle sichtbar ist, an der Sie das Thema platzieren möchten. Im folgenden Screenshot wird das Thema *Launch- und Landingpage* wird nach dem *Übersicht* Thema.

     ![](images/move-topic-adv-map-editor.png){width="350" align="left"}

   - Um die Eigenschaften Ihrer Zuordnungsdatei zu überprüfen, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im Zuordnungsbearbeitungsbereich und wählen Sie **Eigenschaften** aus dem Kontextmenü aus. Basierend auf Ihrer AEM können Sie Eigenschaften wie Metadaten, Aktivierung planen \(de\), Verweise, Dokumentstatus und mehr sehen.

1. Klicken Sie auf **Speichern**.


## In der Symbolleiste des Erweiterten Map-Editors verfügbare Funktionen {#id205DEC0005Z}

Die Symbolleiste im Editor für erweiterte Zuordnungen ähnelt dem Thema Web Editor. Die grundlegenden Vorgänge wie das Umschalten des linken Bedienfelds, das Speichern der Zuordnung, das Erstellen einer neuen Version der Zuordnung, das Rückgängigmachen/Wiederholen des letzten Vorgangs und das Löschen der ausgewählten Elemente sind in beiden Editoren üblich. Weitere Informationen zur Funktionsweise dieser Vorgänge finden Sie unter [Funktionen des Web Editors kennen](web-editor-features.md#) Abschnitt.

Die folgenden zuordnungsspezifischen Vorgänge sind auch in der Symbolleiste in den Layoutansichten und Autorenansichten verfügbar:

## Layoutansicht {#id205DEC0005Z_layout_view}

Wenn Sie eine Karte zur Bearbeitung öffnen, wird die Layoutansicht des Map-Editors geöffnet. In der Layout-Ansicht wird die Zuordnungshierarchie in einer Baumansicht angezeigt, sodass Sie die Themen in einer Zuordnung organisieren können.

>[!NOTE]
>
> In der Ansicht &quot;Layout&quot;werden nur die in einer Zuordnung vorhandenen Verweise angezeigt. Wenn Verweise fehlen, wird links neben der Referenz ein kleines Kreuzsymbol angezeigt

Sie können die folgenden Aufgaben in der Ansicht &quot;Layout&quot;ausführen:

**Themenreferenz einfügen** - ![](images/insert-topic-reference.png)

Zeigt das Dialogfeld &quot;Themensuche&quot;an. Navigieren Sie zur Themen-/Zuordnungsdatei, die Sie einfügen möchten, und klicken Sie auf Auswählen , um sie der Zuordnung hinzuzufügen.
![](images/insert-topic-reference-dialog.png){width="800" align="left"}


**Themengruppe einfügen** - ![](images/insert-topic-group.png)

Fügen Sie die `topicgroup` -Element. Weitere Informationen zu Gruppierungsthemen finden Sie unter [topicgroup](https://docs.oasis-open.org/dita/v1.0/langspec/topicgroup.html) Dokumentation in OASIS DITA Language Specification.

**Schlüsseldefinition einfügen** - ![](images/Key_icon.svg)

Zeigt das Dialogfeld Keydef einfügen an. Verwenden Sie dieses Dialogfeld, um eine beliebige Schlüsseldefinition zu definieren, die Sie in der Zuordnung verwenden möchten.

![](images/insert-key-definition-dialog.png){width="300" align="left"}

**Einfügen vor/Einfügen nach** - ![](images/insert_element_before_icon.svg) / ![](images/insert_element_after_icon.svg)

Zeigt das Dialogfeld Element einfügen an. Wählen Sie das Element aus, das Sie in die Zuordnung einfügen möchten. Je nach Vorgang wird das neue Element vor oder nach dem aktuellen Element in die Zuordnung eingefügt.

**Einfügen von Vorder-Matches** - ![](images/frontmatter.svg)

Dieses Symbol wird angezeigt, wenn Sie eine Lesekarte zur Bearbeitung öffnen. Sie können Komponenten wie Inhaltsverzeichnisse, Indexe und Tabellen am Anfang des Buches einfügen.

**Rücken einfügen** - ![](images/backmatter.svg)

Dieses Symbol wird angezeigt, wenn Sie eine Lesekarte zur Bearbeitung öffnen. Sie können Komponenten für ein Ende des Buches einfügen, z. B. einen Index, ein Glossar und eine Liste von Abbildungen.

**Ausgewähltes Element nach links/rechts verschieben** - ![](images/left-arrow-icon.png) / ![](images/right-arrow-icon.png)

Klicken Sie auf den Pfeil nach links, um das Thema in der Hierarchie nach links zu verschieben. Dies fördert im Wesentlichen das jeweilige Thema auf einer Ebene in der Hierarchie. Wenn Sie beispielsweise auf den Pfeil nach links klicken, während ein untergeordnetes Thema ausgewählt ist, wird es zum gleichrangigen Thema. Wenn Sie auf den Pfeil nach rechts klicken, wird das Thema auf die rechte Seite verschoben, sodass es zum untergeordneten Element des Themas darüber wird.

**Ausgewähltes Element nach oben/unten verschieben![](images/arrowup.svg)** - / ![](images/arrowdown.svg)

Klicken Sie auf die Pfeilsymbole nach oben oder unten, um das Thema in der Hierarchie nach oben oder unten zu verschieben.

>[!NOTE]
>
> Sie können die Verweise auch per Drag &amp; Drop in eine Karte verschieben.

**Sperren/Entsperren** - ![](images/LockClosed_icon.svg) / ![](images/LockOpen_icon.svg)

Ruft eine Sperre in der Zuordnungsdatei ab und lässt die Sperre los. Wenn Sie nicht gespeicherte Änderungen in Ihrer Zuordnungsdatei haben, werden Sie zum Zeitpunkt der Freigabe der Sperre aufgefordert, die Zuordnungsdatei zu speichern. Die Änderungen werden in der aktuellen Version der Map-Datei gespeichert.

**Zusammenführen** - ![](images/merge-icon.svg)

Weitere Informationen zum Zusammenführen von Inhalten aus einer anderen Version derselben oder einer anderen Datei finden Sie unter [Zusammenführen](web-editor-features.md#id205DF04E0HS) im Web-Editor.

**Versionsverlauf** - ![](images/version-history-web-editor-ico.svg)

Überprüfen Sie die verfügbaren Versionen und Beschriftungen für Ihr aktives Thema und stellen Sie im Editor selbst eine beliebige Version wieder her.

**Versionsetikett** - ![](images/version-label-icon.svg)

Zeigt das Dialogfeld zur Verwaltung der Versionsbeschriftungen an. Wählen Sie eine Version aus der Dropdownliste aus. Wählen Sie den Titel aus, den Sie auf die ausgewählte Version anwenden möchten, und klicken Sie auf **Titel hinzufügen** , um es hinzuzufügen.

**Anzeigeoptionen** - ![](images/view-options.svg)

Zeigt eine Dropdown-Liste an, in der Sie die Option &quot;Zeilennummern anzeigen&quot;, &quot;Kontrollkästchen anzeigen&quot;und &quot;Dateinamen anzeigen&quot;wählen können.

- **Zeilennummern anzeigen**

Blendet die Zeilennummer für jedes Thema ein oder aus. Die Zeilennummern werden in Abhängigkeit von der Hierarchieebene angezeigt.

- **Kontrollkästchen anzeigen**

Blendet ein Kontrollkästchen für jedes Thema ein oder aus. Sie können das Kontrollkästchen verwenden, um das/die Thema(e\) auszuwählen und mithilfe des Menüs &quot;Optionen&quot;verschiedene Aufgaben auszuführen. Weitere Informationen finden Sie unter [Optionen](#id228ID8006H8) Menü.

- **Dateiname anzeigen**

Zeigt den Dateinamen der Titel der Themen an.

>[!NOTE]
>
> Wenn Sie den Mauszeiger über den Titel eines Themas bewegen, wird Ihnen der Dateipfad angezeigt.


**Anzeigen von Themen basierend auf bedingten Filtern** Wenn Sie Bedingungen für ein Thema angewendet haben, wird rechts neben dem Thema ein Filtersymbol angezeigt. Wenn Sie den Mauszeiger über ein Filtersymbol bewegen, werden Ihnen die angewendete Bedingung und ihr Attributwert angezeigt.

**Menü &quot;Optionen&quot;in der Ansicht &quot;Layout&quot;**

Neben der Organisation von Themen in der Map-Datei können Sie auch die folgenden Aktionen über das Menü Optionen durchführen, das für ein Element in der Layout-Ansicht verfügbar ist:

![](images/map-editor-options-menu.png){width="650" align="left"}

- **Hinzufügen**: Sie können im Map Editor ein neues Thema oder einen leeren Verweis hinzufügen:
   - **Leere Referenz**: Mit dieser Option können Sie in Ihrer DITA-Zuordnung einen leeren Verweis hinzufügen. Sie können später auf den eingefügten leeren Verweis doppelklicken und die Themendetails hinzufügen. Weitere Informationen finden Sie unter [Thema erstellen](web-editor-features.md#id228ICI0105U) im Web-Editor.
   - **Neues Thema**: Wenn Sie ein neues Thema aus dem Menü erstellen, wird das Dialogfeld Neues Thema erstellen angezeigt. Geben Sie im Dialogfeld Neues Thema erstellen die erforderlichen Details ein und klicken Sie auf Erstellen . Weitere Informationen finden Sie unter [Thema erstellen](web-editor-features.md#id228ICI0105U) im Web-Editor.
- **Verschieben**: Sie können ein Thema in der Hierarchie nach oben/unten/rechts/links verschieben. Sie können auch per Drag-and-Drop ein Thema oder eine Zuordnung aus dem Repository-Bedienfeld in die im Map Editor geöffnete Karte ziehen.
- **Rückgängig**: Machen Sie den letzten Vorgang in der Ansicht &quot;Layout&quot;rückgängig.
- **Wiederholen**: Wiederholen Sie den letzten Vorgang in der Ansicht &quot;Layout&quot;.
- **Kopieren**: Kopieren Sie die ausgewählte Referenz aus der Zuordnungsdatei.

  >[!NOTE]
  >
  > Sie können die Kontrollkästchen anzeigen und dann auswählen, um mehrere Verweise zu kopieren.

- **Einfügen**: Fügen Sie die kopierten Verweise an der aktuellen Position in der Hierarchie ein.
- **Löschen**: Löschen Sie die ausgewählten Verweise aus der Zuordnungsdatei.

  >[!NOTE]
  >
  > Sie können die Kontrollkästchen anzeigen und dann auswählen, um mehrere Verweise zu löschen.


## Rechter Bereich im Map Editor

Im rechten Bereich werden die Inhaltseigenschaften und die Zuordnungseigenschaften in der Ansicht &quot;Layout&quot;des Map-Editors angezeigt.

**Inhaltseigenschaften**

Der Bereich &quot;Inhaltseigenschaften&quot;enthält Informationen zum Typ des aktuell ausgewählten Themas in der Zuordnung, zur Link-URL und zu den Attributen. Weitere Informationen finden Sie unter [Inhaltseigenschaften](web-editor-features.md#id228IDB00HMM) im Web-Editor.

- **Andere Attribute** Wenn Ihr Administrator ein Profil für Attribute erstellt hat, erhalten Sie diese Attribute zusammen mit den konfigurierten Werten. Im Bereich &quot;Inhaltseigenschaften&quot;können Sie diese Attribute auswählen und sie relevanten Inhalten in Ihrem Thema zuweisen. Sie können auch Attribute zuweisen, die von Ihrem Administrator unter der **Anzeigenattribute** in den Editor-Einstellungen. Die für ein Element definierten Attribute werden im Layout und in der Gliederungsansicht angezeigt. Auf diese Weise können Sie sich alle Themen in einer Zuordnung, für die ein bestimmtes Attribut definiert ist, kurz ansehen. Beispielsweise alle Themen, für die das Plattformattribut als &quot;Android&quot;definiert ist.

  ![Layoutansicht](images/layout-inline-attributes.png){width="650" align="left"}


  Weitere Informationen finden Sie unter *Anzeigenattribute* innerhalb der *Editor-Einstellungen* Funktionsbeschreibung in [Linke Leiste](web-editor-features.md#id2051EA0M0HS) Abschnitt.

- **Metadaten** Mithilfe der Metadaten können Sie die Metadateninformationen festlegen. Sie können den Navigationstitel, den Linktext, die Kurzbeschreibung und die Suchbegriffe definieren.

Weitere Informationen zu den standardmäßigen Themenattributen und Metadaten finden Sie in der [topicref](https://docs.oasis-open.org/dita/v1.2/os/spec/langref/topicref.html) Dokumentation in OASIS DITA Language Specification.

**Zuordnungseigenschaften**

Zeigt das Dialogfeld Zuordnungseigenschaften an, in dem Sie die Attribute und Metadateninformationen für die Zuordnung festlegen können.

## Autorenansicht {#id205DEC0005Z_author_view}

Die **Autor** -Ansicht können Sie Ihre DITA-Zuordnung im Web-Editor bearbeiten. Dies zeigt die WYSIWYG-Ansicht des Map-Editors und einige der in der Autorenansicht angezeigten Symbole sind mit der Layout-Ansicht identisch. Weitere Informationen finden Sie unter [Layoutansicht](#id205DEC0005Z_layout_view). Darüber hinaus können Sie die folgenden Symbole sehen und die entsprechenden Aufgaben in der Autorenansicht ausführen:

**Einfügen vor/Einfügen nach** - ![](images/insert_element_before_icon.svg) / ![](images/insert_element_after_icon.svg)

Zeigt das Dialogfeld Element einfügen an. Wählen Sie das Element aus, das Sie in die Zuordnung einfügen möchten. Je nach Vorgang wird das neue Element vor oder nach dem aktuellen Element in die Zuordnung eingefügt.

**Element einfügen** - ![](images/Add_icon.svg)

Zeigt das Dialogfeld Element einfügen an. Wählen Sie das Element aus, das Sie einfügen möchten. Mit der Tastatur können Sie durch die Liste der Elemente blättern und die Eingabetaste drücken, um das gewünschte Element einzufügen. Alternativ können Sie direkt auf das Element klicken, um es in die Zuordnung einzufügen.

**Beziehungstabelle einfügen** - ![](images/relationship_table_icon.svg)

Fügt eine Beziehungstabelle in die Zuordnung ein. Da das Konzept der Arbeit mit der Beziehungstabelle mit dem im Abschnitt &quot;Grundlegender Map-Editor&quot;erläuterten Konzept übereinstimmt, lesen Sie [Arbeiten mit Beziehungstabellen im Basic Map Editor](map-editor-basic-map-editor.md#id1944B0I0COB) für weitere Details.

**Wiederverwendbaren Inhalt einfügen** - ![](images/content-reuse-icon.png)

Zeigt das Dialogfeld Inhalt wiederverwenden an. Verwenden Sie dieses Dialogfeld, um den Inhalt, den Sie wiederverwenden möchten, in Ihre Zuordnung einzufügen.

**Navigationstitel-Attribut aktualisieren** - ![](images/navtitle-refresh-icon.svg)

Synchronisiert die `title` -Element einer referenzierten Datei in einer Zuordnung mit dem in `@navtitle` -Attribut. Sie können verschiedene Arten von Referenzdateien zu einer Zuordnung hinzufügen, z. B. Themen-, Referenz-, Aufgaben-, \(Unter-)Maps usw. Die meisten dieser Dateien unterstützen die `@navtitle` -Attribut. Wenn eine Datei die `@navtitle` -Attribut, dann die `@navtitle` -Attribut für dieselbe Datei in der Zuordnung aktualisiert wird. In diesem Fall `@navtitle` -Attribut nicht vorhanden ist, wird die `@navtitle` -Attribut dieser Referenzdatei hinzugefügt und ihr `title` wird auch aktualisiert, um die `@navtitle`.

>[!NOTE]
>
> Ihr Administrator kann das automatische Hinzufügen konfigurieren `@navtitle` -Attribut zu jeder Referenzdatei zuordnen, die Sie einer Zuordnung hinzufügen. Weitere Informationen zum Konfigurieren des automatischen Hinzufügens `@navtitle` -Attribut, siehe *Standardmäßig Attribut @navtitle einschließen* unter Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern as a Cloud Service.

Klicken Sie auf das Symbol Navigationstitel-Attribut aktualisieren , um die `title` -Element und `@navtitle` -Attributs.

**Anzeigen von Tags ein/aus** - ![](images/Label_icon.svg)

Blendet die XML-Tags ein oder aus. Die Tags dienen als visuelle Hinweise zur Begrenzung eines Elements. Wenn Sie in diesem Modus einen Thema-/Zuordnungsverweis einfügen möchten, ziehen Sie die gewünschte Datei vor oder nach dem Tag per Drag-and-Drop. Die horizontale Leiste wird im Modus Tags-Ansicht nicht angezeigt.

**Änderungen aktivieren/deaktivieren** - ![](images/track-change-icon.svg)

Sie können alle in der Zuordnungsdatei vorgenommenen Aktualisierungen verfolgen, indem Sie den Modus Änderungen verfolgen aktivieren. Nachdem Sie die Verfolgungsänderungen aktiviert haben, werden alle Einfügungen und Löschungen im Dokument erfasst. Weitere Informationen finden Sie unter [Änderungen aktivieren/deaktivieren](web-editor-features.md#id205DF0203Y4) im Web-Editor.

**Bewertungsaufgabe erstellen** - ![](images/create-review-task-icon.svg)

Sie können eine Prüfungsaufgabe des aktuellen Themas oder der Zuordnungsdatei direkt im Web-Editor erstellen. Öffnen Sie die Datei, für die Sie die Prüfungsaufgabe erstellen möchten, und klicken Sie auf Prüfungsaufgabe erstellen , um den Überprüfungserstellungsprozess zu starten. Befolgen Sie die Anweisungen im Abschnitt [Themen oder Zuordnungen überprüfen](review.md#) für weitere Details.

## Themen über DITA-Map bearbeiten {#id17ACJ0F0FHS}

Die Bearbeitung eines einzelnen Themas gibt dem Autor keinen vollständigen Kontext. Ein Autor hätte keine Informationen darüber, wo ein Thema in einer DITA-Zuordnung platziert wird. Ohne diese kontextbezogenen Informationen wird es für Autoren ein wenig schwierig, Inhalte zu erstellen.

AEM Guides ermöglichen es Autoren, eine DITA-Map im Web Editor zu öffnen und die Platzierung von Themen in der Map anzuzeigen. Auf diese Weise können Autoren erkennen, wo genau das Thema in der Zuordnung platziert wird, und relevantere Inhalte erstellen. Wenn mehrere Autoren an einem Projekt arbeiten, können sie außerdem wissen, welche Themen in der Karte verfügbar sind, und Inhalte wiederverwenden, wo immer dies erforderlich ist.

Um Themen über eine DITA-Zuordnung zu bearbeiten, führen Sie die folgenden Schritte aus:

1. Navigieren Sie in der Assets-Benutzeroberfläche zu der DITA-Zuordnung, die die Themen enthält, die Sie bearbeiten möchten.
1. Klicken Sie auf die DITA-Karte, um sie in der DITA-Map-Konsole zu öffnen.
1. Wählen Sie die **Themen** um eine Liste der in der DITA-Map verfügbaren Themen anzuzeigen.

   >[!TIP]
   >
   > Im Tab Themen können Sie die Zuordnungsdatei mit ihren abhängigen Elementen herunterladen. Weitere Informationen finden Sie unter [DITA-Map-Datei exportieren](authoring-download-assets.md#id218UBA00IXA).

1. Klicken Sie in der Symbolleiste auf **Themen bearbeiten**.

   Die DITA-Zuordnung wird im Web-Editor geöffnet.

   >[!NOTE]
   >
   > Sie können auch die DITA-Map-Datei in der Assets-Benutzeroberfläche auswählen und auf **Themen bearbeiten** in der Hauptsymbolleiste, um den Web Editor zu starten.

   ![](images/web-editor-map-view_cs.png){width="350" align="left"}

1. \(*Optional*\) Sie können auch ein Thema aus der Zuordnung auswählen und die Datei vor der Bearbeitung auschecken. Um die Datei auszuchecken, wählen Sie mindestens eine Datei aus dem linken Bereich aus und klicken Sie auf **Checkout**. Sie können die Sperre auch für jede Datei freigeben, indem Sie die ausgecheckte Datei auswählen und auf **Auschecken und Entsperren abbrechen** in der Kartenansicht.

   >[!IMPORTANT]
   >
   > Wenn Ihr Administrator die **Bearbeitung ohne Checkout deaktivieren** auswählen, müssen Sie die Datei vor der Bearbeitung auschecken. Wenn Sie die Datei nicht auschecken, wird das Dokument im schreibgeschützten Modus im Editor geöffnet.

   Im folgenden Screenshot werden die Symbole für Auschecken und Sperren \(A\), Auschecken abbrechen und Entsperren \(B\), Als neue Version speichern und Entsperren \(C\), Bearbeiten \(D\), Vorschau \(E\), verschiedene Symbole mit verschiedenen DITA-Dateitypen \(F\) und Dateien, die ausgecheckt werden \(G\), hervorgehoben.

   ![](images/file-checkout-map-editor.png){width="550" align="left"}

1. Klicken Sie auf einen beliebigen Themenlink, um ihn im Webeditor zur Bearbeitung zu öffnen.

   Sie können mehrere Themen im Editor öffnen und jedes Thema wird in einer neuen Registerkarte im Editor geöffnet. Selbst wenn Ihre DITA-Map Unterkarten enthält, werden Themen aus den Unterkarten auch in einer neuen Registerkarte zur Bearbeitung geöffnet. Wenn Sie die Themen unter einer Unterkarte anzeigen möchten, können Sie auf klicken und die Unterkarte erweitern.

   ![](images/web-editor-multiple-topics.png){width="800" align="left"}

   Wenn Sie auf eine Zuordnungsdatei klicken, wird die Zuordnung in einer neuen Registerkarte des Webbrowsers geöffnet.

1. Nachdem Sie die Bearbeitung der Themen abgeschlossen haben, haben Sie folgende Möglichkeiten:

   - Sie können sie einzeln speichern. Wenn Sie auf **Ohne Speichern schließen** In den Themen wird ein Dialogfeld angezeigt, in dem Sie aufgefordert werden, die nicht gespeicherten Themen zu speichern:

     ![](images/save-multiple-topics.PNG){width="550" align="left"}

     Sie können festlegen, dass alle ausgewählten Themen gespeichert werden, oder Sie können die Themen, die Sie nicht speichern möchten, deaktivieren.

   - Sie können das Thema mit dem **Als neue Version speichern und entsperren** Schaltfläche. Wenn Sie eine Revision des Themas speichern, wird eine neue Revision erstellt und die Sperre wird ebenfalls veröffentlicht.
   - Wenn Ihr Administrator die Option zum Einchecken von Dateien beim Schließen aktiviert hat, wird Ihnen eine Eingabeaufforderung zum Speichern von Dateien angezeigt, sobald die ausgecheckten Dateien geschlossen werden. Wenn diese Option aktiviert ist, wird Ihnen beim Schließen des Editors mit geänderten Dateien die Liste der ausgecheckten Dateien angezeigt, die gespeichert werden müssen. Die ausgecheckten Dateien werden mit einem Sperrsymbol angezeigt:

     ![](images/save-on-close.PNG){width="550" align="left"}

      - Klicken auf **Ohne Speichern schließen** -Schaltfläche schließt die Dateien, ohne die Änderungen zu speichern.

      - Klicken Sie auf **Speichern** speichert die Änderungen, checkt die Dateien jedoch nicht ein.

      - Auswählen der **Überprüfen von Dateien** und klicken Sie dann auf **Speichern** -Schaltfläche checkt die Dateien ein \(erstellt eine andere Version\) und speichert auch die Dateien.


## Vorschau einer Landkarte

Zusätzlich zur Möglichkeit, die Position jeder Themendatei in einer Zuordnung zu sehen, ist es wünschenswert, den Zuordnungsinhalt in einem aufeinander folgenden Fluss zu sehen. Mit der Funktion &quot;Zuordnungsvorschau&quot;können Sie den gesamten Inhalt der Zuordnungsdatei mit einem Klick anzeigen. Sie müssen keine Ausgabe der Map-Datei generieren, um zu sehen, wie die gesamte Karte nach der Veröffentlichung aussehen wird. Sie können einfach auf die Vorschau der Karte zugreifen und alle Themen und Unterkarten werden in Form eines Buches gerendert.

Sie können auf die Vorschau einer Karte wie folgt zugreifen:

- **Assets-Benutzeroberfläche**: Navigieren Sie in der Assets-Benutzeroberfläche zum Zuordnungsspeicherort, wählen Sie die Zuordnungsdatei aus und wählen Sie **Vorschau anzeigen** in der Symbolleiste. Die Vorschau der Karte wird in einem neuen Tab angezeigt. Sie können den Inhalt aller Themen im Vorschaumodus anzeigen. In dieser Ansicht können Sie kein Thema bearbeiten.

  >[!NOTE]
  >
  > Wenn die Variable *Vorschau anzeigen* nicht in der Hauptsymbolleiste sichtbar ist, wurde sie möglicherweise unter die **Mehr** Symbolleistenmenü.

- **Erweiterter Map-Editor**: Klicken Sie im erweiterten Map-Editor auf das Symbol Vorschau , um die Vorschau der aktuellen Zuordnung anzuzeigen.

  ![](images/map-preview-icon.png){width="350" align="left"}

  Sie können die folgenden zusätzlichen Aufgaben im Vorschaumodus ausführen:

   - Klicken Sie mit der rechten Maustaste auf ein Thema und wählen Sie **Bearbeiten** , um das Thema zur Bearbeitung in einer neuen Registerkarte zu öffnen.

     >[!NOTE]
     >
     > Wenn Sie keine Bearbeitungsrechte haben, wird das Thema im schreibgeschützten Modus geöffnet.

   - Springen Sie zum gewünschten Thema, indem Sie auf den Thementitel in der Zuordnungsstruktur klicken \(im linken Bereich\).

   - Das aktuelle Thema in der Zuordnungsvorschau wird ebenfalls in der Zuordnungsstruktur hervorgehoben.


**Übergeordnetes Thema:**[ Arbeiten mit dem Map Editor](map-editor.md)
