---
title: Native PDF | Unterstützung für Sprachvariablen
description: Verwenden Sie Sprachvariablen in der PDF-Ausgabe- und Ausgabevorlage.
source-git-commit: 6de4b4666d804c678674faa6fe1a54ef9b9dbbe0
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 0%

---


# Unterstützung für Sprachvariablen

AEM Guides bieten die Funktion zur Verwendung von Sprachvariablen. Sie können Sprachvariablen verwenden, um lokalisierte Zeichenfolgen in der PDF-Ausgabe zu definieren oder statischen Text in den Ausgabevorlagen zu lokalisieren. Sie können CSS-Stile verwenden, um die aus einer CSS stammenden Zeichenfolgen zu lokalisieren.

## Sprachvariablen in der PDF-Ausgabe verwenden

Sie können Sprachvariablen verwenden, um eine lokalisierte Version der vordefinierten Beschriftungen wie Hinweis, Vorsicht und Warnung oder statischen Text in der PDF-Ausgabe zu definieren. Der Variablenname ist für alle Sprachen identisch, kann aber für die verschiedenen Sprachen unterschiedliche Werte aufweisen. Sie können den Wert für diese Variablen in einer oder mehreren Sprachen aktualisieren und dann wird der lokalisierte Wert automatisch in der PDF-Ausgabe ausgewählt.

Sie können beispielsweise die folgenden Methoden verwenden, um die Beschriftung anzuzeigen `Note` in der PDF-Ausgabe:

- Englisch: Hinweis

- Französisch: Remarque

- Deutsch: Verweis

<img alt= "Ausgabe in dem Dokument, das Sprachvariablen enthält" src="./assets/language-variable-output.png" width="550">

*Eine Beispielnote in englischer, französischer und deutscher Sprache.*

>[!NOTE]
>
> Wenn der Wert für eine Variable nicht in einer bestimmten Sprache definiert ist, wählt AEM Guides die Zeichenfolge aus der Sprache der Benutzeroberfläche (Benutzeroberfläche der Anwendung) als Ausweichmechanismus aus.
>
> Wenn Sie den Wert nicht in der Sprache der Benutzeroberfläche definiert haben, wird nach Englisch gesucht (`en_us`) oder andernfalls wird die englische (`en`) und zeigt dasselbe in der PDF-Ausgabe an.

## Typen von Sprachvariablen

AEM Guides unterstützen zwei Variablentypen: Anwendungs- und Benutzervariablen.

### Anwendungsvariablen

AEM Guides bieten eine Reihe vordefinierter oder vordefinierter Anwendungsvariablen. Sie können diese vordefinierten Variablen verwenden, um Informationen zu einem für AEM Guides spezifischen Dokument hinzuzufügen. Beispiel: die `chapter-number` zeigt, falls in einer Seite enthalten, die Kapitelnummer an, zu der die Seite gehört. Die `author-label` zeigt den Namen des Dokumentautors an.

>[!NOTE]
>
> Sie können den Wert für eine Anwendungsvariable überschreiben.


### Benutzervariablen

Sie können auch neue Sprachvariablen erstellen. Sie können beispielsweise eine Benutzervariable Publisher für die Bezeichnung des Herausgebers für das Dokument erstellen.

>[!NOTE]
>
>  Sie sollten über Administratorrechte verfügen, um Benutzervariablen zu erstellen und die Anwendungsvariablen zu bearbeiten.

<img alt="Fenster für Sprachvariablen" src="./assets/add-language-variables.png" width="550">

*Fügen Sie die Sprachvariablen für eine ausgewählte Sprache hinzu und zeigen Sie sie an.*

## Neue Sprachvariable hinzufügen

