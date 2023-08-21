---
title: Konvertieren von Nicht-UUID-Inhalten mit Versionen in UUID-Inhalt
description: Erfahren Sie, wie Sie Nicht-UUID-Inhalte mit Versionen migrieren.
source-git-commit: 33cdc1b14db0d123c01bbc719c2833ce0df4c9d9
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 4%

---




# Migrieren von Nicht-UUID-Inhalten mit Versionen

Führen Sie diese Schritte aus, um Ihren Nicht-UUID-Inhalt mit Versionen zu UUID-Inhalten zu migrieren.

## Kompatibilitätsmatrix

| Aktuelle AEM Guides-Version (Nicht-UUID) | Erforderliche Version für die Migration zu UUID | Unterstützter Aktualisierungspfad |
|---|---|---|
| 3.8.5 | 4.0 non-UUID | Installieren Sie 4.1 (UUID) und führen Sie die Migration aus. |
| 4.0, 4.0.x, 4.1 oder 4.1.x | Wie aktuelle Nicht-UUID | Installieren Sie 4.1 (UUID) und führen Sie die Migration aus. |
| 4.2 oder höher | nicht vorhanden | Noch nicht unterstützt |

## Erforderliche Pakete

1. **Versionsbereinigung**: `com.adobe.guides.version-purge-1.0.11.zip` (optional)
1. **Vormigration**: `com.adobe.guides.pre-uuid-migration-1.0.7.zip`
1. **Migration**: `com.adobe.guides.uuid-upgrade-1.0.17`
1. **Nachmigration**: `com.adobe.guides.post-uuid-migration-1.0.2.zip`


## Vormigration

1. (Optional) Führen Sie eine Versionsbereinigung für den Inhalt durch, um unnötige Versionen zu entfernen und den Migrationsprozess zu beschleunigen. Um die Versionsbereinigung für Version 4.1 durchzuführen (NICHT unterstützt für Version 4.0), installieren Sie das Paket `com.adobe.guides.version-purge-1.0.11.zip`und gehen Sie mithilfe dieser URL zur Benutzeroberfläche `http://<server-name> /libs/fmdita/clientlibs/xmleditor_version_purge/page.html`.

   >[!NOTE]
   >
   >Dieses Dienstprogramm entfernt keine Versionen, die in Grundlinien- oder Rezensionen verwendet werden, oder hat Beschriftungen.
1. Installieren Sie das Vormigrationspaket (`com.adobe.guides.pre-uuid-migration-1.0.7.zip`).

1. Führen Sie die folgende Abfrage aus, um einen Bericht mit einer geschätzten Zeitdauer (ETA) zu erhalten, wie lange die Migration dauern wird, und meldet, ob es Dateien mit Inhaltsproblemen gibt, die nicht migriert würden.

>[!NOTE]
>
>Sie benötigen Administratorrechte, um die Migration ausführen zu können.


| Endpunkt-URL | Anfragetyp | Abfrageparameter | Erwartete Ergebnisse |
|---|---|---|---|
| `/bin/guides/pre_uuid_upgrade` <br> <br>**Beispiel**: http://localhost:4502/bin/guides/pre_uuid_upgrade?root=/content/dam | GET | **root**: Stammordner<br> **Wert**: `/content/dam` für das gesamte Repository. | Es wird ein Vormigrationsbericht (.csv) erstellt, in dem die Anzahl der Dateien, die Gesamtversionen und die Fehler aufgelistet werden. <br><br> **Beispielausgabe**:<br>RootFolder: /content/dam <br>Dateien insgesamt: 2697 <br>Versionen insgesamt: 10380 <br>Anzahl der fehlerhaften Dateien: 28 <br>Ein detaillierter Bericht wird über AEM CRX unter `/content/uuid-pgrade/UuidMigrationReport_1688400131039.csv` |

