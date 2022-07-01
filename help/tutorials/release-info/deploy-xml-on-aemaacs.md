---
title: Hinzufügen von [!DNL AEM Guides] auf [!DNL AEM as a Cloud Service] Umgebung
description: Erfahren Sie, wie Sie [!DNL AEM Guides] auf [!DNL AEM as a Cloud Service] Umgebung
exl-id: a1e020c2-360c-4d71-b5fd-8179d9ceacda
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# [!DNL AEM Guides] as a Cloud Service Implementierung

Erfahren Sie, wie Sie [!DNL Guides] auf [!DNL AEM as a Cloud Service] Umgebung.

## Manuelle Implementierung über die Git-Pipeline von Cloud Manager

Wenn Sie gekauft haben [!DNL AEM Guides] Befolgen Sie as a Cloud Service vor dem 29. März 2022 die folgenden Bereitstellungsanweisungen:

* Wenn Sie die Aktualisierung starten, können Sie den automatisch von [!UICONTROL Cloud Manager] mit dem Code aus dem folgenden Repo, das bereits das XML-Plug-in integriert hat: https://github.com/Adobe-TCS/XML-documentation-for-AEMaaCS

* Wenn Sie bereits eingecheckte Anpassungen in [!UICONTROL Cloud Manager] git repo, finden Sie im folgenden Repo Anweisungen zum Hinzufügen des XML-Plug-ins in Ihrem vorhandenen Code: https://github.com/Adobe-TCS/DoX-Installer-for-AEMaaCS

## Implementierung über Cloud Manager

Wenn Sie ein Kunde sind, der [!DNL AEM Guides] as a Cloud Service am oder nach dem 29.03.2022, befolgen Sie diese Anweisungen zum Hinzufügen von [!DNL Guides] auf [!DNL AEM as a Cloud Service] Umgebung:

1. Anmelden bei [!UICONTROL Cloud Manager].

1. Bearbeiten Sie das Programm, für das Sie konfigurieren möchten [!DNL AEM Guides].

1. Wechseln zu **[!UICONTROL Lösungen und Add-ons]** Registerkarte.

1. Im **[!UICONTROL Lösungen und Add-ons]** Tabelle, klicken Sie auf **[!UICONTROL Assets]**.

1. Auswählen **[!UICONTROL Handbücher]** und wählen Sie **[!UICONTROL Speichern]**.

Sie haben Ihr Programm erfolgreich für die automatische Bereitstellung der AEM Guides-Lösung konfiguriert.

![Konfigurieren AEM Guides-Lösung](assets/addon-configuration.png)

>[!NOTE]
>
>Installieren [!DNL AEM Guides] in jeder Umgebung des integrierten Programms müssen Sie die mit der Umgebung verknüpfte Pipeline ausführen. Für die Installation von [!DNL AEM Guides].
