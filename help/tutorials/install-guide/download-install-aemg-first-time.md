---
title: erstmaliges Herunterladen und Installieren AEM Handbücher
description: Erfahren Sie, wie Sie zum ersten Mal AEM Handbücher herunterladen und installieren
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# erstmaliges Herunterladen und Installieren AEM Handbücher {#id213BCL00KEV}

Führen Sie die folgenden Schritte aus, um AEM Guides zum ersten Mal auf einen Computer herunterzuladen und zu installieren:

>[!IMPORTANT]
>
> Wenn Sie Livefyre zusammen mit AEM Guides verwenden möchten, stellen Sie sicher, dass Sie die Livefyre-Versionen vor Version 3.0 installieren, bevor Sie AEM Guides installieren. Wenn Sie Livefyre Version 3.0 oder höher verwenden, gibt es keine solche Einschränkung.

1. Laden Sie AEM Handbücher vom Adobe Software Distribution-Portal herunter.

1. Melden Sie sich bei Ihrer AEM-Instanz an und navigieren Sie zum CRX Package Manager. Die Standard-URL für den Zugriff auf den Paketmanager lautet:

   ```http
   http://<server name>:<port>/crx/packmgr/index.jsp
   ```

   Der Package Manager verwaltet die Pakete in Ihrer lokalen AEM-Installation. Weitere Informationen zum Arbeiten mit Package Manager finden Sie unter [Arbeiten mit Paketen](https://helpx.adobe.com/de/experience-manager/6-5/sites/administering/using/package-manager.html) in AEM Dokumentation.

   ![](assets/package-manager.png){width="650" align="left"}

1. Um das Package AEM Guides hochzuladen, klicken Sie auf **Paket hochladen**.

1. Navigieren Sie im Dialogfeld &quot;Paket hochladen&quot;zur Datei &quot;AEM Guides&quot;, die Sie in Schritt 1 heruntergeladen haben, und klicken Sie auf **OK**.

   Das Paket wird in Ihre AEM-Instanz hochgeladen.

1. Um das Paket zu installieren, klicken Sie auf **Installieren**.

   ![](assets/install-package.png){width="650" align="left"}

1. Klicken Sie im Dialogfeld Paket installieren auf **Installieren**.

1. Um mit AEM Guides zu beginnen, klicken Sie auf die Schaltfläche &quot;Startseite&quot; ![](assets/home-button.png) in der linken oberen Ecke des CRX Package Manager.


>[!NOTE]
>
> Führen Sie den Installationsvorgang für alle Instanzen von AEM-Servern in Ihrer Einrichtung durch.

**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)

