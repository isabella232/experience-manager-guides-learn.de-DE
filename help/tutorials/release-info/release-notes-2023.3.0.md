---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version März 2023
description: Version der Adobe Experience Manager-Handbücher as a Cloud Service im März
source-git-commit: 99ca14a816630f5f0ec1dc72ba77994ffa71dff6
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---


# Version der Adobe Experience Manager-Handbücher as a Cloud Service im März 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version März 2023 der Adobe Experience Manager-Handbücher behobenen Probleme (später auch als *AEM as a Cloud Service Handbücher*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version AEM Guides as a Cloud Service im März 2023](whats-new-2023.3.0.md).

## Aktualisierung auf Version März 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der AEM Guides zu aktualisieren:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2023.3.242.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die Version AEM Guides im März 2023 as a Cloud Service zu aktualisieren.

## Schritte zum Indexieren des vorhandenen Inhalts (nur, wenn Sie eine Version vor der September-Version von AEM Guides as a Cloud Service verwenden)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungsebene zu suchen und zu ersetzen:

* Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>/bin/guides/map-find/indexing`.
(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert || Beispiel : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Beispiel: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von AEM Guides as a Cloud Service im März 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| AEM zu Handbüchern as a Cloud - Version | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | Nicht kompatibel | 2022 oder höher |
|  |  |  |


### Sauerstoffanschluss

| AEM zu Handbüchern as a Cloud - Version | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


