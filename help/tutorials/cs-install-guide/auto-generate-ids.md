---
title: Element-IDs automatisch generieren
description: Erfahren Sie, wie Sie Element-IDs automatisch generieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---

# Element-IDs automatisch generieren {#id20CIL40016I}

AEM Guides generieren eine Dokument-ID für jedes neue Dokument, das Sie erstellen. Wenn Sie beispielsweise eine DITA-Zuordnung erstellen, wird eine ID wie `map.ditamap_random_digits` wird der ID der Zuordnung zugewiesen. Sie können auch Elemente definieren, für die automatisch eine ID generiert und zugewiesen wird.

AEM Guides bieten einfache Konfigurationseinstellungen, bei denen Sie die Elemente definieren müssen, für die eine ID automatisch generiert wird, sowie ein Muster für die ID. Standardmäßig sind einige Elemente wie `section`, `table`, `ul`, `ol`, werden für die automatische Generierung der ID konfiguriert. Sie können weitere Elemente zu dieser Liste hinzufügen, sodass AEM Guides bei jeder Einfügung dieser Elemente in ein Dokument eine Kennung generieren und zuweisen, die auf dem angegebenen Muster basiert

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um automatisch generierte Element-IDs zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.classes` | Geben Sie eine kommagetrennte Liste von Elementen an. <br> **Standardwert**: `"topic, section, table, simpletable, fig, image, ul, ol"` |

Um ein Muster für automatisch generierte ID zu konfigurieren, erstellen Sie eine Konfigurationsdatei mit den folgenden Eigenschaften:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.pattern` | Der Standardwert für dieses Feld ist auf `${elementName}_${id}`. Die `${elementName}` durch den Namen des Elements ersetzt. Die `${id}` generiert eine sequenzielle Zahl für das Element. Wenn Sie beispielsweise das Absatzelement mit automatisch generierten IDs zuweisen, erhält der erste Absatz im Thema oder Dokument eine ID wie p\_1, der nächste Absatz erhält p\_2 usw. In einem anderen Dokument wird der ID-Generierungsprozess jedoch neu gestartet. Das bedeutet, dass in einem anderen Dokument IDs wie p\_1 und p\_2 Absatzelementen zugewiesen werden können. **Standardwert**: ``${elementName}_${id}`` |

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
