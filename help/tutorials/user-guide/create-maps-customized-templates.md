---
title: Erstellen von Karten basierend auf benutzerdefinierten Vorlagen
description: Erfahren Sie, wie Sie Karten basierend auf benutzerdefinierten Vorlagen erstellen
exl-id: 02513148-3876-4549-962a-9984f619030f
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

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

**Themenvorlage**

Führen Sie die folgenden Schritte aus, um eine Themenvorlage zu erstellen:

1. Im **Assets-Benutzeroberfläche**, navigieren Sie zum Ordner dita-templates .

   ![](images/dita-templates.png){width="800" align="left"}

1. Klicken **topics** Ordner, um ihn zu öffnen. Klicken Sie auf **Erstellen von \> DITA-Vorlage**.
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
1. Klicken **maps** Ordner, um ihn zu öffnen.
1. Klicken **Erstellen Sie \> DITA-Vorlage.**

   ![](images/create-dita-template.png){width="300" align="left"}

1. Wählen Sie auf der Blueprint-Seite **Zuordnung** und klicken Sie auf **Nächste**.
1. Geben Sie auf der Seite Eigenschaften die Zuordnungsvorlage an **Titel**.
1. Datei angeben **Name**.

   >[!NOTE]
   >
   > Der Dateiname muss die Erweiterung .ditamap aufweisen.

1. (Optional\) Fügen Sie eine Beschreibung hinzu. Klicken Sie auf **Erstellen**. Die erstellte Meldung wird angezeigt. Anschließend können Sie die Zuordnungsvorlage öffnen und bearbeiten. Sie können die Referenzen für die Themenvorlagen, Zuordnungsvorlagen und auch andere Assets in der Zuordnungsvorlage hinzufügen.

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
> Die Zuordnungsvorlage muss von Ihrem Administrator konfiguriert und für die Bearbeitung zur Verfügung gestellt werden. Weitere Informationen finden Sie unter *Bearbeitungsvorlagen konfigurieren* im as a Cloud Service Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern.

Führen Sie die folgenden Schritte aus, um eine Zuordnung mithilfe der benutzerdefinierten Zuordnungsvorlage zu erstellen:

1. Im **Assets-Benutzeroberfläche,** Navigieren Sie zu dem Ordner, in dem Sie die Zuordnung erstellen möchten.
1. Klicken **Erstellen von \> DITA Map**.
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
- Wenn die Zuordnung einen generischen Verweis auf ein Thema oder eine Zuordnung außerhalb der `dita-templates/topics` oder `dita-templates/maps` -Ordner, wird nur auf denselben verwiesen und es wird keine Kopie erstellt.

   >[!NOTE]
   >
   > `dita-templates/topics` und `dita-templates/maps` sind die Standardpfade in Guides und können konfiguriert werden.


   Wenn sich in der Zuordnungsvorlage eine Schlüsseldefinition für die Themenvorlage befindet, wird ein neuer Schlüssel &quot;\(also neues Thema\)&quot;erstellt und in der Zuordnung auf diesen verwiesen.

- Wenn eine andere Zuordnung oder ein anderes Thema auf derselben Ebene im Ordner erstellt wird, werden die Namen der neu erstellten Assets mit 0,1,2 usw. angehängt. Sie können wählen, ob Sie die Karte zur Bearbeitung öffnen oder die Zuordnungsdatei im Repository speichern möchten.

**Übergeordnetes Thema:**[ Arbeiten mit dem Map Editor](map-editor.md)