Dieser Schritt kann fehlschlagen, wenn sich im System viele DITA-Dateien befinden. Erhöhen Sie dazu die Anzahl der in der Abfrage durchsuchten Dateien, indem Sie den Wert von *Limit zum Lesen des Speichers (queryLimitReads)* in Apache Jackrabbit Query Engine Settings Service von 10000 eine Zahl, die größer ist als die Gesamtzahl der im System vorhandenen DITA-Assets.

## Migration

### Schritt 1: Konfiguration aktualisieren

1. Stellen Sie sicher, dass der verfügbare freie Speicherplatz mindestens dem 10-fachen des Speicherplatz entspricht, den AEM (crx-quickstart-Verzeichnis) während der Migration benötigt. Nach Abschluss der Migration können Sie den Großteil des Festplattenspeichers durch Ausführen der Komprimierung zurückgewinnen (siehe [Revisionsbereinigung](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=en)).

1. Aktivieren *Aktivieren von Workflow-Startern für Nachbearbeitung* in `com.adobe.fmdita.config.ConfigManager` und *Aktivieren der Versionspostverarbeitung* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation.`

1. Installieren Sie die UUID-Version der unterstützten Version über die Nicht-UUID-Version. Wenn Sie beispielsweise einen 4.0-Nicht-UUID-Build oder einen 4.1-Nicht-UUID-Build verwenden, müssen Sie UUID-Version 4.1 installieren.

1. Installieren Sie das neue Paket für die UUID-Migration (`com.adobe.guides.uuid-upgrade-1.0.17`).

1. Deaktivieren Sie die folgenden Workflows und jeden anderen Workflow, der ausgeführt wird `/content/dam` Verwenden von Startern in `http://localhost:4502/libs/cq/workflow/content/console.html`.

   * Workflow „DAM-Update-Asset“
   * DAM-Metadaten-Writeback-Workflow

1. Deaktivieren *Aktivieren von Workflow-Startern für Nachbearbeitung* in `com.adobe.fmdita.config.ConfigManager` und deaktivieren *Aktivieren der Versionspostverarbeitung* in `com.adobe.fmdita.postprocess.version.PostProcessVersionObservation`.

1. Deaktivieren Sie die Eigenschaft Validierung aktivieren (`validation.enabled`) in Day CQ Tagging Service.

1. Stellen Sie sicher, dass `uuid.regex` Eigenschaftsordner wird ordnungsgemäß in `com.adobe.fmdita.config.ConfigManager`. Wenn es leer ist, setzen Sie es auf den Standardwert - `^GUID-(?<id>.*)`.
1. Hinzufügen einer separaten Protokollfunktion für `com.adobe.fmdita.uuid.upgrade.UuidUpgrade` Die Browserantwort ist auch unter folgender Adresse verfügbar: `/content/uuid-upgrade/logs`.

### Schritt 2: Ausführen des Skripts und Validieren

Führen Sie die angegebene Abfrage für einen Ordner mit kleineren Daten aus, bevor Sie sie ausführen. `/content/dam`.

>[!TIP]
>
>Sie können überprüfen, ob alle Dateien im Ordner ordnungsgemäß aktualisiert wurden und ob alle Funktionen nur für diesen Ordner funktionieren.

| Endpunkt-URL | Anfragetyp | Abfrageparameter | Erwartete Ergebnisse |
|---|---|---|---|
| `/bin/guides/uuid_upgrade`<br><br> **Beispiel**: `http://localhost:4502/bin/guides/uuid_upgrade?root=/content/dam/test` | GET | **root**: Stammordner <br>**Wert**: /content/dam für das gesamte Repository.<br><br>**ignoreImageVersions**<br> **Wert**: true/false (ignoriert die Verarbeitung von Bildversionen. Der Standardwert lautet false) | Migrationsbericht mit Liste der erfolgreich migrierten Dateien, fehlgeschlagene Aktualisierung, fehlerhafte Aktualisierung und Gesamtdauer der Aktualisierung. <br><br> **Beispielausgabe**: <br> [INFO] Liste der fehlgeschlagenen Dateien:0 <br>[INFO] Anzahl der erfolgreich aktualisierten Dateien: 2241 <br>[INFO] Anzahl Fehlerbehebung bei fehlerhaften Dateien: 28 <br>[INFO] Anzahl von Dateien fehlgeschlagen Aktualisierung: 0 <br> [INFO] Gesamtbesuchszeit: 0:37:03 131 |

