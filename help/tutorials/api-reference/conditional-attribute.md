---
title: REST-API zum Arbeiten mit bedingten Attributen
description: Erfahren Sie mehr über die REST-API für die Verwendung mit bedingten Attributen.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# REST-API zum Arbeiten mit bedingten Attributen {#id175UB30E05Z}

Mit der folgenden REST-API können Sie bedingte Attribute zu einem Ordnerprofil hinzufügen.

## Bedingtes Attribut in einem Profil auf Ordnerebene hinzufügen

Eine POST -Methode, die einem angegebenen Ordnerprofil bedingte Attribute hinzufügt.

**Anforderungs-URL**:\
http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/folderprofiles

**Parameter**:\
|Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`:operation`|String|Ja|Name des aufzurufenden Vorgangs. Der Wert dieses Parameters lautet ``ADDATTRIBUTEPROFILES``. <br> **Hinweis:** Beim Wert wird nicht zwischen Groß- und Kleinschreibung unterschieden.| |`profilename`|Zeichenfolge|Ja|Anzeigename des Profils auf Ordnerebene, dem die bedingten Attribute hinzugefügt werden müssen.| |`conditionalprofiles`|JSON-Array|Ja|Ein JSON-Array, das aus dem bedingten Attributnamen und den Werten besteht. Das folgende Beispielcodefragment zeigt das JSON-Array mit zwei Attributen - `platform` und `product` mit mehreren zugewiesenen Werten.|

```JSON
[  {    name: "platform",    
        values: [       
                {value: "win", label: "Windows"},       
                {value: "mac", label: "Mac OS"}    
                ]},
                {    
                    name: "product",    
                    values: [      
                        {value: "aem_1", label: "AEM 6.1"},     
                        {value: "aem_4,  label: "AEM 6.4"}  
                        ]  
                }]
```

**Antwortwerte**:\
Gibt eine HTTP-Antwort 200 \(Erfolgreich\) zurück.
