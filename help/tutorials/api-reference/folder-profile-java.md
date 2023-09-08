---
title: Java-basierte API für die Arbeit mit Ordnerprofilen
description: Erfahren Sie mehr über die Java-basierte API für die Arbeit mit Ordnerprofilen
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Java-basierte API für die Arbeit mit Ordnerprofilen {#id175UB30E05Z}

Mit der folgenden Java-basierten API können Sie bedingte Attribute zu einem Profil auf Ordnerebene hinzufügen. Diese API ist in Form eines Bundles verfügbar. Sie müssen dieses Bundle in Ihren Code aufnehmen, um diese APIs verwenden zu können.

Paketdetails:

- Gruppen-ID: **com.adobe.fmdita**

- Artefakt-ID: **api**

- Version: **3,2**

- Package: **com.adobe.fmdita.api.profiles**

- Klassendetails:

  ```JAVA
  public class FolderProfileUtils extends Object
  ```

  Die **`FolderProfileUtils`** -Klasse enthält eine Methode zum Hinzufügen von bedingten Attributen zu einem Ordnerprofil.


## Hinzufügen bedingter Attribute zu einem Ordnerprofil

Die ``addAttributeProfiles`` -Methode fügt einem Profil auf Ordnerebene bedingte Attribute hinzu.

**Syntax**:

```JAVA
public static boolean addAttributeProfiles
(List
<String> attributeNames, 
List
    <String> values, 
List
        <String> labels,
String profileName, 
Session session) throws GuidesApiException
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |``attributeNames``|Zeichenfolge|Eine Liste von Attributnamen.| |``values``|Zeichenfolge|Eine Liste von Werten für die angegebenen Attribute.| |`labels`|Zeichenfolge|Eine Liste von Bezeichnungen für die `attribute`- `value` Paare. [1](#fntarg_1)| |`profileName`|Zeichenfolge|Der Name des Profils auf Ordnerebene, auf das diese Attribute, Werte und Beschriftungen angewendet werden müssen. **Wichtig:** Alle vorhandenen im Profil definierten Attribute-Werte-Beschriftungen werden überschrieben.| |`session`|javax.jcr.Session|Eine gültige JCR-Sitzung.|

**Rückgabe**:
`true` für Erfolg. Im Falle eines Fehlers wird eine Ausnahme ausgelöst.

**Ausnahme**: Threads ``java.lang.Exception`` in den folgenden Szenarien:

- Wenn die API nicht `resourceResolverFactory` -Objekt. In diesem Fall sollten Sie das Bundle neu starten.
- Wenn an die API übergebene Parameter ungültig sind.
- Wenn die API über eine nicht autorisierte Benutzersitzung aufgerufen wird, z. B. der Benutzer, der kein Administrator für das angegebene Ordnerprofil ist.

[1](#fnsrc_1) Die `attributeNames`, `values`, und `labels` in einer Array-Liste muss demselben Eintrag entsprechen.