>[!NOTE]
>
> Die Inhaltsmigration kann auf Ordnerebene oder nach Abschluss der `/content/dam` oder sich im selben Ordner befinden (Migration erneut ausführen).

Darüber hinaus ist es wichtig sicherzustellen, dass die Inhaltsmigration auch für alle Medien-Assets durchgeführt wird, z. B. für Bilder und Grafiken, die Sie im DITA-Inhalt verwendet haben.

#### Grundlegende Migration

Führen Sie die Abfrage für den Ordner aus, den Sie bereits migriert haben, um die Grundlinien darauf zu migrieren.

| Endpunkt-URL | Anfragetyp | Abfrageparameter | Erwartete Ergebnisse |
|---|---|---|---|
| `/bin/guides/baseline_uuid_upgrade`<br><br> **Beispiel**: ` http://localhost:4502/bin/guides/baseline_uuid_upgrade?root=/content/dam/test` | GET | **root**: Stammordner <br> **Wert**: /content/dam für das gesamte Repository. <br><br> **ignoreImageVersions**<br> **Wert**: true/false <br>(Die Verarbeitung von Bildversionen wird ignoriert. Der Standardwert lautet false) <br><br> **doReviews** <br> **Wert**: true/false <br> (Wenn Überprüfungen aktualisiert werden müssen oder nicht. Der Standardwert lautet false.) Migrationsbericht mit Liste der erfolgreich migrierten Dateien, fehlgeschlagene Aktualisierung, fehlerhafte Aktualisierung und Gesamtdauer der Aktualisierung. <br> <br> **Beispielausgabe**:<br>[INFO] Liste der fehlgeschlagenen Dateien <br> [INFO] Anzahl der erfolgreich aktualisierten Dateien 2241<br> [INFO] Anzahl von Dateien, die mit Fehlern aktualisiert wurden 28<br>[INFO] Anzahl von Dateien fehlgeschlagen Aktualisierung 0<br>[INFO] Gesamtbesuchszeit: 0:37:03 131 |


### Schritt 3: Konfiguration wiederherstellen

Nachdem der Server erfolgreich migriert wurde, aktivieren Sie die Nachbearbeitung, das Tagging und die folgenden Workflows (einschließlich aller anderen Workflows, die während der Migration ursprünglich deaktiviert wurden), um weiterhin auf dem Server zu arbeiten.

* Workflow „DAM-Update-Asset“
* DAM-Metadaten-Workflow

>[!NOTE]
>
>Wenn einige Dateien vor der Migration nicht verarbeitet werden oder beschädigt sind und sie vor der Migration beschädigt werden und auch nach der Migration beschädigt bleiben.

## Migrationsvalidierung

1. Installieren Sie das Post-UUID-Migrationspaket (`com.adobe.guides.post-uuid-migration-1.0.2.zip`).

1. Führen Sie die folgende Abfrage aus, um zu überprüfen, ob während der Migration keine Fehler aufgetreten sind, die dazu geführt haben, dass Links fehlerhaft waren. Dieses Skript ermittelt, ob es Links gab, die zuvor nicht beschädigt, aber aus irgendeinem Grund jetzt beschädigt wurden.

   | Endpunkt-URL | Anfragetyp | Abfrageparameter | Erwartete Ergebnisse |
   |---|---|---|---|
   | `/bin/guides/get_broken_links` <br> <br> **Beispiel**:<br>`http://localhost:4502/bin/guides/get_broken_links` | GET | nicht vorhanden | Migrationsbericht mit der Gesamtzahl der Dateien, die UUIDs beschädigt haben, und den entsprechenden Dateipfaden. <br> <br> **Beispielausgabe**:<br>[DEBUG] Überprüfen, ob alle diese GUIDs im Inhalt verwendet werden.<br>[DEBUG] Gesamtzahl der Dateien, die möglicherweise UIDs beschädigt haben: 0 <br>[DEBUG] Pfade mit potenziell beschädigten UUIDs:0 |

