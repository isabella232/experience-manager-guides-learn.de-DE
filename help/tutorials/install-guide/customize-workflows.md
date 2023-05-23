---
title: Workflows konfigurieren und anpassen
description: Erfahren Sie, wie Sie Workflows konfigurieren und anpassen.
source-git-commit: 9fe396dcfd2e3570ec386c958d7d4efdb4d608e5
workflow-type: tm+mt
source-wordcount: '1781'
ht-degree: 5%

---


# Workflows konfigurieren und anpassen {#id181AI0OJ0RO}

Mit Workflows können Sie Adobe Experience Manager \(AEM\)-Aktivitäten automatisieren. Ein Workflow besteht aus einer Reihe von Schritten, die in einer bestimmten Reihenfolge ausgeführt werden. Sie können für jeden Schritt eine eigene Aktivität definieren. Sie können beispielsweise eine E-Mail-Benachrichtigung an alle validierungsverantwortlichen Benutzer einer Gruppe senden, wenn eine Themenüberprüfung erstellt wird. Sie können auch eine Benachrichtigung an den Herausgeber senden, wenn eine Aufgabe zur Generierung der Ausgabe abgeschlossen ist.

Weitere Informationen zu Workflows in AEM finden Sie unter:

- [Verwalten von Workflows](https://helpx.adobe.com/de/experience-manager/6-5/sites/administering/using/workflows.html)

- Anwenden von und Teilnehmen an Workflows: [Arbeiten mit Workflows](https://helpx.adobe.com/de/experience-manager/6-5/sites/authoring/using/workflows.html).

- Das Erstellen von Workflow-Modellen und die Erweiterung der Workflow-Funktionalität: [Entwickeln und Erweitern von Workflows](https://helpx.adobe.com/de/experience-manager/6-5/sites/developing/using/workflows.html).

- Verbesserung der Leistung von Workflows, die umfangreiche Serverressourcen nutzen: [Gleichzeitige Workflow-Verarbeitung](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/configuring-performance.html#ConfiguringforPerformance).


Die Abschnitte in diesem Thema führen Sie durch verschiedene Anpassungen, die Sie in den Standard-Workflows vornehmen können, die in AEM Handbüchern enthalten sind.

## Anpassen des Prüfungs-Workflows {#id176NE0C00HS}

Das Content-Authoring-Team jedes Unternehmens arbeitet auf eine bestimmte Weise, um seine Geschäftsanforderungen zu erfüllen. In einigen Unternehmen gibt es einen dedizierten Editor, während einige andere Organisationen ein automatisiertes Redaktionsüberprüfungssystem einrichten könnten. In einer Organisation könnte beispielsweise ein typischer Bearbeitungs- und Veröffentlichungsarbeitsablauf Aufgaben wie beispielsweise umfassen: Wenn ein Autor mit Authoring-Inhalten fertig ist, wird er automatisch an die Validierer gesendet und nach Abschluss der Überprüfung wird er zum Generieren der endgültigen Ausgabe an den Herausgeber weitergeleitet. In AEM können Aktivitäten, die Sie mit Ihren Inhalten und Assets durchführen, in Form eines Prozesses kombiniert und einem AEM Workflow zugeordnet werden. Weitere Informationen zu Workflows in AEM finden Sie unter [Verwalten von Workflows](https://helpx.adobe.com/de/experience-manager/6-5/sites/administering/using/workflows.html) in AEM Dokumentation.

Mit AEM Guides können Sie den standardmäßigen Prüfungs-Workflow anpassen. Sie können die folgenden vier benutzerdefinierten Review-bezogenen Prozesse mit Ihren anderen Authoring- oder Publishing-Workflows verwenden.

- **Prüfung erstellen**: Dieser Prozess bereitet die zum Erstellen einer Prüfungsaufgabe erforderlichen Metadaten vor. Beispielsweise werden den Validierungsverantwortlichen Prüfungsberechtigungen zugewiesen, der Status der zu überprüfenden Themen festgelegt, Zeitpläne für die Überprüfung festgelegt und mehr. Von den vier Prozessen ist dies der einzige erforderliche Prozess, der in Ihren benutzerdefinierten Workflow aufgenommen werden muss. Im Workflow können Sie die drei anderen Prozesse ein- oder ausschließen.

- **Prüfungsaufgabe zuweisen**: Dieser Prozess erstellt die Prüfungsaufgabe und sendet die Aufgabenbenachrichtigung an den Initiator und die Überprüfer.

- **Überprüfungs-E-Mail senden**: Dieser Prozess sendet die Überprüfungs-E-Mail an den Initiator und die Überprüfer.

- **Vorgang planen zum Schließen der Überprüfung**: Dadurch wird sichergestellt, dass der Überprüfungsprozess mit Erreichen der Frist abgeschlossen ist.


Wenn Sie einen benutzerdefinierten Überprüfungs-Workflow erstellen, besteht die erste Aufgabe darin, die erforderlichen Metadaten festzulegen, die für den Prozess zum Erstellen einer Überprüfung erforderlich sind. Dazu können Sie ein ECMA-Skript erstellen. Nachfolgend finden Sie ein Beispiel für das ECMA-Skript, das die Metadaten zuweist:

```json
var workflowdata=workItem.getWorkflowData();
workflowdata.getMetaDataMap().put("initiator","admin");
workflowdata.getMetaDataMap().put("operation","AEM_REVIEW");
workflowdata.getMetaDataMap().put("orgTopics","/content/dam/xml-solution/review.xml");
workflowdata.getMetaDataMap().put("payloadJson","{\"base\":\"/content/dam/xml-solution\",\"asset\":[\"/content/dam/xml-solution/review.xml\"],\"referrer\":\""}");
workflowdata.getMetaDataMap().put("deadline","2017-06-27T13:19:00.000+05:30");
workflowdata.getMetaDataMap().put("title","Review through custom workflow");
workflowdata.getMetaDataMap().put("description","Initiate this review process using the AEM workflow");
workflowdata.getMetaDataMap().put("assignee","user-one", "user-two");
workflowdata.getMetaDataMap().put("status","1");
workflowdata.getMetaDataMap().put("projectPath","/content/projects/review");
workflowdata.getMetaDataMap().put("startTime", System.currentTimeMillis());
```

Sie können dieses Skript im `/etc/workflows/scripts` Knoten. In der folgenden Tabelle werden die von diesem ECMA-Skript zugewiesenen Eigenschaften beschrieben:

| Eigenschaft | Typ | Beschreibung |
|--------|----|-----------|
| `initiator` | Zeichenfolge | Benutzer-ID des Benutzers, der die Prüfungsaufgabe initiiert. |
| `operation` | Zeichenfolge | Ein statischer Wert, festgelegt als `AEM_REVIEW`. |
| `orgTopics` | Zeichenfolge | Pfad der Themen, die zur Überprüfung freigegeben werden. Geben Sie mehrere Themen durch Kommas getrennt an. |
| `payloadJson` | JSON-Objekt | Geben Sie die folgenden Werte an:<br> - `base`: Pfad des übergeordneten Ordners, der das Thema enthält, das zur Überprüfung gesendet wird.<br>- `asset`: Pfad des Themas, das zur Überprüfung gesendet wird. <br>- `referrer`: Lassen Sie es leer. |
| `deadline` | Zeichenfolge | Geben Sie die Uhrzeit in `yyyy-MM-dd'T'HH:mm:ss.SSSXXX` Format. |
| `title` | Zeichenfolge | Geben Sie einen Titel für die Prüfungsaufgabe ein. |
| `description` | Zeichenfolge | Geben Sie eine Beschreibung für die Prüfungsaufgabe ein. |
| `assignee` | Zeichenfolge | Benutzer-ID der Benutzer, an die Sie die Themen senden möchten\(n), um sie zu überprüfen. |
| `status` | Ganzzahl | Ein statischer Wert, der auf 1 gesetzt ist. |
| `startTime` | Long | Verwenden Sie die `System.currentTimeMillis()` -Funktion, um die aktuelle Systemzeit abzurufen. |

Nachdem Sie das Skript erstellt haben, rufen Sie es auf, bevor Sie in Ihrem Workflow den Prozess Überprüfung erstellen aufrufen. Anschließend können Sie je nach Ihren Anforderungen die anderen Workflow-Prozesse für Überprüfungen aufrufen.

### Entfernen Sie den Überprüfungs-Workflow aus der Bereinigungskonfiguration

Um die Leistung der Workflow-Engine zu verbessern, können Sie regelmäßig abgeschlossene Workflow-Instanzen aus dem AEM-Repository bereinigen. Wenn Sie die standardmäßigen AEM verwenden, werden alle abgeschlossenen Workflow-Instanzen nach einem bestimmten Zeitraum bereinigt. Dies führt auch dazu, dass alle Prüfungs-Workflows aus dem AEM-Repository gelöscht werden.

Sie können die automatische Bereinigung von Überprüfungs-Workflows verhindern, indem Sie das Überprüfungs-Workflow-Modell \(Informationen\) aus der automatischen Bereinigungskonfiguration entfernen. Sie müssen die **Adobe Granite-Workflow-Bereinigungskonfiguration** , um die Überprüfungs-Workflow-Modelle aus der Liste der automatischen Bereinigung zu entfernen.

Im **Adobe Granite-Workflow-Bereinigungskonfiguration**, stellen Sie sicher, dass Sie mindestens einen Workflow auflisten, den Sie sicher bereinigen können. Sie können beispielsweise einen der folgenden, von AEM Guides erstellten Workflows verwenden:

- /etc/workflow/models/publishditamap/jcr:content/model
- /etc/workflow/models/post-dita-project-creation-tasks/ jcr:content/model

Hinzufügen eines Workflows im **Adobe Granite-Workflow-Bereinigungskonfiguration** stellt sicher, dass AEM nur die in der Konfiguration aufgelisteten Workflows löscht. Dadurch wird verhindert, dass AEM die Informationen des Prüfungs-Workflows bereinigen.

Weitere Informationen zum Konfigurieren der **Adobe Granite-Workflow-Bereinigungskonfiguration**, siehe *Verwalten von Workflow-Instanzen* in AEM Dokumentation.

### E-Mail-Vorlagen anpassen

Einige der Workflows für AEM Guides nutzen E-Mail-Benachrichtigungen. Wenn Sie beispielsweise eine Prüfungsaufgabe starten, wird eine E-Mail-Benachrichtigung an die Validierer gesendet. Um jedoch sicherzustellen, dass die E-Mail-Benachrichtigung gesendet wird, müssen Sie diese Funktion in AEM aktivieren. Informationen zum Aktivieren von E-Mail-Benachrichtigungen in AEM finden Sie im Artikel . [Konfigurieren von E-Mail-Benachrichtigungen](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=de) in AEM Dokumentation.

AEM Guides enthalten eine Reihe von E-Mail-Vorlagen, die Sie anpassen können. Führen Sie die folgenden Schritte aus, um diese Vorlagen anzupassen:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. Navigieren Sie auf der Registerkarte Navigator zum folgenden Speicherort:

   `/libs/fmdita/mail`

   >[!NOTE]
   >
   > Nehmen Sie keine Anpassungen in den Standardkonfigurationsdateien vor, die im ``libs`` Knoten. Sie müssen eine Überlagerung der ``libs`` Knoten in ``apps`` und aktualisieren Sie die erforderlichen Dateien im ``apps`` nur Knoten.

1. Der E-Mail-Ordner enthält die folgenden anpassbaren Vorlagen:

   | Vorlagendateiname | Beschreibung |
   |-----------------|-----------|
   | closereview.html | Diese E-Mail-Vorlage wird verwendet, wenn eine Prüfungsaufgabe geschlossen wird. |
   | createreview.html | Diese E-Mail-Vorlage wird verwendet, wenn eine neue Prüfungsaufgabe erstellt wird. |
   | reviewapproval.css | Diese CSS-Datei enthält den Stil von E-Mail-Vorlagen. |


## Arbeitsablauf für die Generierung nach der Ausgabe anpassen {#id17A6GI004Y4}

AEM Handbücher bieten Ihnen die Flexibilität, einen Workflow zur Erstellung nach der Ausgabe festzulegen. Sie können einige Nachbearbeitungsaufgaben für die Ausgabe ausführen, die mithilfe von AEM-Handbüchern generiert wird. Sie können beispielsweise einige CQ-Tags auf die generierte AEM Site-Ausgabe anwenden oder bestimmte Eigenschaften für die PDF-Ausgabe festlegen oder eine E-Mail an eine Gruppe von Benutzern senden, sobald die Ausgabe generiert wurde.

Sie können ein neues Workflow-Modell erstellen, das als Workflow für die Generierung nach der Ausgabe verwendet wird. Wenn ein Workflow zur Generierung nach der Ausgabe ausgelöst wird, gibt der Workflow zur Generierung der Ausgabe Kontextdaten über die Workflow-Metadatenzuordnung frei, die Sie zur Verarbeitung der generierten Ausgabe verwenden können. In der folgenden Tabelle werden die als Metadaten freigegebenen Kontextdaten beschrieben:

| Eigenschaft | Typ | Beschreibung |
|--------|----|-----------|
| ``outputName`` | Zeichenfolge | Name der Ausgabevorgabe, die zum Generieren der Ausgabe verwendet wird. |
| `generatedPath` | Zeichenfolge | Pfad in DAM, in dem die generierte Ausgabe gespeichert wird. |
| `outputType` | com.adobe.fmdita.output.OutputType | Typ der Ausgabevorgabe. |
| `outputTitle` | Zeichenfolge | Titel der Ausgabevorgabe. |
| `outputHistoryPath` | Zeichenfolge | Repository-Pfad des Verlaufsknotens. |
| `isSuccess` | Boolesch | Eine Markierung, die den finalen Status des Generierungsprozesses der Ausgabe darstellt - Erfolg oder Fehler. |
| `logPath` | Zeichenfolge | Pfad in DAM, in dem die Ausgabegenerierungsprotokolle gespeichert werden. |
| `generatedTime` | Long | Zeitpunkt, zu dem der Output-Generierungsprozess ausgelöst wurde. |
| `initiator` | Zeichenfolge | Die Benutzer-ID des Benutzers, der den Workflow zur Generierung der Ausgabe ausgelöst hat. |

Um die Metadaten zur Ausgabegenerierung zu verwenden, können Sie ein ECMA-Skript oder ein OSGi-Bundle erstellen. Nachfolgend finden Sie ein Beispiel für das ECMA-Skript, das die Metadaten verwendet:

>[!NOTE]
>
> Sie können dieses Skript im ``/etc/workflows/scripts`` Knoten.

```json
var session = workflowSession.getSession(); // Obtain session object to read/write the repository.
var payload = workItem.getWorkflowData().getPayload().toString(); // Get the workflow payload (the ditamap file on which the generation was triggered)
var metadata = workItem.getWorkflowData().getMetaDataMap(); // Get the workflow metadata object
var generatedPath = metadata.get("generatedPath"); // supplied by AEM Guides
var username = metadata.get("initiator"); // supplied by AEM Guides
var successful = metadata.get("isSuccess"); // supplied by AEM Guides
var title = metadata.get("outputTitle"); // supplied by AEM Guides
var subject = "Output Generation Finished";
var message = "Generation of output " + title + " just finished " + 
(successful ? "successfully. " : "unsuccessfully. ");
    message += "It was triggered by " + username;    
if (successful) {
    message += "<br/><br/>The path to the generated output is " + 
generatedPath;
}
/*
    MailerAPI.sendMail("dl-docs-authors", subject, message);
*/
```

Rufen Sie nach der Erstellung des Skripts das benutzerdefinierte Skript in Ihrem Workflow auf. Anschließend können Sie entsprechend Ihren Anforderungen die anderen Workflow-Prozesse aufrufen. Nachdem Sie Ihren benutzerdefinierten Workflow entworfen haben, rufen Sie die *Post-Generierung abschließen* als letzten Schritt in Ihrem Workflow-Prozess. Die *Post-Generierung abschließen* Schritt stellt sicher, dass der Status der Ausgabegenerierungsaufgabe aktualisiert wird auf *Abgeschlossen* nach Abschluss des Generierungsprozesses der Ausgabe. Nach der Erstellung eines benutzerdefinierten Workflows für die Erstellung nach der Ausgabe können Sie ihn mit einer beliebigen Ausgabegenerierungsvoreinstellung konfigurieren. Wählen Sie den gewünschten Workflow im *Workflow &quot;Nach der Erstellung ausführen&quot;* -Eigenschaft der erforderlichen Vorgabe. Wenn Sie eine Ausgabegenerierungsaufgabe mit der konfigurierten Ausgabevorgabe ausführen, ändert sich der Aufgabenstatus \(auf der Registerkarte &quot;Ausgabe&quot;\) in *Nachbearbeitung*.

## Workflow &quot;Asset-Update anpassen&quot; {#id18C3D0I0B5Z}

Standardmäßig wird die *DAM-Update-Asset* Workflow-Trigger jedes Mal, wenn Sie ein AEM Asset erstellen oder aktualisieren \(XML oder Nicht-XML\). Wenn Sie beispielsweise ein Thema erstellen oder aktualisieren, wird die *DAM-Update-Asset* wird ausgeführt. Die *DAM-Update-Asset* Workflow versucht, relevante Metadaten aus Assets zu extrahieren. Die vordefinierten *Asset-Update-Workflow* verfügt über keine Schritte zum Extrahieren relevanter Metadaten aus einer DITA-Datei und die *DAM-Update-Asset* Der Workflow erzeugt zum Zeitpunkt der Ausführung eine Vielzahl von Protokollen. Wenn Sie die zusätzlichen Protokolle vermeiden möchten, können Sie den Workflow so konfigurieren, dass alle XML-Dateien von der Verarbeitung übersprungen werden.

Führen Sie die folgenden Schritte aus, um die *DAM-Update-Asset* workflow:

1. Öffnen Sie die **Workflow-Starter** Seite.

   Die Standard-URL für den Zugriff auf die Seite &quot;Workflow-Starter&quot;lautet:

   ```http
   http://<server name>:<port>/libs/cq/workflow/admin/console/content/launchers.html
   ```

1. Öffnen Sie in der Liste der Workflow-Starter die Eigenschaften des **DAM-Update-Asset** Arbeitsablauf.

1. Fügen Sie eine Bedingung mit dem folgenden Ausdruck hinzu:

   ```json
   jcr:content/metadata/dc:format!=application/xml
   ```

1. Klicken Sie auf **Speichern und schließen**.


## Konfigurieren des Nachbearbeitungs-XML-Workflows {#id18CJB03J0Y4}

AEM Guides erstellen eine Reihe von Workflows, mit denen Sie mit DITA-Inhalten in AEM arbeiten können. Es gibt beispielsweise Workflows, die ausgeführt werden, wenn Sie DITA-Inhalte hochladen oder vorhandene Inhalte aktualisieren. Diese Workflows analysieren DITA-Dokumente und führen verschiedene Aufgaben durch, z. B. das Festlegen der Metadaten, das Hinzufügen von standardmäßigen Ausgabevorgaben zu neuen DITA-Maps und andere damit verbundene Aufgaben.

>[!NOTE]
>
> Um die standardmäßigen Nachbearbeitungs-Workflows anzupassen oder zu erweitern, können Sie den Ereignis-Handler für die Nachbearbeitung verwenden, der im Abschnitt *API-Referenz für Adobe Experience Manager-Handbücher*.

Die folgenden Eigenschaften steuern, wie AEM Guides die Nachbearbeitungs-Workflows ausführen:

>[!NOTE]
>
> Auf die folgenden Eigenschaften kann über die Web-Konsole zugegriffen werden: http://&lt;server name=&quot;&quot;>:&lt;port>/system/console/configMgr.

| Eigenschaft | Bundle-Name | Beschreibung |
|--------|-----------|-----------|
| Dynamische Outrefs | `com.adobe.fmdita.postprocess.PostProcessObservation` | Bei allen Dateien, bei denen die Nachbearbeitung nicht durchgeführt wurde, werden die ausgehenden Verweise abgerufen, indem die Themendateien analysiert werden. Es wird empfohlen, diese Option deaktiviert zu lassen, da es möglich ist, das System zu überlasten, wenn die Anzahl der zu verarbeitenden Dateien groß ist. |
| Nachbearbeitungs-Threads | `com.adobe.fmdita.config.ConfigManager` | Legt die Anzahl der Nachbearbeitungs-Threads fest, die für Nachbearbeitungs-Workflows verwendet werden sollen. <br>Der Standardwert ist 1. |

