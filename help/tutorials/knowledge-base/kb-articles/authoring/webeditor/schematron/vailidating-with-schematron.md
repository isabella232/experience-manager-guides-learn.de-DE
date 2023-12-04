---
title: Schematron-Unterstützung für Wearditor
description: Arbeiten mit Schematron im Wearditor
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Kontrollieren der Qualität von Inhalten im Web-Editor

Dieser Artikel gibt einen Überblick über die Validierungsmöglichkeiten im Web-Editor AEM Guides.
Der Design-Web-Editor nutzt das DITA-Schema-Setup im System, um Benutzer dazu zu zwingen, DITA-konforme Inhalte zu erstellen. Dadurch ist der gesamte im System gespeicherte Inhalt strukturiert, wiederverwendbar und gültig.

Neben der Unterstützung für DITA-Regeln unterstützt der Web-Editor auch die Validierung von Inhalten, die auf &quot;*Schematron*&quot;.

&quot;*Schematron*&quot; bezieht sich auf eine regelbasierte Validierungssprache, die zum Definieren von Tests für eine XML-Datei verwendet wird. Sie können die Schemadateien importieren und sie auch im Web-Editor bearbeiten. Mithilfe einer Schematron-Datei können Sie bestimmte Regeln definieren und sie dann für ein DITA-Thema oder eine Zuordnung validieren. Schemaregeln können die Konsistenz der XML-Struktur sicherstellen, indem als Regeln definierte Einschränkungen auferlegt werden. Diese Beschränkungen werden von KMU getragen, die die Qualität und Konsistenz der Inhalte besitzen.

    HINWEIS: Der Webeditor unterstützt ISO-Schemata.


## Funktionsweise von &quot;Schema&quot;im Web-Editor

### Konfigurieren von Schemaregeln

Siehe Abschnitt &quot;Unterstützung für Schematron-Dateien&quot;im [Benutzerhandbuch](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=148)


### Validierungsregeln beim Speichern von Dateien durchsetzen

Mit den Webeditor-Einstellungen können Power-User Schemaregeln/-Dateien einrichten, die jedes Mal ausgeführt werden, wenn ein Benutzer den Inhalt aktualisiert. Weitere Informationen finden Sie im Abschnitt &quot;Validierung&quot;unter [Benutzerhandbuch](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=58)

![Regeln aus den Einstellungen des Web-Editors festlegen](../../../assets/authoring/schematron-editorsettings-validation-tab.png)


### Können Sie die Validierung manuell ausführen?

Ja, als Autor/Benutzer können Sie beim Erstellen von Inhalten das Bedienfeld &quot;Schematron&quot;im Webeditor verwenden, um eine Schematrator-Datei hochzuladen und Überprüfungen für die im Editor geöffnete Datei durchzuführen.

    Damit dies funktioniert, muss der Ordnerprofiladministrator allen Benutzern erlauben, Schemadateien im Überprüfungsfenster hinzuzufügen. Siehe Editor-Einstellungen (Screenshot oben)

![Schematron-Datei auswählen](../../../assets/authoring/schematron-rightpanel-validation-addsch.png)
![Validierung ausführen](../../../assets/authoring/schematron-rightpanel-validation-runsch.png)


### Unterstützte Regeln

Die aktuelle Version von AEM Guides unterstützt nur die Validierung, die ausschließlich auf &quot;Zusicherung&quot;basierende Regeln verwendet. (siehe [Asset vs. Bericht](https://schematron.com/document/205.html)) Auf &quot;Berichten&quot;basierende Regeln werden noch nicht unterstützt.


### Beispiele und weitere Hilfe zu Schemakontrollen-Regeln

#### Anwendungsbeispiele

- Überprüfen Sie, ob ein Link extern ist und den Bereich &quot;extern&quot;aufweist.

  ```
  <sch:pattern>
      <sch:rule context="xref[contains(@href, 'http') or contains(@href, 'https')]">
          <sch:assert test="@scope = 'external' and @format = 'html'">
              All external xref links must be with scope='external' and format='html'
          </sch:assert>
      </sch:rule>
  </sch:pattern>
  ```

- Überprüfen Sie, ob mindestens eine &quot;topicref&quot;in einer Zuordnung oder mindestens ein &quot;li&quot;unter einer &quot;ul&quot;vorhanden ist.

  ```
  <sch:pattern>
      <sch:rule context="map">
          <sch:assert test="count(topicref) > 0">
              There should be atleast one topicref in map
          </sch:assert>
      </sch:rule>
  
      <sch:rule context="ul">
          <sch:assert test="count(li) > 1" >
              A list must have more than one item.
          </sch:assert>
      </sch:rule>
  </sch:pattern>
  ```

- Das Element &quot;indexterm&quot;sollte immer in einem &quot;prolog&quot;vorhanden sein

  ```
  <sch:pattern>
      <sch:rule context="*[contains(@class, ' topic/indexterm ')]">
          <sch:assert test="ancestor::node()/local-name() = 'prolog'">
              The indexterm element should be in a prolog.
          </sch:assert>
      </sch:rule>
  </sch:pattern>
  ```

#### Ressourcen

- Grundlagen  [Schematron-Grundlagen](https://da2022.xatapult.com/#what-is-schematron)
- Weitere Informationen [Zusicherungsregeln in Schematron](https://www.xml.com/pub/a/2003/11/12/schematron.html#Assertions)
- [Beispielschema-Datei](../../../assets/authoring/sample_schematron.sch)
