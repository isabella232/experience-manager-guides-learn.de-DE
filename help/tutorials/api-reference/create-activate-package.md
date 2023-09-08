---
title: REST-API zum Erstellen und Aktivieren von Paketen
description: Erfahren Sie mehr über die REST-API zum Erstellen und Aktivieren von Paketen
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# REST-API zum Erstellen und Aktivieren von Paketen {#id198CF0260Y4}

Mit der folgenden REST-API können Sie CRX-Pakete erstellen und aktivieren.

## Package erstellen und aktivieren

Eine POST-Methode, die das CRX-Paket erstellt und aktiviert.

**Anforderungs-URL**: http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/activate

**Parameter**: Die Anforderungsabfrage besteht aus der JSON-Regelzeichenfolge. Der Inhaltstyp der POST-Anforderung muss auf `application/json; charset=UTF-8`.

**Beispiel**: Die folgenden Beispiele zeigen den API-Aufruf mithilfe des curl-Befehls:

    &quot;
    curl -u &lt;*username*>:&lt;*password*> -H &quot;Content-Type: application/json; charset=UTF-8&quot; -k -X POST -d &quot;{[JSON rules string](create-activate-package-java.md#example-create-activate-package-id198JH0B905Z)}&quot; http://&lt; em-guides-server*>:&lt;*port-number*>/bin/fmdita/activate
    &quot;
