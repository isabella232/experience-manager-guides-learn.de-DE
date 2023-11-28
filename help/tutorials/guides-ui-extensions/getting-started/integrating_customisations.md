---
sidebar_position: 2
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 2%

---


# Installieren und Verwenden des Erweiterungspakets AEM Guides

Mit Erweiterungen können Sie Ihre AEM Guides-App an Ihre Anforderungen anpassen. Dieses Erweiterungs-Framework wird mit AEM Guides ab Version 4.3 (On-Premise) und 2310 (Cloud) unterstützt.

## Voraussetzungen

Dieses Paket erfordert [Git Bash](https://github.com/git-guides/install-git) und npm

## Installation

Die einfachste Möglichkeit, das Bootstrapping AEM Guides-Framework durchzuführen, ist durch CLI

```bash
npx @adobe/create-guides-extension
```

## Hinzufügen von Anpassungscode

1. Codedateien für jede Komponente hinzufügen, die Sie im Abschnitt `src/` Verzeichnis. Einige Beispieldateien wurden bereits hinzugefügt.
2. Jetzt im `index.ts` Datei im `src/` directory :
   - Importieren Sie `.ts` -Dateien mit den Anpassungen, die Sie in Ihrem Build hinzufügen möchten.
   - Importe zu hinzufügen `window.extension`
   - Registrieren Sie die angepassten Komponenten `id` und der entsprechenden Einfuhr `tcx extensions`
   - Siehe Beispiel . [index.ts](../../../src/index.ts)

## Erstellen des benutzerdefinierten Codes

- Ausführen `npm run build` im Stammverzeichnis. Sie erhalten 3 Dateien im Verzeichnis, `dist/`:
   - `build.css`
   - `guides-extension.js`
   - `guides-extension.umd.cjs`

![Ausgabe erstellen](./../imgs/build_output.png)

## Hinzufügen der Anpassung zu AEM

- Öffnen Sie das `CRXDE` `crx/de/index.jsp#/`
- Unter dem `apps` Ordner erstellen, erstellen Sie einen neuen Knoten des Typs `cq:ClientLibraryFolder`

![Ordnerstruktur](./../imgs/crxde_folder_structure.png)

- Im `properties` Wählen Sie im Knoten `Multi` Fügen Sie den folgenden Eigenschaftsnamen hinzu: `categories`
Typ: `String []`
Wert: `apps.fmdita.review_overrides`, `apps.fmdita.xml_editor.page_overrides`

![Ordnereigenschaften](./../imgs/crxde_folder_properties.png)

- Um die erstellte JS hinzuzufügen, erstellen Sie eine neue Datei, z. B.: `tcx1.js` im oben erstellten Knoten. Fügen Sie hier den Code aus `dist/guides-extension.umd.cjs` oder `dist/guides-extension.js`. Erstellen Sie jetzt eine neue Datei. `js.txt`Fügen wir hier den Namen unserer JS-Datei hinzu, der in diesem Fall wie folgt lauten würde:

```t
#base=.
tcx1.js
```

- Um den erstellten CSS hinzuzufügen, erstellen Sie eine neue Datei, z. B. `tcx1.css` im oben erstellten Knoten. Fügen Sie hier den Code aus `dist/build.css`. Erstellen Sie jetzt eine neue Datei. `css.txt`Fügen wir hier den Namen unserer CSS-Datei hinzu, der in diesem Fall wie folgt lauten würde:

```t
#base=.
tcx1.css
```

- Führen Sie einen `shift + refresh` , um die App mit den Anpassungen zu laden!

## Fehlerbehebung

Überprüfen Sie, ob alle oben genannten Schritte korrekt ausgeführt wurden.
Nachdem Sie Ihren Code zu tcx.js hinzugefügt haben, stellen Sie sicher, dass Sie eine harte Aktualisierung durchführen (Umschalt+Aktualisieren).
Öffnen Sie nun AEM, klicken Sie mit der rechten Maustaste und klicken Sie `Inspect`
Gehen Sie zu Quellen und suchen Sie nach Ihrer `[node_name].js` (z. B.: extensions.js). Führen Sie ein Steuerelement / Befehl + D aus, um nach Ihrer Datei zu suchen. Wenn die Variable `.js` -Datei mit dem JS-Code vorhanden ist, aus dem Sie eingefügt haben `dist/guides-extension.umd.cjs` oder `dist/guides-extension.js`festgelegt ist, ist die Einrichtung abgeschlossen.
