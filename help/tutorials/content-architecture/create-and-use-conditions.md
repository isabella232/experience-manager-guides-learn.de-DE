---
title: Erstellen und Verwenden von Bedingungen
description: Erfahren Sie, wie Sie Bedingungen erstellen und dann die Generierung bedingter Inhalte in [!DNL AEM Guides]
role: User
exl-id: a86007e3-48d1-458b-84a7-b683e113e5b2
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 2%

---

# Erstellen und Verwenden von Bedingungen und Generieren einer bedingten Ausgabe

**Anwendungsfall**


* Autoren können Bedingungen für ein Inhaltselement festlegen, damit sie steuern können, ob es in der Ausgabe angezeigt wird.

* Autoren können bei der Veröffentlichung auswählen, ob unterschiedliche Bedingungen angezeigt oder ausgeblendet werden sollen.

* Beispielsweise können Autoren Attribute als Version 1.0 und Version 2.0 zum Inhalt hinzufügen und Bedingungen verwenden, um Version 1.0 für Version 1.0 einzubeziehen und Version 2.0 auszuschließen.

**Schritt 1**

Bedingungen für die Dokumentation definieren unter [!UICONTROL Ordnerprofile]: Siehe Abschnitt **Bedingte Attribute für globale Profile oder Profile auf Ordnerebene konfigurieren** in [Seite 64 des Installations- und Konfigurationshandbuchs](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-8/XML-Documentation-for-Adobe-Experience-Manager_Installation-Configuration-Guide_EN.pdf)

![Bedingungen in Ordnerprofilen konfigurieren](assets/conditions-in-profiles.png)

**Schritt 2**

Wählen Sie die **[!UICONTROL Ordnerprofil]** definiert in Schritt 1 unter **Benutzereinstellungen** im XML-Editor: Siehe Abschnitt **Benutzereinstellungen** in [Seite 39 des Benutzerhandbuchs](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-8/XML-Documentation-for-Adobe-Experience-Manager_User-Guide_EN.pdf)


**Schritt 3**

Verwenden Sie die Bedingungen, um Abschnitte des Inhalts mit Bedingungen zu versehen: Siehe Abschnitt **Bedingungen** in [Seite 81 des Benutzerhandbuchs](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-8/XML-Documentation-for-Adobe-Experience-Manager_User-Guide_EN.pdf)

![Nutzungsbedingungen im Web-Editor](assets/conditions-in-web-editor.png)

**Schritt 4**

Definieren Sie Bedingungsvorgaben auf Zuordnungsebene, um zu wählen, welche Bedingungen in der Ausgabe aktiviert werden sollen: Siehe Abschnitt **Verwenden von Bedingungsvorgaben** in [Seite 184 des Benutzerhandbuchs](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-8/XML-Documentation-for-Adobe-Experience-Manager_User-Guide_EN.pdf)