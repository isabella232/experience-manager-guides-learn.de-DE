---
title: Benutzerdefinierte DITA-Zuordnungsvorlage konfigurieren
description: Erfahren Sie, wie Sie eine benutzerdefinierte DITA-Zuordnungsvorlage konfigurieren
exl-id: 2ad0fc50-97fd-437e-94cc-db5f51f3bc3f
source-git-commit: 0dea2f1d17e7d9b12d07b459a10a00c1dd7460a5
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 1%

---

# Benutzerdefinierte DITA-Zuordnungsvorlage konfigurieren {#id1774F04F05Z}

AEM Guides sind mit zwei nativen Kartenvorlagen ausgestattet - DITA-Map und Bookmap. Sie können basierend auf diesen Vorlagen Karten erstellen. oder Sie können Ihre eigenen Zuordnungsvorlagen definieren, die dann zum Erstellen neuer Zuordnungen verwendet werden können.

Führen Sie die folgenden Schritte aus, um Ihre benutzerdefinierten Zuordnungsvorlagen hinzuzufügen:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an.

1. Navigieren Sie in der Assets-Benutzeroberfläche zu dem Ordner, der zum Speichern der Zuordnungsvorlagendateien konfiguriert ist. Standardmäßig werden alle Zuordnungsvorlagen im Ordner /content/dam/dita-templates/maps gespeichert.

   >[!NOTE]
   >
   > Informationen zum Konfigurieren eines benutzerdefinierten Speicherorts zum Speichern von Themen oder Zuordnungsvorlagen finden Sie unter [Benutzerdefinierten DITA-Vorlagenordnerpfad konfigurieren](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z)

1. Klicken **Erstellen** \> **DITA-Vorlage**.

1. Wählen Sie auf der Blueprint-Seite den Typ der zu erstellenden Zuordnungsvorlage aus.

   >[!NOTE]
   >
   > Sie können die Vorlage Map oder Bookmap als Basis für Ihre neue Vorlage verwenden.

1. Klicken Sie auf **Weiter**.

1. Geben Sie auf der Seite mit den neuen Vorlageneigenschaften eine **Titel** und **Name** für die Vorlage.

   >[!NOTE]
   >
   > Der Name wird basierend auf dem Titel der Vorlage automatisch vorgeschlagen. Wenn Sie den Namen manuell angeben möchten, stellen Sie sicher, dass der Name keine Leerzeichen, Apostroph oder Klammern enthält und mit .ditamap endet.

1. Klicken Sie auf **Erstellen**.

   Die Meldung Zuordnungserstellung wird angezeigt.

   Sie können die Vorlage zum Bearbeiten im Map Editor öffnen oder die Vorlagendatei am Speicherort der Vorlage speichern. Nachdem die Vorlage erstellt wurde, können Sie mit dem Map Editor die Vorlage entsprechend Ihren Authoring-Anforderungen anpassen. Nachdem eine Vorlage erstellt wurde, stellen Sie sicher, dass Sie sie entweder mit einem globalen Profil oder einem Profil auf Ordnerebene verknüpfen.


Wenn Sie das nächste Mal eine neue Zuordnung erstellen, wird Ihre Vorlage auf der Blueprint-Seite angezeigt. Weitere Informationen zum Erstellen einer DITA-Zuordnung finden Sie unter *Verwenden von Adobe Experience Manager-Handbüchern*.

>[!TIP]
>
> Siehe *Benutzerdefinierte Vorlagen* im Handbuch Best Practices für Best Practices zur Verwendung benutzerdefinierter Zuordnungsvorlagen.

**Übergeordnetes Thema:** [Konfigurieren von Themen- und Zuordnungsvorlagen](conf-template-tags.md)
