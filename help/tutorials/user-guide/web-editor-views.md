---
title: Web-Editor-Ansichten
description: Dokumente im Autoren-, Quell- und Vorschaumodus anzeigen. Erfahren Sie, wie Sie Inhalte basierend auf bedingten Filtern anzeigen, die Markierungen von Änderungen verfolgen und ein Thema als PDF in AEM Guides exportieren können.
exl-id: 86d8abc2-1d0e-4744-91c9-848c00447971
source-git-commit: 3cc7a9bf91881ed09173077be7d7fc7705295e4b
workflow-type: tm+mt
source-wordcount: '1449'
ht-degree: 0%

---

# Web-Editor-Ansichten {#id204GK0D0V5Z}

Der Web Editor von AEM Guides unterstützt das Anzeigen von Dokumenten in drei verschiedenen Modi oder Ansichten:

## Autor

Dies ist eine typische Ansicht des Web-Editors, was Sie sehen, was Sie \(WYSISYG\) erhalten. Sie können das Thema wie in jedem normalen Rich-Text-Editor bearbeiten. In der Autorenansicht haben Sie die Möglichkeit, eine Revision des Dokuments zu speichern, Inhalte zu suchen und zu ersetzen, Elemente einzufügen, Hyperlinks einzufügen, Inhaltsreferenz einzufügen und vieles mehr.

>[!NOTE]
>
> Wenn Sie den Inhaltsverweis verwenden, wird der referenzierte Inhalt auch in der Autorenansicht in blauer Farbe angezeigt. Der referenzierte Inhalt kann nicht bearbeitet werden.

## Quelle

Die Quellansicht zeigt die zugrunde liegende XML an, aus der das Thema besteht. Wenn Sie es bequem haben, direkt mit XML zu arbeiten, sollten Sie die Quellansicht verwenden. Sie können in dieser Ansicht nicht nur reguläre Textänderungen vornehmen, sondern auch Elemente und Attribute mithilfe des Smart-Katalogs hinzufügen oder Text, Elemente oder Attribute suchen und ersetzen.

- Um den Smart-Katalog aufzurufen, platzieren Sie den Cursor am Ende jedes Element-Tags, in das Sie das neue Element einfügen möchten, und geben Sie &quot;&lt;&quot;ein. Der Editor zeigt eine Liste aller gültigen XML-Elemente an, die Sie an diesem Speicherort einfügen können. Verwenden Sie die Pfeiltasten, um das einzufügende Element auszuwählen, und drücken Sie die Eingabetaste. Wenn Sie die schließende Klammer &quot;\> eingeben, wird das schließende Tag für das Element automatisch hinzugefügt.

  ![](images/smart-catalog-elements.png){width="400" align="left"}

- Sie können ein Element auch einfach in der Quellansicht ändern. Wenn Sie beispielsweise das öffnende -Tag eines `p` Element zu `note`, dann das Ende `p` -Tag automatisch in `/note`. Wenn Sie ein Element durch ein falsches Element ersetzen, wird Ihnen sofort der Validierungsfehler angezeigt.

- Wenn Sie einem Element ein Attribut hinzufügen möchten, platzieren Sie den Cursor in das Element-Tag und drücken Sie die Leertaste. Eine Liste gültiger Attribute für dieses Element wird im Smart-Katalog angezeigt. Wählen Sie mithilfe der Pfeiltasten das gewünschte Element aus und drücken Sie die Eingabetaste , um das Element einzufügen. Um einen Wert für das Attribut anzugeben, geben Sie das Gleichheitszeichen \(=\) ein und der Editor gibt automatisch die öffnenden und schließenden Anführungszeichen &quot;&quot; ein, wobei Sie den Wert des Attributs angeben können.

  ![](images/smart-catalog-attribute.png){width="350" align="left"}

- In der Quellansicht gibt es eine Option für den automatischen Einzug, mit der der XML-Code in einem lesbaren und darstellbaren Format neu organisiert wird. Wenn Sie einen Text auswählen und von der Autoren- zur Quelle- oder zur Autorenansicht wechseln, wird der ausgewählte Text auch in der anderen Ansicht hervorgehoben.
- Eine weitere leistungsstarke Funktion in der Quellansicht ist die XML-Validierung in Ihrem Dokument. Wenn Sie ein Dokument öffnen, das ungültiges XML enthält, wird es in der Quellansicht mit Informationen zu ungültigem XML geöffnet. Im folgenden Screenshot erhalten Sie beispielsweise im Popup Parse-Fehler die genauen Informationen zur fehlerhaften XML-Datei.

  ![](images/invalid-topic-xml.png){width="650" align="left"}

  Im obigen Screenshot wird eine Kreuzmarkierung verwendet, um auf die Zeile zu verweisen, die fehlerhaftes XML enthält.

