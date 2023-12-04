---
title: REST-API zur Registrierung eines Datenquellen-Connectors
description: Erfahren Sie mehr über die REST-API zur Registrierung eines Datenquellen-Connectors.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# REST-API zur Registrierung eines Datenquellen-Connectors {#id236LG0Y0CXA}

Mit der folgenden REST-API können Sie einen Datenquellen-Connector registrieren.

## Datenquellen-Connector registrieren

Eine GET, die einen Datenquellen-Connector registriert.

**Anforderungs-URL**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`path`|Zeichenfolge|Ja|Eine Zeichenfolge, die auf einen Pfad im AEM Repository verweist. Es kann sich um einen Pfad im `/content/dam or /var/dxml`.|

**Beispiel**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`
