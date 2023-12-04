---
title: Element-IDs automatisch generieren
description: Erfahren Sie, wie Sie Element-IDs automatisch generieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Element-IDs automatisch generieren {#id20CIL40016I}

AEM Guides generieren eine Dokument-ID für jedes neue Dokument, das Sie erstellen. Wenn Sie beispielsweise eine DITA-Zuordnung erstellen, wird eine ID wie `map.ditamap_random_digits` wird der ID der Zuordnung zugewiesen. Sie können auch Elemente definieren, für die automatisch eine ID generiert und zugewiesen wird.

AEM Guides bieten einfache Konfigurationseinstellungen, bei denen Sie die Elemente definieren müssen, für die eine ID automatisch generiert wird, sowie ein Muster für die ID. Standardmäßig sind einige Elemente wie `section`, `table`, `ul`, `ol`, werden für die automatische Generierung der ID konfiguriert. Sie können weitere Elemente zu dieser Liste hinzufügen, sodass AEM Guides bei jeder Einfügung dieser Elemente in ein Dokument eine Kennung generieren und zuweisen, die auf dem angegebenen Muster basiert

Führen Sie die folgenden Schritte aus, um Elemente so zu konfigurieren, dass sie eine automatisch generierte ID aufweisen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** Bundle

1. Im *XmlEditorConfig* -Einstellungen ein oder mehrere Elemente in der **Automatische Generierung von IDs für Element-Tags** -Feld.

   >[!NOTE]
   >
   > Element-Tags sind DITA-Elementnamen, z. B. `body`, `title`, `codeblock`usw. Um mehrere Elemente anzugeben, trennen Sie Elementnamen durch ein Komma.

1. Im **Muster für das Generieren von IDs** -Feld ein Muster zum Generieren einer ID angeben.

   Der Standardwert für dieses Feld ist auf `${elementName}_${id}`. Die `${elementName}` durch den Namen des Elements ersetzt. Die `${id}` generiert eine sequenzielle Zahl für das Element. Wenn Sie beispielsweise das Absatzelement mit automatisch generierten IDs zuweisen, erhält der erste Absatz im Thema oder Dokument eine ID wie p\_1, der nächste Absatz erhält p\_2 usw. In einem anderen Dokument wird der ID-Generierungsprozess jedoch neu gestartet. Das bedeutet, dass in einem anderen Dokument IDs wie p\_1 und p\_2 Absatzelementen zugewiesen werden können.

   Wenn Ihr Dokument bereits IDs im angegebenen Muster enthält, weist der Prozess der automatischen Generierung diese IDs neuen Elementen nicht zu.

1. Klicken Sie auf **Speichern**.


**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
