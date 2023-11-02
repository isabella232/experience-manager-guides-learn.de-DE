---
title: Versionshinweise | Upgrade-Anweisungen und behobene Probleme in Adobe Experience Manager-Handbüchern, Version November 2023
description: Erfahren Sie mehr über die Fehlerbehebungen und wie Sie auf die Version November 2023 von Adobe Experience Manager Guides as a Cloud Service aktualisieren können
source-git-commit: 1d8f00a82e92e1648615c409d4652b6ce3da7a1f
workflow-type: tm+mt
source-wordcount: '1640'
ht-degree: 3%

---

# Version der Adobe Experience Manager-Handbücher as a Cloud Service im November 2023

In diesem Versionshinweis werden die Upgrade-Anweisungen, die Kompatibilitätsmatrix und die in Version November 2023 der Adobe Experience Manager-Handbücher as a Cloud Service behobenen Probleme behandelt (später auch als *Experience Manager Guides as a Cloud Service*).

Weitere Informationen zu den neuen Funktionen und Verbesserungen finden Sie unter [Neue Funktionen in der Version von Experience Manager Guides as a Cloud Service im November 2023](whats-new-2023.11.0.md).

## Aktualisierung auf Version November 2023

Führen Sie die folgenden Schritte aus, um die aktuelle as a Cloud Service Einrichtung der Experience Manager-Handbücher zu aktualisieren:

1. Sehen Sie sich den Git-Code des Cloud Service an und wechseln Sie zu der Verzweigung, die in der Cloud Service-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
2. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Service-Git-Codes auf 2023.11.0.406.
3. Übertragen Sie die Änderungen und führen Sie die Cloud Service-Pipeline aus, um auf die Version November 2023 der Experience Manager-Handbücher as a Cloud Service zu aktualisieren.

## Schritte zum Aktivieren des Triggers eines Skripts über ein Servlet

(Nur wenn Sie eine Version vor der Version von Experience Manager Guides im Juni 2023 as a Cloud Service haben)

Nachdem Sie die Installation abgeschlossen haben, können Sie den Trigger drücken, um den Übersetzungsauftrag zu starten:

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

In der vorherigen Antwort JSON, der Schlüssel `lockNodePath` enthält den Pfad zum Knoten, der im Repository erstellt wurde und auf den gesendeten Auftrag verweist. Nach Abschluss des Auftrags wird der Vorgang automatisch gelöscht. Anschließend können Sie diesen Knoten für den Auftragsstatus aufrufen.

Warten Sie, bis dieser Auftrag abgeschlossen ist, bevor Sie mit den nächsten Schritten fortfahren.

>[!NOTE]
>
> Sie sollten überprüfen, ob der Knoten noch vorhanden ist, und den Status des Auftrags überprüfen.

```
GET
http://<aem_domain>/var/dxml/executor-locks/translation-map-upgrade/1683190032886.json
```

## Schritte zum Nachbearbeiten des vorhandenen Inhalts zur Verwendung des Berichts über einen fehlerhaften Link

(Nur wenn Sie eine Version vor der Version von Experience Manager Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte für die Nachbearbeitung des vorhandenen Inhalts und die Verwendung des neuen Berichts über fehlerhafte Links aus:

1. (Optional) Wenn mehr als 100.000 DITA-Dateien im System vorhanden sind, aktualisieren Sie die `queryLimitReads` und `queryLimitInMemory` under `org.apache.jackrabbit.oak.query.QueryEngineSettingsService` auf einen größeren Wert (ein Wert, der größer ist als die Anzahl der vorhandenen Assets, z. B. 200.000), und dann erneut bereitgestellt werden.

   - Verwenden Sie die im Abschnitt *Konfigurationsüberschreibungen* im Abschnitt Adobe Experience Manager-Handbücher as a Cloud Service installieren und konfigurieren , um die Konfigurationsdatei zu erstellen.
   - Geben Sie in der Konfigurationsdatei die folgenden (Eigenschaft-)Details an, um die `queryLimitReads` und `queryLimitInMemory` Option:

     | PID | Eigenschaftenschlüssel | Eigenschaftswert |
     |---|---|---|
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitReads | Wert: 200000 Standardwert: 100000 |
     | org.apache.jackrabbit.oak.query.QueryEngineSettingsService | queryLimitInMemory | Wert: 200000 Standardwert: 100000 |

1. Führen Sie eine POST-Anfrage an den Server aus (mit der richtigen Authentifizierung) - `http://<server:port>//bin/guides/reports/upgrade`.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port>/bin/guides/reports/upgrade?jobId= {jobId}`
(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678`)

