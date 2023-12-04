---
title: Konfigurieren Sie die JSON-basierte Zuordnung zwischen einem Thema und einem Inhaltsfragmentmodell.
description: Erfahren Sie, wie Sie die JSON-basierte Zuordnung zwischen einem Thema und einem Inhaltsfragmentmodell konfigurieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Erstellen einer Zuordnung zwischen einem Thema und einem Inhaltsfragment

AEM Guides bieten die Funktion zum Erstellen einer JSON-basierten Zuordnung zwischen einem Thema und einem Inhaltsfragmentmodell. Sie können diese Zuordnung verwenden, um Inhalte in einigen oder allen Elementen innerhalb eines Themas in einem Inhaltsfragment zu veröffentlichen.

1. So laden Sie die *contentFragmentMapping.json*, melden Sie sich als Administrator bei Adobe Experience Manager an.
1. Wählen Sie oben den Link Adobe Experience Manager aus und wählen Sie **Instrumente**.
1. Wählen Sie in der Liste der Tools die Option Guides aus und wählen Sie die **Ordnerprofile**.
1. Wählen Sie die **Globales Profil** Kachel.
1. Wählen Sie die **Konfiguration des XML-Editors** und wählen Sie die **Bearbeiten** Symbol oben.
1. Wählen Sie die **Herunterladen** zum Herunterladen des *contentFragmentMapping.json*  -Datei auf Ihrem lokalen System. Anschließend können Sie Änderungen an der Datei vornehmen und diese dann hochladen.

1. Sie müssen die folgenden Validierungen befolgen:

   1. Es sollte sich um eine JSON-Datei handeln
   2. Sie sollte ein Array enthalten, das mindestens ein Objekt enthält. Jedes Objekt sollte Folgendes enthalten:


      `"name": string `

      `"mapping": array`

      Jedes Objekt der Zuordnung muss Folgendes enthalten:

      `"modelField": string`

      `"xpath": string`

      `"outputType": string`
1. Speichern Sie die Datei und laden Sie sie hoch.

Beispieldatei:

```
[
  {
    "mapping": [
      {
        "modelField": "title",
        "xpath": "/topic[1]/title[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "shortdesc",
        "xpath": "/topic[1]/shortdesc[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "topicData",
        "xpath": "/topic[1]/body[1]",
        "outputType": "outerHTML"
      }
    ],
    "name": "Full Topic"
  },
  {
    "mapping": [
      {
        "modelField": "title",
        "xpath": "/topic[1]/title[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "shortdesc",
        "xpath": "/topic[1]/shortdesc[1]",
        "outputType": "textContent"
      },
      {
        "modelField": "heroImage",
        "xpath": "/topic[1]/body[1]/p[1]/image[1]",
        "outputType": "outerHTML"
      },
      {
        "modelField": "dataTable",
        "xpath": "/topic[1]/body[1]/table[1]",
        "outputType": "outerHTML"
      }
    ],
    "name": "Sample Example with XPath"
  }
]
```

Sie können das gesamte Thema mit der Standardzuordnung veröffentlichen. Wählen Sie die `Full Topic` Zuordnung aus dem Dropdown-Menü im **Als Inhaltsfragment veröffentlichen** und weisen das Feld &quot;topicData&quot;im Inhaltsfragmentmodell auf.
