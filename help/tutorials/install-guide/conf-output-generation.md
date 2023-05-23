---
title: Ausgabegenerierungseinstellungen konfigurieren
description: Erfahren Sie, wie Sie die Einstellungen für die Generierung von Ausgaben konfigurieren
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '5761'
ht-degree: 1%

---

# Ausgabegenerierungseinstellungen konfigurieren {#id181AI0B0E30}

AEM Guides verfügen über eine Vielzahl von Konfigurationsoptionen, mit denen Sie den Prozess zur Generierung der Ausgabe anpassen können. In diesem Thema werden alle Konfigurationen und Anpassungen behandelt, die Ihnen bei der Einrichtung Ihres Ausgabegenerierungsprozesses helfen.

## Konfigurieren der Registerkarte &quot;Grundlinie&quot;im DITA-Map-Dashboard {#id223MD0D0YRM}

Sie können die Registerkarte &quot;Grundlinie&quot;im Dashboard der Karte konfigurieren und ausblenden.

Die **Registerkarte &quot;Grundlinie ausblenden&quot;** ist nicht standardmäßig aktiviert und Sie müssen dies über configMgr aktivieren. Führen Sie die folgenden Schritte aus, um die Option standardmäßig im Web-Editor zu aktivieren:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Wählen Sie die **Registerkarte &quot;Grundlinie ausblenden&quot;** -Option.

1. Klicken Sie auf **Speichern**.

   >[!NOTE]
   >
   > Diese Konfiguration ist standardmäßig deaktiviert und die Registerkarte &quot;Grundlinie&quot;ist im Landkarten-Dashboard verfügbar.


## FrameMaker Publishing Server konfigurieren {#id1678G0Z0TN6}

Sie können FrameMaker Publishing Server \(FMPS\) verwenden, um eine Ausgabe für Ihren DITA-Inhalt zu generieren. Durch die Konfiguration von FMPS können Sie die Ausgabe in mehreren Formaten generieren, die von FMPS unterstützt werden.

>[!NOTE]
>
> Um die Ausgabe mit FMPS zu generieren, müssen Sie über den FMPS-Server verfügen. Informationen zur Installation und Konfiguration finden Sie im Benutzerhandbuch für FrameMaker Publishing Server.

Um AEM Guides für die Verwendung von FMPS zu konfigurieren, aktualisieren Sie die folgenden Eigenschaften der `com.adobe.fmdita.config.ConfigManager` Bundle in der Web-Konsole.

>[!NOTE]
>
> Zugriff http://&lt;server name=&quot;&quot;>:&lt;port>/system/console/configMgr URL zum Öffnen der Web-Konsole.

