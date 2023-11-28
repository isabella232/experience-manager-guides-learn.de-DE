---
sidebar_position: 2
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Kontextmenüs anpassen

Die folgenden Kontextmenüs können angepasst werden:

- `file_options`
Controller:
   - Kartenansicht: `ditamap_viewer_controller`
   - Repository-Bereich: `repository_panel_controller`
   - Favoriten-Bedienfeld: `collection_tree_controller`
   - Dateieigenschaften - Referenzlinks: `file_references_links_controller`
   - Repository-Suchbereich: `repository_search_controller`
   - Betreff-Panel: `subject_scheme_tree_controller`

- `folder_options`
Controller:
   - Repository-Bereich: `repository_panel_controller`
   - Favoriten-Bedienfeld: `collection_tree_controller`

- `collection_options`
Controller:
   - Favoriten-Bedienfeld: `collection_tree_controller`

- `map_view_options`
Controller:
   - Kartenansicht: `ditamap_viewer_controller`

- `baseline_panel_menu`
Controller:
   - Grundlinien-Bedienfeld: `baseline_panel`

- `preset_item_menu`
Controller:
   - Vorgabenbereich: `preset_panel`

Sie können auch Ihr eigenes Kontextmenü erstellen, indem Sie eine neue eindeutige ID definieren.

Jetzt verfügt jedes Kontextmenü über eine `controller id` zugeordnet wurde. Dieser Controller verarbeitet die `on-event` Funktionen für die verschiedenen Kontextmenüoptionen

Nehmen wir ein Beispiel, um

```js title=customise_context_menu.js"
const fileOptions = {
    id: "file_options",
    contextMenuWidget: "repository_panel",
    view: {
            items: [
                {
                    component: "div",
                    target: {
                        key:"displayName",value: "Delete",                    
                        viewState: VIEW_STATE.REPLACE
                    }
                },
                {
                    component: "div",
                    target: {
                        key:"displayName",value: "Edit",                    
                        viewState: VIEW_STATE.REPLACE
                    }
                },
                {
                    "displayName": "Download",
                    "data": {
                      "eventid": "downloadFile"
                    },
                    "icon": "downloadFromCloud",
                    "class": "menu-separator",         
                    target: {
                        key:"displayName",value: "Duplicate",                    
                        viewState: VIEW_STATE.REPLACE
                    }
                },
            ]

    },

    controller: {
        downloadFile(){
            const path  = this.model.selectedItem.path
            this.loader.loadDitaFile(path).then((file) => {
              function download_file(name, contents) {
                const mime_type = "text/plain";
        
                const blob = new Blob([contents], {type: mime_type});
        
                const dlink = document.createElement('a');
                dlink.download = name;
                dlink.href = window.URL.createObjectURL(blob);
                dlink.onclick = function() {
                    // revokeObjectURL needs a delay to work properly
                    const that = this;
                    setTimeout(function() {
                        window.URL.revokeObjectURL(that.href);
                    }, 1500);
                };
        
                dlink.click();
                dlink.remove();
            }
            download_file(path,file.xml)
            });
          }
    }
}
```

Lassen Sie uns nun verstehen, was dieser Code tut.

1. `id` wird verwendet, um das Kontextmenü zu identifizieren, das wir anpassen möchten.
2. `contextMenuWidget` wird verwendet, um die `widget id` oder `component` , das das Kontextmenü aufruft und das `events`.

Der Rest bleibt derselbe, wobei `view` zum Definieren der Elemente verwendet wird, `target` gibt an, wo die Option ersetzt, angehängt oder vorangestellt werden soll, und `contextMenuWidget` Controller verarbeitet die `on-click` -Ereignisse.
