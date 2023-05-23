---
title: Migration von Nicht-UUID-zu-UUID-Inhalten
description: Erfahren Sie, wie Sie die Migration von Nicht-UUID-zu-UUID-Inhalten durchführen.
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# Migration von Nicht-UUID-zu-UUID-Inhalten {#id226TI0U20XA}

>[!IMPORTANT]
>
> Sie können Ihre Nicht-UUID-Inhalte auf den UUID-Server migrieren. Um auf den UUID-Server zu migrieren, sollte der Nicht-UUID-Server mit AEM Guides Version 4.0 installiert sein.

Führen Sie die folgenden Schritte aus, um Ihre Nicht-UUID-Inhalte zu migrieren:

>[!NOTE]
>
> Jeder Schritt ist von entscheidender Bedeutung, und das Fehlen eines der Schritte kann zu fehlgeschlagenen oder beschädigten Serverdaten führen. Stellen Sie sicher, dass Sie alle Schritte ausführen.

1. Stellen Sie sicher, dass **Aktivieren von Workflow-Startern für Nachbearbeitung** in *com.adobe.fmdita.config.ConfigManager* und **Versionspostverarbeitung aktivieren** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation* aktiviert sind.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Installieren Sie die UUID-Version der nächsten Hauptversion gegenüber der Nicht-UUID-Version. Wenn Sie beispielsweise 4.0 Nicht-UUID-Build verwenden, müssen Sie UUID Version 4.1 installieren.

1. Deaktivieren Sie auf der Registerkarte &quot;Launcher&quot;die folgenden Workflows und jeden anderen Workflow, der unter /content/dam mit den Startern in ausgeführt wird. `http://localhost:4502/libs/cq/workflow/content/console.html`:

   - **DAM-Update-Asset** Workflow
   - **DAM-Metadaten-Writeback** Workflow

1. Deaktivieren **Aktivieren von Workflow-Startern für Nachbearbeitung** in *com.adobe.fmdita.config.ConfigManager* und deaktivieren **Versionspostverarbeitung aktivieren** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation*.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Hinzufügen einer separaten Protokollfunktion für `com.adobe.fmdita.uuid.upgrade.UuidUpgrade.`

   Die Browserantwort ist auch unter /content/uuid-upgrade/logs verfügbar.

1. Führen Sie die angegebene Abfrage für einen Ordner mit kleineren Daten mit `doReviews=false` bevor sie auf /content/dam ausgeführt wird: `http://localhost:4502/bin/dxml/uuid_upgrade?root=/content/dam/test&doReviews=false`

   >[!TIP]
   >
   >  Sie können überprüfen, ob alle Dateien im Ordner ordnungsgemäß aktualisiert wurden und alle Funktionen nur für diesen Ordner funktionieren.

**Parameter für die Abfrage:**

    - &quot;root&quot;: Stammordner, in dem die Aktualisierung durchgeführt werden muss \(Verwenden Sie /content/dam für alle Repositorys.\)
    - &quot;doReviews&quot;: true/false \(Wenn Reviews aktualisiert werden müssen oder nicht. Der Standardwert lautet „false“. \)
    - &quot;doBaselines&quot;: true/false \(Wenn Grundlinien aktualisiert werden müssen oder nicht. Der Standardwert ist &quot;true&quot;.\)
    - &quot;processLevel&quot;: -1\(fehlgeschlagen ohne Wiederherstellung\), 0\(fehlgeschlagen mit Wiederherstellung\), 1\(fehlgeschlagen mit Fehlern\), 2\(erfolgreich aktualisiert\) \(Wenn das Skript nach einem Fehler erneut versucht wird, werden nur Dateien mit &quot;fmUpgradeStatus&quot; &lt;= processLevel erneut verarbeitet, andernfalls wird es ignoriert. Der Standardwert ist 1.\)
    - &quot;ignoreImageVersions&quot;: true/false \(ignoriert die Verarbeitung von Bildversionen. Der Standardwert lautet „false“. \)
    >[!NOTE]
    >
    > Wir können die Inhaltsmigration auf Ordnerebene oder auf den vollständigen Inhalt/DAM oder auf demselben Ordner ausführen \(Migration erneut ausführen\).

1. Nachdem der Server erfolgreich migriert wurde, aktivieren Sie die folgenden Workflows und Nachbearbeitungen, damit sie weiterhin auf dem Server arbeiten:

   - **DAM-Update-Asset** Workflow
   - **DAM-Metadaten** Workflow

>[!NOTE]
>
> Wenn einige Dateien nicht verarbeitet werden oder vor der Migration beschädigt sind, bleiben sie auch nach der Migration beschädigt.

