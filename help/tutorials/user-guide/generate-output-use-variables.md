---
title: Verwenden Sie Variablen zum Festlegen der Optionen "Zielpfad", "Site-Name"oder "Dateiname"
description: Erfahren Sie, wie Sie Variablen zum Festlegen der Optionen für Zielpfad, Site-Name oder Dateiname verwenden. Lernen Sie native Variablen kennen, die in AEM Guides unterstützt werden.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Verwenden Sie Variablen zum Festlegen der Optionen &quot;Zielpfad&quot;, &quot;Site-Name&quot;oder &quot;Dateiname&quot;


Beim Generieren von Ausgaben in AEM Site oder PDF können Sie Variablen verwenden, um die Optionen Zielpfad, AEM Site-Name oder PDF-Dateiname zu definieren. Sie können eine einzelne oder eine Kombination von Variablen verwenden, um diese Optionen zu definieren.

In der folgenden Tabelle sind die Variablen aufgeführt, die standardmäßig unterstützt werden:

| Variable | Endziel-Pfad | Beispiel |
| --- | --- | --- |
| `${map_filename}` | Verwendet den Namen der DITA-Map-Dateien, um den Zielpfad zu erstellen. | **DITA-Map-Dateiname**:<br>`AEMGuides.ditamap`<br><br>**Zielpfad** konfiguriert als:<br>`/content/output/sites/${map_filename}`<br><br>**Endlicher Ausgabeort**:<br>`/content/output/sites/aemGuides/AEMGuides.html` |
| `${map_title}` | Verwendet den DITA-Map-Titel, um den Zielpfad zu erstellen. | **DITA-Map-Dateiname**:<br>`AEMGuides.ditamap`<br><br>**DITA-Map-Titel**:<br>`AEMGuides`<br><br>**Zielpfad** konfiguriert als:<br>`/content/output/sites/${map_title}`<br><br>**Endlicher Ausgabeort**:<br>`/content/output/sites/AEMGuides/AEMGuides.html` |
| `${preset_name}` | Verwendet den Namen der Ausgabevorgabe, um den Zielpfad zu erstellen. | **Name der Ausgabevorgabe**:<br>`AEM Guides PDF Output`<br><br>**DITA-Map-Dateiname**:<br>`SampleDita.ditamap`<br><br>**Zielpfad** konfiguriert als:<br>`/content/output/sites/${preset_name}`<br><br>**Endlicher Ausgabeort**:<br>`/content/output/sites/AEM Guides PDF Output/SampleDita.html` |
| `${language_code}` | Verwendet den Sprachcode, in dem sich die Map-Datei befindet, um den Zielpfad zu erstellen. | **DITA-Map-Dateiname**:<br>`SampleDita.ditamap`<br><br>**DITA-Map-Dateipfad**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Zielpfad** konfiguriert als:<br>`/content/output/sites/${language_code}`<br><br>**Endlicher Ausgabeort**:<br>`/content/output/sites/en/SampleDita.html` |
| `${map_parentpath}` | Verwendet den vollständigen Pfad der Map-Datei, um den Zielpfad zu erstellen.<br><br>**Hinweis**:Diese Variable kann nicht verwendet werden, um den AEM Site-Namen oder PDF-Dateinamen anzugeben. | **DITA-Map-Dateiname**:<br>`SampleDita.ditamap`<br><br>**DITA-Map-Dateipfad**:<br>`/content/dam/projects/AEM-Guides/en/user-guide`/<br><br>**Zielpfad** konfiguriert als:<br>`/content/output/sites/${map_parentpath}`<br><br>**Endlicher Ausgabeort**:<br>`/content/output/sites/content/dam/projects/AEM-Guides/en/user-guide/SampleDita.html` |
| `${path_after_langfolder}` | Verwendet den Pfad der Map-Datei nach dem Sprachordner, um den Zielpfad zu erstellen.<br><br>**Hinweis**: Diese Variable kann nicht verwendet werden, um den AEM Site-Namen oder PDF-Dateinamen anzugeben. | **DITA-Map-Dateiname**:<br>`SampleDita.ditamap`<br><br>**DITA-Map-Dateipfad**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Zielpfad** konfiguriert als:<br>`/content/output/sites/${path\_after\_langfolder}`<br><br>**Endlicher Ausgabeort**:<br>`/content/output/sites/user-guide/SampleDita.html` |
| `${system_date}` | Verwendet das aktuelle Server-Datum, um den Zielpfad zu erstellen. | **DITA-Map-Dateiname**: <br> `SampleDita.ditamap` <br><br> **DITA-Map-Dateipfad:** <br> `/content/dam/projects/AEM-Guides/en/user-guide/` <br><br> **Zielpfad** konfiguriert als: <br> `/content/output/sites/${system_date}` <br> <br> **Endlicher Ausgabespeicherort:** <br> /`content/output/sites/08252023/SampleDita.html` |
| `${system_time}` | Verwendet die aktuelle Serverzeit zum Erstellen des Zielpfads. | **DITA-Map-Dateiname:** <br>`SampleDita.ditamap` <br> <br> **DITA-Map-Dateipfad:** <br>`/content/dam/projects/AEM-Guides/en/user-guide/` <br><Br>**Zielpfad** konfiguriert als: <br> `/content/output/sites/${system_time}`<br><br>**Endlicher Ausgabespeicherort:**<br>`/content/output/sites/055612/SampleDita.html` |

Darüber hinaus können Sie auch die für die DITA-Map- oder Bookmap-Datei definierten Metadaten als Variablen verwenden. Die Metadaten finden Sie unter der `/jcr:content/metadata` -Knoten der DITA-Map- oder Bookmap-Datei. Beispielsweise wird eine der Metadateneigenschaften definiert, die im `/jcr:content/metadata` node is `dc:title`. Sie können `${dc:title}` und der Titelwert in der endgültigen Ausgabe verwendet wird.
**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)
