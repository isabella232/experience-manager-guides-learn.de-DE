---
title: Übergeben der Metadaten an die Ausgabe mithilfe von DITA-OT
description: Erfahren Sie, wie Sie die Metadaten mithilfe von DITA-OT an die Ausgabe übergeben.
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Übergeben der Metadaten an die Ausgabe mithilfe von DITA-OT {#id21BJ00QD0XA}

Metadaten sind zusätzliche Informationen zur Ausgabe. In AEM Handbüchern können Sie die vorhandenen Metadaten übergeben oder benutzerdefinierte Metadaten-Tags erstellen. Sie können Metadaten mithilfe der DITA-OT-Veröffentlichung an AEM-, PDF-, HTML5-, EPUB- und benutzerdefinierte Formatausgaben übergeben.

Führen Sie die folgenden Schritte aus, um die Metadaten mithilfe der DITA-OT-Veröffentlichung an die Ausgabe zu übergeben:

1. Im **Assets-Benutzeroberfläche**, navigieren Sie zur DITA-Map-Datei, für die Sie die Metadaten an DITA-OT übergeben möchten, und klicken Sie darauf.
1. Wählen Sie eine Ausgabevorgabe aus und bearbeiten Sie sie, an die Sie die Metadatenfelder übergeben möchten. Wählen Sie beispielsweise eine PDF-Ausgabevorgabe aus.
1. Auswählen **DITA-OT** unter Generieren &lt;output> Verwenden der Option in der ausgewählten Ausgabevorgabe.

   ![](images/custom-meta-data-output-preset.png)

1. Wählen Sie in der Dropdown-Liste Eigenschaften die Metadaten aus, die Sie an die DITA-OT-Veröffentlichung übergeben möchten.

   In der Dropdown-Liste Eigenschaften werden sowohl die benutzerdefinierten als auch die Standardeigenschaften aufgelistet. Im obigen Screenshot-Autor ist beispielsweise die benutzerdefinierte Eigenschaft, während `dc:description`, `dc:language`, `dc:title`und `docstate` sind die Standardeigenschaften.

   >[!NOTE]
   >
   > Diese Eigenschaften werden aus der Datei metadataList ausgewählt, die am folgenden Speicherort verfügbar ist:`/libs/fmdita/config/metadataList`. In dieser Datei sind standardmäßig vier Eigenschaften aufgeführt: `dc:description`, `dc:language`, `dc:title`und `docstate`.

   Diese Datei kann überlagert werden unter: `/apps/fmdita/config/metadataList`.

   Informationen zum Übergeben einer benutzerdefinierten Eigenschaft, für die Sie die Werte bereits definiert haben, finden Sie unter [Verwenden AEM Metadaten in der DITA-OT-PDF-Ausgabe](https://experienceleaguecommunities.adobe.com/t5/xml-documentation-discussions/use-aem-metadata-in-dita-ot-pdf-output/td-p/411880).

1. Aus dem **Eigenschaften** Dropdown-Liste die gewünschten benutzerdefinierten und standardmäßigen Eigenschaften aus. Wählen Sie beispielsweise `author`, `dc:title`und `dc:description`. Dies sind die Standardwerte `metadata/properties` wird erstellt, sobald wir eine Datei erstellen. Die ausgewählten Eigenschaften werden unter dem Dropbox-Menü aufgeführt.

   ![](images/selected-metadata-properties.png)

1. Klicken **Fertig** oben links, um die Änderungen zu speichern.
1. Generieren Sie die Ausgabe.

Die ausgewählten Metadateneigenschaften werden an die mit DITA-OT generierte Ausgabe übergeben.

**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)

