---
title: Smart-Tagging
description: Erfahren Sie, wie Sie Smart-Tags in AEM Handbüchern hinzufügen. Verwenden Sie das XML-Tool zur Suchbegriffextraktion , um relevante Suchbegriffe zu extrahieren.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Smart-Tagging {#id216KH0ID0Y8}

>[!IMPORTANT]
>
> Die Funktion für Smart-Tagging ist nicht standardmäßig verfügbar und erfordert eine benutzerdefinierte Implementierung, für die Sie sich an Ihren Systemadministrator wenden müssen.

AEM Guides enthalten die Funktion zum Hinzufügen von Smart-Tags. Sie können das XML-Tool zur Suchbegriffextraktion verwenden, um Smart-Tags zu extrahieren. Dieses Tool verwendet künstliche Intelligenz, um den Inhalt zu verstehen und relevante Schlüsselwörter bereitzustellen. Sie können Smart-Tags verwenden, um die Suchmaschinenoptimierung \(SEO\) zu verbessern und den Benutzern bei der Suche nach zugehörigen Inhalten zu helfen.

Führen Sie die folgenden Schritte aus, um Smart-Tags zu erstellen:

1. Navigieren Sie in der Assets-Benutzeroberfläche zu dem Thema, für das Sie die Smart-Tags erstellen möchten.
1. Öffnen Sie das Thema im Vorschaumodus und wählen Sie **Assets erneut verarbeiten** in der Hauptsymbolleiste.
1. Wählen Sie XML-Suchbegriffextraktion aus, um relevante Suchbegriffe zu extrahieren.

   ![](images/smart-tag-reprocess-asset.png){width="300" align="left"}

1. Wählen Sie die Option Nachbearbeitungsprozess ausführen aus. Bei erfolgreichem Toolstart wird eine Meldung angezeigt.
1. Die Tags werden automatisch extrahiert und können auf der Seite Eigenschaften des ausgewählten Themas eingesehen werden.

   ![](images/properties-smart-tags.png){width="800" align="left"}

   >[!NOTE]
   >
   > Neben der Extraktion der Suchbegriffe über das XML-Tool zur Suchbegriffextraktion können Sie auch die Smart-Tags auf der Eigenschaftsseite hinzufügen, löschen oder anpassen.


*Wenden Sie sich an Ihr Customer Success Team, um diese Funktion in der Umgebung aktivieren zu lassen. Dies ist im Rahmen der nativen Unterstützung nicht aktiviert.*

**Übergeordnetes Thema:**[ Verwalten von Metadaten](manage-metadata.md)