1. Nach Abschluss der Migration kann der Großteil des Festplattenspeichers durch Ausführen der Komprimierung wiederhergestellt werden (siehe `https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=en`).

## Delta-Inhaltsmigration

1. Um den Delta-Inhalt vom aktiven Server (Nicht-UUID) auf den aktuellen UUID-Server zu migrieren, installieren Sie das Vormigrationsskript auf dem Nicht-UUID-Server.

1. Führen Sie die folgende Abfrage für den gesamten Datensatz (oder Unterordner) aus, um alle Dateien zu identifizieren und zu exportieren, die nach dem angegebenen Zeitstempel geändert wurden: Der Zeitstempel verwendet das ISO8601-Format für Datum und Uhrzeit ( YYYY-MM-DDTHH ).:mm:ss.SSSZ) und erlaubt auch partielle Darstellungen, wie JJJJ-MM-TT.

   | Endpunkt-URL | Anfragetyp | Abfrageparameter | Erwartete Ergebnisse |
   |---|---|---|---|
   | `/bin/guides/data_export`<br><br>**Beispiel**: <br> `http://localhost:4502/bin/guides/data_export?timestamp=2023-07-11&root=/content/dam` | GET | **timestamp** <br> **Wert**: YYY-MM-DD<br><br> **root**: Stammordner <br> **Wert**: `/content/dam` für das gesamte Repository. | Eine ZIP-Datei mit Delta-Inhalt wird unter /var/dxml/exports erstellt. <br> <br>**Beispiel**: dataexport_1689761491218.zip (Datei wird erstellt) |

1. Laden Sie die vom Skript exportierte ZIP-Datei herunter. Die letzte Zeile der Antwort sollte den Pfad der generierten ZIP-Datei angeben (gespeichert in /var/dxml/exports im System).

1. Laden Sie die ZIP-Datei auf den UUID-Server unter dem gewünschten Pfad in der Assets-Benutzeroberfläche hoch.

1. Stellen Sie sicher, dass das Post-Migration-Package auf dem UUID-Server installiert ist.

1. Führen Sie die folgende Abfrage aus, um den Delta-Inhalt aus der hochgeladenen ZIP-Datei in das System zu importieren. Die Abfrage sollte den Pfad der hochgeladenen ZIP-Datei enthalten, um die Daten ordnungsgemäß zu identifizieren und zu verarbeiten.

   | Endpunkt-URL | Anfragetyp | Abfrageparameter | Erwartete Ergebnisse |
   |---|---|---|---|
   | `/bin/guides/data_import`<br> **Beispiel**:`http://localhost:4502/bin/guides/data_import?path=/content/dam/dataexport_1689344927551.zip&createVersion=true` | POST | **path**<br> **Wert**: `/content/dam/filename.zip`(Speicherort der hochgeladenen Datei) **createVersion** <br> **Wert**: true/false<br>(Der Standardwert von createVersion ist &quot;false&quot;). | Die Datei wird in den gewünschten Inhaltspfad hochgeladen.<br><br>**Beispiel**: `dataexport_1689761491218.zip`<br><br> (Dieselbe Datei, die im vorherigen Schritt exportiert wurde, wird in den gewünschten Pfad unter `/content/dam`). |

1. Das Skript erstellt eine neue Datei, falls sie nicht vorhanden ist, oder überschreibt die vorhandene Datei, wenn sie geändert wurde.

>[!NOTE]
>
> Der Versionsverlauf und alle anderen auf dem Server vorgenommenen Änderungen (wie Workflows und Überprüfungen ) müssen manuell aktualisiert werden.