1. Gehen Sie im Web Editor zur Registerkarte Ausgabe .
1. Auswählen **Sprachvariablen** <img src="./assets/language-variables.svg" width="25"> im linken Bereich.
1. Auswählen **Bearbeiten** , um die **Sprachvariablen** Fenster. Die in der ausgewählten Sprache vorhandenen Anwendungs- und Benutzervariablen werden in alphabetischer Reihenfolge aufgelistet. Die Werte werden entsprechend der ausgewählten Sprache angezeigt. Wenn Sie beispielsweise die französische Sprache auswählen, wird &quot;Tipp&quot;als &quot;Conseil&quot;angezeigt.
1. Aus dem **Sprache** wählen Sie die gewünschte Sprache aus, in der Sie eine Variable bearbeiten möchten.

   >[!NOTE]
   >
   > Wenn Sie die gewünschten Sprachen nicht anzeigen, aktivieren Sie die gewünschte Sprache über die **Sprachvariableneinstellungen**. Einstellungen auswählen <img src="./assets/settings-icon.svg" width="25">  , um die **Sprachvariableneinstellungen** angezeigt.

1. Geben Sie den Variablennamen in die **Name** und deren Wert in **Wert** Spalte.

   >[!NOTE]
   >
   >Sie können jeden beliebigen HTML-Inhalt als Variablenwert verwenden, um den Variablenwert in einer bestimmten Formatierung anzuzeigen. Sie können beispielsweise `<b>` -Tag auf den Variablenwert hinzu, um den Herausgeber fett anzuzeigen.

1. Auswählen **Sprachvariable hinzufügen** <img src="./assets/add-language-variable.svg" width="25"> , um der ausgewählten Sprache eine neue Sprachvariable hinzuzufügen. Wenn Sie eine Variable zu einer Sprache hinzufügen, wird sie automatisch allen Sprachen hinzugefügt. Sie können keine Variable mit demselben Namen wie eine vorhandene Variable erstellen. Es wird ein Fehler angezeigt.

>[!NOTE]
>
> Wenn Sie nicht **Sprachvariable hinzufügen**, wird die Variable nicht erstellt und der Liste hinzugefügt.

## Exportieren und Importieren von Sprachvariablen

Experience Manager-Handbücher unterstützen den Export und Import der in der ausgewählten Sprache vorhandenen Sprachvariablen. Sie können alle Sprachvariablen zusammen mit den definierten Werten einfach exportieren. Dies umfasst sowohl Anwendungs- als auch Benutzervariablen. Verwenden Sie die exportierte Datei, um die gewünschten Änderungen an den Werten vorzunehmen oder sie in andere Sprachen zu lokalisieren.

Sie können auch die XML-Datei importieren, die die Sprachvariablen enthält. Experience Manager Guides importieren nur die bereits definierten Sprachvariablen, einschließlich Anwendungs- und Benutzervariablen. Es werden keine noch nicht definierten Variablen importiert.

### Exportieren von Sprachvariablen

Um die Sprachvariablen für eine Sprache zu exportieren, wählen Sie die Sprache aus der Dropdown-Liste aus und wählen Sie **Export** <img src="./assets/language-variable-export-icon.svg" alt="Exportsymbol" width="25">.
Es wird eine XML-Datei im Format erstellt `language_variable_<ln>` where `<ln>` ist der Code der ausgewählten Sprache. Beispiel: `language_variable_en.xml` für Englisch und `language_variable_fr.xml` für Französisch.

>[!NOTE]
> 
>Wenn Sie nicht gespeicherte Änderungen an den Sprachvariablen haben, können Sie diese nicht exportieren. Speichern Sie die Änderungen, um die aktivierte **Export** <img src="./assets/language-variable-export-icon.svg" alt="Importsymbol" width="25"> Symbol.

### Sprachvariablen importieren

So importieren Sie die Sprachvariablen:

1. Wählen Sie eine Sprache aus der Dropdown-Liste aus und wählen Sie **Import** <img src="./assets/language-variable-import-icon.svg" width="25">.
2. Suchen Sie nach der XML, die die Sprachvariablen enthält, und wählen Sie sie aus. Beispielsweise language_variable_en.xml.
Sie können XML-Dateien im folgenden Format importieren:

```
<?xml version="1.0" encoding="UTF-8"?>
<variables>    
<variable id="note-important">Important: </variable>    
<variable id="note-caution">Avertir: </variable>    
<variable id="image-with-text">Text and image &lt;img src=&quot;/content/dam/assets/images/image_with_text.png&quot; /&gt; </variable> 
</variables> 
```

