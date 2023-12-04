---
title: Ausgabegenerierungseinstellungen konfigurieren
description: Erfahren Sie, wie Sie die Einstellungen für die Generierung von Ausgaben konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '5470'
ht-degree: 1%

---

# Ausgabegenerierungseinstellungen konfigurieren {#id181AI0B0E30}

AEM Guides verfügen über eine Vielzahl von Konfigurationsoptionen, mit denen Sie den Prozess zur Generierung der Ausgabe anpassen können. In diesem Thema werden alle Konfigurationen und Anpassungen behandelt, die Ihnen bei der Einrichtung Ihres Ausgabegenerierungsprozesses helfen.

## Konfigurieren der Registerkarte &quot;Grundlinie&quot;im DITA-Map-Dashboard {#id223MD0D0YRM}

So blenden Sie die Registerkarte &quot;Grundlinie&quot;im DITA-Map-Dashboard aus:

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die Registerkarte &quot;Grundlinie&quot;im Map-Dashboard zu konfigurieren.

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `hide.tabs.baseline` | Boolesch\(`true/false`\).**Standardwert**: `true` |

>[!NOTE]
>
> Diese Konfiguration ist standardmäßig aktiviert und die Registerkarte &quot;Grundlinie&quot;ist nicht im Landkarten-Dashboard verfügbar.

## Gemischte Veröffentlichung auf einer vorhandenen AEM-Site konfigurieren {#id1691I0V0MGR}

Wenn Sie über eine AEM-Site verfügen, die DITA-Inhalte enthält, können Sie Ihre AEM Site-Ausgabe so konfigurieren, dass DITA-Inhalte an einer vordefinierten Stelle auf Ihrer Site veröffentlicht werden. Im folgenden Screenshot einer AEM Site-Seite wird beispielsweise die `ditacontent` -Knoten ist zum Speichern von DITA-Inhalten reserviert:

![](assets/publish-in-aem-site.png)

Die verbleibenden Knoten auf der Seite werden direkt im AEM Site-Editor erstellt. Durch die Konfiguration der Veröffentlichungseinstellung zum Veröffentlichen von DITA-Inhalten an einem vordefinierten Speicherort wird sichergestellt, dass keiner Ihrer vorhandenen Nicht-DITA-Inhalte durch den Veröffentlichungsprozess der AEM Guides geändert wird.

Sie müssen die folgenden Konfigurationen auf Ihrer vorhandenen Site durchführen, um die Veröffentlichung von DITA-Inhalten in einem vordefinierten Knoten zu ermöglichen:

- Vorlageneigenschaften Ihrer Site konfigurieren

- Knoten zu Ihrer Site hinzufügen, um DITA-Inhalte zu veröffentlichen


Führen Sie die folgenden Schritte aus, um die Vorlageneigenschaften Ihrer vorhandenen Site zu konfigurieren:

1. Verwenden Sie den Package Manager, um die Datei /libs/fmdita/config/templates/default herunterzuladen.

   >[!NOTE]
   >
   > Nehmen Sie keine Anpassungen in den Standardkonfigurationsdateien vor, die im `libs` Knoten. Sie müssen eine Überlagerung der `libs` Knoten in `apps` und aktualisieren Sie die erforderlichen Dateien im `apps` nur Knoten.

1. Fügen Sie die folgenden Eigenschaften hinzu:

   | Eigenschaftsname | Typ | Wert |
   |-------------|----|-----|
   | `topicContentNode` | Zeichenfolge | Geben Sie den Knotennamen an, unter dem Sie den DITA-Inhalt veröffentlichen möchten. Der Standardknoten, unter dem AEM Guides DITA-Inhalte veröffentlicht, lautet beispielsweise: <br> `jcr:content/contentnode` |
   | `topicHeadNode` | Zeichenfolge | Geben Sie den Knotennamen an, unter dem Sie die Metadateninformationen Ihres DITA-Inhalts speichern möchten. Der Standardknoten, in dem AEM Guides Metadateninformationen speichert, lautet beispielsweise: <br> `jcr:content/headnode` |


Wenn Sie das nächste Mal DITA-Inhalte mithilfe der Vorlagenkonfigurationen Ihrer Site veröffentlichen, wird der Inhalt in den Knoten veröffentlicht, die in der `topicContentNode` und `topicHeadNode` Eigenschaften.

## AEM Site-Ausgabe anpassen {#id166TG0B30WR}

Die AEM-Handbücher unterstützen das Erstellen von Ausgaben in folgenden Formaten:

- AEM Site
- PDF
- HTML5
- EPUB
- Benutzerdefinierte Ausgabe über DITA-OT

Für die AEM Site-Ausgabe können Sie verschiedene Designvorlagen mit verschiedenen Ausgabeaufgaben zuweisen. Diese Designvorlagen können den DITA-Inhalt in verschiedenen Layouts rendern. Sie können beispielsweise verschiedene Designvorlagen für interne und externe Zielgruppen angeben.

Sie können auch benutzerdefinierte DITA Open Toolkit \(DITA-OT\)-Plug-ins mit den AEM-Handbüchern verwenden. Sie können diese benutzerdefinierten DITA-OT-Plug-ins hochladen, um eine PDF-Ausgabe auf eine bestimmte Art zu generieren.

>[!TIP]
>
> Siehe *AEM Site-Veröffentlichung* im Handbuch Best Practices für Best Practices zur Erstellung AEM Site-Ausgabe.


### Anpassen der Designvorlage zum Generieren der Ausgabe {#customize_xml-add-on}

Die AEM Guides verwenden eine Reihe vordefinierter Designvorlagen, um AEM Site-Ausgabe zu generieren. Sie können die Designvorlagen der AEM Guides anpassen, um die Ausgabe zu generieren, die Ihrem UnternehmensBranding entspricht. Eine Designvorlage ist eine Sammlung verschiedener Stile \(CSS\), Skripte \(Server- und Client-seitig\), Ressourcen \(Bilder, Logos und andere Assets\) und JCR-Knoten, die alle diese Ressourcen miteinander verknüpfen. Eine Designvorlage kann so einfach sein wie ein einzelnes serverseitiges Skript mit nur einigen JCR-Knoten oder eine komplexe Kombination von Stilen, Ressourcen und JCR-Knoten. Design-Vorlagen werden vom Publishing-Subsystem AEM Guides verwendet, während AEM Site-Ausgabe generiert wird. Sie steuern die Struktur, das Erscheinungsbild der generierten Ausgabe.

Es gibt keine Einschränkung, wo sich die Ressourcen für die Designvorlage auf dem Server befinden sollten, aber sie sind in der Regel entsprechend ihrer Funktion logisch organisiert. Beispielsweise werden in der Standardvorlage alle JavaScript- und CSS-Dateien gespeichert unter `/etc/designs/fmdita/clientlibs/siteoutput/default` Ordner. Wo immer sich diese Dateien befinden, werden sie durch eine Sammlung von JCR-Knoten verknüpft. Gemeinsam bilden diese JCR-Knoten und die Dateien die gesamte Designvorlage.

