---
title: Installation AEM Guides überprüfen
description: Erfahren Sie, wie Sie die Installation AEM Guides überprüfen
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# Installation AEM Guides überprüfen {#id213BD030FBE}

Nach der Installation AEM Guides müssen Sie überprüfen, ob die Installation erfolgreich war oder nicht. Führen Sie die folgenden Schritte aus, um den Installationsprozess zu überprüfen:

1. Melden Sie sich bei Ihrer AEM-Instanz an und navigieren Sie zur Seite AEM Web Console Bundles . Die Standard-URL für den Zugriff auf die Bundles-Seite lautet:

   ```http
   http://<server name>:<port>/system/console/bundles
   ```

   Eine Liste von Bundles wird angezeigt.

1. Filtern Sie die Liste der Bundles, indem Sie das Format in das Filtertextfeld eingeben und die Eingabetaste drücken **Eingabe**.

   Die Liste der Bundles wird gefiltert, um die von AEM Guides installierten Bundles anzuzeigen. Wenn die Installation erfolgreich war, verfügen alle installierten Bundles über eine **Status** von **Aktiv**.

   Wenn eines der Bundles keine **Aktiv** und überprüfen Sie dann die AEM, um das Installationsproblem zu beheben.


>[!IMPORTANT]
>
> Es gibt eine Reihe von Empfehlungen zur Leistungsoptimierung, die Sie zur Verbesserung der Systemleistung in Betracht ziehen können. Siehe [Recommendations zur Leistungsoptimierung](download-install-recommend-perf-optimiz.md#) für Details.

**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)
