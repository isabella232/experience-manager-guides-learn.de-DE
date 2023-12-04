---
title: Hinzufügen benutzerdefinierter Stile zum Guides-Editor
description: Erfahren Sie, wie Sie benutzerdefinierte Stile hinzufügen, um das Erscheinungsbild des Guides-Editors zu ändern.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Hinzufügen benutzerdefinierter Stile zum Guides-Editor

In diesem Artikel erfahren Sie, wie Sie benutzerdefinierte Stile hinzufügen können, um das Erscheinungsbild und die Standardeinstellung für den Webserver zu ändern.

Dies umfasst die folgenden Schritte:
- Hinzufügen benutzerdefinierter Stile über die Konfiguration des XML-Editors für Ordnerprofile
- Auswählen des entsprechenden Ordnerprofils im WebEditor und Testen der Änderungen


## Implementieren anhand eines Beispiels

Sehen wir uns dazu ein Beispiel an, in dem wir die kurze Beschreibung und den Titel als separaten Block mit einigen Stilaspekten im Editor anzeigen möchten.

![Vorschau des Webeditors mit benutzerdefinierten Stilen](../../../assets/authoring/webeditor-customstyles-preview.png)


## Implementieren


### Hinzufügen der benutzerdefinierten CSS zum Ordnerprofil

Verwenden Sie die Ordnerprofile, um die *css_layout.css* Fügen Sie auf der Registerkarte &quot;XML-Editor-Konfiguration&quot;die CSS-Datei mit benutzerdefinierten Stilen hinzu.

[Verwenden Sie diesen Link, um mehr über das Ordnerprofil und das Konfigurieren des CSS-Vorlagenlayouts zu erfahren.](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=en#customize-the-css-template-layout)

Verwenden Sie Folgendes, um den obigen Stil in Ihrem Webserver einzurichten:
- Verwendung [css_layout.css](../../../assets/authoring/webeditor-customstyles-css_layout.css) und laden Sie es in das Ordnerprofil Ihrer Wahl hoch.
- Installieren Sie das angehängte Paket [webeditor-styles-resources.zip](../../../assets/authoring/webeditor-styles-resources.zip) Verwenden AEM Paketmanagers zur Installation der in der obigen CSS-Datei verwendeten Ressourcen

```
This will install the resources at path "/content/dam/resources" which will include sub-folders "fonts" and "images"
```


### Testen

- Öffnen Sie den Web-Editor
- Wählen Sie in den Benutzereinstellungen das Ordnerprofil aus, in dem Sie die benutzerdefinierten Stile hinzugefügt haben. Wenn Sie es zum globalen Profil hinzugefügt haben, verwenden Sie es wahrscheinlich bereits.
- Öffnen Sie ein Thema. Sie werden feststellen, dass der Bearbeitungsbereich über eine benutzerdefinierte Benutzeroberfläche verfügen sollte.

```
Please note this is compatible to AEM Guides version 4.2 and AEM Guides cloud version 2303 (March)
```


## Verweise

Sie interessieren sich möglicherweise auch für die Expertensitzung zu Wetterkonfigurationen und -anpassungen, die unter [Expertensitzung zum Webeditor](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/expert-session/webbased-authoring-jan2023.html?lang=en)