Mit der im Lieferumfang der AEM-Handbücher enthaltenen Standard-Designvorlage können Sie die Komponenten für Landingpages, Themen und Suchseiten anpassen. Sie können eine Kopie des Standarddesigns und der entsprechenden Referenzvorlagen erstellen und verschiedene Komponenten angeben, um die gewünschte Ausgabe zu generieren.

Führen Sie die folgenden Schritte aus, um Ihre eigene Designvorlage für AEM Site-Ausgabegenerierung festzulegen:

1. Verwenden Sie Package Manager, um die Standardentwurfsvorlage vom folgenden Speicherort herunterzuladen:

   /libs/fmdita/config/templates

1. Erstellen Sie eine Kopie der heruntergeladenen Dateien an folgendem Speicherort im Git-Repository von Cloud Manager:

   /apps/fmdita/config/templates

1. Sie müssen auch die referenzierten Vorlagen aus dem Standardvorlagenknoten herunterladen und kopieren. Die referenzierten Vorlagen befinden sich unter:

   /libs/fmdita/templates/default/cqtemplates

   Die Eigenschaften der Designvorlage AEM Guides werden in der folgenden Tabelle beschrieben.

   | Eigenschaft | Beschreibung |
   |--------|-----------|
   | `landingPageTemplate`, `searchPageTemplate`, `topicPageTemplate`, `shadowPageTemplate` | Geben Sie die `cq:Template` Knoten für diese entsprechenden Seiten \(Landingpage, Suche und Thema\). Standardmäßig wird die `cq:Template` -Knoten für diese Seiten finden Sie unter `/libs/fmdita/templates/default/cqtemplates` Knoten. Dieser Knoten definiert die Struktur und Eigenschaften der Landingpage, der Such- und der Themenseite.<br> Die `shadowPageTemplate` wird zur Optimierung des Chunked-Inhalts verwendet. Sie müssen den Wert dieser Eigenschaft auf Folgendes festlegen: `fmdita/templates/default/cqtemplates/shadowpage` <br> **Hinweis:** Sie müssen einen Wert für `topicPageTemplate`. Die `landingPageTemplate` und `searchPageTemplate` sind optionale Eigenschaften. Wenn Sie nicht möchten, dass die Such- und Landingpages generiert werden, geben Sie diese Eigenschaften nicht an. |
   | `title` | Ein beschreibender Name Ihrer Designvorlage. |
   | `topicContentNode` | Der Speicherort des Knotens, der den DITA-Inhalt auf einer Themenseite enthält. Der Pfad ist relativ zur Themenseite. |
   | `topicHeadNode` | Der Speicherort des Knotens, der die Kopfwerte \(oder Metadaten\) enthält, die aus dem DITA-Inhalt abgeleitet wurden. Der Pfad ist relativ zur Themenseite. |
   | `tocNode` | Der Speicherort des Knotens, der das Inhaltsverzeichnis enthalten wird. Der Pfad ist relativ zur Landingpage oder zum Zielpfad. |
   | `basePathProp` | Der Eigenschaftsname zum Speichern des Pfads des Stammverzeichnisses der veröffentlichten Site. |
   | `indexPathProp` | Der Eigenschaftsname zum Speichern des Pfads der Landingpage/Indexseite der veröffentlichten Site. |
   | `pdfPathProp` | Der Eigenschaftsname zum Speichern des PDF-Pfads des Themas, wenn die PDF-Generierung des Themas aktiviert ist. |
   | `pdfTypeProp` | Der Eigenschaftsname zum Speichern des Typs der PDF-Generierung. Derzeit enthält diese Eigenschaft immer &quot;Thema&quot;. |
   | `searchPathProp` | Der Eigenschaftsname zum Speichern des Pfads der Suchseite, wenn die Vorlage eine Suchseite enthält. |
   | `siteTitleProp` | Der Eigenschaftsname zum Speichern des Titels der veröffentlichten Site. Dieser Titel ist normalerweise mit dem Titel der zu veröffentlichenden Karte identisch. |
   | `sourcePathProp` | Der Eigenschaftsname zum Speichern des Pfads des DITA-Quellthemas für die aktuelle Seite. |
   | `tocPathProp` | Der Eigenschaftsname zum Speichern des Pfads des TOC-Stammverzeichnisses für die veröffentlichte Site. |


>[!NOTE]
>
> Nachdem Sie einen benutzerdefinierten Designvorlagenknoten erstellt haben, müssen Sie die Option Design in den AEM Site-Ausgabevorgaben aktualisieren, um den benutzerdefinierten Designvorlagenknoten zu verwenden.

Weitere Informationen finden Sie unter [Erstellen der ersten Adobe Experience Manager-Website](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=de) und [Grundlagen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/develop-wknd-tutorial.html?lang=en) der Entwicklung Ihrer eigenen Website auf AEM.

### Dokumenttitel zum Generieren AEM Site-Ausgabe verwenden

Beim Generieren AEM Site-Ausgabe spielt die Art und Weise, wie URLs generiert werden, eine wichtige Rolle bei der Entdeckung Ihres Inhalts. Wenn Sie UUID-basierte Dateinamen verwenden, wäre das Generieren von URLs basierend auf der UUID Ihrer Dateien nicht suchfreundlich. Als Administrator oder Herausgeber haben Sie die Kontrolle darüber, wie Sie die URLs für Ihre AEM Site-Ausgabe generieren möchten. AEM Handbücher bieten eine Konfiguration, mit der Sie die URLs AEM Site-Ausgabe mithilfe des Dateinamens und nicht der UUID-basierten Dateinamen generieren können. Standardmäßig ist diese Option bei UUID-basierten Dateisystemen aktiviert. Dies bedeutet, dass beim Generieren AEM Site-Ausgabe für UUID-basierte Dateisysteme die Dateinamen zum Generieren der URLs und nicht der UUIDs der Dateien verwendet werden.