- Mit der Funktion &quot;Suchen und Ersetzen&quot;können Sie in der Quellansicht nach Text, Elementen oder Attributen suchen.
Weitere Informationen finden Sie unter **Suchen und Ersetzen** Funktionsbeschreibung in [Hauptleiste](web-editor-features.md#id#id2051EA0G05Z) Abschnitt.

- Die Quellansicht bietet viele Tastaturbefehle, mit denen Sie schnell zu einem Dokument navigieren und daran arbeiten können. In der folgenden Tabelle sind die unterstützten Aktionen und ihre Tastaturbefehle aufgeführt:

  | Gehen Sie hierfür wie folgt vor | Verwenden Sie diesen Tastaturbefehl |
  |----------|-----------------|
  | Mehrere Cursor hinzufügen | **Strg**+Links klicken |
  | Mehrere nicht aufeinander folgende Textauswahlen | **Strg**+ Linksklick zum Ziehen und Auswählen von Text |
  | Text über und zwischen Zeilen auswählen | **Alt**+ Linksklick zum Ziehen und Auswählen von Text |
  | Mehrfachauswahl rückgängig machen oder Vollbildmodus beenden | **Esc** |
  | Automatische Vervollständigung anzeigen | **Strg**+**Leerzeichen** |
  | Navigieren Sie zum öffnenden oder schließenden -Tag des aktuellen Tags | **Strg**+**J** |
  | Erweitern oder Reduzieren des aktuellen Tags und seines Inhalts | **Strg**+**Q** |
  | Aktuelles Element und Inhalt auswählen | **Strg**+**L** |
  | Aktuelles Element ausschließen | **Umschalt**+**Registerkarte** |
  | Aktuelles Element und Inhalt löschen | **Umschalt**+**Strg**+**K** |
  | Cursor ein Wort nach links verschieben | **Alt**+**Linkspfeil** |
  | Cursor ein Wort nach rechts verschieben | **Alt**+**Rechtspfeil** |
  | Scrollen Sie eine Zeile nach oben, ohne die Cursorposition zu ändern. | **Strg**+**Aufwärtspfeil** |
  | Scrollen Sie eine Zeile nach unten, ohne die Cursorposition zu ändern | **Strg**+**Abwärtspfeil** |
  | Vollbild ein/aus | **F11** |
  | Fügen Sie eine neue Zeile nach dem aktuellen Element ein | **Strg**+**Eingabe** |
  | Einfügen einer neuen Zeile vor dem aktuellen Element | **Umschalt**+**Strg**+**Eingabe** |
  | Suchen und wählen Sie das nächste Vorkommen des aktuellen Wortes aus | **Strg**+**D** |
  | Verschieben Sie das aktuelle Element und seinen Inhalt um ein Element nach oben | **Umschalt**+**Strg**+**Aufwärtspfeil** |
  | Verschieben Sie das aktuelle Element und seinen Inhalt um ein Element nach unten | **Umschalt**+**Strg**+**Abwärtspfeil** |
  | Umschließen des aktuellen Elements im Kommentar-Tag | **Strg**+**/** |
  | Aktuelles Element und Inhalt duplizieren | **Umschalt**+**Strg**+**D** |
  | Löschen Sie Text nach dem Cursor. Wenn der Cursor vor einem öffnenden Element steht, wird das gesamte Element gelöscht. | **Strg**+**K**+**K** |
  | Löschen Sie Text links neben dem Cursor in der aktuellen Zeile. Wenn der Cursor hinter dem schließenden -Tag eines Elements steht, wird das gesamte Element gelöscht. | **Strg**+**K**+**Rücktaste** |
  | Aktuellen Text in Großbuchstaben konvertieren | **Strg**+**K**+**U** |
  | Aktuellen Text in Kleinbuchstaben konvertieren | **Strg**+**K**+**L** |
  | Scrollen Sie im aktuellen Element zur Mitte des Editors | **Strg**+**K**+**C** |
  | Cursor über der aktuellen Position hinzufügen | **Strg**+**Alt**+**Aufwärtspfeil** |
  | Cursor unterhalb der aktuellen Position hinzufügen | **Strg**+**Alt**+**Abwärtspfeil** |
  | Suchen Sie rekursiv das aktuelle Wort \(in Vorwärtsrichtung\). | **Strg**+**F3** |
  | Suchen Sie rekursiv das aktuelle Wort \(in Rückwärtsrichtung\). | **Umschalt**+**Strg**+**F3** |


## Vorschau

Beim Öffnen eines Themas im Vorschaumodus wird angezeigt, wie ein Thema angezeigt wird, wenn es von einem Benutzer in seinem Browser angezeigt wird. Bei einer DITA-Zuordnung wird eine Vorschau der Karte angezeigt, wobei ein einzelnes zusammengesetztes Dokument aller Themen innerhalb der Karte angezeigt wird.

Im Vorschau -Modus stehen folgende Funktionen zur Verfügung:

- [Anzeigen von Inhalten basierend auf bedingten Filtern](#id2114BI00VXA)
- [Anzeigen der Markierungen von Änderungen](#id2114BJ00CE8)
- [Thema als PDF exportieren](#id2114BL00B5U)

### Anzeigen von Inhalten basierend auf bedingten Filtern {#id2114BI00VXA}

Wenn Sie Bedingungen in Ihrem Thema oder Ihrer Zuordnung verwendet haben, werden diese Bedingungen im Bedienfeld Filter angezeigt. Standardmäßig werden alle Bedingungen ausgewählt und der gesamte Inhalt angezeigt. Wenn Sie die Auswahl einer Bedingung aufheben, wird der Inhalt mit dieser Bedingung aus der Ansicht entfernt. Sie können auch bedingte Inhalte hervorheben.

Die folgende Abbildung zeigt ein Thema, das zwei Bedingungen verwendet — `Audience` und `Product`. Der konditionalisierte Inhalt wird durch einen gelben Hintergrund hervorgehoben.

![](images/preview-filters.png){width="800" align="left"}

### Anzeigen der Markierungen von Änderungen {#id2114BJ00CE8}

Wenn ein Dokument Änderungen verfolgen enthält \(oder visuelle Hinweise\), können Sie auch eine Vorschau des Dokuments mit oder ohne diese Markups anzeigen. Bei der Vorschau eines Dokuments enthält der rechte Bereich die Optionen Filter und Verfolgung .

![](images/preview-tracking_cs.png){width="400" align="left"}

Es gibt drei **Tracking** Optionen, aus denen Sie auswählen können:

- **Keine Markup**: In dieser Ansicht werden alle Einfügungen und Löschungen akzeptiert und eine einfache Ansicht des Dokuments angezeigt. In dieser Ansicht werden keine Markups von Änderungen verfolgt.
- **Original**: In dieser Ansicht werden alle Einfügungen abgelehnt und alle Löschungen wiederhergestellt. Anschließend wird eine Vorschau angezeigt. Einfach erhalten Sie die Originalform des Dokuments, bevor Sie den Modus Änderungen verfolgen aktiviert haben.
- **Markup anzeigen**: In dieser Ansicht erhalten Sie alle Markups für eingefügten und gelöschten Inhalt.

  Die folgende Abbildung zeigt die Vorschau einer Map-Datei mit Markups:

  ![](images/preview-map-with-track-changes.PNG){width="800" align="left"}


### Thema als PDF exportieren {#id2114BL00B5U}

PDF ist eines der gängigsten Ausgabeformate, das in jeder Phase des Dokumententwicklungszyklus verwendet wird. AEM Guides bieten Ihnen die Flexibilität, die PDF eines einzelnen Themas oder einer ganzen Map-Datei zu generieren. Die Funktion &quot;Als PDF exportieren&quot;ermöglicht es dem Autor, Publisher oder einem Administrator, die PDF-Ausgabe für ein bestimmtes Thema einfach zu generieren. Es verwendet die im Ordnerprofil gespeicherten DITA-OT-Konfigurationen, um die PDF zu generieren.

Diese Funktion unterstützt die folgenden Funktionen:

- Generieren Sie die PDF der derzeit aktiven Arbeitskopie eines Themas.
- Akzeptieren Sie den DITA-OT-Transformationsnamen und die Befehlszeilenargumente, um die PDF zu generieren.
- Speichern Sie die generierte Ausgabe auf dem lokalen System.
- Lösen Sie die im Thema verwendeten Schlüssel- und Inhaltsreferenzen, bevor Sie die Ausgabe generieren.

Gehen Sie wie folgt vor, um ein Thema als PDF zu exportieren:

1. Öffnen Sie das Thema im Vorschaumodus.

1. Klicken Sie auf **Als PDF exportieren** \(![](images/export-as-pdf-icon.svg)\).

   Das Dialogfeld Als PDF exportieren wird angezeigt.

   ![](images/export-as-pdf-dialog.png){width="350" align="left"}

1. *\(Optional\)* Geben Sie den DITA-OT-Transformationsnamen und alle Befehlszeilenargumente an, die Sie verwenden möchten.

1. Klicken Sie auf **Download**.

   >[!NOTE]
   >
   > Vergewissern Sie sich, dass Sie das Popup-Fenster in der Browserkonfiguration aktiviert haben. Andernfalls wird die PDF nicht heruntergeladen.

   Die PDF wird in einer neuen Registerkarte generiert und geöffnet oder Sie erhalten ein Dialogfeld zum Speichern der PDF auf Ihrem lokalen System.


**Übergeordnetes Thema:**[ Arbeiten mit dem Web-Editor](web-editor.md)