| Eigenschaft | Beschreibung |
|--------|-----------|
| Anmeldedomäne für FrameMaker Publishing Server | Geben Sie den Domänennamen oder den Arbeitsgruppennamen an, auf dem der FrameMaker Publishing Server gehostet wird. Geben Sie je nach FMPS-Version den Domänennamen wie folgt an:-   **FMPS 2020**: IP-Adresse: 192.168.1.101 <br>- **FMPS 2019 und früher**: IP-Adresse oder Domänenname |
| URL des FrameMaker Publishing Server | Geben Sie die URL des FrameMaker Publishing Server an. Stellen Sie die FMPS-URL basierend auf der FMPS-Version wie folgt bereit:<br>- **FMPS 2020**: `http://<fmps_ip>:<port>` \(http://192.168.1.101:7000\) <br> - **FMPS 2019 und früher**: `http://<fmps_ip>:<port>/fmserver/v1/` |
| FMPS-Version | Geben Sie die Versionsnummer des FrameMaker Publishing Server an. Geben Sie je nach FMPS-Version die Versionsinformationen wie folgt an: <br>- **FMPS 2020**: 2020 <br> - **FMPS 2019 und früher**: 2019 oder 2017 |
| Benutzername und Kennwort für FrameMaker Publishing Server | Geben Sie den Benutzernamen und das Kennwort für den Zugriff auf den FrameMaker Publishing Server an. |
| FMPS-Zeitüberschreitung | \(*Optional*\) Geben Sie die Zeit \(in Sekunden\) an, für die AEM Guides auf eine Antwort vom FrameMaker Publishing Server warten. Wenn keine Antwort in der angegebenen Zeit empfangen wurde, beendet AEM Guides die Veröffentlichungsaufgabe und die Aufgabe wird als fehlgeschlagen gekennzeichnet. <br> Standardwert: 300 Sekunden \(5 Minuten\) |
| Externe AEM-URL | *\(Optional\)* Die AEM-URL, in der der FrameMaker Publishing Server die generierten Ausgabedateien platziert. Beispiel: `http://<server-name>:<port>/`. |
| AEM Admin-Benutzername und -Passwort | *\(Optional\)* Der Benutzername und das Kennwort für einen Administrator Ihrer AEM. Dies wird von FrameMaker Publishing Server zur Kommunikation mit AEM verwendet. |
| Timeout für die Ausführung von FMPS-Aufgaben | Diese Einstellung gilt nur für FMPS 2020. Geben Sie die Zeit \(in Sekunden\) an, nach der FMPS nicht mehr auf die Ausführung dieses Prozesses warten soll. |

## Gemischte Veröffentlichung auf einer vorhandenen AEM-Site konfigurieren {#id1691I0V0MGR}

Wenn Sie über eine AEM-Site verfügen, die DITA-Inhalte enthält, können Sie Ihre AEM Site-Ausgabe so konfigurieren, dass DITA-Inhalte an einer vordefinierten Stelle auf Ihrer Site veröffentlicht werden. Im folgenden Screenshot einer AEM Site-Seite wird beispielsweise die `ditacontent` -Knoten ist zum Speichern von DITA-Inhalten reserviert:

![](assets/publish-in-aem-site.png){width="300" align="left"}

Die verbleibenden Knoten auf der Seite werden direkt im AEM Site-Editor erstellt. Durch die Konfiguration der Veröffentlichungseinstellung zum Veröffentlichen von DITA-Inhalten an einem vordefinierten Speicherort wird sichergestellt, dass keiner Ihrer vorhandenen Nicht-DITA-Inhalte durch den Veröffentlichungsprozess der AEM Guides geändert wird.

Sie müssen die folgenden Konfigurationen auf Ihrer vorhandenen Site durchführen, um die Veröffentlichung von DITA-Inhalten in einem vordefinierten Knoten zu ermöglichen:

- Vorlageneigenschaften Ihrer Site konfigurieren

- Knoten zu Ihrer Site hinzufügen, um DITA-Inhalte zu veröffentlichen


Führen Sie die folgenden Schritte aus, um die Vorlageneigenschaften Ihrer vorhandenen Site zu konfigurieren:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. Navigieren Sie zum Vorlagenkonfigurationsknoten Ihrer Site. Beispielsweise speichert AEM Guides die standardmäßigen Vorlagenkonfigurationen im folgenden Knoten:

   `/libs/fmdita/config/templates/default`

   >[!NOTE]
   >
   > Nehmen Sie keine Anpassungen in den Standardkonfigurationsdateien vor, die im `libs` Knoten. Sie müssen eine Überlagerung der `libs` Knoten in `apps` und aktualisieren Sie die erforderlichen Dateien im `apps` nur Knoten.

1. Fügen Sie die folgenden Eigenschaften hinzu:

   | Eigenschaftsname | Typ | Wert |
   |-------------|----|-----|
   | `topicContentNode` | Zeichenfolge | Geben Sie den Knotennamen an, unter dem Sie den DITA-Inhalt veröffentlichen möchten. Der Standardknoten, unter dem AEM Guides DITA-Inhalte veröffentlicht, lautet beispielsweise: <br>`jcr:content/contentnode` |
   | `topicHeadNode` | Zeichenfolge | Geben Sie den Knotennamen an, unter dem Sie die Metadateninformationen Ihres DITA-Inhalts speichern möchten. Der Standardknoten, in dem AEM Guides Metadateninformationen speichert, lautet beispielsweise: <br>`jcr:content/headnode` |


Der folgende Screenshot zeigt die Eigenschaften, die im Standardvorlagenknoten von AEM Guides hinzugefügt wurden:

![](assets/add-content-node.png){width="800" align="left"}

Wenn Sie das nächste Mal DITA-Inhalte mithilfe der Vorlagenkonfigurationen Ihrer Site veröffentlichen, wird der Inhalt in den Knoten veröffentlicht, die in der `topicContentNode` und `topicHeadNode` Eigenschaften.

Bei vorhandenen Sites müssen Sie jedoch die `topicContentNode` und `topicHeadNode` Knoten.

Führen Sie die folgenden Schritte aus, um die erforderlichen Knoten zu Ihrer vorhandenen Site hinzuzufügen:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. Suchen `jcr:content` innerhalb Ihres Site-Knotens.

1. Hinzufügen `topicContentNode` und `topicHeadNode` Knoten mit demselben Namen, den Sie in den Vorlagenkonfigurationen der Site angegeben haben.


## AEM Site-Ausgabe anpassen {#id166TG0B30WR}

AEM Guides unterstützen das Erstellen von Ausgaben in folgenden Formaten:

- AEM Site

- PDF

- HTML 5
- EPUB
- Benutzerdefinierte Ausgabe über DITA-OT

Für die AEM Site-Ausgabe können Sie verschiedene Designvorlagen mit verschiedenen Ausgabeaufgaben zuweisen. Diese Designvorlagen können den DITA-Inhalt in verschiedenen Layouts rendern. Sie können beispielsweise verschiedene Designvorlagen für interne und externe Zielgruppen angeben.

Sie können auch benutzerdefinierte DITA Open Toolkit \(DITA-OT\)-Plug-ins mit AEM Handbüchern verwenden. Sie können diese benutzerdefinierten DITA-OT-Plug-ins hochladen, um eine PDF-Ausgabe auf eine bestimmte Art zu generieren.

>[!TIP]
>
> Siehe *AEM Site-Veröffentlichung* Abschnitt im Handbuch zu Best Practices[Anhang.md\#](appendix.md#) für Best Practices beim Erstellen AEM Site-Ausgabe.

### Anpassen der Designvorlage zum Generieren der Ausgabe {#customize_xml-add-on}

AEM Guides verwenden eine Reihe vordefinierter Designvorlagen, um AEM Site-Ausgabe zu generieren. Sie können die Designvorlagen der AEM-Handbücher anpassen, um die Ausgabe zu generieren, die Ihrem Corporate Branding entspricht. Eine Designvorlage ist eine Sammlung verschiedener Stile \(CSS\), Skripte \(Server- und Client-seitig\), Ressourcen \(Bilder, Logos und andere Assets\) und JCR-Knoten, die alle diese Ressourcen miteinander verknüpfen. Eine Designvorlage kann so einfach sein wie ein einzelnes serverseitiges Skript mit nur einigen JCR-Knoten oder eine komplexe Kombination von Stilen, Ressourcen und JCR-Knoten. Design-Vorlagen werden vom Publishing-Subsystem AEM Guides verwendet, während AEM Site-Ausgabe generiert wird. Sie steuern die Struktur, das Erscheinungsbild der generierten Ausgabe.

Es gibt keine Einschränkung, wo sich die Ressourcen für die Designvorlage auf dem Server befinden sollten, aber sie sind in der Regel entsprechend ihrer Funktion logisch organisiert. Beispielsweise werden in der Standardvorlage alle JavaScript- und CSS-Dateien gespeichert unter `/etc/designs/fmdita/clientlibs/siteoutput/default` Ordner. Wo immer sich diese Dateien befinden, werden sie durch eine Sammlung von JCR-Knoten verknüpft. Gemeinsam bilden diese JCR-Knoten und die Dateien die gesamte Designvorlage.

Mit der im Lieferumfang von AEM Guides enthaltenen Standard-Designvorlage können Sie die Komponenten für Landingpages, Themen und Suchseiten anpassen. Sie können eine Kopie des Standarddesigns und der entsprechenden Referenzvorlagen erstellen und verschiedene Komponenten angeben, um die gewünschte Ausgabe zu generieren.

Führen Sie die folgenden Schritte aus, um Ihre eigene Designvorlage für AEM Site-Ausgabegenerierung festzulegen:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. Navigieren Sie zum Knoten der Standard-Designvorlage . Der Speicherort des Standardknotens der Designvorlage lautet:

   `/libs/fmdita/config/templates/`

   ![](assets/templates-node.png){width="300" align="left"}

   >[!NOTE]
   >
   > Erstellen Sie eine Kopie der Standard-Designvorlagen aus dem `libs` Ordner in `apps` und nehmen Sie Änderungen in der `apps` Ordner. Außerdem müssen Sie Änderungen an den Vorlagen vornehmen, auf die über den Standardvorlagenknoten verwiesen wird. Die referenzierten Vorlagen befinden sich unter `/libs/fmdita/templates/default/cqtemplates` Knoten. Erstellen Sie eine Kopie der referenzierten Vorlagen im `apps` Ordner, bevor Sie Änderungen vornehmen.

1. Klicken Sie auf *default* -Komponente in *templates* -Knoten, um auf seine Eigenschaften zuzugreifen.

   Die Eigenschaften der Designvorlage AEM Guides werden in der folgenden Tabelle beschrieben.

   | Eigenschaft | Beschreibung |
   |--------|-----------|
   | `landingPageTemplate`, `searchPageTemplate`, `topicPageTemplate`, `shadowPageTemplate` | Geben Sie die `cq:Template` Knoten für diese entsprechenden Seiten \(Landingpage, Suche und Thema\). Standardmäßig wird die `cq:Template` -Knoten für diese Seiten finden Sie unter `/libs/fmdita/templates/default/cqtemplates` Knoten. Dieser Knoten definiert die Struktur und Eigenschaften der Landingpage, der Such- und der Themenseite. <br>Die `shadowPageTemplate` wird verwendet, um den Chunked-Inhalt zu optimieren. Sie müssen den Wert dieser Eigenschaft auf Folgendes festlegen: <br> `fmdita/templates/default/cqtemplates/shadowpage` <br> **Hinweis** Sie müssen einen Wert für die `topicPageTemplate`. Die `landingPageTemplate` und `searchPageTemplate` sind optionale Eigenschaften. Wenn Sie nicht möchten, dass die Such- und Landingpages generiert werden, geben Sie diese Eigenschaften nicht an. |
   | `title` | Ein beschreibender Name Ihrer Designvorlage. |
   | `topicContentNode` | Der Speicherort des Knotens, der den DITA-Inhalt auf einer Themenseite enthält. Der Pfad ist relativ zur Themenseite. |
   | `topicHeadNode` | Der Speicherort des Knotens, der die Kopfwerte \(oder Metadaten\) enthält, die aus dem DITA-Inhalt abgeleitet wurden. Der Pfad ist relativ zur Themenseite. |
   | `tocNode` | Der Speicherort des Knotens, der das Inhaltsverzeichnis enthalten wird. Der Pfad ist relativ zur Landingpage oder zum Zielpfad. |
   | `basePathProp` | Der Eigenschaftsname zum Speichern des Pfads des Stammverzeichnisses der veröffentlichten Site. |
   | `indexPathProp` | Der Eigenschaftsname zum Speichern des Pfads der Landingpage/Indexseite der veröffentlichten Site. |
   | `pdfPathProp` | Der Eigenschaftsname zum Speichern des Themen-PDF-Pfads, wenn die PDF-Generierung des Themas aktiviert ist. |
   | `pdfTypeProp` | Der Eigenschaftsname zum Speichern des Typs der PDF-Generierung. Derzeit enthält diese Eigenschaft immer &quot;Thema&quot;. |
   | `searchPathProp` | Der Eigenschaftsname zum Speichern des Pfads der Suchseite, wenn die Vorlage eine Suchseite enthält. |
   | `siteTitleProp` | Der Eigenschaftsname zum Speichern des Titels der veröffentlichten Site. Dieser Titel ist normalerweise mit dem Titel der zu veröffentlichenden Karte identisch. |
   | `sourcePathProp` | Der Eigenschaftsname zum Speichern des Pfads des Quell-DITA-Themas für die aktuelle Seite. |
   | `tocPathProp` | Der Eigenschaftsname zum Speichern des Pfads des TOC-Stammverzeichnisses für die veröffentlichte Site. |


>[!NOTE]
>
> Nachdem Sie einen benutzerdefinierten Designvorlagenknoten erstellt haben, müssen Sie die Option Design in den AEM Site-Ausgabevorgaben aktualisieren, um den benutzerdefinierten Designvorlagenknoten zu verwenden.

Weitere Informationen finden Sie unter [Erstellen der ersten Adobe Experience Manager 6.3-Website](https://helpx.adobe.com/experience-manager/using/first_aem63_website.html) und [Grundlagen](https://helpx.adobe.com/de/experience-manager/6-3/sites/developing/using/the-basics.html) der Entwicklung Ihrer eigenen Website auf AEM.

### Dokumenttitel zum Generieren AEM Site-Ausgabe verwenden

Beim Generieren AEM Site-Ausgabe spielt die Art und Weise, wie URLs generiert werden, eine wichtige Rolle bei der Entdeckung Ihres Inhalts. Wenn Sie UUID-basierte Dateinamen verwenden, wäre das Generieren von URLs basierend auf der UUID Ihrer Dateien nicht suchfreundlich. Als Administrator oder Herausgeber haben Sie die Kontrolle darüber, wie Sie die URLs für Ihre AEM Site-Ausgabe generieren möchten. AEM Handbücher bieten eine Konfiguration, mit der Sie die URLs AEM Site-Ausgabe mithilfe des Dateinamens und nicht der UUID-basierten Dateinamen generieren können. Standardmäßig ist diese Option bei UUID-basierten Dateisystemen aktiviert. Dies bedeutet, dass beim Generieren AEM Site-Ausgabe für UUID-basierte Dateisysteme die Dateinamen zum Generieren der URLs und nicht der UUIDs der Dateien verwendet werden.

Beim Generieren AEM Site-Ausgabe spielt die Art und Weise, wie URLs generiert werden, eine wichtige Rolle bei der Entdeckung Ihres Inhalts. Bei nicht UUID-basierten Dateisystemen wird die AEM Site-Ausgabe unter Verwendung der Dateinamen und nicht der Dateinamen generiert. Als Administrator oder Herausgeber haben Sie die Kontrolle darüber, wie Sie die URLs für Ihre AEM Site-Ausgabe generieren möchten. AEM Handbücher bieten eine Konfiguration, mit der Sie die URLs AEM Site-Ausgabe mithilfe des Dateinamens und nicht der Dateinamen generieren können. Standardmäßig ist diese Option deaktiviert. Dies bedeutet, dass beim Generieren AEM Site-Ausgabe die Dateinamen zum Generieren der URLs und nicht des Dateinamens verwendet werden. Sie können die URLs anhand der Dateinamen generieren, indem Sie diese Option aktivieren.

>[!NOTE]
>
> Sie können Regeln weiter konfigurieren, sodass nur ein Zeichensatz in den URLs einer AEM Site-Ausgabe zulässig ist. Weitere Informationen finden Sie unter [Konfigurieren von Bereinigungsregeln für Dateinamen zum Erstellen von Themen und Veröffentlichen AEM Site-Ausgabe](#id2164D0KD0XA).

Um die URLs zu konfigurieren, die in AEM Site-Ausgabe generiert werden, führen Sie die folgenden Schritte aus:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Wählen Sie die **Verwenden des Titels für AEM Site-Seitennamen** -Option.

   >[!NOTE]
   >
   > Wenn Sie die Ausgabe mit den Dateinamen generieren möchten, deaktivieren Sie diese Option.

1. Klicken Sie auf **Speichern**.


### Konfigurieren von Bereinigungsregeln für Dateinamen zum Erstellen von Themen und Veröffentlichen AEM Site-Ausgabe {#id2164D0KD0XA}

Als Administrator können Sie eine Liste gültiger Sonderzeichen definieren, die in Dateinamen zulässig sind und letztendlich die URL einer AEM Site-Ausgabe bilden. In früheren Versionen konnten Benutzer Dateinamen mit Sonderzeichen wie `@`, `$`, `>`und mehr. Diese Sonderzeichen führten bei der Generierung AEM Site-Seiten zu einer kodierten URL.

Ab Version 3.8 wurden Konfigurationen hinzugefügt, um eine Liste von Sonderzeichen zu definieren, die in Dateinamen zulässig sind. Standardmäßig enthält die gültige Dateinamenkonfiguration &quot;`a-z A-Z 0-9 - _`&quot;. Dies bedeutet, dass Sie beim Erstellen einer Datei beliebige Sonderzeichen im Dateinamen haben können, diese jedoch intern durch einen Bindestrich \(`-`\) im Dateinamen. Sie können beispielsweise den Titel der Datei als Einführung 1 oder Introduction@1 festlegen. Der entsprechende Dateiname, der für beide Fälle generiert wurde, wäre Einführung-1.

Beachten Sie bei der Definition einer Liste gültiger Zeichen, dass diese Zeichen &quot;`*/:[\]|#%{}?&<>"/+`&quot; und `a space` wird immer durch einen Bindestrich \(`-`\).

>[!NOTE]
>
> Wenn Sie die Liste der gültigen Sonderzeichen nicht konfigurieren, kann der Dateierstellungsprozess zu unerwarteten Ergebnissen führen.

So konfigurieren Sie die gültigen Sonderzeichen in Dateinamen und AEM Site-Ausgabe:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf *com.adobe.fmdita.common.SanitizeNodeNameImpl* Bundle.

1. Im **Unzulässige Zeichensätze für die Veröffentlichung in AEM Sites** -Eigenschaft festlegen, stellen Sie sicher, dass die -Eigenschaft auf ```'<>`@$```. Sie können dieser Liste weitere Sonderzeichen hinzufügen. Diese müssen jedoch über die folgenden Sonderzeichen verfügen.

   >[!NOTE]
   >
   > Sie können auch die anderen Eigenschaften konfigurieren, z. B. **Kleinbuchstaben verwenden** in Dateinamen, **Trennzeichen** um ungültige Zeichen zu verarbeiten, und **Maximale Zeichenanzahl** in den Dateinamen erlaubt.

1. Klicken Sie auf **Speichern**.

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Im **Regex für gültige Zeichen** -Eigenschaft festlegen, stellen Sie sicher, dass die -Eigenschaft auf `[-a-zA-Z0-9_]`. Sie können dieser Liste weitere Zeichen hinzufügen. Sie muss jedoch diese einfachen Zeichen enthalten und die Liste muss mit einem Bindestrich \(`-`\).

   >[!NOTE]
   >
   > Diese Eigenschaft definiert die Liste der gültigen Zeichen, die zum Erstellen einer neuen Datei verwendet werden.

1. Klicken Sie auf **Speichern**.


### Reduzieren AEM Site-Knotenstruktur konfigurieren

Wenn Sie AEM Site-Ausgabe generieren, wird intern ein Knoten für jedes Element in den Themen erstellt. Für eine DITA-Map mit Tausenden von Themen kann diese Knotenstruktur zu tief werden. Diese Art von tief verschachtelter Knotenstruktur kann Leistungsprobleme bei größeren Sites haben. Die folgende Momentaufnahme zeigt eine tief verschachtelte Knotenstruktur für eine AEM Site-Ausgabe:

![](assets/deep-nested-aem-site-node-structure.png){width="300" align="left"}

Beachten Sie, dass im obigen Schnappschuss für jeden `p` -Element und die nachfolgenden Unterelemente sowie eine ähnliche Struktur werden für jedes andere Element erstellt, das im Thema verwendet wird.

Mit AEM Guides können Sie konfigurieren, wie die Knotenstruktur AEM Site-Ausgabe intern erstellt wird. Sie können die Knotenstruktur bei bestimmten Elementen reduzieren. Das bedeutet, dass Sie ein Element definieren können, das als Hauptelement betrachtet wird. Alle darin enthaltenen Unterelemente werden mit dem Hauptelement zusammengeführt. Wenn Sie beispielsweise die `p` -Element, dann jedes Element, das innerhalb der `p` -Element wird mit dem Hauptelement zusammengeführt `p` -Element. Für kein Unterelement innerhalb der Variablen `p` -Element. Der folgende Schnappschuss zeigt die Knotenstruktur, reduziert auf `p` element:

![](assets/flattened-aem-site-node-structure.png){width="300" align="left"}

So reduzieren Sie AEM Site-Knotenstruktur:

1. Geben Sie das Element an, bei dem Sie die Knotenstruktur reduzieren möchten.

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

1. Aktivieren Sie die Reduzierungskonfiguration des Site-Knotens in der configMgr.

   1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

      Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

      ```http
      http://<server name>:<port>/system/console/configMgr
      ```

   1. Suchen Sie nach und klicken Sie auf *com.adobe.dxml.flattening.FlateningConfigurationService* Bundle.

   1. Wählen Sie die **Eigenschaft flattening.enabled** -Option.

   1. Klicken Sie auf **Speichern**.


>[!IMPORTANT]
>
> Wenn Sie Änderungen an der Datei elementmapping.xml vorgenommen haben, stellen Sie sicher, dass Sie configMgr öffnen und jedes Bundle speichern, damit Änderungen wirksam werden.

Wenn Sie jetzt die AEM Site-Ausgabe generieren, befinden sich die Knoten im `p` -Element reduziert und im `p` -Element selbst. Sie finden die neuen Reduzierungseigenschaften für die `p` -Element in CRXDE.

![](assets/flatten-aem-site-note-props-crxde.png){width="650" align="left"}

**Reduzieren der Struktur AEM Site-Anmerkungen verhindern**

Ähnlich wie beim Festlegen des Knotens, der in AEM Site-Ausgabe reduziert werden soll, können Sie auch ein Element angeben, das Sie aus dieser Konfiguration ausschließen möchten. Beispiel: Wenn Sie Knoten reduzieren möchten bei `body` -Element, Sie möchten jedoch keine `table` -Element in `body` zum Reduzieren hinzufügen, können Sie die Eigenschaft exclude innerhalb der `table` -Elements.

So schließen Sie die `table` -Element aus der Reduzierung hinzufügen, fügen Sie die folgende Eigenschaft zum `table` Definition des Elements:

`<preventancestorflattening>true|false</preventancestorflattening>`

### Versionierung für gelöschte Seiten in AEM Site-Ausgabe konfigurieren

Wenn Sie AEM Site-Ausgabe mit **Löschen und** Erstellen ****für die Einstellung Vorhandene Ausgabeseiten ausgewählt wurde, wird eine Version für die zu löschende(n) Seite(n\) erstellt. Sie können das System so konfigurieren, dass vor dem Löschen die Erstellung einer Version angehalten wird.

Führen Sie die folgenden Schritte aus, um die Erstellung einer Version für die zu löschende(n\) Seite zu stoppen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf *com.adobe.fmdita.config.ConfigManager* Bundle.

1. Auswählen **Keine Version für gelöschte Seiten erstellen** -Option.

   >[!NOTE]
   >
   > Wenn diese Option aktiviert ist, können Benutzer alle Seiten direkt löschen, ohne eine Version für sie zu erstellen. Wenn die Option nicht ausgewählt ist, wird eine Version erstellt, bevor die Seite\(n\) gelöscht wird.

1. Klicken Sie auf **Speichern**.

## Verwenden von Metadaten zur Veröffentlichung der Ausgabe über DITA-OT {#id191LF0U0TY4}

AEM Guides bieten eine Möglichkeit, benutzerdefinierte Metadaten beim Veröffentlichen der Ausgabe mithilfe von DITA-OT zu übergeben. Als Administrator und Herausgeber müssen Sie die folgenden Aufgaben ausführen, um benutzerdefinierte Metadaten in der veröffentlichten Ausgabe zu konfigurieren und zu verwenden:

- Fügen Sie als Administrator die erforderlichen Metadaten im System hinzu, damit sie auf der Seite Eigenschaften der DITA-Zuordnung verfügbar gemacht werden.

- Fügen Sie als Administrator die benutzerdefinierten Metadaten in die Metadatenliste ein, damit sie in der DITA-Map-Konsole angezeigt werden.

- Konfigurieren und fügen Sie als Publisher die benutzerdefinierten Metadaten mit der DITA-Zuordnung hinzu und generieren Sie die erforderliche Ausgabe.


Um die erforderlichen Metadaten im System hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Assets** aus der Liste der Tools.

1. Klicken Sie auf **Metadatenschemata** Kachel.

   Die Seite Metadatenschema-Formulare wird angezeigt.

1. Wählen Sie die **default** aus der Liste.

   >[!NOTE]
   >
   > Die Eigenschaften, die auf der Seite Eigenschaften für eine DITA-Zuordnung angezeigt werden, stammen aus diesem Formular.

1. Klicken Sie auf **Bearbeiten**.

1. Fügen Sie die benutzerdefinierten Metadaten hinzu, die Sie in Ihren veröffentlichten Ausgaben verwenden möchten. Beispielsweise werden wir Zielgruppen-Metadaten mithilfe der folgenden Schritte hinzufügen:

   1. Aus dem **Formular erstellen** Komponentenliste, Drag &amp; Drop **Einzelzeilentext** auf das Formular.

   1. Wählen Sie das neue Feld aus, um die **Einstellungen** des Felds.

   1. Im **Feldbezeichnung**, geben Sie den Metadatennamen ein: Zielgruppe.

   1. Im **Zu Eigenschaft zuordnen** festlegen, geben Sie an./jcr:content/metadata/&lt;name of=&quot;&quot; the=&quot;&quot; metadata=&quot;&quot;>. Für unser Beispiel setzen wir es auf ./jcr:content/metadata/audience.

   Fügen Sie mithilfe dieser Schritte alle erforderlichen Metadatenparameter hinzu.

1. Klicken Sie auf **Speichern**.


Der neue Parameter wird jetzt auf der Seite Eigenschaften für alle DITA-Maps angezeigt.

![](assets/properties-page-custom-metadata.PNG){width="650" align="left"}

Als Nächstes müssen Sie die benutzerdefinierten Metadaten in der DITA-Map-Konsole verfügbar machen. Führen Sie die folgenden Schritte aus, um die benutzerdefinierten Metadaten auf der DITA Map-Dashboards verfügbar zu machen:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. Greifen Sie auf die Datei metadataList zu, die unter folgendem Speicherort verfügbar ist:

   /libs/fmdita/config/metadataList

   >[!NOTE]
   >
   > Die Datei &quot;metadataList&quot;enthält eine Liste der Eigenschaften, die in der Variablen **Eigenschaften** Dropdown-Liste einer DITA-Map im Landkarten-Dashboard. Standardmäßig sind in dieser Datei vier Eigenschaften aufgelistet: docstate, dc:language, dc:description und dc:title.

1. Fügen Sie die benutzerdefinierten Metadaten hinzu, die Sie auf der Seite &quot;Metadatenschema-Forms&quot;hinzugefügt haben. Fügen Sie für unser Beispiel den Zielgruppenparameter am Ende der Standardliste hinzu.

1. Klicken Sie auf **Alle speichern**.


Jetzt werden die benutzerdefinierten Metadaten in der DITA-Map-Konsole angezeigt. **Eigenschaften** Dropdown-Liste.

Als Herausgeber müssen Sie schließlich die benutzerdefinierten Metadaten in die veröffentlichte Ausgabe aufnehmen. Um die benutzerdefinierten Metadaten beim Generieren der Ausgabe zu verarbeiten, führen Sie die folgenden Schritte aus:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnung, die Sie veröffentlichen möchten.

1. Wählen Sie die DITA-Map-Datei aus und öffnen Sie die zugehörige Eigenschaftenseite.

1. Geben Sie auf der Seite Eigenschaften den Wert für die benutzerdefinierten Metadaten an. Für unser Beispiel haben wir den Wert &quot;External&quot;für den Zielgruppenparameter angegeben.

   ![](assets/properties-page-custom-metadata-value.png){width="650" align="left"}

1. Klicken Sie auf **Speichern und schließen**.

1. Klicken Sie auf die DITA-Zuordnungsdatei, um die DITA-Zuordnungskonsole zu öffnen.

1. Im **Ausgabevorgaben** -Registerkarte die Ausgabevorgabe auswählen, die Sie zum Generieren der Ausgabe verwenden möchten.

1. Klicken Sie auf **Bearbeiten**.

1. Aus dem **Eigenschaften** Wählen Sie die Eigenschaften aus, die Sie an den Veröffentlichungsprozess weitergeben möchten.

   ![](assets/props-in-publish-output.PNG){width="650" align="left"}


Die ausgewählten Eigenschaften/Metadaten werden an den Veröffentlichungsprozess übergeben und in der endgültigen Ausgabe verfügbar gemacht.

## DITA-Elementzuordnung mit AEM Komponenten anpassen {#id1679J600HEL}

DITA-Elemente in AEM Guides werden ihren entsprechenden AEM Komponenten zugeordnet. AEM Guides verwenden diese Zuordnung in Workflows wie Veröffentlichung und Überprüfung, um DITA-Elemente in eine entsprechende AEM zu konvertieren. Die Zuordnung wird im Abschnitt `elementmapping.xml` -Datei, auf die über den Modus CRXDE Lite zugegriffen werden kann. Greifen Sie im Modus CRXDE Lite auf die folgende URL zu:

`/libs/fmdita/config/elementmapping.xml`

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

   - COMPOSITE: Element zur Komponente *Die Zuordnung wird für untergeordnete Elemente fortgesetzt* sowie

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
       <class>- topic/title</class> 
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

   - Wenn `rel=source`, dann den Wert von `href` in Bezug auf die DITA-Quelldatei aufgelöst, die derzeit verarbeitet wird. Der Wert von `href` aufgelöst und in den Wert von `fileReference` -Eigenschaft.

   - Wenn `rel=target`, dann den Wert von `href` in Bezug auf den Speicherort der Stammveröffentlichung aufgelöst. Der Wert von `href` aufgelöst und in den Wert von `fileReference` -Eigenschaft.

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
    <attribute from="attrname" to="propname" ispath="true|false" rel="source|target" />     
    </attributemap>     
    <skip>true|false</skip> 
</ditaelement>
```

In der folgenden Tabelle werden die Elemente im DITA-Elementschema beschrieben:

| Element | Beschreibung |
|-------|-----------|
| `<ditaelement>` | Der Knoten der obersten Ebene für jedes Zuordnungselement. |
| `<class>` | Das Klassenattribut des DITA-Zielelements, für das Sie die Komponente schreiben. <br>Beispielsweise lautet das Klassenattribut für das DITA-Thema: <br>`topic/topic` |
| `<componentpath>` | Der CRXDE-Pfad der zugeordneten AEM-Komponente. |
| `<type>` | Mögliche Werte: <br>- **COMPOSITE**: Verarbeiten von untergeordneten Elementen <br>- **STANDALON**: Überspringt die Verarbeitung untergeordneter Elemente |
| `<attributeprop>` | Wird für die Zuordnung von serialisierten DITA-Attributen und -Werten zu AEM Knoten als Eigenschaft verwendet. Wenn Sie beispielsweise `<note type="Caution">` -Element und die für dieses Element zugeordnete Komponente `<attributeprop>attr_t</ attributeprop>`, dann werden das Attribut und der Wert des Knotens serialisiert auf `attr_t` Eigenschaft des entsprechenden AEM-Knotens \( `attr_t->type="caution"`\). |
| `<textprop>propname_t</textprop>` | Speichern Sie die `getTextContent()` Ausgabe in Eigenschaft definiert durch `propname_t.` **Hinweis:**  Dies ist eine optimierte Eigenschaft. |
| `<xmlprop>propname_x </xmlprop>` | Speichern Sie serialisiertes XML dieses Knotens in der Eigenschaft, die durch definiert wird. `propname_x.` **Hinweis:** Dies ist eine optimierte Eigenschaft. |
| `<xpath>` | Wenn das XPath-Element in der Elementzuordnung bereitgestellt wird, sollte die XPath-Bedingung zusammen mit dem Elementnamen und der Klasse ebenfalls erfüllt sein, damit die Komponentenzuordnung verwendet wird. |
| `<target>` | Platzieren Sie für das DITA-Element im CRX-Repository an dem angegebenen Speicherort. <br>Mögliche Werte:<br>- **head**: Unter dem Kopfknoten <br>- **text**: Unter dem Absatzknoten |
| `<wrapelement>` | Das HTML-Element, in das der Inhalt eingeschlossen werden soll. |
| `<wrapclass>` | Der Elementwert der Eigenschaft `wrapclass.` |
| `<attributemap>` | Container-Knoten, der eine oder mehrere `<attribute>` Knoten. |
| `<attribute from="attrname" to="propname" ispath="true|false" rel="source|target" />` | Ordnet die DITA-Attribute AEM Eigenschaften zu:<br>- **`from`**: DITA-Attributname<br>- **`to`**: Name der Komponenteneigenschaft <br>- **`ispath`**: Wenn das Attribut ein Pfadwert ist \(z. B.: *image*\)<br>- **`rel`**: Wenn der Pfad die Quelle oder das Ziel ist <br>**Hinweis:** Wenn `attrname` beginnt mit `%`, dann map `attrname minus '%'` to prop &#39; `propname`&quot;. |

**Weitere Hinweise**

- Wenn Sie die standardmäßige Elementzuordnung überschreiben möchten, sollten Sie die Änderungen nicht in der Standardeinstellung `elementmapping.xml` -Datei. Sie sollten eine neue Mapping-XML-Datei erstellen und die Datei an einem anderen Speicherort ablegen, vorzugsweise in dem von Ihnen erstellten benutzerdefinierten Apps-Ordner.

- Im `elementmapping.xml` -Datei, gibt es viele Zuordnungseinträge, die auf die Komponente fmdita/components/dita/wrapper verweisen. Wrapper ist eine generische Komponente, die relativ einfache DITA-Konstrukte rendert, die Eigenschaften auf ihrem Site-Knoten verwenden, um relevante HTML zu generieren. Sie verwendet die `wrapelement` -Eigenschaft zum Generieren von einschließenden Tags und Delegieren des untergeordneten Renderings an die entsprechenden Komponenten. Dies ist nützlich in Fällen, in denen Sie nur eine Container-Komponente benötigen. Anstatt eine neue Komponente zu erstellen, die ein bestimmtes Container-Tag wie `div` oder `p`, können Sie die Wrapper-Komponente mit der `wrapelement` und `wrapclass` -Eigenschaften verwenden, um denselben Effekt zu erzielen.

- Es wird nicht empfohlen, große Textmengen in String JCR-Eigenschaften zu speichern. Die optimierte Berechnung des Eigenschaftstyps bei der Ausgabegenerierung stellt sicher, dass große Textinhalte nicht als Zeichenfolgentyp gespeichert werden. Wenn stattdessen Inhalte gespeichert werden müssen, die größer als ein bestimmter Schwellenwert sind, wird der Eigenschaftstyp in binär geändert. Standardmäßig ist dieser Schwellenwert auf 512 Byte konfiguriert, kann jedoch im Configuration Manager \(*com.adobe.fmdita.config.ConfigManager*\) durch Ändern der **Als binären Schwellenwert speichern** -Einstellung.

- Wenn Sie einige \(und nicht alle\) der Elementzuordnungen überschreiben möchten, müssen Sie nicht die gesamte `elementmapping.xml` -Datei. Sie müssen eine neue XML-Zuordnungsdatei erstellen und nur die Elemente definieren, die Sie überschreiben.

- Nachdem Sie die XML-Datei am benutzerdefinierten Speicherort erstellt haben, aktualisieren Sie die `Override Element Mapping` -Einstellung in `com.adobe.fmdita.config.ConfigManager` Bundle.


## DITA-Map-Konsole anpassen {#id188HC08M0CZ}

AEM Guides bieten Ihnen die Flexibilität, die Funktionen der DITA-Map-Konsole zu erweitern. Wenn Sie beispielsweise eine Reihe von Berichten haben, die sich von den in AEM Guides verfügbaren unterscheiden, können Sie diese Berichte zur Zuordnungskonsole hinzufügen. Um die Zuordnungskonsole anzupassen, müssen Sie eine AEM Client-Bibliothek \(oder ClientLib\) erstellen, die den Code enthält, um die benötigten Funktionen auszuführen.

>[!NOTE]
>
> Eine direkte Änderung an Seitenkomponenten wird nicht empfohlen, da sie durch neue Versionen des Produkts überschrieben wird.

AEM Guides bieten die `apps.fmdita.dashboard-extn` Kategorie zum Anpassen der Zuordnungskonsole. Bei jedem Laden der Zuordnungskonsole wird die unter der `apps.fmdita.dashboard-extn` -Kategorie ausgeführt und geladen wird.

>[!NOTE]
>
> Weitere Informationen zum Erstellen AEM Client-Bibliothek finden Sie unter [Verwenden Client-seitiger Bibliotheken](https://helpx.adobe.com/de/experience-manager/6-4/sites/developing/using/clientlibs.html).

## Verarbeiten der Bilddarstellung während der Ausgabegenerierung {#id177BF0G0VY4}

AEM enthält eine Reihe von Standard-Workflows und Medien-Handles zur Verarbeitung von Assets. In AEM gibt es vordefinierte Workflows für die Verarbeitung von Assets für die häufigsten MIME-Typen. Normalerweise erstellt AEM für jedes Bild, das Sie hochladen, mehrere Ausgabeformate desselben Binärformats. Diese Ausgabedarstellungen können unterschiedlich groß sein, mit einer anderen Auflösung, einem hinzugefügten Wasserzeichen oder anderen geänderten Eigenschaften. Weitere Informationen dazu, wie AEM mit Assets umgehen, finden Sie unter [Verarbeitung von Assets mithilfe von Medien-Handlern und Workflows](https://helpx.adobe.com/experience-manager/6-5/assets/using/media-handlers.html) in AEM Dokumentation.

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

Die `mimetype` -Element gibt den MIME-Typ des Dateiformats an. Die `rendition output` -Element gibt den Typ des Ausgabeformats und den Namen der Ausgabedarstellung an \(z. B. `cq5dam.web.1280.1280.jpeg`\), die zum Veröffentlichen der angegebenen Ausgabe verwendet werden soll. Sie können die Bildausgabeformate angeben, die für alle unterstützten Ausgabeformate verwendet werden sollen - AEMSITE, PDF, HTML5, EPUB und CUSTOM.

Wenn die angegebene Ausgabedarstellung nicht vorhanden ist, sucht AEM Publishing-Prozess für Guides zunächst nach der Web-Ausgabe des angegebenen Bildes. Wenn selbst die Webausgabe nicht gefunden wird, wird die ursprüngliche Ausgabe des Bildes verwendet.

>[!NOTE]
>
> Diese Bildausgabeformate steuern nur die Ausgabegenerierung. Die Webausgabe eines Bildes wird verwendet, wenn Sie ein Dokument zur Vorschau oder Überprüfung öffnen.

## Konfigurieren des Zeitrahmens für die automatische Bereinigung für den Ausgabedarstellungsverlauf {#id19AAI070V8Q}

Wenn Sie eine Ausgabe generieren, wird die Ausgabe zusammen mit den Ausgabsprotokollen erstellt. Bei großen DITA-Maps können diese Protokolle viel Platz in Ihrem Repository beanspruchen. Standardmäßig werden die Protokolle am folgenden Speicherort im Repository gespeichert:

/var/dxml/metadata/outputHistory/

Über einen bestimmten Zeitraum konnte die kollektive Größe aller Protokolldateien in GBs dargestellt werden. AEM Guides können Sie einen Zeitraum konfigurieren, um diese Protokolldateien im Repository zu speichern. Nach dem angegebenen Zeitraum werden die Protokolle zusammen mit dem Ausgabegenerierungsverlauf aus dem Repository gelöscht.

>[!NOTE]
>
> Der Ausgabegenerierungsverlauf ist der Protokolleintrag in der Liste Erzeugte Ausgaben auf der Registerkarte Ausgaben .

Die Konfiguration der Verlaufsbereinigungsfunktion wirkt sich auf die Generierung der Ausgabe für alle DITA-Maps im Repository aus. Auf der Registerkarte &quot;Outputs&quot;einer DITA-Zuordnung wird der Verlauf nach der angegebenen Anzahl von Tagen und zu der in der Einstellung festgelegten Zeit bereinigt.

>[!NOTE]
>
> Das Entfernen der Protokolldateien und des Ausgabegenerierungsverlaufs hat keine Auswirkungen auf die generierte Ausgabe.

Führen Sie die folgenden Schritte aus, um einen Tag und eine Uhrzeit für die Bereinigung des Ausgabedarstellungsverlaufs und der -protokolle festzulegen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Im **Bereinigungszeitraum für den Output-Verlauf** -Eigenschaft festlegen, geben Sie die Anzahl der Tage an, nach denen der Ausgabedarstellungsverlauf zusammen mit den Ausgabsprotokollen bereinigt wird. Standardmäßig ist er auf 5 Tage eingestellt. Wenn Sie diese Funktion deaktivieren möchten, legen Sie diese Eigenschaft auf 0 fest.

1. Im **Bereinigungszeit des Ausgabeverlaufs** -Eigenschaft, geben Sie den Zeitpunkt an, zu dem der Bereinigungsprozess eingeleitet wird. Standardmäßig ist sie auf 0:00 \(oder 12:00 Mitternacht\) eingestellt. Zu diesem Zeitpunkt wird der Bereinigungsprozess täglich für Ausgaben ausgeführt, die vor der in der Variablen **Bereinigungszeitraum für den Output-Verlauf** -Eigenschaft.

   >[!NOTE]
   >
   > Standardmäßig wird die Bereinigungsfunktion jeden Mitternacht bei Ausgaben ausgeführt, die älter als 5 Tage sind.

1. Klicken Sie auf **Speichern**.


## Ändern der zuletzt generierten Ausgabelistenbegrenzung {#id1679JH0H0O2}

Sie können die maximale Anzahl der generierten Ausgaben ändern, die auf der Registerkarte &quot;Ausgaben&quot;für eine DITA-Zuordnung angezeigt werden. Standardmäßig wird eine Liste der letzten 25 generierten Ausgaben angezeigt. Um die Anzahl der Ausgaben zu ändern, die in der Liste angezeigt werden sollen, aktualisieren Sie die **Begrenzung der Ausgabenliste** -Einstellung in `com.adobe.fmdita.config.ConfigManager` Bundle.

>[!TIP]
>
> Siehe *Ausgabeverlauf* Abschnitt im Handbuch zu Best Practices[Anhang.md\#](appendix.md#) für Best Practices zum Arbeiten mit dem Ausgabedarstellungsverlauf.

## Leistungsoptimierung der Ausgabenerstellung {#id176LB050VUI}

Mit AEM Guides können Sie die Poolgröße der Ausgabegenerierungsprozesse konfigurieren, die die Anzahl der gleichzeitig ausgeführten Output-Generierungsprozesse steuert. Standardmäßig ist die Größe des Prozess-Pools auf die Anzahl der in Ihrem System verfügbaren Prozessorkerne plus 1 eingestellt. Sie können diesen Wert in 1 ändern, falls Sie eine sequenzielle Veröffentlichung wünschen. In diesem Fall wird die erste Veröffentlichungsaufgabe ausgeführt und die nächste Veröffentlichungsaufgabe wird in der Veröffentlichungswarteschlange gespeichert.

Um die Poolgröße für die Verarbeitung der Ausgabenerzeugung zu ändern, aktualisieren Sie die **Erstellungspoolgröße** -Einstellung in `com.adobe.fmdita.publish.manager.PublishThreadManagerImpl` Bundle.