>[!NOTE]
>
> Sie können Regeln weiter konfigurieren, sodass nur ein Zeichensatz in den URLs einer AEM Site-Ausgabe zulässig ist. Weitere Informationen finden Sie unter [Konfigurieren von Bereinigungsregeln für Dateinamen zum Erstellen von Themen und Veröffentlichen AEM Site-Ausgabe](#id2164D0KD0XA).

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(property\) Details an, um die URLs zu konfigurieren, die in AEM Site-Ausgabe generiert werden:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `aemsite.pagetitle` | Boolesch \(true/false\). Wenn Sie die Ausgabe mithilfe des Seitentitels generieren möchten, setzen Sie diese Eigenschaft auf &quot;true&quot;. Standardmäßig ist die Verwendung des Dateinamens festgelegt.<br> **Standardwert**: false |

### URL der Ausgabe der AEM Site zur Verwendung des Dokumenttitels konfigurieren

Sie können die Dokumenttitel in der URL der AEM Site-Ausgabe verwenden. Wenn der Dateiname nicht vorhanden ist oder alle Sonderzeichen enthält, können Sie das System so konfigurieren, dass die Sonderzeichen in der URL der AEM Site-Ausgabe durch ein Trennzeichen ersetzt werden. Sie können sie auch so konfigurieren, dass sie durch den Namen des ersten untergeordneten Themas ersetzt werden.


Um die Seitennamen zu konfigurieren, führen Sie die folgenden Schritte aus:

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden (Eigenschaft-)Details an, um die Seitennamen für die Themen zu konfigurieren.

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeName` | `nodename.systemDefinedPageName` | Boolesch (`true/false`). **Standardwert**: `false` |

Wenn beispielsweise die Variable *@navtitle* in `<topichead>` enthält alle Sonderzeichen und Sie legen `aemsite.pagetitle` -Eigenschaft auf &quot;true&quot;gesetzt ist, wird standardmäßig ein Trennzeichen verwendet. Wenn Sie die `nodename.systemDefinedPageName` auf &quot;true&quot;gesetzt ist, wird der Name des ersten untergeordneten Themas angezeigt.


### Konfigurieren von Bereinigungsregeln für Dateinamen zum Erstellen von Themen und Veröffentlichen AEM Site-Ausgabe {#id2164D0KD0XA}

Als Administrator können Sie eine Liste gültiger Sonderzeichen definieren, die in Dateinamen zulässig sind und letztendlich die URL einer AEM Site-Ausgabe bilden. In früheren Versionen konnten Benutzer Dateinamen mit Sonderzeichen wie `@`, `$`, `>`und mehr. Diese Sonderzeichen führten bei der Generierung AEM Site-Seiten zu einer kodierten URL.

Ab Version 3.8 wurden Konfigurationen hinzugefügt, um eine Liste von Sonderzeichen zu definieren, die in Dateinamen zulässig sind. Standardmäßig enthält die gültige Dateinamenkonfiguration &quot;`a-z A-Z 0-9 - _`&quot;. Dies bedeutet, dass Sie beim Erstellen einer Datei beliebige Sonderzeichen im Dateinamen haben können, diese jedoch intern durch einen Bindestrich \(`-`\) in den Dateinamen. Sie können beispielsweise den Titel der Datei als Einführung 1 oder Introduction@1 festlegen. Der entsprechende Dateiname, der für beide Fälle generiert wurde, wäre Einführung-1.

Beachten Sie bei der Definition einer Liste gültiger Zeichen, dass diese Zeichen &quot;`*/:[\]|#%{}?&<>"/+`&quot; und `a space` wird immer durch einen Bindestrich \(`-`\).

>[!NOTE]
>
> Wenn Sie die Liste der gültigen Sonderzeichen nicht konfigurieren, kann der Dateierstellungsprozess zu unerwarteten Ergebnissen führen.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die gültigen Sonderzeichen in Dateinamen und AEM Site-Ausgabe zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.common.SanitizeNodeNameImpl` | `aemsite.DisallowedFileNameChars` | Stellen Sie sicher, dass die Eigenschaft auf ``'<>`@$``. Sie können dieser Liste weitere Sonderzeichen hinzufügen. |

Sie können auch die anderen Eigenschaften konfigurieren, z. B. Kleinschreibung in Dateinamen, Trennzeichen zur Verarbeitung ungültiger Zeichen und maximal zulässige Anzahl von Zeichen in Dateinamen. Um diese Eigenschaften zu konfigurieren, fügen Sie die folgenden Schlüssel-Wert-Paare in die Konfigurationsdatei ein:

| Eigenschaftenschlüssel | Eigenschaftswert |
|------------|--------------|
| `nodename.uselower` | Boolesch \(true/false\).<br> **Standardwert**: true |
| `nodename.separator` | Jedes Zeichen. <br> **Standardwert**: \_ *\(Unterstrich\)* |
| `nodename.maxlength` | Ganzzahlwert.<br> **Standardwert**: 50 |

### Reduzieren AEM Site-Knotenstruktur konfigurieren

Wenn Sie AEM Site-Ausgabe generieren, wird intern ein Knoten für jedes Element in den Themen erstellt. Für eine DITA-Map mit Tausenden von Themen kann diese Knotenstruktur zu tief werden. Diese Art von tief verschachtelter Knotenstruktur kann Leistungsprobleme bei größeren Sites haben. Die folgende Momentaufnahme zeigt eine tief verschachtelte Knotenstruktur für eine AEM Site-Ausgabe:

![](assets/deep-nested-aem-site-node-structure.png)

Beachten Sie, dass im obigen Schnappschuss für jeden `p` -Element und die nachfolgenden Unterelemente sowie eine ähnliche Struktur werden für jedes andere Element erstellt, das im Thema verwendet wird.

Mit AEM Guides können Sie konfigurieren, wie die Knotenstruktur AEM Site-Ausgabe intern erstellt wird. Sie können die Knotenstruktur bei bestimmten Elementen reduzieren. Das bedeutet, dass Sie ein Element definieren können, das als Hauptelement betrachtet wird. Alle darin enthaltenen Unterelemente werden mit dem Hauptelement zusammengeführt. Wenn Sie beispielsweise die `p` -Element, dann jedes Element, das innerhalb der `p` -Element wird mit dem Hauptelement zusammengeführt `p` -Element. Eine separate Anmerkung wird für kein Unterelement im `p` -Element. Der folgende Schnappschuss zeigt die Knotenstruktur, reduziert auf `p` element:

![](assets/flattened-aem-site-node-structure.png)

So reduzieren Sie AEM Site-Knotenstruktur:

1. Identifizieren Sie die Elemente\(s\), in denen Sie die Knotenstruktur reduzieren möchten:

1. Überlagerung der `libs` Knoten in `apps` Knoten und öffnen Sie die Datei &quot;elementmapping.xml&quot;.

1. Fügen Sie die `<flatten>true</flatten>` -Eigenschaft in der Definition des Elements, in dem Sie die Knotenstruktur reduzieren möchten. Wenn Sie beispielsweise die Knotenstruktur auf der `p` -Element ein und fügen Sie dann das Attribut flatten in der Definition von `p` Element wie unten gezeigt:

   ```XML
   <ditaelement>
         <name>p</name>
         <class>- topic/p</class>
         <componentpath>fmdita/components/dita/wrapper</componentpath>
         <type>COMPOSITE</type>
         <target>para</target>
         <flatten>true</flatten>
         <wrapelement>div</wrapelement>
      </ditaelement>
   ```

   >[!NOTE]
   >
   > Standardmäßig wurde die Eigenschaft flatten-Knoten im `p` -Element.

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden \(property\) Details an:

   | PID | Eigenschaftenschlüssel | Eigenschaftswert |
   |---|------------|--------------|
   | `com.adobe.dxml.flattening.FlatteningConfigurationService` | `flattening.enabled` | Boolesch \(true/false\).<br> **Standardwert**: `false` |


Wenn Sie jetzt die AEM Site-Ausgabe generieren, befinden sich die Knoten im `p` -Element reduziert und im `p` -Element selbst. Die neuen Reduzierungseigenschaften für `p` -Element in CRXDE.

![](assets/flatten-aem-site-note-props-crxde.png)

**Suchen Sie eine Zeichenfolge innerhalb des Inhalts in AEM Site-Ausgabe.**

Standardmäßig können Sie in den Titeln nur in der AEM Site-Ausgabe nach einer Zeichenfolge suchen. Sie können das System so konfigurieren, dass sowohl in den Titeln als auch im Inhalt oder im Hauptteil der AEM Site-Ausgabe nach einer Zeichenfolge gesucht wird.

>[!NOTE]
>
> Manchmal funktioniert Ihre Suche möglicherweise für einige Elemente im Inhalt, aber Sie können sie so konfigurieren, dass sie für den gesamten Inhalt funktioniert.

![](assets/flatten-aem-site-note-props-crxde-search.png)

Um die Suche zu aktivieren, sollten Sie die Reduzierung AEM Site-Knotenstruktur konfigurieren.

VORSICHT:

Sie können bis zu 1 MB reduzierten Inhalt durchsuchen. Im vorherigen Screenshot können Sie beispielsweise suchen, ob der Inhalt unter &lt;p> -Tag ist &lt;= 1 MB.

>[!NOTE]
>
> Die Suche funktioniert nur bei Elementen, wenn die `<flatten>`auf &quot;true&quot;gesetzt ist. Standardmäßig verfügt AEM Guides über die `<flatten>` -Attribut für häufig verwendete Textelemente wie &lt;p> &lt;ul> &lt;li>. Wenn Sie jedoch einige benutzerdefinierte Elemente erstellt haben, sollten Sie die `<flatten>` in der Datei &quot;elementmapping.xml&quot;auf &quot;true&quot;gesetzt.

**Reduzieren AEM Site-Knotenstruktur verhindern**

Ähnlich wie beim Festlegen des Knotens, der in AEM Site-Ausgabe reduziert werden soll, können Sie auch ein Element angeben, das Sie aus dieser Konfiguration ausschließen möchten. Beispiel: Wenn Sie Knoten reduzieren möchten bei `body` -Element, Sie möchten jedoch keine `table` -Element in `body` zum Reduzieren hinzufügen, können Sie die Eigenschaft exclude innerhalb der `table` -Element definiert.

So schließen Sie die `table` -Element aus der Reduzierung hinzufügen, fügen Sie die folgende Eigenschaft zum `table` Definition des Elements:

`<preventancestorflattening>true|false</preventancestorflattening>`

### Versionierung für gelöschte Seiten in AEM Site-Ausgabe konfigurieren

Wenn Sie AEM Site-Ausgabe mit **Löschen und** Erstellen ****für die Einstellung Vorhandene Ausgabeseiten ausgewählt wurde, wird eine Version für die zu löschende(n) Seite(n\) erstellt. Sie können das System so konfigurieren, dass vor dem Löschen die Erstellung einer Version angehalten wird.

Führen Sie die folgenden Schritte aus, um die Erstellung einer Version für die zu löschende(n\) Seite zu stoppen:

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die **Keine Version für gelöschte Seiten erstellen** Option:

   | PID | Eigenschaftenschlüssel | Eigenschaftswert |
   |---|------------|--------------|
   | `com.adobe.fmdita.confi g.ConfigManager` | `no.version.creation.on.deletion` | Boolesch \(true/false\).<br> **Standardwert**: `true` |

   >[!NOTE]
   >
   > Wenn diese Option aktiviert ist, können Benutzer alle Seiten direkt löschen, ohne eine Version für sie zu erstellen. Wenn die Option nicht ausgewählt ist, wird eine Version erstellt, bevor die Seite\(n\) gelöscht wird.

### Einrichten eines benutzerdefinierten Rewriters mit Experience Manager-Handbüchern {#custom-rewriter}

Experience Manager Guides verfügen über ein benutzerdefiniertes Sling [**rewriter**](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html) -Modul zur Behandlung der im Fall von Querkarten generierten Links (Verknüpfungen zwischen den Themen zweier verschiedener Karten). Diese Rewriter-Konfiguration wird unter folgendem Pfad installiert: <br> `/apps/fmdita/config/rewriter/fmdita-crossmap-link-patcher`.

Wenn Sie einen anderen benutzerdefinierten Sling-Rewriter in Ihrer Codebase haben, verwenden Sie eine `'order'` Wert größer als 50, da der Experience Manager Guides Sling Rewriter verwendet `'order'` 50.  Um dies zu überschreiben, benötigen Sie einen Wert > 50 . Weitere Informationen finden Sie unter [Pipelines zum Neuschreiben der Ausgabe](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).


## Verwenden von Metadaten bei der Veröffentlichung der Ausgabe über DITA-OT {#id191LF0U0TY4}

AEM Guides bieten eine Möglichkeit, benutzerdefinierte Metadaten beim Veröffentlichen der Ausgabe mithilfe von DITA-OT zu übergeben. Als Administrator und Herausgeber müssen Sie die folgenden Aufgaben ausführen, um benutzerdefinierte Metadaten in der veröffentlichten Ausgabe zu konfigurieren und zu verwenden:

- Fügen Sie als Administrator die erforderlichen Metadaten im System hinzu, damit sie auf der Seite Eigenschaften der DITA-Zuordnung verfügbar gemacht werden.

- Fügen Sie als Administrator die benutzerdefinierten Metadaten in die Metadatenliste ein, damit sie in der DITA-Map-Konsole angezeigt werden.

- Konfigurieren und fügen Sie als Publisher die benutzerdefinierten Metadaten mit der DITA-Zuordnung hinzu und generieren Sie die erforderliche Ausgabe.


Um die erforderlichen Metadaten im System hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Assets** aus der Liste der Tools.

1. Klicken Sie auf **Metadatenschemata** Kachel.

   Die Seite Metadatenschema Forms wird angezeigt.

1. Wählen Sie die **default** Formular aus der Liste.

   >[!NOTE]
   >
   > Die Eigenschaften, die auf der Seite Eigenschaften für eine DITA-Zuordnung angezeigt werden, stammen aus diesem Formular.

1. Klicken Sie auf **Bearbeiten**.

1. Fügen Sie die benutzerdefinierten Metadaten hinzu, die Sie in Ihren veröffentlichten Ausgaben verwenden möchten. Beispielsweise werden wir Zielgruppen-Metadaten mithilfe der folgenden Schritte hinzufügen:

   1. Aus dem **Formular erstellen** Komponentenliste, Drag &amp; Drop **Einzelzeilentext** auf das Formular.

   2. Wählen Sie das neue Feld aus, um die **Einstellungen** des Felds.

   3. Im **Feldbezeichnung**, geben Sie den Metadatennamen ein: Zielgruppe.

   4. Im **Zu Eigenschaft zuordnen** festlegen, geben Sie an./jcr:content/metadata/&lt;name of=&quot;&quot; the=&quot;&quot; metadata=&quot;&quot;>. Für unser Beispiel setzen wir es auf ./jcr:content/metadata/audience.

   Fügen Sie mithilfe dieser Schritte alle erforderlichen Metadatenparameter hinzu.

1. Klicken Sie auf **Speichern**.


Der neue Parameter wird jetzt auf der Seite Eigenschaften für alle DITA-Maps angezeigt.

![](assets/properties-page-custom-metadata.PNG)

Als Nächstes müssen Sie die benutzerdefinierten Metadaten in der DITA-Map-Konsole verfügbar machen. Führen Sie die folgenden Schritte aus, um die benutzerdefinierten Metadaten auf der DITA Map-Dashboards verfügbar zu machen:

1. Verwenden Sie den Paketmanager, um auf die Datei &quot;metadataList&quot;zuzugreifen, die im Git-Repository von Cloud Manager unter folgendem Speicherort verfügbar ist:

   /libs/fmdita/config/metadataList

   >[!NOTE]
   >
   > Die Datei &quot;metadataList&quot;enthält eine Liste der Eigenschaften, die in der Variablen **Eigenschaften** Dropdown-Liste einer DITA-Map im Landkarten-Dashboard. Standardmäßig sind in dieser Datei vier Eigenschaften aufgelistet: docstate, dc:language, dc:description und dc:title.

1. Fügen Sie die benutzerdefinierten Metadaten hinzu, die Sie auf der Seite &quot;Metadatenschema-Forms&quot;hinzugefügt haben. Fügen Sie für unser Beispiel den Zielgruppenparameter am Ende der Standardliste hinzu.


Jetzt werden die benutzerdefinierten Metadaten in der DITA-Map-Konsole angezeigt. **Eigenschaften** Dropdown-Liste.

Als Herausgeber müssen Sie schließlich die benutzerdefinierten Metadaten in die veröffentlichte Ausgabe aufnehmen. Um die benutzerdefinierten Metadaten beim Generieren der Ausgabe zu verarbeiten, führen Sie die folgenden Schritte aus:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnung, die Sie veröffentlichen möchten.

1. Wählen Sie die DITA-Map-Datei aus und öffnen Sie die zugehörige Eigenschaftenseite.

1. Geben Sie auf der Seite Eigenschaften den Wert für die benutzerdefinierten Metadaten an. Für unser Beispiel haben wir den Wert &quot;External&quot;für den Zielgruppenparameter angegeben.

   ![](assets/properties-page-custom-metadata-value.png)

1. Klicken Sie auf **Speichern und schließen**.

1. Klicken Sie auf die DITA-Zuordnungsdatei, um die DITA-Zuordnungskonsole zu öffnen.

1. Im **Ausgabevorgaben** -Registerkarte die Ausgabevorgabe auswählen, die Sie zum Generieren der Ausgabe verwenden möchten.

1. Klicken Sie auf **Bearbeiten**.

1. Aus dem **Eigenschaften** Wählen Sie die Eigenschaften aus, die Sie an den Veröffentlichungsprozess weitergeben möchten.

   ![](assets/props-in-publish-output.PNG)


Die ausgewählten Eigenschaften/Metadaten werden an den Veröffentlichungsprozess übergeben und in der endgültigen Ausgabe verfügbar gemacht.

### Validieren von Metadaten, die zur Verarbeitung an DITA-OT übergeben werden

Um die an DITA-OT übergebenen Metadatenwerte zu überprüfen, kann eine lokale Umgebung mit einer Cloud-fähigen JAR-Datei verwendet werden. Da wir nicht auf das lokale Dateisystem in der Cloud zugreifen können, ist die einzige Möglichkeit, die Metadatendatei zu überprüfen, über die Cloud-fähige JAR-Datei.

- Dateiname: metadata.xml
- Dateispeicherort: crx-quickstart/profiles/ditamaps/&lt;ditamap-1234>

  So greifen Sie auf metadata.xml zu:

   - Melden Sie sich bei dem Server-Speicherort an, auf dem AEM Instanz ausgeführt wird.
   - Migration zu crx-quickstart/profiles/ditamaps/&lt;newly-created-directory-name>/metadata.xml
- Beispieldateiformat:

  **metadata.xml**

  ```XML
  <?xml version="1.0" encoding="UTF-8" standalone="no"?>
  <root>
     <Path id="/absolutePath/sampleMap.ditamap">
        <metadata>
           <meta isArray="false" key="dc:description">This is a file</meta>
           <meta isArray="false" key="dc:title">Myfile</meta>
           <meta isArray="true" key="multivalueText">One;Two;Three</meta>
        </metadata>
     </Path>
     <Path id="/absolutePath/sampleTopic.dita">
        <metadata>
           <meta isArray="false" key="dc:description">description for the accountability</meta>
           <meta isArray="false" key="dc:title">accountability title</meta>
           <meta isArray="true" key="multivalueText">value1</meta>
        </metadata>
     </Path>
  </root>
  ```


- isArray: Ein boolesches Attribut, das definiert, ob die Metadaten ein Mehrwert \(Array\) sind oder nicht. Die Werte werden durch ein Semikolon getrennt.
- Pfad-ID: Absoluter Pfad zur Datei, die im temporären Verzeichnis gespeichert ist.

>[!NOTE]
>
> Wenn bestimmte Metadaten für die Datei nicht vorhanden sind, &lt;meta> -Tag mit dem Schlüssel wird nicht als Eigenschaft für diese Datei in der Datei &quot;metadata.xml&quot;angezeigt.

## DITA-Elementzuordnung mit AEM Komponenten anpassen {#id1679J600HEL}

DITA-Elemente in den AEM Guides werden ihren entsprechenden AEM Komponenten zugeordnet. AEM Guides verwenden diese Zuordnung in Workflows wie Veröffentlichung und Überprüfung, um DITA-Elemente in eine entsprechende AEM zu konvertieren. Die Zuordnung wird im Abschnitt `elementmapping.xml` -Datei, auf die über den Package Manager zugegriffen werden kann.

>[!NOTE]
>
> Nehmen Sie keine Anpassungen in den Standardkonfigurationsdateien vor, die im ``libs`` Knoten. Sie müssen eine Überlagerung der ``libs`` Knoten in ``apps`` und aktualisieren Sie die erforderlichen Dateien im ``apps`` nur Knoten.

Sie können die vordefinierten DITA-Elementzuordnungen verwenden oder DITA-Elemente Ihren benutzerdefinierten AEM zuordnen. Um Ihre benutzerdefinierten AEM verwenden zu können, müssen Sie die Struktur der `elementmapping.xml` -Datei.

### elementmapping.xml structure

Eine allgemeine Übersicht über die `elementmapping.xml` Struktur wird nachfolgend erläutert:

1. Jedes DITA-Element wird zuerst nach einer entsprechenden Komponentenzuordnung basierend auf dem Elementnamen gesucht. Beispiel:

   ```XML
   <ditaelement>     
      <name>**substeps**</name>  
      <class>- topic/ol task/substeps</class>  
      <componentpath>dita/components/ditaolist</componentpath>  
      <type>COMPOSITE</type>  
      <target>para</target>
   </ditaelement>
   ```

   Im obigen Beispiel werden alle `substeps` DITA-Elemente werden mit der `dita/components/ditaolist` -Komponente.

1. Wenn ein DITA-Element keine Übereinstimmung basierend auf dem Namen findet, wird eine Übereinstimmung anhand der `class` abgeschlossen ist. Beispiel:

   ```XML
   <ditaelement>  
      <name>topic</name>  
      <class>**- topic/topic**</class>  
      <componentpath>fmdita/components/dita/topic</componentpath>  
      <type>COMPOSITE</type>  
      <target>para</target>  
      <attributemap> 
         <attribute from="id" to="id" />  
      </attributemap>
   </ditaelement>
   ```

   Wenn im obigen Beispiel keine Zuordnung für die `task` -Element, dann die `task` -Element der obigen Komponente zugeordnet ist, da `task` von der `topic` -Komponente.

1. Wenn ein Element über eine entsprechende Komponentenzuordnung verfügt, wird die weitere Verarbeitung seiner untergeordneten Elemente durch `type`. Beispiel:

   ```XML
   <ditaelement>  
      <name>title</name>  
      <class>- topic/title</class>  
      <componentpath>foundation/components/title</componentpath>  
      <type>**STANDALONE**</type>  
      <target>para</target>  
      <textprop>jcr:title</textprop>
   </ditaelement>
   ```

   `type` akzeptiert die folgenden Werte:

   - COMPOSITE: Element zu Komponente *Die Zuordnung wird für untergeordnete Elemente fortgesetzt* sowie.

   - STANDALONE: untergeordnete Elemente des aktuellen Elements sind *nicht weiter zugeordnet*.

   Wenn im obigen Beispiel die Variable `<title>` -Element untergeordnete Elemente enthält, werden sie keiner anderen Komponente zugeordnet. Die Komponente für `<title>` -Element ist für das Rendern aller untergeordneten Elemente innerhalb der `<title>` -Element.

1. Wenn einem einzelnen DITA-Element mehrere Komponenten zugeordnet sind, wird die beste Übereinstimmung für das Element ausgewählt. Um die beste Übereinstimmungskomponente auszuwählen, werden die Domäne und die strukturelle Spezialisierung von DITA-Elementen berücksichtigt.

   Wenn DITA-Elemente mit Domänenspezialisierung vorhanden sind und eine Komponente für die Domänenspezialisierung zugeordnet ist, erhält diese Komponente eine hohe Priorität.

   Wenn es DITA-Elemente mit struktureller Spezialisierung gibt und eine Komponente für strukturelle Spezialisierung zugeordnet ist, erhält diese Komponente eine hohe Priorität.

1. Sie können `<attributemap>` in der Elementzuordnung, um Attributwerte den entsprechenden Knoteneigenschaften zuzuordnen.
1. `textprop` kann für die Serialisierung des Textinhalts eines DITA-Elements in eine Knoteneigenschaft verwendet werden. Darüber hinaus kann es mehrmals in einem Element-Tag verwendet werden, um den Textinhalt an mehreren Stellen in der veröffentlichten Hierarchie zu serialisieren. Sie können auch den Speicherort und Namen der Ziel-Property anpassen. Beispiel:

   ```XML
   <ditaelement>
      <name>title</name>
      <componentpath>foundation/components/title</componentpath>
      <type>STANDALONE</type>
      <target>para</target>
       <textprop>**jcr:title**</textprop>
   </ditaelement>
   ```

   Die obige Elementzuordnung gibt an, dass der Textinhalt von `<title>` -Element wird als Wert einer Eigenschaft mit dem Namen `jcr:title` auf dem Ausgabeknoten.

1. `xmlprop` kann zum Serialisieren der gesamten XML für ein bestimmtes Element mit einer Knoteneigenschaft verwendet werden. Die Komponente kann dann diese Knoteneigenschaft lesen und benutzerdefiniertes Rendering durchführen. Beispiel:

   ```XML
   <ditaelement>
       <name>svg-container</name>
      <class>+ topic/foreign svg-d/svg-container</class>
       <componentpath>fmdita/components/dita/svg</componentpath>
       <type>STANDALONE</type>
       <target>para</target>
      <xmlprop>**data**</xmlprop>
   </ditaelement>
   ```

   Die obige Elementzuordnung gibt an, dass das gesamte XML-Markup für das Element `<svg-container>` wird als Wert einer Eigenschaft mit dem Namen `data` auf dem Ausgabeknoten.

1. Es gibt eine spezielle Attributzuordnung zur Verarbeitung der Pfadauflösung im Prozess der Ausgabegenerierung. Beispiel:

   ```XML
   <attributemap>
      <attribute from="href" to="fileReference" ispath="true" rel="source" />
      <attribute from="height" to="height" />
       <attribute from="width" to="width" />
   </attributemap>
   ```

   Für die oben genannten `attributemap`, die `href` -Attribut in Ihrem DITA-Element wird einer Knoteneigenschaft mit dem Namen `fileReference`. Seit `ispath` auf `true`, löst der Prozess zur Generierung der Ausgabe diesen Pfad auf und legt ihn dann in `fileReference` Knoteneigenschaft.

   Wie diese Auflösung abläuft, wird auf der Grundlage des Wertes der `rel` -Attribut in der Attributzuordnung.

   - Wenn `rel=source`, dann den Wert von `href` in Bezug auf die DITA-Quelldatei aufgelöst, die derzeit verarbeitet wird. Der Wert von `href` wird aufgelöst und in den Wert von `fileReference` -Eigenschaft.

   - Wenn `rel=target`, dann den Wert von `href` in Bezug auf den Speicherort der Stammveröffentlichung aufgelöst. Der Wert von `href` wird aufgelöst und in den Wert von `fileReference` -Eigenschaft.

   Wenn Sie nicht möchten, dass eine Vorverarbeitung oder Auflösung für Pfadattribute erfolgt, müssen Sie die `ispath` -Attribut. Der Wert wird unverändert kopiert und die Komponente kann die erforderliche Auflösung durchführen.


### DITA-Elementschema

Im Folgenden finden Sie ein Beispiel für das DITA-Elementschema in `elementmapping.xml` Datei:

```XML
<ditaelement>        
    <name>element_name</name>    
    <class>element_class</class>    
    <componentpath>fmdita/components/dita/component_name</componentpath>    
    <type>COMPOSITE|STANDALONE</type>     
    <attributeprop>propname_a</attributeprop>      
    <textprop>propname_t</textprop>    
    <xmlprop>propname_x</xmlprop>     
    <xpath>xpath expression string</xpath>     
    <target>head|para</target>     
    <wrapelement>div</wrapelement>     
    <wrapclass>class_name</wrapclass>     
    <attributemap>         
        <attribute from="attrname"         to="propname"         ispath="true|false"         rel="source|target" />    
    </attributemap>    
    <skip>true|false</skip> 
</ditaelement>
```

In der folgenden Tabelle werden die Elemente im DITA-Elementschema beschrieben:

| Element | Beschreibung |
|-------|-----------|
| `<ditaelement>` | Der Knoten der obersten Ebene für jedes Zuordnungselement. |
| `<class>` | Das Klassenattribut des DITA-Zielelements, für das Sie die Komponente schreiben.<br> Beispielsweise lautet das Klassenattribut für das DITA-Thema: <br> `- topic/topic` |
| `<componentpath>` | Der CRXDE-Pfad der zugeordneten AEM. |
| `<type>` | Mögliche Werte:<br> -   **COMPOSITE**: Verarbeiten Sie auch untergeordnete Elemente <br> -   **STANDALON**: Überspringt die Verarbeitung untergeordneter Elemente |
| `<attributeprop>` | Wird für die Zuordnung von serialisierten DITA-Attributen und -Werten zu AEM Knoten als Eigenschaft verwendet. Wenn Sie beispielsweise `<note type="Caution">` -Element und die für dieses Element zugeordnete Komponente `<attributeprop>attr_t</ attributeprop>`, dann werden das Attribut und der Wert des Knotens serialisiert auf `attr_t` Eigenschaft des entsprechenden AEM-Knotens \( `attr_t->type="caution"`\). |
| `<textprop>propname_t</textprop>` | Speichern Sie die `getTextContent()` Ausgabe in Eigenschaft definiert durch `propname_t.` <br> **Hinweis:** Dies ist eine optimierte Eigenschaft. |
| `<xmlprop>propname_x </xmlprop>` | Speichern Sie serialisiertes XML dieses Knotens in der Eigenschaft, die von `propname_x.<br> `**Hinweis:** Dies ist eine optimierte Eigenschaft. |
| `<xpath>` | Wenn das XPath-Element in der Elementzuordnung bereitgestellt wird, sollte die XPath-Bedingung zusammen mit dem Elementnamen und der Klasse ebenfalls erfüllt sein, damit die Komponentenzuordnung verwendet wird. |
| `<target>` | Platzieren Sie für das DITA-Element im CRX-Repository an dem angegebenen Speicherort.<br> Mögliche Werte: <br> - **head**: Unter dem Kopfknoten <br> - **text**: Unter dem Absatzknoten |
| `<wrapelement>` | Das HTML-Element, in das der Inhalt eingeschlossen werden soll. |
| `<wrapclass>` | Der Elementwert der Eigenschaft `wrapclass.` |
| `<attributemap>` | Container-Knoten, der eine oder mehrere `<attribute>` Knoten. |
| `<attribute from="attrname" to="propname" ispath="true|false" rel="source|target" />` | Ordnet die DITA-Attribute AEM Eigenschaften zu: <br> -   **`from`**: DITA-Attributname <br> -   **`to`**: Name AEM Komponenteneigenschaft <br> -   **`ispath`**: Wenn das Attribut ein Pfadwert ist \(z. B.: *image*\) <br> -   **`rel`**: Wenn der Pfad die Quelle oder das Ziel ist <br> **Hinweis:** Wenn `attrname` beginnt mit `%`, dann map `attrname minus '%'` to prop &#39; `propname`&quot;. |

**Weitere Hinweise**

- Wenn Sie die standardmäßige Elementzuordnung überschreiben möchten, sollten Sie die Änderungen nicht in der Standardeinstellung `elementmapping.xml` -Datei. Sie sollten eine neue Mapping-XML-Datei erstellen und die Datei an einem anderen Speicherort ablegen, vorzugsweise in dem von Ihnen erstellten benutzerdefinierten Apps-Ordner.

- Im `elementmapping.xml` -Datei, gibt es viele Zuordnungseinträge, die auf die Komponente fmdita/components/dita/wrapper verweisen. Wrapper ist eine generische Komponente, die relativ einfache DITA-Konstrukte rendert, die Eigenschaften auf ihrem Site-Knoten verwenden, um relevante HTML zu generieren. Sie verwendet die `wrapelement` -Eigenschaft zum Generieren von einschließenden Tags und Delegieren des untergeordneten Renderings an die entsprechenden Komponenten. Dies ist nützlich in Fällen, in denen Sie nur eine Container-Komponente benötigen. Anstatt eine neue Komponente zu erstellen, die ein bestimmtes Container-Tag wie `div` oder `p`, können Sie die Wrapper-Komponente mit der `wrapelement` und `wrapclass` -Eigenschaften verwenden, um denselben Effekt zu erzielen.

- Es wird nicht empfohlen, große Textmengen in String JCR-Eigenschaften zu speichern. Die optimierte Berechnung des Eigenschaftstyps bei der Ausgabegenerierung stellt sicher, dass große Textinhalte nicht als Zeichenfolgentyp gespeichert werden. Wenn stattdessen Inhalte gespeichert werden müssen, die größer als ein bestimmter Schwellenwert sind, wird der Eigenschaftstyp in binär geändert. Standardmäßig ist dieser Schwellenwert auf 512 Byte konfiguriert, kann jedoch im Configuration Manager \(*com.adobe.fmdita.config.ConfigManager*\) durch Ändern der **Als binären Schwellenwert speichern** -Einstellung.

- Wenn Sie einige \(und nicht alle\) der Elementzuordnungen überschreiben möchten, müssen Sie nicht die gesamte `elementmapping.xml` -Datei. Sie müssen eine neue XML-Zuordnungsdatei erstellen und nur die Elemente definieren, die Sie überschreiben.

- Nachdem Sie die XML-Datei am benutzerdefinierten Speicherort erstellt haben, aktualisieren Sie die `Override Element Mapping` -Einstellung in `com.adobe.fmdita.config.ConfigManager` Bundle


## DITA-Map-Konsole anpassen {#id188HC08M0CZ}

AEM Guides bieten Ihnen die Flexibilität, die Funktionen der DITA-Map-Konsole zu erweitern. Wenn Sie beispielsweise eine Reihe von Berichten haben, die sich von den in den AEM Guides verfügbaren unterscheiden, können Sie diese Berichte zur Zuordnungskonsole hinzufügen. Um die Zuordnungskonsole anzupassen, müssen Sie eine AEM Client-Bibliothek \(oder ClientLib\) erstellen, die den Code enthält, um die benötigten Funktionen auszuführen.

>[!NOTE]
>
> Eine direkte Änderung an Seitenkomponenten wird nicht empfohlen, da sie durch neue Versionen des Produkts überschrieben wird.

AEM Guides bieten die `apps.fmdita.dashboard-extn` Kategorie zum Anpassen der Zuordnungskonsole. Bei jedem Laden der Zuordnungskonsole wird die unter der `apps.fmdita.dashboard-extn` -Kategorie ausgeführt und geladen wird.

>[!NOTE]
>
> Weitere Informationen zum Erstellen AEM Client-Bibliothek finden Sie unter [Verwenden Client-seitiger Bibliotheken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=en).

## Verarbeiten der Bilddarstellung während der Ausgabegenerierung {#id177BF0G0VY4}

AEM enthält eine Reihe von Standard-Workflows und Medien-Handles zur Verarbeitung von Assets. In AEM gibt es vordefinierte Workflows für die Verarbeitung von Assets für die häufigsten MIME-Typen. Normalerweise erstellt AEM für jedes Bild, das Sie hochladen, mehrere Ausgabeformate desselben Binärformats. Diese Ausgabedarstellungen können unterschiedlich groß sein, mit einer anderen Auflösung, einem hinzugefügten Wasserzeichen oder anderen geänderten Eigenschaften. Weitere Informationen dazu, wie AEM mit Assets umgehen, finden Sie unter [Verarbeitung von Assets mithilfe von Medien-Handlern und Workflows](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=en) in AEM Dokumentation.

Mit AEM Guides können Sie konfigurieren, welche Bilddarstellung zum Zeitpunkt der Generierung der Ausgabe für Ihre Dokumente verwendet werden soll. Sie können beispielsweise aus einer der standardmäßigen Bildausgabeformate wählen oder eine erstellen und zum Veröffentlichen Ihrer Dokumente dasselbe verwenden. Die Bildwiedergabe-Zuordnung für die Veröffentlichung Ihrer Dokumente wird im `/libs/fmdita/config/ **renditionmap.xml**` -Datei. Ein Snippet aus `renditionmap.xml` -Datei wie folgt lautet:

>[!NOTE]
>
> Es wird empfohlen, eine Kopie der `renditionmap.xml` in der Datei `apps` Ordner für alle Anpassungen.

```XML
<renditionmap>
   <mapelement>
      <mimetype>image/png</mimetype>
      <rendition output="AEMSITE">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="PDF">original</rendition>
      <rendition output="HTML5">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="EPUB">cq5dam.web.1280.1280.jpeg</rendition>
      <rendition output="CUSTOM">cq5dam.web.1280.1280.jpeg</rendition>
   </mapelement>
...
</renditionmap>
```

Die `mimetype` -Element gibt den MIME-Typ des Dateiformats an. Die `rendition output` -Element gibt den Typ des Ausgabeformats und den Namen der Ausgabe an \(z. B. `cq5dam.web.1280.1280.jpeg`\), die zum Veröffentlichen der angegebenen Ausgabe verwendet werden soll. Sie können die Bildausgabeformate angeben, die für alle unterstützten Ausgabeformate verwendet werden sollen - AEMSITE, PDF, HTML5, EPUB und CUSTOM.

Wenn die angegebene Ausgabedarstellung nicht vorhanden ist, sucht AEM Publishing-Prozess für Guides zunächst nach der Web-Ausgabe des angegebenen Bildes. Wenn selbst die Webausgabe nicht gefunden wird, wird die ursprüngliche Ausgabe des Bildes verwendet.

>[!NOTE]
>
> Diese Bildausgabeformate steuern nur die Ausgabegenerierung. Die Webausgabe eines Bildes wird verwendet, wenn Sie ein Dokument zur Vorschau oder Überprüfung öffnen.

## Konfigurieren des Zeitrahmens für die automatische Bereinigung für den Ausgabestverlauf {#id19AAI070V8Q}

Wenn Sie eine Ausgabe generieren, wird die Ausgabe zusammen mit den Ausgabsprotokollen erstellt. Bei großen DITA-Maps können diese Protokolle viel Platz in Ihrem Repository beanspruchen. Standardmäßig werden die Protokolle am folgenden Speicherort im Repository gespeichert:

`/var/dxml/metadata/outputHistory`

Über einen bestimmten Zeitraum konnte die kollektive Größe aller Protokolldateien in GBs dargestellt werden. AEM Guides können Sie einen Zeitraum konfigurieren, um diese Protokolldateien im Repository zu speichern. Nach dem angegebenen Zeitraum werden die Protokolle zusammen mit dem Ausgabegenerierungsverlauf aus dem Repository gelöscht.

>[!NOTE]
>
> Der Ausgabegenerierungsverlauf ist der Protokolleintrag in der Liste Erzeugte Ausgaben auf der Registerkarte Ausgaben .

Die Konfiguration der Verlaufsbereinigungsfunktion wirkt sich auf die Generierung der Ausgabe für alle DITA-Maps im Repository aus. Auf der Registerkarte &quot;Outputs&quot;einer DITA-Zuordnung wird der Verlauf nach der angegebenen Anzahl von Tagen und zu der in der Einstellung festgelegten Zeit bereinigt.

>[!NOTE]
>
> Das Entfernen der Protokolldateien und des Ausgabegenerierungsverlaufs hat keine Auswirkungen auf die generierte Ausgabe.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um einen Tag und eine Uhrzeit für die Bereinigung des Ausgabedarstellungsverlaufs und der -protokolle festzulegen:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `output.history.purgeperiod` | Geben Sie die Anzahl der Tage an, nach denen der Ausgabedarstellungsverlauf zusammen mit den Ausgabsprotokollen bereinigt wird. Wenn Sie diese Funktion deaktivieren möchten, legen Sie diese Eigenschaft zum angegebenen Zeitpunkt für die Ausführung des Bereinigungsprozesses für Ausgaben fest, die vor der in dieser Eigenschaft angegebenen Anzahl von Tagen generiert wurden. <br> **Standardwert**: 5 |
| `output.history.purgetime` | Geben Sie den Zeitpunkt an, zu dem der Bereinigungsprozess eingeleitet wird. <br> **Standardwert**: 0:00 \(oder 12:00 Mitternacht\) |

## Ändern der zuletzt generierten Ausgabelistenbegrenzung {#id1679JH0H0O2}

Sie können die maximale Anzahl der generierten Ausgaben ändern, die auf der Registerkarte &quot;Ausgaben&quot;für eine DITA-Zuordnung angezeigt werden.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die Anzahl der Ausgaben zu ändern, die in der Liste angezeigt werden sollen:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `output.historylimit` | Ganzzahlwert.<br> **Standardwert**: 25 |

>[!TIP]
>
> Siehe *Ausgabeverlauf* im Handbuch Best Practices für Best Practices zum Arbeiten mit dem Ausgabedarstellungsverlauf.