Die Variablen mit derselben ID werden nach dem Import der Datei importiert. Die Werte für die Variablen in der ausgewählten Sprache werden mit denen in der XML-Datei aktualisiert.  Es wird eine Meldung über die Anzahl der aktualisierten Variablen angezeigt.

>[!NOTE]
> 
><ul><li>Wenn es sich bei der Datei nicht um eine XML-Datei handelt oder die Datei ein falsches Format enthält, das nicht den Sprachvariablen zugeordnet ist, wird ein Fehler angezeigt, dass ein Problem mit der XML-Datei vorliegt. 
&gt;<li>Wenn die Datei keine Variablen mit derselben ID enthält, wird eine Warnung angezeigt, dass in der importierten Datei keine übereinstimmende Sprachvariable gefunden wird.

### Optionen für eine Sprachvariable

Bewegen Sie den Mauszeiger über die Variable, um die **Optionen** auswählen.

<img width="550" alt="Optionsmenü für Sprachvariablen" src="./assets/language-variable-user-options.png">

*Verwenden Sie die **Optionen**Menü zum Löschen, Anzeigen einer Vorschau oder Duplizieren einer Sprachvariablen.*

Sie können sowohl Anwendungs- als auch Benutzervariablen in der Vorschau anzeigen. Um anzuzeigen, wie der Variablenwert in der Ausgabe angezeigt wird, wählen Sie **Vorschau** aus dem **Optionen** Menü der ausgewählten Variablen.
Sie können auch **Löschen** oder **Duplizieren** die Benutzervariablen. Wenn Sie eine Variable aus einer Sprache löschen, wird sie automatisch aus allen Sprachen gelöscht.

### Bearbeiten oder Wiederherstellen der Anwendungsvariablen

Sie können auch die Werte für eine Anwendungsvariable bearbeiten. Später können Sie eine Anwendungsvariable auf den ursprünglichen Wert zurücksetzen. **Variable zurücksetzen** <img src="./assets/application-variable-revert.svg" width="25">  wird für eine Anwendungsvariable mit einem geänderten Wert angezeigt.

## Sprachvariablen in Ausgabevorlagen verwenden

Sie sollten Sprachvariablen zu Ihren lokalisierten Dokumenten hinzufügen. Sie können diese Sprachvariablen in das Seitenlayout einfügen, das auf verschiedenen Seiten in Ihren lokalisierten Dokumenten angezeigt wird. Sie können beispielsweise die Sprachvariable für die Variable `author-name` im Kopfzeilenbereich des Seitenlayouts (oder in einem anderen Teil wie der Fußzeile oder dem Hauptteil) angezeigt wird.



<img alt="Seitenlayout eines PDF-Dokuments" src="./assets/language-variable-page-layout.png" width="550">


*Der Autor und der Markenname, der in der für die französische PDF generierten Ausgabe lokalisiert ist.*

So fügen Sie eine Sprachvariable wie Ihre `copyright-label` Führen Sie im Kopfzeilenbereich die folgenden Schritte aus:

