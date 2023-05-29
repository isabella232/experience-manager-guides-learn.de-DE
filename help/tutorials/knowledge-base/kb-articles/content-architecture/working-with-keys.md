---
title: Arbeiten mit Schlüsseln
description: Erstellen von Schlüsseln zur Verwendung in unternehmensübergreifenden Inhalten
role: Admin
exl-id: b8e3a6d2-ea82-4fdb-bd16-3f4b6594af52
source-git-commit: c8feab55ed3b8e7b36ec46b21f63155766627e40
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Schlüssel erstellen

Unternehmen sollten Schlüssel verwenden, wenn sie einen wiederverwendbaren und gemeinsamen Text haben, wie Produktname oder Produktplatzierung, der an vielen Stellen verwendet wird, sich aber ändern kann. Durch die Verwendung von Schlüsseln für diesen wiederverwendbaren Text können Sie eine Aktualisierung an mehreren Stellen senden, indem Sie die Änderung an einer einzigen Stelle vornehmen, z. B. im Schlüsselwert.

## Schritt 1: Erstellen einer globalen Zuordnung zum Speichern Ihrer Schlüssel

Erstellen Sie eine Zuordnung und fügen Sie die [!UICONTROL keyref] -Element.

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "technicalContent/dtd/map.dtd">
<mapid="map.ditamap_ffbdbf06-8658-4311-ad84-1c631bba904f">
  <title>global-keys-map</title>
  <keydefkeys="adobe">
    <topicmeta>
      <linktext>Adobe Systems</linktext>
    </topicmeta>
  </keydef>
  <keydefkeys="AEM">
    <topicmeta>
      <linktext>Adobe Experience Manager</linktext>
    </topicmeta>
  </keydef>
</map>
```

Hier haben Sie zwei Definitionen definiert, wie oben gezeigt, und eine [!UICONTROL keyref] as _AEM_ für _Adobe Experience Manager_ Text.

## Schritt 2: Hinzufügen dieser Karte zu Ihrer Publikationskarte

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "technicalContent/dtd/map.dtd">
<mapid="map.ditamap_cbf4a96d-e382-4e8c-8830-bcc093fe6638">
  <title>sample-map</title>
  <topicrefhref="sample-topic-using-the-keys.dita"type="topic">
  </topicref>
  <maprefformat="ditamap"href="global-keys-map.ditamap"type="map">
  </mapref>
</map>
```

## Schritt 3: Verwenden Sie die Schlüssel, um auf die in der globalen Schlüsselzuordnung definierten Variablen zu verweisen

+ Bearbeiten Sie das Thema und fügen Sie den Schlüsselwert mithilfe des [!UICONTROL keyref].
+ Wie im Screenshot gezeigt, wird ein kleines Fenster angezeigt, in dem Keywords ausgewählt werden können. Dies wird angezeigt, wenn Sie das Element &quot;keyword&quot;hinzufügen.
   ![Element einfügen](assets/insert_element.png)
   ![Key Ref](assets/key_ref.png)

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE topic PUBLIC "-//OASIS//DTD DITA Topic//EN" "technicalContent/dtd/topic.dtd">
<topicid="topic.dita_31b00e61-04b5-4193-af7a-68503e88b087">
  <title>sample-topic-using-the-keys</title>
  <shortdesc></shortdesc>
  <body>
    <p>This is a sample topic using the keys defined in the global map</p>
    <p>here i am using the key definition for AEM :<keywordkeyref="AEM"></keyword></p>
  </body>
</topic>
```
