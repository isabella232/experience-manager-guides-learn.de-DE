---
title: Arbeiten mit dem Basic Map Editor
description: Erfahren Sie, wie Sie mit dem Basic Map Editor arbeiten.
source-git-commit: af5c64312a608affe95fd552b3dd1b2e05ea2b8e
workflow-type: tm+mt
source-wordcount: '1394'
ht-degree: 0%

---


# Arbeiten mit dem Basic Map Editor {#id1942CM005Y4}

Der Basic Map Editor bietet eine einfache Drag-and-Drop-Funktion, um Themen aus Ihrem AEM-Repository hinzuzufügen und die DITA-Map oder -Lesekarte zu erstellen. Sie können verschachtelte Themen, Beziehungstabellen \(reltable\), Attribute und Metadateninformationen hinzufügen und die Zuordnung auch auf Richtigkeit überprüfen.

>[!NOTE]
>
> Wenn Ihr Administrator die Option Erweiterter Map-Editor aktiviert hat, haben Sie keinen Zugriff auf den Basic Map Editor. Alle Zuordnungsdateien werden standardmäßig im erweiterten Map-Editor geöffnet.

In den folgenden Abschnitten werden die verschiedenen Funktionen beschrieben, die im Basic Map Editor verfügbar sind.

## Hinzufügen von Themen zu einer Map-Datei {#id193CBL0505Z}

Nachdem eine Zuordnungsdatei erstellt wurde, müssen Sie der Zuordnungsdatei Themen hinzufügen. Mit dem Basic Map Editor können Sie Themen, Beziehungstabellen oder andere Zuordnungsdateien hinzufügen.

Führen Sie die folgenden Schritte aus, um Ihre Zuordnungsdatei zu erstellen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur Zuordnungsdatei, die Sie bearbeiten möchten.

1. Um eine exklusive Sperre für die Zuordnungsdatei zu erhalten, wählen Sie die Zuordnungsdatei aus und klicken Sie auf **Auschecken**.

   >[!NOTE]
   >
   > Sobald Sie eine exklusive Sperre für eine Map-Datei haben, können andere Benutzer die Karte nicht mehr bearbeiten. Sie können jedoch an den Themen in der Map-Datei arbeiten.

1. Klicken Sie bei ausgewählter Zuordnungsdatei auf **Bearbeiten**.

   Die Zuordnungsdatei wird zur Bearbeitung im Map Editor geöffnet. Mit dem Map Editor erstellen Sie eine Zuordnung mithilfe der derzeit verfügbaren Themen, die in der Leiste &quot;Verweise&quot;angezeigt werden.

   ![](images/dita-map-01.png)

1. Verwenden der **Verweise** navigieren Sie zu dem Ordner, der die Themen oder Unterkarten enthält, die Sie hinzufügen möchten.

   >[!NOTE]
   >
   > Sie können in der Leiste &quot;Verweise&quot;Themen oder Unterkarten aus einem beliebigen Ordner hinzufügen.

1. Um das erste Thema zur Karte hinzuzufügen, ziehen Sie das Thema per Drag-and-Drop in den Basic Map Editor.

   >[!NOTE]
   >
   > Nach dem Hinzufügen des ersten Links ist der Link Neue Referenz hinzufügen verfügbar, wenn Sie den Mauszeiger über ein vorhandenes Thema in der Karte bewegen.

1. Um nachfolgende Themen oder eine Unterzuordnung hinzuzufügen, ziehen Sie das Thema oder die Unterzuordnung per Drag-and-Drop an die gewünschte Position in der Zuordnung.

   Wenn Sie Ihrer DITA-Zuordnung eine Unterzuordnung hinzufügen, wird die Unterzuordnung als Link in der DITA-Zuordnung angezeigt. Um alle Themen der Unterzuordnung anzuzeigen, klicken Sie auf den Unterzuordnungslink. Der Inhalt der Unterkarte wird in einem neuen Tab angezeigt.

   >[!NOTE]
   >
   > Wenn Sie ein neues Thema auf ein vorhandenes Thema in der Karte ablegen, erhalten Sie eine Nachricht zum Ersetzen des Themas. Klicken Sie auf Ja , wenn Sie das Thema ersetzen möchten, klicken Sie auf Nein , wenn Sie das Thema nicht ersetzen möchten. Sie können STRG+Z und STRG+Y verwenden, um jede Änderung in der Karte rückgängig zu machen oder wiederherzustellen.

1. Klicken Sie auf **Speichern**.


## In der Symbolleiste des Basic Map Editors verfügbare Funktionen