1. Öffnen Sie das gewünschte Seitenlayout zur Bearbeitung.

   >[!NOTE]
   >
   > Ansicht [Seitenlayout anpassen](../native-pdf/components-pdf-template.md#customize-a-page-layout-customize-page-layout) zum Öffnen eines Seitenlayouts zur Anpassung oder Bearbeitung.

1. Wählen Sie die Kopfzeile aus, damit das Einfügen einer Variablen aktiviert wird.
1. Auswählen **Variable einfügen**  <img src="./assets/insert-language-variable.svg" width="25"> in der Symbolleiste.
1. Im **Variable einfügen** Popup, wählen Sie den Namen der einzufügenden Sprachvariablen aus und klicken Sie auf **Einfügen** , um sie in den Kopfzeilenbereich einzufügen.

   >[!NOTE]
   >
   > Sie können auch die Suchzeichenfolge in das Textfeld eingeben. Die Variablennamen, die die angegebene Zeichenfolge enthalten, werden gefiltert und in der Liste angezeigt.
   > Die ausgewählte Sprachvariable wird in den Kopfzeilenbereich eingefügt.



<img alt="Variable in den Kopfzeilenbereich einfügen" src="./assets/language-variable-header.png" width="550">

*Die `copyright-label` im Kopfzeilenbereich hinzugefügt.*

### Anwenden des Inhaltsstils auf Sprachvariablen

Neben dem Wert, den Sie einer Sprachvariablen zuweisen, können Sie auch HTML-Tags verwenden, um den Variablenwert in einer bestimmten Formatierung anzuzeigen. Sie können beispielsweise den Wert der Variablen `publisher-label` fett gedruckt.

- Sie können die Stile der Werte auch mit <span> -Tag. Beispielsweise können Sie mit der Sprachvariable &quot;page-number&quot;die Seitenzahl im römischen Zahlenformat in englischer Sprache anzeigen und das Format für andere Sprachen angeben.

  Wert für Englisch:
  `<span data-field="page-number" data-format="upper-roman">1</span>`

  Wert für Tamil:
  `<span data-field="page-number" data-format="tamil">1</span>`

Auf ähnliche Weise können Sie Sprachvariablen hinzufügen und andere Felder formatieren, die im Feature &quot;Felder einfügen&quot;der Seitenlayouts aufgeführt sind. Weitere Informationen zum Hinzufügen von Feldern finden Sie unter [Felder und Metadaten hinzufügen](../native-pdf/design-page-layout.md#add-fields-metadata).

- Sie können den Werten auch lokalisierte Bilder hinzufügen. Sie können beispielsweise ein Bildsymbol in der Sprache der Kapitelnummer hinzufügen und lokalisierte Bilder des Symbols in der PDF-Ausgabe abrufen.

  Für Englisch kann der Variablenwert für ein Bild wie folgt lauten: `<img src="banner-en.jpg">`und für dieselbe Variable in deutscher Sprache kann sie `<img src="banner-de.jpg">`. Es nimmt also die Bilder in Abhängigkeit von der Sprache auf.

## Lokalisieren der Zeichenfolgen mit CSS-Stilen

Mithilfe von CSS-Stilen können Sie auch die in der Autonummer verwendeten Zeichenfolgen wie Kapitel, Abschnitt, Abbildung und Tabelle lokalisieren. Da diese Zeichenfolgen aus CSS-Dateien stammen, können Sie sie nicht mithilfe von Sprachvariablen lokalisieren. Um diese Zeichenfolgen zu lokalisieren, können Sie CSS-Stile für jede Sprache erstellen, in der Sie sie lokalisieren möchten.
Beispielsweise können Sie die folgende CSS verwenden, um das Kapitelpräfix und das entsprechende Zahlenformat in verschiedenen Sprachen anzuzeigen.
Beispielsweise können Sie die folgende CSS verwenden, um Kapitel als Hoofdstuk in deutscher Sprache und die Kapitelnummer im Dezimalformat anzuzeigen. Für Japanisch können Sie das japanische Zahlenformat verwenden, um die Kapitelnummern im Inhaltsverzeichnis anzuzeigen.

```
// for English
h1:before {
  counter-increment: h11;
  content: "Chapter " counter(h11, decimal)".";
}

// for German
:root:lang(de) h1:before {
  content: "Hoofdstuk " counter(h11, decimal)".";
}

// for Japanese
:root:lang(ja) h1:before {
  content: "章 " counter(h11, japanese-formal)".";
}
```

Die folgenden Screenshots zeigen die in der Ausgabe auf Deutsch und Japanisch lokalisierten Zeichenfolgen an.

<img alt=" japanische Ausgabe mit Sprachvariable" src="./assets/localize-chapter-german.png" width="550">



<img alt="Deutsche Ausgabe mit Sprachvariable" src="./assets/localize-chapter-japanese.png" width="550">



### Präfixe formatieren

Mithilfe von CSS-Stilen können Sie auch die Präfixe formatieren. Sie können beispielsweise die Bezeichnung `Note` in der PDF-Ausgabe verschiedener Sprachen in roter Farbe angezeigt.

```
.note .prefix-content 
{
color: red;
} 
```



