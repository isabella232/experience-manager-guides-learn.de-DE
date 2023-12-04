---
title: Benutzerdefinierte DITA-Themenvorlage konfigurieren
description: Erfahren Sie, wie Sie benutzerdefinierte DITA-Themenvorlagen konfigurieren
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 2%

---

# Benutzerdefinierte DITA-Themenvorlage konfigurieren {#id16A7G0O02TD}

Die AEM Guides enthalten die folgenden DITA-Themenvorlagen:

- Thema

- Aufgabe

- Konzept

- Verweis

- Glossar

- Fehlerbehebung

- Leer


Sie können diese Vorlagen verwenden, um Themenvorlagen gemäß Ihren Authoring-Anforderungen zu erstellen. Die leere DITA-Vorlage enthält keine Struktur oder Elemente wie die anderen Vorlagen. Sie können die leere Vorlage als Grundlage verwenden, wenn Ihre Vorlage stark angepasst ist und nicht auf normalen DITA-Themenvorlagen basiert.

Um die DITA-Themenvorlage anzupassen und sie für das Authoring zu verwenden, müssen Sie die folgenden drei Hauptaufgaben ausführen:

1. *\(Optional\)* [Benutzerdefinierten DITA-Vorlagenordnerpfad konfigurieren](#id191LCF0095Z)

1. [Benutzerdefinierte Authoring-Vorlage erstellen](conf-folder-level.md#id1917D0EG0HJ)

1. Fügen Sie eine benutzerdefinierte Vorlage zum Profil auf globaler Ebene oder auf Ordnerebene hinzu, wie im Abschnitt [Authoring-Vorlagen konfigurieren](conf-folder-level.md#id1889D0IL0Y4) Abschnitt


## Benutzerdefinierten DITA-Vorlagenordnerpfad konfigurieren {#id191LCF0095Z}

Mit AEM Guides können Sie einen Ordner zum Speichern Ihrer benutzerdefinierten DITA-Map und -Vorlagen konfigurieren. Standardmäßig werden die Vorlagendateien im folgenden Ordner in DAM gespeichert:

`/content/dam/dita-templates/`

Zum Verwalten von Themen- und Zuordnungsvorlagendateien gibt es spezielle Ordner zum Speichern der Themen- und Zuordnungsvorlagen. Standardmäßig werden alle Themenvorlagen unter dem `/content/dam/dita-templates/topics`

Ordner. Alle Zuordnungsvorlagen werden im `/content/dam/dita-templates/maps` Ordner.

Als Administrator können Sie benutzerdefinierte Zuordnungs- oder Themenvorlagen im Standardordner erstellen oder einen eigenen Ordner zum Speichern benutzerdefinierter Vorlagen erstellen. Wenn Sie den Standardordner verwenden möchten, können Sie diesen Prozess überspringen.

Um einen Ordner für Ihre benutzerdefinierten DITA-Themenvorlagen zu konfigurieren, führen Sie die folgenden Schritte aus:

>[!IMPORTANT]
>
> Sie können diesen Prozess überspringen, wenn Sie den Standardordner zum Speichern benutzerdefinierter Vorlagen verwenden möchten.

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf *com.adobe.fmdita.config.ConfigManager* Bundle

1. Im **Vorlagenspeicherort** -Eigenschaft, geben Sie einen Speicherort für benutzerdefinierte Vorlagen an.

1. Klicken Sie auf **Speichern**.


Wenn der angegebene Speicherort in DAM vorhanden ist, werden alle standardmäßigen Zuordnungs- und Themenvorlagen in diesen Ordner kopiert. Wenn der Speicherort nicht vorhanden ist, wird der Ordner mit allen standardmäßigen Zuordnungs- und Themenvorlagen erstellt.

**Übergeordnetes Thema:**[ Konfigurieren von Themen- und Zuordnungsvorlagen](conf-template-tags.md)
