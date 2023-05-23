---
title: Gültige Dateinamen für AEM Site-Ausgabe konfigurieren
description: Erfahren Sie, wie Sie gültige Dateinamen für AEM Site-Ausgabe konfigurieren.
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# Gültige Dateinamen für AEM Site-Ausgabe konfigurieren {#id214GK0X0KXA}

Ähnlich wie bei der Liste gültiger Dateinamenzeichen, die für DITA-Themen zulässig sind, können Sie auch eine Liste gültiger Dateinamenzeichen für AEM Site-Ausgabe konfigurieren. Einige der bekannten Zeichen, die in einer URL nicht zulässig sind, sind: ```'<>`@$```. Diese Zeichen werden so konfiguriert, dass sie automatisch in einen Unterstrich (_) umgewandelt werden, wenn sie beim Generieren AEM Site-Ausgabedateinamen gefunden werden. Die Konfiguration, mit der Sie gültige Zeichen in AEM Site-Ausgabe festlegen können, ist in der `com.adobe.fmdita.common.SanitizeNodeNameImpl` Bundle. **Festlegen des Zeichensatzes &quot;Unzulässig&quot;für die Veröffentlichung in AEM Sites** -Einstellung, um Zeichen einzuschließen, die Sie durch einen Unterstrich in die Namen der AEM Site-Ausgabedateien ersetzen möchten.

**Übergeordnetes Thema:**[ Dateinamen konfigurieren](conf-file-names.md)