1. Nach Abschluss des Auftrags antwortet die vorherige GET-Anfrage erfolgreich. Wenn der Auftrag aus irgendeinem Grund fehlschlägt, kann in den Serverprotokollen ein Fehler angezeigt werden.

1. Auf den standardmäßigen oder vorherigen vorhandenen Wert von zurücksetzen `queryLimitReads` wenn Sie es in Schritt 1 geändert haben.

## Schritte zum Indexieren des vorhandenen Inhalts zur Verwendung der neuen Suchen- und Ersetzen- und Themenliste auf der Registerkarte Berichte :

(Nur wenn Sie eine Version vor der Version von Experience Manager Guides im Juni 2023 as a Cloud Service haben)

Führen Sie die folgenden Schritte aus, um den vorhandenen Inhalt zu indizieren und den neuen Text auf Zuordnungs- und Themenliste auf der Registerkarte Berichte zu finden und zu ersetzen:

1. Führen Sie eine POST-Anfrage an den Server aus \(mit korrekter Authentifizierung\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Optional: Sie können bestimmte Pfade der Maps übergeben, um sie zu indizieren. Standardmäßig werden alle Maps indiziert \|\| Beispiel : `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

1. Sie können auch einen Stammordner übergeben, um die DITA-Maps eines bestimmten Ordners (und seiner Unterordner) zu indizieren. Beispiel: `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Beachten Sie, dass nur der Pfadparameter berücksichtigt wird, wenn sowohl der Pfadparameter als auch der Stammparameter übergeben werden.

1. Die API gibt eine jobId zurück. Um den Status des Auftrags zu überprüfen, können Sie eine GET-Anfrage mit Auftrags-ID an denselben Endpunkt senden - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Beispiel: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


1. Nach Abschluss des Auftrags antwortet die vorherige GET-Anfrage mit Erfolg und gibt an, ob Zuordnungen fehlgeschlagen sind. Die erfolgreich indizierten Maps können über die Serverprotokolle bestätigt werden.

## Schritte zum Verarbeiten der `'fmdita rewriter'` Konflikt

Experience Manager-Handbücher verfügen über eine [**benutzerdefinierte Sling-Rewriter**](../cs-install-guide/conf-output-generation.md#custom-rewriter) -Modul zur Behandlung der im Fall von Querkarten generierten Links (Verknüpfungen zwischen den Themen zweier verschiedener Karten).

Wenn Sie einen anderen benutzerdefinierten Sling-Rewriter in Ihrer Codebase haben, verwenden Sie eine `'order'` Wert größer als 50, da der Experience Manager Guides Sling Rewriter verwendet `'order'` 50.  Um dies zu überschreiben, benötigen Sie einen Wert > 50. Weitere Informationen finden Sie unter [Pipelines zum Neuschreiben der Ausgabe](https://sling.apache.org/documentation/bundles/output-rewriting-pipelines-org-apache-sling-rewriter.html).

Während dieses Upgrades, seit der `'order'` -Wert von 1000 auf 50 geändert wird, müssen Sie die vorhandene benutzerdefinierte Rewriter, sofern vorhanden, mit `'fmdita-rewriter'`.


## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die Softwareanwendungen aufgelistet, die von der Experience Manager-Guides-Version vom as a Cloud Service November 2023 unterstützt werden.

### FrameMaker und FrameMaker Publishing Server

| Experience Manager-Handbücher für as a Cloud-Versionen | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.11.0 | Nicht kompatibel | 2022 oder höher |
| | | |


### Sauerstoffanschluss

| Experience Manager-Handbücher für as a Cloud | Sauerstoff Connector Windows | Sauerstoff Connector Mac | In Oxygen Windows bearbeiten | In Oxygen Mac bearbeiten |
| --- | --- | --- | --- | --- |
| 2023.11.0 | 3.2-uuid 5 | 3.2-uuid 5 | 2.3 | 2.3 |
|  |  |  |  |


### Knowledgebase-Vorlagenversion

| Name des Komponentenpakets | Komponentenversion | Vorlagenversion |
|---|---|---|
| Experience Manager Guides-Komponenteninhaltspaket für Cloud Service | dxml-components.all-1.2.2 | aem-site-template-dxml.all-1.0.15 |

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:



### Authoring

- Leerzeichen nach conref `<ph>` -Element beim Speichern des Themas verschwindet. (13642)
- Anwendungsfehler tritt auf, wenn versucht wird, DITA-Dateien zu speichern, bevor die Nachbearbeitung abgeschlossen ist. (13571)
- Wenn der Titel eines Themas einen Schrägstrich enthält `/`, zeigt die Registerkarte im Editor nur die Buchstaben an, die danach folgen. (13455)
- Die Bildvorschau wird nach der Anzeige der Vorschau im Editor nicht ausgeblendet. (13454)
- Das Popup-Fenster &quot;Keyword einfügen&quot;wird nicht angezeigt, wenn in anderen Themen Schlüssel mit der root-Map verwendet werden. (12950)
- Schließen-Symbole sind nicht sichtbar, wenn sehr große Grafiken im Bereich Versionsverlauf in der Vorschau angezeigt werden. (12867)
- Die Zeitzone von kann nicht geändert werden **Version erstellt am** für die Grundlinien. (12711)
- Die **Versionsverlauf** in der Assets-Benutzeroberfläche einen falschen Zeitstempel für die **Aktuell** -Feld. (12624)
- Das Erstellen einer DITA-Datei aus einer Vorlage mit einem Dateinamen, der mit numerischen Zeichen beginnt, führt zu einem Namespace-Fehler. (12188)
- Im Web-Editor wird die **Schlüsselverweise** beim Einfügen des `varname` -Tag. (10940)
- ZIP-Dateien werden im Web Editor nicht erkannt und können nicht per Drag-and-Drop eingefügt werden. (12709)
- Der Inhalt mit einigen darauf angewendeten Attributen wird im Autoren- oder Vorschaumodus nicht hervorgehoben. (11063)
- Wenn Sie ein Thema nach der Bearbeitung schließen, werden Sie zur AEM-Startseite weitergeleitet, anstatt zur Ordneransicht zurückzukehren. (13306)
- Bei der Nachbearbeitung von Dateien, die kopiert und in die Cloud Services eingefügt wurden, kommt es zu einer Verzögerung. (12457)
- Die Rootmap-Einstellung bleibt im Web Editor erhalten, auch wenn der Benutzer sie nicht explizit in den Benutzereinstellungen festgelegt hat. (11551)


### Veröffentlichung

- Die Funktion zum Veröffentlichen von Inhaltsfragmenten funktioniert nicht für Dateien, die in den Suchergebnissen aufgeführt sind. (14090)
- Bei der nativen PDF-Veröffentlichung erfordert die Auswahl der Hintergrundfarbe im Vorlagenlayout eine erneute Seitenladung, wenn auf `None`. (13621)
- Problem beim Zuweisen zum Datenspeicher für eine große DITA-Zuordnung mit Perimeter-Peer-Links in AEM Site-Veröffentlichung. (13530)
- Bei der nativen PDF-Veröffentlichung ist die Barrierefreiheit beeinträchtigt, da Bilder in der Kopf- und Fußzeile keinen alternativen Text anzeigen. (12829)
- Das Duplizieren des Seitenlayouts im nativen PDF funktioniert nicht, ohne dass automatisch eine Erweiterung hinzugefügt wird. (12534)
- Beim Generieren der PDF-Ausgabe mit nativer PDF-Veröffentlichung wird der Dateiname nach einem Punkt abgeschnitten. (13620)
- Falsches Symbol und falsche QuickInfos werden angezeigt für  **Inhalt bearbeiten** in der Symbolleiste &quot;Seitenlayouts&quot;der Vorlagen, die beim nativen PDF-Publishing verwendet werden. (13492)
- Benutzerdefinierte Metadaten sind in der endgültigen Ausgabe nicht verfügbar. (12116)
- fmdita rewriter steht in Konflikt mit der Rewriter-Konfiguration des Benutzers und führt zur Anzeige langer URLs anstelle der Links. (12076)
- In der Vorgabe AEM Site wird die Option **Separate PDF für jedes Thema generieren** nicht funktionsfähig ist. (11555)
- Für die Konvertierung von CMYK-Farbräumen wird bei der nativen PDF-Veröffentlichung nicht unterstützt. (10754)
- Dynamische Grundlinien-Aufrufe verwenden den Namen anstelle des Titels, was zu einem Fehler bei der Export von DITA Map-API führt. (14268)

### Verwaltung

- Die Inhaltsreferenz beim Kopieren und Einfügen der DITA-Dateien mit Selbstverweis-Links ohne GUID ist fehlerhaft. (13540)
- Im Web-Editor zeigt die Grundlinie den Titel der vorherigen Version anstelle der ausgewählten Version der DITA-Datei an. (13444)
- Die **Berichte** in der Web Editor-Benutzeroberfläche kann die Themenliste für alte DITA-Maps nicht angezeigt werden, die vor der Aktualisierung der Experience Manager-Handbücher im Juli 2023 as a Cloud Service erstellt wurden. (11852)
- Bedingungsvorgaben für große DITA-Maps werden nicht erstellt. (10936)
- Unter der Liste der fehlerhaften Links in Berichten wird ein Selbsthilfe-Link angezeigt. (13539)

### Überprüfung

- Die Bedienfelder der vorherigen und der aktuellen Versionen im Webeditor wurden in der as a Cloud Service Version der Experience Manager-Handbücher vom Oktober 2023 nicht korrekt nebeneinander angezeigt. (14156)
- Anpassung von E-Mail-Vorlagen für **Überprüfen** Der Workflow funktioniert nicht mit dem Überlagern der Knoten. (13954)
- Die **Schließen** -Schaltfläche auf der Seite &quot;Überprüfen&quot;in den Experience Manager-Handbüchern führt die Benutzer zur AEM Homepage. (13535)
- Beim Erstellen der Codefragmente in koreanischer Sprache werden ungültige Zeichen angezeigt. (13489)
- Koreanische Anlagen im Bildschirm &quot;Überprüfung der Experience Manager-Guides&quot;können nicht angeklickt werden. (13436)
- Der Titel der Karte wird im Bildschirm für Überprüfung und Zusammenarbeit abgeschnitten, ohne dass eine Option zum Anzeigen des vollständigen Titels verfügbar ist. (13012)

### Übersetzung

- Die automatische Genehmigung funktioniert manchmal nicht und es treten Ausnahmen auf, wenn ein falscher Wert auf **Übersetzungsstatus**. (13607)
- Die über das Dashboard &quot;Übersetzung&quot;exportierte Grundlinie schlägt fehl und wird nicht in der Zielsprache geöffnet. (12993)

## Bekanntes Problem

Adobe hat das folgende bekannte Problem für die Version November 2023 identifiziert.

- Die Neuerstellung des selektiven Themas für AEM Site-Ausgabe schlägt fehl.