Über die Hauptsymbolleiste im Editor für einfache Zuordnungen können Sie die folgenden Aufgaben ausführen:

![](images/ditamap-toolbar-actions.png)

**A: Suche**

Sie können die erforderlichen Themen aus DAM suchen und darin einbeziehen. Wenn Sie auf dieses Symbol klicken, wird das Dialogfeld Suchen angezeigt:

![](images/search-dita-map.png)

Geben Sie die Suchbegriffe ein, nach denen Sie suchen möchten. Diese Suchbegriffe werden in Dateinamen, Inhalt und sogar Attributwerten des Themas abgeglichen. Sobald die Suchergebnisse verfügbar sind, wählen Sie das gewünschte Thema aus und klicken Sie auf die Schaltfläche Überprüfen , um die ausgewählten Dateien am Ende Ihrer Zuordnungsstruktur hinzuzufügen. Sie können Ihre Suchergebnisse filtern, indem Sie die Parameter Datum ändern angeben.

**B: Gruppe**

Aktivieren Sie das Kontrollkästchen links neben den Themen und klicken Sie in der Symbolleiste auf Gruppe , um die ausgewählten Themen zu gruppieren. Weitere Informationen zu Gruppierungsthemen finden Sie unter [topicgroup](https://docs.oasis-open.org/dita/v1.0/langspec/topicgroup.html) Dokumentation in OASIS DITA Language Specification.

**C: Löschen**

Aktivieren Sie das Kontrollkästchen links neben einem Thema und klicken Sie in der Symbolleiste auf Löschen , um die ausgewählten Themen aus der Karte zu entfernen.

**D: Zahlen anzeigen/ausblenden**

Zeigt die \(oder blendet\) Nummerierung für die Themen auf der Karte an.

**E: Bestätigen**

Überprüfen Sie, ob die Zuordnung gültig ist oder Fehler aufweist.

**F: Standardmodus/XML-Modus**

Im **Standardmodus**, wenn Sie auf einen Themenlink klicken, wird die Vorschau des Themas in einer neuen Registerkarte angezeigt. Klicken Sie auf die **Standardmodus** ändert den Modus in **XML-Modus**. In **XML-Modus** Wenn Sie auf eine beliebige Stelle in einer Themenzeile klicken, wird die zugrunde liegende XML der Themenreferenzen innerhalb des Themas angezeigt. In der XML-Quellansicht gibt es eine **Auto-Einzug** -Option, die den XML-Code im lesbaren und leicht lesbaren Format neu organisiert. Wenn Sie eine Zuordnung manuell bearbeiten, führt die Quellansicht auch Validierungsprüfungen durch. Wenn Ihre XML Fehler enthält, wird dasselbe im **XML-Modus** und Sie dürfen die DITA-Map-Datei nicht speichern. Wenn Sie die XML-Datei für die gesamte Zuordnung anzeigen möchten, klicken Sie auf eine beliebige Stelle außerhalb der Themengrenze.


**Hinweis:** Im Standardmodus können Sie die Tastaturbefehle verwenden, um \(`Ctrl+z`\) oder wiederholen Sie \(`Ctrl+y`\) die letzte Aktion.


![](images/dita-map-invalid-source.png)

**G: Zuordnungseigenschaften**

Zeigen Sie das Dialogfeld Zuordnungseigenschaften an, in dem Sie die Attribute und Metadateninformationen für die Zuordnung festlegen können. Um ein Attribut hinzuzufügen, klicken Sie auf die **Hinzufügen** Schaltfläche unten links im Dialogfeld, um die **Attribut** Dropdown-Liste. Wählen Sie in der Liste das Attribut aus, das Sie hinzufügen möchten. Wenn das ausgewählte Attribut vordefinierte Werte enthält, die in der DTD angegeben sind, werden diese Werte in einer neuen Dropdown-Liste angezeigt. Sie können den gewünschten Wert aus der Dropdownliste auswählen. Wenn kein vordefinierter Wert vorhanden ist, wird Ihnen ein Textfeld angezeigt, in das Sie einen Wert für das ausgewählte Attribut eingeben können.

![](images/map-properties.png)

## Auf Themenebene verfügbare Funktionen im Basic Map Editor

Wenn Sie den Mauszeiger im Basic Map Editor über ein Thema oder eine Unterzuordnungsdatei bewegen, können Sie die folgenden Aufgaben ausführen:

![](images/ditamap-actions.png)

**A: Nach links oder Nach rechts verschieben**

Klicken Sie auf die Pfeilsymbole links oder rechts, um das Thema nach links oder rechts zu verschieben. Wenn Sie ein Thema so verschieben, wird es zu einem untergeordneten Element \(verschachteln\) oder Geschwister \(Verschachtelung entfernen\) im Hinblick auf das obige Thema.

**B: Eigenschaften**

Klicken Sie auf das Symbol Eigenschaften , um das Dialogfeld Eigenschaften von Topicref zu öffnen. Mithilfe dieses Dialogfelds können Sie die Themenattribute und Metadateninformationen festlegen. Weitere Informationen zu den standardmäßigen Themenattributen und Metadaten finden Sie in der [topicref](https://docs.oasis-open.org/dita/v1.2/os/spec/langref/topicref.html) Dokumentation in OASIS DITA Language Specification.


![](images/map-properties-metadata.png)

**C: Neue Referenz hinzufügen**

Klicken Sie auf das Symbol Neue Referenz hinzufügen , um eine neue Referenz als gleichrangiges Element des aktuellen Themas hinzuzufügen.

**D: Neue Schlüsseldefinition hinzufügen**

Klicken Sie auf das Symbol Schlüssel , um eine neue Schlüsseldefinition hinzuzufügen. Jeder überschriebene Schlüssel oder Schlüssel, der bereits in der Zuordnung definiert wurde, wird rot angezeigt. Wenn Sie in einer Schlüsseldefinition auf das Symbol Eigenschaften klicken, wird das Dialogfeld Keydef-Eigenschaften angezeigt.

## Arbeiten mit Beziehungstabellen im Basic Map Editor {#id1944B0I0COB}

Die Zuordnungs-Editoren AEM Guides verfügen über eine leistungsstarke Funktion, mit der Sie Beziehungstabellen in Ihrer DITA-Zuordnung erstellen und bearbeiten können.

Führen Sie die folgenden Schritte aus, um mit Beziehungstabellen im Basic Map Editor zu arbeiten:

1. Navigieren Sie in der Assets-Benutzeroberfläche zur DITA-Zuordnung, in der Sie die Beziehungstabelle erstellen möchten.

1. Klicken Sie auf die DITA-Karte, um sie in der DITA-Map-Konsole zu öffnen.

1. Wählen Sie die **Themen** um eine Liste der in der DITA-Map verfügbaren Themen anzuzeigen.

   >[!TIP]
   >
   > Im Tab Themen haben Sie die Möglichkeit, die Zuordnungsdatei mit ihren abhängigen Elementen herunterzuladen. Weitere Informationen finden Sie unter [DITA-Map-Datei exportieren](authoring-download-assets.md#id218UBA00IXA).

1. Klicken Sie in der Symbolleiste auf **Bearbeiten**.

   Die Zuordnungsdatei wird im Basic Map Editor geöffnet.

1. Auswählen **Reltable** aus der Symbolleiste.

   ![](images/reltable.png)

1. Ziehen Sie Themen per Drag-and-Drop aus der Themenliste in den Editor &quot;Reltable&quot;.

   >[!NOTE]
   >
   > Sie können Themen aus einem beliebigen Ordner in der Leiste &quot;Verweise&quot;hinzufügen.

   ![](images/create-reltable.png)

1. Um Ihrer Beziehungstabelle eine Kopfzeile hinzuzufügen, klicken Sie auf **Relheader hinzufügen**.

1. Um Ihrer Beziehungstabelle eine Spalte hinzuzufügen, klicken Sie auf **Spalte hinzufügen**.

   ![](images/complete-reltable.png)

1. Klicken Sie auf **Speichern**.


Sie können auch die folgenden Aktionen im Beziehungstabelle-Editor durchführen:

**Zeilen oder Spalten löschen**

Wenn Sie eine Spalte aus Ihrer Tabelle löschen möchten, aktivieren Sie das Kontrollkästchen in der Spaltenüberschrift und klicken Sie auf &quot;Löschen&quot;. Wenn Sie eine Zeile aus der Tabelle entfernen möchten, aktivieren Sie das Kontrollkästchen in der ersten Spalte der entsprechenden Zeile und klicken Sie auf &quot;Löschen&quot;.

**Thema löschen**

Wenn Sie ein Thema aus Ihrer Tabelle löschen möchten, klicken Sie auf das Kreuzsymbol neben dem Thema.

**Beziehungstabelle löschen**

Wenn Sie die Beziehungstabelle löschen möchten, klicken Sie auf eine beliebige Stelle außerhalb der Beziehungstabelle und klicken Sie auf &quot;Löschen&quot;.

**Übergeordnetes Thema:**[ Arbeiten mit dem Map Editor](map-editor.md)

