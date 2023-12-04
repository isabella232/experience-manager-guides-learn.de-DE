---
title: Hochladen von Dateien
description: Erfahren Sie, wie Sie Ihre Dateien in das AEM-Repository hochladen und Fehler beheben können. Erfahren Sie mehr über die Benutzeroberfläche der Asset-Konsole, AEM Desktop-Programm, die Erfassung von Asset-Massen und die Verwendung von FrameMaker für Massen-Uploads.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---

# Hochladen von Dateien {#id176FF000JUI}

Wahrscheinlich verfügen Sie über ein Repository mit vorhandenen DITA-Inhalten, das Sie mit AEM Guides verwenden möchten. Für solche vorhandenen Inhalte können Sie einen der folgenden Ansätze verwenden, um Ihre Inhalte stapelweise in AEM Repository hochzuladen:

>[!IMPORTANT]
>
> Siehe [Hinzufügen digitaler Assets zu Adobe Experience Manager as a Cloud Service Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html) für detaillierte Informationen in den unterstützten Methoden zum Hochladen von Inhalten in AEM.

## Benutzeroberfläche der Assets-Konsole

Sie können Inhalte auf Ihrem Desktop auswählen und auf die AEM-Benutzeroberfläche ziehen, \(Webbrowser\), um sie in den Zielordner zu verschieben. Weitere Informationen finden Sie unter [Hochladen von Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html#upload-assets) in AEM Dokumentation.

## AEM-Desktop-Programm

Verwenden Sie AEM Desktop-Programm, wenn Sie Kreativprofis sind und die Assets auf Ihrem lokalen Desktop verwalten möchten. Sie können diese Assets mit Ihren Desktop-Applikationen öffnen und bearbeiten. Sie können auch Versionen verwalten und Ihre Dateien für andere Benutzer freigeben. Weitere Informationen finden Sie unter [AEM Desktop-Programm](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html?lang=de).

## Asset-Massenaufnahme

Wenn Sie über umfangreiche Migrationen und gelegentliche Massenaufnahmen verfügen, verwenden Sie Asset-Massenaufnahmen, um Ihre Inhalte hochzuladen. Mit diesem Tool können Sie Masseninhalte aus unterstützten Datenspeichern wie Azure oder S3 hochladen. Weitere Informationen finden Sie unter [Asset-Massenaufnahme](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=en#asset-bulk-ingestor).

## FrameMaker für Massen-Upload verwenden

Adobe FrameMaker verfügt über einen leistungsstarken AEM-Connector, mit dem Sie Ihre vorhandenen DITA- und anderen FrameMaker-Dokumente \(`.book` und `.fm`\) in AEM. Sie können verschiedene Funktionen zum Hochladen von Dateien verwenden, z. B. das Hochladen einer einzelnen Datei, das Hochladen eines vollständigen Ordners mit oder ohne Abhängigkeiten \(z. B. Inhaltsreferenzen, Querverweise und Grafiken\).

Weitere Informationen zur Verwendung der Massen-Upload-Funktion unter FrameMaker finden Sie im Abschnitt . *Erstellen eines CRX-Ordners und Hochladen von Dateien* im FrameMaker-Benutzerhandbuch.

## Umgang mit Fehlern beim Hochladen von Inhalten {#id201MI0I04Y4}

Falls eine oder mehrere Dateien nicht hochgeladen werden konnten, wird am Ende des Upload-Prozesses eine Eingabeaufforderung mit einer Liste der Dateien angezeigt, die nicht hochgeladen werden konnten:

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Weitere Informationen zu den verschiedenen Szenarien für das Hochladen von Dateien finden Sie unter [DITA-Inhalt hochladen](authoring-file-management.md#).

Wenn Sie ein Tool wie AEM Desktop-Programm oder Asset-Massenaufnahme verwenden, wird die Aktion, die für eine duplizierte Datei ausgeführt werden soll, durch eine Einstellung auf dem AEM-Server gesteuert. Wenden Sie sich an Ihren Systemadministrator, um Informationen zu dieser Konfiguration zu erhalten.

**Übergeordnetes Thema:**[ Inhalt verwalten](authoring.md)
