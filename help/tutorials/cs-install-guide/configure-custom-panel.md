---
title: Benutzerdefiniertes Bedienfeld im linken Bereich konfigurieren
description: Erfahren Sie, wie Sie ein benutzerdefiniertes Bedienfeld im linken Bedienfeld konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# Benutzerdefiniertes Bedienfeld im linken Bereich konfigurieren {#id224JI200Y6F}

Führen Sie die folgenden Schritte aus, um ein benutzerdefiniertes Bedienfeld im linken Bereich des Web-Editors hinzuzufügen:

1. Erstellen Sie eine *clientlib* und fügen Sie Ihre JavaScript- und CSS-Datei in diesen Ordner ein.
1. Aktualisieren Sie die categories-Eigenschaft des *clientlib* Ordner, indem ihm der Wert von *apps.format.xml\_editor.page\_overrides*.

Beispielcode zum Konfigurieren eines benutzerdefinierten Bedienfelds:

```
tcx.ready(function () { //Ready will call the callback after editor code is set for events and global variable excess
 
 
    // APP_ADD_AUTHOR_LEFT_TAB event will add a new left tab in the left panel, user can show hide it using editor settings
    tcx.eventHandler.next(tcx.eventHandler.KEYS.APP_ADD_AUTHOR_LEFT_TAB, {
            id: 'my_panel',
            class: 'my-panel-tab',
            icon: 'file', //Any valid Adobe Spectrum icon name https://spectrum.adobe.com/page/icons/
            label: 'My Tab',
            prevTabID: 'repository_panel' //Existing tab ids are 'collection_panel', 'repository_panel', 'map_panel', 'outline_panel', 'conref_panel', 'glossary_panel', 'condition_panel', 'subject_scheme_panel', 'snippet_panel', 'template_panel', 'search_panel'
    })
 
    // APP_PANEL_DID_MOUNT event will be called after user has selected the panel and panel is rendered in the DOM
    tcx.eventHandler.subscribe({
        key: tcx.eventHandler.KEYS.APP_PANEL_DID_MOUNT,
        next: function(opts) {
            // TODO create panel ui inside $el
            let $el = opts.$el //$el is Tab panel content html node
            let id = opts.id //id is tab panel id (my_panel)
            console.log("mounted", opts)
        }
    })
 
  // APP_PANEL_WILL_UNMOUNT will be called before destorying the new left panel
  tcx.eventHandler.subscribe({
        key: tcx.eventHandler.KEYS.APP_PANEL_WILL_UNMOUNT,
        next: function(opts) {
            //TODO do some cleanup
            let id = opts.id //id is tab panel id (my_panel)
            console.log("unmounted", opts)
        }
    })
 
});
```

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
