---
sidebar_position: 3
source-git-commit: 42052b37724f97e34ab007db4cc3d9f9524ad3a2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Verzeichnisstruktur des AEM-Erweiterungspakets

```text
├── src
│   ├── **/*{js,ts}
│   ├── index.ts
├── dist
│   ├── guides-extension.js
│   ├── guides-extension.umd.cjs
│   ├── build.css
├── node_modules
├── package.json
├── package-lock.json 
└── .gitignore
└── buildCSS.mjs // for creating tailwind classes
└── vite.config.js // config for specifying TS and javascript build options
└── taliwind.config.js // config for tailwind we can add custom config for a design system here
├── jsons // jsons for the aem app
│   ├── context_menus // jsons for the context menus
│   ├── review_app // jsons for the review app
│   ├── xmleditor // jsons for xmleditor
```

## /src

```text
├── src
│   ├── **/*{js,ts}
│   ├── index.ts
```

Das Quellverzeichnis enthält die typescript- oder JavaScript-Dateien für Ihre Erweiterung. Die Datei index.ts ist der Einstiegspunkt für Ihre Erweiterung. Sie können alle Komponenten hier importieren und als ein Objekt exportieren. Dieses Objekt wird von der Erweiterung zum Rendern der Komponenten verwendet.

### /dist

Dies ist das endgültige Build-Verzeichnis. Dies enthält das endgültige JS und CSS, die in den AEM kopiert werden müssen

```test
├── dist
│   ├── gudies-extension.js // you can either choose es module (this one) or .cjs(other one) file
│   ├── gudies-extension.umd.cjs
│   ├── build.css // this is your tailwind css output
```

## /jsons

Dieser Ordner enthält die JSONs für die verschiedenen Ansichten. Sie können diese JSONs verwenden, um die Ziele zu identifizieren und die Ansicht anzupassen.

```text
├── jsons // jsons for the aem app
│   ├── context_menus // jsons for the context menus
│   ├── review_app // jsons for the review app
│   ├── xmleditor // jsons for xmleditor
```
