---
title: Adobe Experience Manager-Handbücher aktualisieren
description: Erfahren Sie, wie Sie Adobe Experience Manager-Handbücher aktualisieren
source-git-commit: 629a3714e7b75af609238a506688da2674bf31cc
workflow-type: tm+mt
source-wordcount: '2750'
ht-degree: 1%

---


# Adobe Experience Manager-Handbücher aktualisieren {#id224MBE0M0XA}

>[!NOTE]
>
> Befolgen Sie die Upgrade-Anweisungen für die lizenzierte Version Ihres Produkts.

Sie können Ihre aktuelle Version von AEM Guides auf Version 4.2.1 aktualisieren.
- Wenn Sie Version 4.1, 4.1.x oder 4.2 verwenden, können Sie direkt auf Version 4.2.1 aktualisieren.
- Wenn Sie Version 4.0 verwenden, müssen Sie vor der Aktualisierung auf Version 4.2.1 auf Version 4.2 aktualisieren.
- Wenn Sie Version 3.8.5 verwenden, müssen Sie auf Version 4.0 aktualisieren, bevor Sie auf Version 4.2 aktualisieren.
- Wenn Sie eine Version vor 3.8.5 verwenden, finden Sie im Abschnitt AEM Upgrade-Handbuch im produktspezifischen Installationshandbuch weitere Informationen.

>[!NOTE]
>
> Sie müssen AEM Service Pack installieren, bevor Sie AEM Guides-Version aktualisieren.

Weitere Informationen finden Sie in den folgenden Verfahren:

- [Upgrade von 3.8.5 auf Version 4.0](#id2256DK003E1)
- [Upgrade auf Version 4.2](#id22A3F500SXA)
- [Upgrade auf Version 4.2.1](#upgrade-version-4-2-1)


>[!IMPORTANT]
>
> Bevor Sie mit der Aktualisierung beginnen, führen Sie eine vollständige Systemsicherung durch, um Datenverlust zu vermeiden.

## Upgrade von Version 3.8.5 auf Version 4.0 {#id2256DK003E1}

Wenn Sie AEM Guides-Version 3.8.5 verwenden, können Sie auf Version 4.0 von AEM Guides aktualisieren. Mit der Upgrade-Funktion müssen Sie die vorherige Version der AEM Handbücher nicht deinstallieren.

Bevor Sie den Prozess ausführen, müssen Sie bestimmte Aufgaben ausführen. In den folgenden Unterabschnitten werden Sie durch die Voraussetzungen, die Berichterstellung und den Migrationsprozess geführt. Außerdem können Sie nach der Installation AEM Guides Version 4.0 verschiedene Konfigurationen entsprechend den Kundeneinstellungen anpassen.

>[!NOTE]
>
> Dieser Upgrade-Prozess gilt nur von Version 3.8.5 auf Version 4.0. Informationen zum Upgrade von Version 3.4 oder höher auf Version 3.8.5 finden Sie im Abschnitt *AEM* Abschnitt im produktspezifischen Installationshandbuch finden Sie im Abschnitt [Hilfe-Archivierungsseite](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

****Voraussetzungen****

Bevor Sie mit dem Upgrade-Prozess für AEM Guides beginnen, stellen Sie Folgendes sicher:

1. Die Überprüfungskommentare wurden in Themen importiert, die zur Überprüfung geöffnet sind.
1. Alle aktiven Rezensionen wurden geschlossen.
1. Alle Übersetzungsaufgaben wurden geschlossen.
1. Deinstallieren Sie alle AEM Guides Hotfixes, die auf der vorherigen Version installiert sind \(Haupt- oder Patch-Version\) der AEM Guides.

**Vor der Installation von Version 4.0**

Führen Sie vor der Installation von Version 4.0 die folgenden Schritte aus:

1. Stellen Sie sicher, dass an dieser Stelle AEM Guides auf Version 3.8.5 eingestellt sind.
1. Laden Sie das Aktualisierungsskript-Paket herunter. Suchen Sie dazu nach &quot;XML Documentation solution 4.0 Upgrade Package&quot;auf [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) herunterladen, um eine ZIP-Datei herunterzuladen.
1. Laden Sie dieses Paket über Package Manager in AEM hoch und installieren Sie es.
1. Nachdem das Upgrade-Paket installiert wurde, führen Sie die folgenden angegebenen Skripte in derselben Reihenfolge aus und befolgen Sie die angegebenen Anweisungen:

**Überprüfen der Upgrade-Kompatibilitäts-API**

Diese API dient dazu, den aktuellen Systemstatus zu bewerten und darüber zu berichten, ob eine Aktualisierung möglich ist oder nicht. Um dieses Skript auszuführen, geben Sie den folgenden angegebenen Endpunkt ein:

|Endpunkt|/bin/dxml/upgrade/3xto4x/report| |Anfragetyp|**GET** Sie können einen Webbrowser verwenden, in dem Sie als Administrator bei der AEM-Instanz angemeldet sind.| |Erwartete Antwort|- Falls alle erforderlichen Knoten verschoben werden können, erhalten Sie eine übergebene Prüfung. <br>- Wenn sich ein Knoten am Zielspeicherort befindet, wird ein relevanter Fehler ausgegeben. Bereinigen Sie das Repository \(Löschen-Knoten /var/dxml\), installieren Sie das Aktualisierungspaket neu und führen Sie dann erneut einen Trigger für diesen Endpunkt durch. <br>**Hinweis:** Dies ist kein häufiger Fehler, da der Zielort von 3.x-AEM-Handbüchern nicht früher verwendet wird. <br> - Wenn dieses Skript nicht erfolgreich ist, fahren Sie nicht fort und melden Sie es Ihrem Kundenerfolgsteam.|

**Systemdatenmigration-API**

Diese API dient der Migration der Systemdaten, wie im Abschnitt [Migrationszuordnung](#id2244LE040XA) Abschnitt.

1. Führen Sie dieses Skript nicht aus, wenn die API zur Prüfung der Upgrade-Kompatibilität fehlschlägt \(fahren Sie nicht fort\).
1. Sobald die API zur Prüfung der Upgrade-Kompatibilität erfolgreich ist, können Sie das Aktualisierungsskript ausführen.

|Endpunkt|/bin/dxml/upgrade/3xto4x| |Anfragetyp|**POST** Dieses Skript ist eine POST-Anfrage und sollte daher über Agenten wie Postman ausgeführt werden.| |Erwartete Antwort|- Sobald die Migration erfolgreich war, können Sie die XML Documentation-Lösungsversion 4.0 installieren.<br>- Wenn Fehler auftreten, stellen Sie den letzten Checkpoint wieder her und geben Sie die Fehlerprotokolle zusammen mit der API-Ausgabe für Ihr Customer Success Team frei.|

**Migrationszuordnung**: Die obige API migriert alle Daten unter dem Quellspeicherort zum Zielspeicherort.

| Quelle | Ziel |
|------|------|
| /content/fmdita | /var/dxml |
| /content/dxml | /var/dxml |
| /etc/fmdita | /libs/fmdita |

## Installieren Sie Version 4.0 {#id23598G006XA}

1. Installieren Sie Version 4.0 nur, wenn die Aktualisierungsschritte erfolgreich waren.
1. Laden Sie das 4.0-Versionspaket von herunter. [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html):

   - Wenn Sie die UUID-Version der Software verwenden, suchen Sie nach &quot;4.0 UUID Release for XML Documentation solution for AEM 6.5&quot;.
   - Wenn Sie die Nicht-UUID-Version der Software verwenden, suchen Sie nach &quot;4.0 Non-UUID Release for XML Documentation solution for AEM 6.5&quot;.
Laden Sie das Paket mithilfe von CRX Package Manager in die vorhandene AEM-Serverinstanz hoch und installieren Sie es.

   >[!NOTE]
   >
   > Warten Sie, bis alle Systemkomponenten gestartet sind.

1. Löschen Sie den Browser-Cache nach der Installation des Pakets.
1. Wenn ein Dispatcher in der AEM-Autoreninstanz konfiguriert ist, führen Sie die folgenden Schritte aus:
   - Stellen Sie sicher, dass Folgendes in Dispatcher-Regeln verarbeitet wird:
   - Das URL-Muster /home/users/\*/Preferences ist auf der Whitelist.
   - Das URL-Muster /libs/cq/security/userinfo.json wird nicht zwischengespeichert.
1. Dispatcher-Cache löschen \(um alle `clientlibs` zwischengespeichert\).

## Upgrade auf Version 4.2 {#id22A3F500SXA}

Die Aktualisierung auf Version 4.2 hängt von der aktuellen Version der AEM ab.

Wenn Sie Version 4.0, 4.1 oder 4.1.x verwenden, können Sie direkt auf Version 4.2 aktualisieren.

****Voraussetzungen****

Bevor Sie mit dem Upgrade-Prozess für AEM Guides 4.2 beginnen, stellen Sie Folgendes sicher:

1. Aktualisierung auf AEM Guides-Version 4.0, 4.1 oder 4.1.x.
1. Alle Übersetzungsaufgaben wurden geschlossen.
1. Die Protokollebene wurde zu **INFO** für `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` -Klasse und hängen diese Protokolle an eine neue Protokolldatei an, z. B. `logs/translation_upgrade.log.`

>[!NOTE]
>
> Sie sollten alle aktiven Rezensionen schließen. Wenn die Prüfungsaufgaben beim Upgrade auf Version 4.2 nicht abgeschlossen werden, nehmen die älteren laufenden Prüfungsaufgaben weiterhin Benutzer auf den älteren Prüfungsseiten auf und die nach dem Upgrade erstellten Prüfungsaufgaben zeigen die neuesten Funktionsaktualisierungen an.

## Installieren Sie Version 4.2 {#id2245IK0E0EV}

1. Laden Sie das 4.2-Versionspaket herunter. [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installieren Sie das Paket der Version 4.2.
1. Warten Sie nach Abschluss der Paketinstallation auf die folgende(n) Meldung(en\) in den Protokollen:

   `Completed the post deployment setup script`

   Die obige Meldung weist darauf hin, dass alle Installationsschritte abgeschlossen sind.

   Sollten Sie auf eines der folgenden FEHLER-Präfixe stoßen, melden Sie diese Ihrem Kundenerfolgsteam:

   - Fehler beim Setup-Skript nach der Bereitstellung
   - Ausnahme beim Importieren der Übersetzungs-MAP
   - Die Übersetzungszuordnung kann nicht von v1 auf v2 für die Eigenschaft portiert werden
1. Aktualisieren Sie das Oxygen Connector-Plugin, das mit Version 4.2 veröffentlicht wurde \(falls erforderlich\).
1. Löschen Sie den Browser-Cache nach der Installation des Pakets.
1. Fahren Sie mit der Aktualisierung der Anpassungen fort, wie im nächsten Abschnitt beschrieben.

## Nach der Installation von Version 4.2 {#id2326F02004K}

>[!IMPORTANT]
>
> Die Hi-Tech-Vorlage wird auf dem aktualisierten Server nicht angezeigt. Um die High-Tech-Vorlage auf Ihrem Server einzubinden, können Sie sie kopieren: Quelle: /libs/fmdita/pdf/Hi-Tech Destination: /content/dam/dita-templates/pdf

Nach der Installation AEM Guides können Sie die verschiedenen Konfigurationen, die von der neu installierten Version gelten, mit Ihrem Setup zusammenführen.

>[!NOTE]
>
> Das Modell dam-update-asset kann angepasst werden. Wenn also Anpassungen vorgenommen wurden, müssen wir die Anpassungen und AEM Handbücher mit der Arbeitskopie des Modells synchronisieren.

1. **DAM-Update-Asset-Workflow \(Nachbearbeitungs-Änderungen\):**

1. URL öffnen:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Auswählen **Workflow &quot;DAM-Update-Asset&quot;**.
1. Klicken Sie auf **Bearbeiten**.
1. Wenn die Variable **DXML-Nachbearbeitungs-Initiator** -Komponente vorhanden ist, stellen Sie sicher, dass die Anpassungen synchronisiert werden.
1. Wenn die Variable **DXML-Nachbearbeitungs-Initiator** -Komponente fehlt, führen Sie die folgenden Schritte aus, um sie einzufügen:

1. Klicken **Komponente einfügen** \(Verantwortlich für die Nachbearbeitung AEM Guides als letzten Schritt im Prozess\).
1. Konfigurieren Sie die **Prozessschritt** mit folgenden Details:

   **Registerkarte &quot;Allgemein&quot;**

   **Titel:** DXML-Nachbearbeitungs-Initiator

   **Beschreibung**: DXML-Nachbearbeitungs-Initiatorschritt, der einen Sling-Auftrag für die DXML-Nachbearbeitung des geänderten/erstellten Assets Trigger

   **Tab Prozess**

   - Auswählen **DXML-Nachbearbeitungs-Initiator** von **Prozess** Dropdown

   - Auswählen **Handler-Modus**

   - Klicken Sie auf **Fertig**

1. Klicken **Synchronisieren** oben rechts nach Abschluss der Änderungen. Sie erhalten eine Erfolgsbenachrichtigung.

   >[!NOTE]
   >
   > Aktualisieren Sie und überprüfen Sie, ob im endgültigen Workflow-Modell benutzerdefinierte Änderungen und der Nachbearbeitungsschritt AEM Guides vorhanden sind.

1. Einmal **Workflow &quot;DAM-Update-Asset&quot;** validiert wird, überprüfen Sie die entsprechenden Starter-Konfigurationen. Gehen Sie dazu zur Workflow-Oberfläche AEM und öffnen Sie Starter.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Suchen Sie nach den folgenden beiden Startern \(die aktiv sein sollten\) und nehmen Sie Änderungen vor \(falls erforderlich\), die **Workflow &quot;DAM-Update-Asset&quot;**:

1. Starter für &quot;*Knoten erstellt*&quot; **Workflow &quot;DAM-Update-Asset&quot;**- für Bedingungen `"jcr:content/jcr:mimeType!=video"`, sollte der Wert &quot;Globbing&quot;wie folgt lauten:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; sollte `"event-user-data:changedByWorkflowProcess"`.
   - Starter für &quot;*Knoten geändert*&quot; **DAM-Update-Asset-Workflow -** für Bedingung &quot;`jcr:content/jcr:mimeType!=video`&quot;,
   - 
      - Der Wert &quot;Globbing&quot;sollte lauten:

   ```json
   `"/content/dam(/((?!/subassets|/translation_output).)*/)renditions/original"`
   ```

   - &#39;excludeList&#39; sollte `"event-user-data:changedByWorkflowProcess"`.
1. Nachdem das Upgrade abgeschlossen ist, stellen Sie sicher, dass alle Anpassungen/Überlagerungen validiert und aktualisiert wurden, um dem neuen Anwendungscode zu entsprechen. Nachfolgend finden Sie einige Beispiele:
   - Alle aus /libs/fmditaor/libsüberlagerten Komponenten sollten mit dem neuen Produktcode verglichen werden und Aktualisierungen sollten in überlagerten Dateien unter/apps vorgenommen werden.
   - Alle clientlib-Kategorien, die vom Produkt verwendet werden, sollten auf Änderungen überprüft werden. Alle überschriebenen Konfigurationen \(Beispiele unten\) sollten mit den neuesten verglichen werden, um die neuesten Funktionen zu erhalten:
   - elementmapping.xml
   - ui\_config.json\(möglicherweise in Ordnerprofilen festgelegt\)
   - geändert `com.adobe.fmdita.config.ConfigManager`
   - Überprüfen Sie, ob der benutzerspezifische Code alte Pfade verwendet hat \(wie im Abschnitt [Migrationszuordnung](#id2244LE040XA) -Abschnitt\) - sollten auf die neuen Pfade aktualisiert werden, damit die Anpassungen auch erwartungsgemäß funktionieren.
1. Über alle neuen Konfigurationen in der aktuellen Version lesen \(überprüfen Sie [Versionshinweise](../release-info/release-notes-4.2.md)\) und überprüfen Sie, ob irgendwelche Funktionen betroffen sind, und ergreifen Sie geeignete Maßnahmen. Ein Beispiel könnte die Verwendung der in Version 4.0 eingeführten &quot;verbesserten Handhabung von Dateien und Versionen&quot; sein, für die Sie eine Konfiguration aktivieren müssen.

## Schritte zum Indexieren des vorhandenen Inhalts, um das neue Suchen und Ersetzen zu verwenden:

Führen Sie die folgenden Schritte für die Indizierung des vorhandenen Inhalts aus und verwenden Sie den neuen Suchen- und Ersetzen-Text auf Zuordnungsebene:

- Führen Sie eine POST-Anfrage an den Server aus \(mit korrekter Authentifizierung\) - `http://<server:port\>/bin/guides/map-find/indexing`. \(Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert \|\| Beispiel : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`\)

- Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)

- Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Upgrade auf Version 4.2.1 {#upgrade-version-4-2-1}

Die Aktualisierung auf Version 4.2.1 hängt von der aktuellen Version der AEM-Handbücher ab.

Wenn Sie Version 4.1, 4.1.x oder 4.2 verwenden, können Sie direkt auf Version 4.2.1 aktualisieren.

>[!NOTE]
>
>Die Nachbearbeitung und Indizierung kann einige Stunden dauern. Es wird empfohlen, den Aktualisierungsprozess außerhalb der Spitzenzeiten zu starten.

****Voraussetzungen****

Bevor Sie mit dem Upgrade-Prozess für die AEM Guides 4.2.1 beginnen, stellen Sie Folgendes sicher:

1. Aktualisierung auf AEM Guides-Version 4.1, 4.1.x oder 4.2.
1. Alle Übersetzungsaufgaben wurden geschlossen.
1. Die Protokollebene wurde zu **INFO** für `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` -Klasse und hängen diese Protokolle an eine neue Protokolldatei an, z. B. `logs/translation_upgrade.log.`

>[!NOTE]
>
> Sie sollten alle aktiven Rezensionen schließen. Wenn die Prüfungsaufgaben beim Upgrade auf Version 4.2 nicht abgeschlossen werden, nehmen die älteren laufenden Prüfungsaufgaben weiterhin Benutzer auf den älteren Prüfungsseiten auf und die nach dem Upgrade erstellten Prüfungsaufgaben zeigen die neuesten Funktionsaktualisierungen an.

## Installieren Sie Version 4.2.1

1. Laden Sie das 4.2.1-Versionspaket herunter. [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html).
1. Installieren Sie das Paket der Version 4.2.1.
1. Sie können den Trigger drücken, um den Aktualisierungsauftrag für die Übersetzungskarte zu starten. Weitere Informationen finden Sie unter [Aktivieren des Triggers eines Skripts über ein Servlet](#enable-trigger-serverlet).


1. Warten Sie nach Abschluss der Paketinstallation auf die folgende(n) Meldung(en\) in den Protokollen:

   `Completed the post deployment setup script`

   Die obige Meldung weist darauf hin, dass alle Installationsschritte abgeschlossen sind.

   Sollten Sie auf eines der folgenden FEHLER-Präfixe stoßen, melden Sie diese Ihrem Kundenerfolgsteam:

   - Fehler beim Setup-Skript nach der Bereitstellung
   - Ausnahme beim Importieren der Übersetzungs-MAP
   - Die Übersetzungszuordnung kann nicht von v1 auf v2 für die Eigenschaft portiert werden
1. Aktualisieren Sie das Oxygen Connector-Plugin, das mit Version 4.2 veröffentlicht wurde \(falls erforderlich\).
1. Löschen Sie den Browser-Cache nach der Installation des Pakets.
1. Fahren Sie mit der Aktualisierung der Anpassungen fort, wie im nächsten Abschnitt beschrieben.

### Aktivieren des Triggers eines Skripts über ein Servlet{#enable-trigger-serverlet}

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Antwort:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

In der obigen Antwort-JSON wird der Schlüssel `lockNodePath` enthält den Pfad zum Knoten, der im Repository erstellt wurde und auf den gesendeten Auftrag verweist. Er wird automatisch gelöscht, sobald der Auftrag abgeschlossen ist. Bis dahin können Sie den aktuellen Status des Auftrags in diesem Knoten nachlesen.

Beispielprotokoll: Im Folgenden finden Sie ein Beispiel von Protokollen, die in der Protokolldatei angezeigt werden, nachdem Sie das Skript Trigger haben.

```
04.05.2023 14:17:12.876 *INFO* [[0:0:0:0:0:0:0:1] [1683190032736] POST /bin/guides/script/start HTTP/1.1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Acquiring lock for job : translation-map-upgrade
04.05.2023 14:17:12.897 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Starting the thread to upgrade translation map from V1 to V2
04.05.2023 14:17:12.899 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Initiating lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.901 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Starting porting of translation map from V1 to V2
04.05.2023 14:17:12.904 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Memory increase is of : 764 kB
04.05.2023 14:17:12.906 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2
04.05.2023 14:17:12.907 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Releasing lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.909 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2
```

Suchen nach `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2` und `com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2` bevor Sie mit den nächsten Schritten fortfahren.



## Nach der Installation von Version 4.2.1

>[!IMPORTANT]
>
> Die Hi-Tech-Vorlage wird auf dem aktualisierten Server nicht angezeigt. Um die High-Tech-Vorlage auf Ihrem Server einzubinden, können Sie sie kopieren: Quelle: /libs/fmdita/pdf/Hi-Tech Destination: /content/dam/dita-templates/pdf

Nach der Installation AEM Guides können Sie die verschiedenen Konfigurationen, die von der neu installierten Version gelten, mit Ihrem Setup zusammenführen.

>[!NOTE]
>
> Das Modell dam-update-asset kann angepasst werden. Wenn also Anpassungen vorgenommen wurden, müssen wir die Anpassungen und AEM Handbücher mit der Arbeitskopie des Modells synchronisieren.

1. **DAM-Update-Asset-Workflow \(Nachbearbeitungs-Änderungen\):**

1. URL öffnen:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Auswählen **Workflow &quot;DAM-Update-Asset&quot;**.
1. Klicken Sie auf **Bearbeiten**.
1. Wenn die Variable **DXML-Nachbearbeitungs-Initiator** -Komponente vorhanden ist, stellen Sie sicher, dass die Anpassungen synchronisiert werden.
1. Wenn die Variable **DXML-Nachbearbeitungs-Initiator** -Komponente fehlt, führen Sie die folgenden Schritte aus, um sie einzufügen:

1. Klicken **Komponente einfügen** \(Verantwortlich für die Nachbearbeitung AEM Guides als letzten Schritt im Prozess\).
1. Konfigurieren Sie die **Prozessschritt** mit folgenden Details:

   **Registerkarte &quot;Allgemein&quot;**

   **Titel:** DXML-Nachbearbeitungs-Initiator

   **Beschreibung**: DXML-Nachbearbeitungs-Initiatorschritt, der einen Sling-Auftrag für die DXML-Nachbearbeitung des geänderten/erstellten Assets Trigger

   **Tab Prozess**

   - Auswählen **DXML-Nachbearbeitungs-Initiator** von **Prozess** Dropdown

   - Auswählen **Handler-Modus**

   - Klicken Sie auf **Fertig**

1. Klicken **Synchronisieren** oben rechts nach Abschluss der Änderungen. Sie erhalten eine Erfolgsbenachrichtigung.

   >[!NOTE]
   >
   > Aktualisieren Sie und überprüfen Sie, ob im endgültigen Workflow-Modell benutzerdefinierte Änderungen und der Nachbearbeitungsschritt AEM Guides vorhanden sind.

1. Einmal **Workflow &quot;DAM-Update-Asset&quot;** validiert wird, überprüfen Sie die entsprechenden Starter-Konfigurationen. Gehen Sie dazu zur Workflow-Oberfläche AEM und öffnen Sie Starter.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Suchen Sie nach den folgenden beiden Startern \(die aktiv sein sollten\) und nehmen Sie Änderungen vor \(falls erforderlich\), die **Workflow &quot;DAM-Update-Asset&quot;**:

1. Starter für &quot;*Knoten erstellt*&quot; **Workflow &quot;DAM-Update-Asset&quot;**- für Bedingungen `"jcr:content/jcr:mimeType!=video"`, sollte der Wert &quot;Globbing&quot;wie folgt lauten:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; sollte `"event-user-data:changedByWorkflowProcess"`.
   - Starter für &quot;*Knoten geändert*&quot; **DAM-Update-Asset-Workflow -** für Bedingung &quot;`jcr:content/jcr:mimeType!=video`&quot;, sollte der Wert &quot;Globbing&quot;wie folgt lauten:

   ```json
   `"/content/dam(/((?!/subassets|/translation_output).)*/)renditions/original"`
   ```

   - `excludeList` sollte `"event-user-data:changedByWorkflowProcess"`.


1. Nachdem das Upgrade abgeschlossen ist, stellen Sie sicher, dass alle Anpassungen/Überlagerungen validiert und aktualisiert wurden, um dem neuen Anwendungscode zu entsprechen. Nachfolgend finden Sie einige Beispiele:
   - Alle aus /libs/fmditaor/libsüberlagerten Komponenten sollten mit dem neuen Produktcode verglichen werden und Aktualisierungen sollten in überlagerten Dateien unter/apps vorgenommen werden.
   - Alle clientlib-Kategorien, die vom Produkt verwendet werden, sollten auf Änderungen überprüft werden. Alle überschriebenen Konfigurationen \(Beispiele unten\) sollten mit den neuesten verglichen werden, um die neuesten Funktionen zu erhalten:
   - elementmapping.xml
   - ui\_config.json\(möglicherweise in Ordnerprofilen festgelegt\)
   - geändert `com.adobe.fmdita.config.ConfigManager`
   - Überprüfen Sie, ob der benutzerspezifische Code alte Pfade verwendet hat \(wie im Abschnitt [Migrationszuordnung](#id2244LE040XA) -Abschnitt\) - sollten auf die neuen Pfade aktualisiert werden, damit die Anpassungen auch erwartungsgemäß funktionieren.
1. Über alle neuen Konfigurationen in der aktuellen Version lesen \(überprüfen Sie [Versionshinweise](../release-info/release-notes-4.2.1.md)\) und überprüfen Sie, ob irgendwelche Funktionen betroffen sind, und ergreifen Sie geeignete Maßnahmen. Ein Beispiel könnte die Verwendung der in Version 4.0 eingeführten &quot;verbesserten Handhabung von Dateien und Versionen&quot; sein, für die Sie eine Konfiguration aktivieren müssen.

## Schritte zum Indexieren des vorhandenen Inhalts, um das neue Suchen und Ersetzen zu verwenden:

Führen Sie die folgenden Schritte für die Indizierung des vorhandenen Inhalts aus und verwenden Sie den neuen Suchen- und Ersetzen-Text auf Zuordnungsebene:

- Stellen Sie sicher, dass `damAssetLucene` Die Indizierung wurde abgeschlossen. Je nach der auf dem Server vorhandenen Datenmenge kann es bis zu einigen Stunden dauern. Sie können bestätigen, dass die Neuindizierung abgeschlossen ist, indem Sie überprüfen, ob das Neuindizierungsfeld in
   `http://<server:port>/oak:index/damAssetLucene`.  Wenn Sie darüber hinaus Anpassungen in `damAssetLucene`, müssen Sie sie möglicherweise erneut anwenden.

- Führen Sie eine POST-Anfrage an den Server aus \(mit korrekter Authentifizierung\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert \|\| Beispiel : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- Sie können auch einen Stammordner übergeben, um die DITA-Maps eines bestimmten Ordners (und seiner Unterordner) zu indizieren. Beispiel: `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Beachten Sie, dass nur der Pfadparameter berücksichtigt wird, wenn sowohl der Pfadparameter als auch der Stammparameter übergeben werden.

- Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


- Nach Abschluss des Auftrags antwortet die obige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)

