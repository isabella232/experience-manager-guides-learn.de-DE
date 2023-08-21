---
title: Erstellen von Karten basierend auf benutzerdefinierten Vorlagen
description: Erfahren Sie, wie Sie Karten basierend auf benutzerdefinierten Vorlagen erstellen
exl-id: 02513148-3876-4549-962a-9984f619030f
source-git-commit: 3ae28dc4266d418e5730e2036c8eee2a804dc847
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Erstellen von Karten basierend auf benutzerdefinierten Vorlagen {#id225VF0808MP}

Sie können benutzerdefinierte Zuordnungsvorlagen erstellen und diese zum Erstellen von DITA-Maps zusammen mit den Themenvorlagen und Zuordnungsvorlagen verwenden, auf die in der Zuordnungsvorlage verwiesen wird

Sie können von der benutzerdefinierten Zuordnungsvorlage aus auf andere Zuordnungsvorlagen und Themenvorlagen verweisen. Die referenzierten Zuordnungsvorlagen können sich auf verschiedene Zuordnungsvorlagen, Themenvorlagen, Themen, Zuordnungen, Bilder, Videos und andere Assets beziehen. Die benutzerdefinierte Kartenvorlage kann Ihnen dabei helfen, die Zuordnungsvorlagen und die gesamte referenzierte Ordnerstruktur einfach zu replizieren. Diese benutzerdefinierten Vorlagen sind besonders nützlich, um mehrere Karten mit rekursiven Strukturen und Referenzen zu erstellen und neu zu erstellen.

>[!NOTE]
>
> Themenvorlagen werden nicht rekursiv erstellt. Es werden nur Themenvorlagen generiert, die sich direkt in der Zuordnungsvorlage befinden, und jede Themenvorlage innerhalb einer Themenvorlage wird einfach direkt in der übergeordneten Vorlage referenziert.

## Benutzerdefinierte Vorlagen erstellen

Mit AEM Guides können Sie benutzerdefinierte Maps und Themen aus dem Ordner dita-templates erstellen. Sie können diese benutzerdefinierten Vorlagen verwenden, um Ihre Karte und Ihr Thema zu erstellen. Sie können diese Vorlagen auch für Ihre Autoren freigeben und sie zum Erstellen ihrer Dateien verwenden. Mithilfe dieser Vorlagen können Sie Autoren erlauben, separate Kopien bestimmter Ressourcen zu speichern, die sich im Ordner &quot;Vorlagen&quot;befinden.

>[!NOTE]
>
> Alle Ressourcen, auf die nur verwiesen und die in allen Versionen gepflegt werden sollen, müssen außerhalb des Vorlagenordners aufbewahrt werden.


Sie können Zuordnungs- und Themenvorlagen wie folgt erstellen:
1. Bereich &quot;Vorlagen&quot;der [Linke Leiste](./web-editor-features.md#left-panel-id2051ea0m0hs)
1. [Vorlagen in der Assets-Benutzeroberfläche](#templates-assets-ui)
1. [Optionen, Menü](#templates-in-assets-ui)

### Vorlagen in der Assets-Benutzeroberfläche {#templates-assets-ui}

**Themenvorlage**

Führen Sie die folgenden Schritte aus, um eine Themenvorlage zu erstellen:

1. Im **Assets-Benutzeroberfläche**, navigieren Sie zum Ordner dita-templates .

   ![](images/dita-templates.png){width="800" align="left"}

1. Klicks **topics** Ordner, um ihn zu öffnen. Klicken Sie auf **Erstellen von \> DITA-Vorlage**.
1. Wählen Sie auf der Blueprint-Seite **Thema** und klicken Sie anschließend auf **Weiter.**
1. Geben Sie auf der Seite Eigenschaften die Themenvorlage an **Titel**.
1. Datei angeben **Name**

   >[!NOTE]
   >
   > Der Dateiname muss die Erweiterung .dita aufweisen.

1. \(Optional\) Fügen Sie eine Beschreibung hinzu.
1. Klicken Sie auf **Erstellen**. Die Nachricht zur Erstellung der Themenvorlage wird angezeigt. Anschließend können Sie die Themenvorlage öffnen und bearbeiten.

**Zuordnungsvorlage**

Führen Sie die folgenden Schritte aus, um eine Zuordnungsvorlage zu erstellen:

1. Im **Assets-Benutzeroberfläche**, navigieren Sie zum Ordner dita-templates .
1. Klicks **maps** Ordner, um ihn zu öffnen.
1. Klicks **Erstellen** > **DITA-Vorlage.**

   ![](images/create-dita-template.png){width="300" align="left"}

1. Wählen Sie auf der Blueprint-Seite **Zuordnung** und klicken **Nächste**.
1. Geben Sie auf der Seite Eigenschaften die Zuordnungsvorlage an **Titel**.
1. Datei angeben **Name**.

   >[!NOTE]
   >
   > Der Dateiname muss die Erweiterung .ditamap aufweisen.

1. (Optional\) Fügen Sie eine Beschreibung hinzu. Klicken Sie auf **Erstellen**. Die erstellte Meldung wird angezeigt. Anschließend können Sie die Zuordnungsvorlage öffnen und bearbeiten. Sie können die Referenzen für die Themenvorlagen, Zuordnungsvorlagen und auch andere Assets in der Zuordnungsvorlage hinzufügen.

### Optionen, Menü {#options-menu}

Gehen Sie wie folgt vor, um eine Zuordnung oder Themenvorlage zu erstellen:

1. Wählen Sie die **Zuordnung** oder **Thema** im Ordner &quot;Aktuelle Vorlagen&quot;. Beispielsweise den Ordner `dita-templates`.
1. Aus dem **Optionen** Menü auswählen **Erstellen einer Zuordnungsvorlage** oder **Erstellen einer Themenvorlage**.

   Die **Neue Zuordnungsvorlage erstellen** oder **Neue Themenvorlage erstellen** wird geöffnet.
1. Geben Sie den Titel und den Namen der neuen Vorlage ein.
1. Wählen Sie den Vorlagentyp aus, den Sie erstellen möchten, aus dem **Vorlage** Dropdown-Liste.

Die erstellte Meldung wird angezeigt. Sie können die Vorlage Ihrem globalen Profil oder Profil auf Ordnerebene hinzufügen. Die neue Vorlage wird dann im Prozess der Themen- oder Zuordnungserstellung angezeigt und Sie können damit Zuordnungen oder Themen erstellen.


Ihr Administrator kann auch einen Ordner erstellen und so konfigurieren, dass er der Ordner ist, in dem Sie die Vorlagen erstellen und speichern können.

Je nach Setup erfahren Sie, wie Sie den benutzerdefinierten Ordnerpfad für DITA-Vorlagen konfigurieren:
<details>
    <summary> Cloud Services </summary>

Erfahren Sie, wie [benutzerdefinierten Ordnerpfad für DITA-Vorlagen konfigurieren](../install-guide/conf-template-tags-custom-dita-topic-template.md#configure-custom-dita-template-folder-path-id191lcf0095z) im Cloud Service-Installations- und Konfigurationshandbuch.
</details>

<details>
    <summary> On-Premise Software</summary>

Erfahren Sie, wie [benutzerdefinierten Ordnerpfad für DITA-Vorlagen konfigurieren](../cs-install-guide/conf-template-tags-custom-dita-topic-template.md#configure-custom-dita-template-folder-path-id191lcf0095z) im On-Premise-Installations- und Konfigurationshandbuch.
</details>

## Weitergeben des in den Vorlagen definierten Titels

Wenn Sie den Titel des Themas oder der in Ihrer Vorlage verwendeten Zuordnung an die mit dieser Vorlage erstellten DITA-Maps weitergeben möchten, verwenden Sie geschweifte Klammern um den Titel.

Beispiel

```XML
<pubtitle>
   <mainpubtitle outputclass="booktitle">
   {title}
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>

The resultant DITA map with title "Rootmap1" will look like as follows:
<pubtitle>
   <mainpubtitle outputclass="booktitle">Rootmap1
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>
```

>[!NOTE]
> Nur das erste Vorkommen von geschweiften Klammern wird durch den Titel ersetzt.

Wenn Sie keine geschweiften Klammern um den Titel verwenden, wird die resultierende DITA-Zuordnung nur das erste Element ausgewählt und die Verschachtelung des Titels wird nicht aus der Vorlage ausgewählt und sieht wie folgt aus:

```XML
<pubtitle> Rootmap1 </pubtitle>
```

>[!NOTE]
> Sie können auch die geschweiften Klammern um den Text verwenden, um die verschachtelte Struktur von den benutzerdefinierten Vorlagen an Ihre DITA-Maps zu übergeben.

Beispiel

```XML
<title>    
    <sub>        
        <b>{title}</b>    
    </sub>
</title>
```




## Verwenden Sie die Zuordnungsvorlage, um neue Zuordnungen zu erstellen

>[!NOTE]
>
> Die Zuordnungsvorlage muss von Ihrem Administrator konfiguriert und für die Bearbeitung zur Verfügung gestellt werden. Weitere Informationen finden Sie unter *Authoring-Vorlagen konfigurieren* im as a Cloud Service Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern.

Führen Sie die folgenden Schritte aus, um eine Zuordnung mithilfe der benutzerdefinierten Zuordnungsvorlage zu erstellen:

1. Im **Assets-Benutzeroberfläche,** Navigieren Sie zu dem Ordner, in dem Sie die Zuordnung erstellen möchten.
1. Klicks **Erstellen von \> DITA Map**.
1. Wählen Sie auf der Blueprint-Seite die gewünschte Zuordnungsvorlage aus und klicken Sie auf **Nächste**. Wenn Sie beispielsweise eine Zuordnungsvorlage &quot;test-template&quot;erstellt haben, wählen Sie sie aus.
1. Geben Sie auf der Seite Eigenschaften die Zuordnung an **Titel**.
1. Datei angeben **Name**.

   >[!NOTE]
   >
   > Der Dateiname muss die Erweiterung .ditamap aufweisen.

1. Klicken Sie auf **Erstellen**. Die Nachricht Zuordnungserstellung wird angezeigt.


Die Zuordnung generiert alle Assets, auf die im Vorlagenordner verwiesen wird. Einige Asset-Typen, die in einer Zuordnung referenziert werden, können wie folgt aussehen:

- Wenn die Zuordnung den Verweis auf eine Themenvorlage enthält, wird eine Kopie davon innerhalb des Ordners in derselben Hierarchie wie im Themenordner im Ordner `dita-templates` Ordner.
- Wenn die Zuordnung den Verweis auf eine Zuordnungsvorlage enthält, wird eine Kopie davon innerhalb des Ordners in derselben Hierarchie wie im Ordner &quot;maps&quot;im Ordner `dita-templates` Ordner.
- Wenn die Zuordnung einen generischen Verweis auf ein Thema oder eine Zuordnung außerhalb des `dita-templates/topics` oder `dita-templates/maps` -Ordner, wird nur auf denselben verwiesen und es wird keine Kopie erstellt.

  >[!NOTE]
  >
  > `dita-templates/topics` und `dita-templates/maps` sind die Standardpfade in Guides und können konfiguriert werden.


  Wenn sich in der Zuordnungsvorlage eine Schlüsseldefinition für die Themenvorlage befindet, wird ein neuer Schlüssel &quot;\(also neues Thema\)&quot;erstellt und in der Zuordnung auf diesen verwiesen.

- Wenn eine andere Zuordnung oder ein anderes Thema auf derselben Ebene im Ordner erstellt wird, werden die Namen der neu erstellten Assets mit 0,1,2 usw. angehängt. Sie können wählen, ob Sie die Karte zur Bearbeitung öffnen oder die Zuordnungsdatei im Repository speichern möchten.

**Übergeordnetes Thema:**[ Arbeiten mit dem Map Editor](map-editor.md)
