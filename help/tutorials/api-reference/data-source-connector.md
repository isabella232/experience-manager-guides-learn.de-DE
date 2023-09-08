---
title: REST-API zur Registrierung eines Datenquellen-Connectors
description: Erfahren Sie mehr über die REST-API zur Registrierung eines Datenquellen-Connectors.
source-git-commit: 8707acf3ba01b7488eea6597c434da73a901d037
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---


# REST-API zur Registrierung eines Datenquellen-Connectors {#id236LG0Y0CXA}

Mit der folgenden REST-API können Sie einen Datenquellen-Connector registrieren.

## Datenquellen-Connector registrieren

Eine GET, die einen Datenquellen-Connector registriert.

**URL-Anforderung**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Parameter**: |Name|Typ|Erforderlich|Beschreibung| |—|—|—|—|—| |`path`|Zeichenfolge|Ja|Eine Zeichenfolge, die auf einen Pfad im AEM Repository verweist. Es kann sich um einen Pfad im `/content/dam or /var/dxml`.|

**Beispiel**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`

