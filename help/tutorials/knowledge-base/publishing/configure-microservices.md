---
title: Neue mikrodienstbasierte Veröffentlichung für AEM Guides as a Cloud Service konfigurieren
description: Erfahren Sie, wie Sie neue mikrodienstbasierte Veröffentlichungen für AEM-Handbücher konfigurieren.
source-git-commit: afbc1712cf45dd0b570e20683946af6a86edae7e
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Neue mikrodienstbasierte Veröffentlichung für AEM Guides as a Cloud Service konfigurieren

Mit dem neuen Publishing-Microservice können Benutzer gleichzeitig große Veröffentlichungsarbeitslasten auf AEM Handbüchern as a Cloud Service ausführen und die branchenführende Server-lose Adobe I/O Runtime-Plattform nutzen.

Für jede Veröffentlichungsanforderung AEM Handbücher führt as a Cloud Service einen separaten Container aus, der entsprechend den Benutzeranforderungen horizontal skaliert wird. Dadurch erhalten Benutzer die Möglichkeit, mehrere Veröffentlichungsanfragen auszuführen und eine bessere Leistung zu erzielen als ihre großen On-Premise-AEM-Server.

Da der neue Cloud Publishing-Dienst durch die JWT-basierte Authentifizierung von Adobe IMS geschützt ist, sollten Kunden die folgenden Schritte ausführen, um ihre Umgebungen in sichere Token-basierte Authentifizierungsarbeitsabläufe von Adobe zu integrieren und mit der neuen Cloud-basierten skalierbaren Publishing-Lösung zu beginnen.


## Erstellen von IMS-Konfigurationen in der Adobe Developer-Konsole

**Rolle, die zur Erstellung der Verwirrungen erforderlich ist**: Systemadministrator

Führen Sie die folgenden Schritte aus, um IMS-Konfigurationen in der Adobe Developer Console zu erstellen:

1. Öffnen Sie die Entwicklerkonsole: `https://developer.adobe.com/console`.

1. Wechseln zu **Projekte** von oben aus.

   <img src="assets/projects-tab.png" alt="Projekt-Tab" width="500">

1. Um ein neues leeres Projekt zu erstellen, wählen Sie **Leeres Projekt** von **Neues Projekt erstellen** Dropdown-Liste.

   <img src="assets/create-new-project.png" alt="Neues Projekt erstellen" width="500">

1. Auswählen **API** von **Zum Projekt hinzufügen** Dropdown-Liste, um Ihrem Projekt die IO Management-API hinzuzufügen.

   <img src="assets/add-project.png" alt="Projekt hinzufügen" width="300">

   <img src="assets/io-management-api.png" alt="IO-Management" width="500">

1. Erstellen Sie beim Hinzufügen der API ein neues Paar aus privatem/öffentlichem Schlüssel. Dadurch wird automatisch der private Schlüssel auf Ihr System heruntergeladen.

   <img src="assets/generate-key-pair.png" alt="Schlüsselpaar generieren" width="500">

1. Speichern Sie die konfigurierte API.

   <img src="assets/save-api.png" alt="API speichern" width="600">

1. Gehen Sie zurück zu **Projekte** Registerkarte und klicken Sie auf **Projektübersicht** auf der linken Seite.

   <img src="assets/project-overview.png" alt="Projektübersicht" width="500">

1. Klicken **Download** oben auf die Schaltfläche zum Herunterladen der Dienst-JSON.

   <img src="assets/download-json.png" alt="JSON herunterladen" width="500">

Sie haben jetzt die Details zur JWT-Authentifizierung konfiguriert und auch den privaten Schlüssel und die JSON-Datei mit den Dienstdetails heruntergeladen. Halten Sie diese beiden Dateien bereit, da diese Dateien im nächsten Abschnitt benötigt werden.

### Hinzufügen der IMS-Konfiguration zur Umgebung

Führen Sie die folgenden Schritte aus, um der Umgebung die IMS-Konfiguration hinzuzufügen:

1. Öffnen Sie Experience Manager und wählen Sie dann Ihr Programm aus, das die Umgebung enthält, die Sie konfigurieren möchten.
1. Wechseln zu **Umgebungen** Registerkarte.
1. Klicken Sie auf den Umgebungsnamen, den Sie konfigurieren möchten. Dies sollte Sie zur Seite &quot;Umgebungsinformationen&quot;führen.
1. Wechseln zu **Konfiguration** Registerkarte.
1. Laden Sie den privaten Schlüssel und die Projekt-JSON hoch, wie im Screenshot unten dargestellt. Stellen Sie sicher, dass Sie dieselben Namen und Konfigurationen wie unten hervorgehoben verwenden.

   <img src="assets/ims-config-environment.png" alt="ims-Konfigurationen" width="500">

>[!NOTE]
>
> Sie müssen den Inhalt der JSON-Datei mit Details zum privaten Schlüssel und Dienst in die Wertspalte des Konfigurationsbereichs öffnen, kopieren und einfügen, wie im obigen Screenshot gezeigt.

Nachdem Sie die IMS-Konfiguration zur Umgebung hinzugefügt haben, führen Sie die folgenden Schritte aus, um diese Eigenschaften mit OSGi mit AEM Guides zu verknüpfen:

1. Fügen Sie in Ihrem Git-Projektcode des Cloud Manager die folgenden beiden Dateien hinzu (Dateiinhalte finden Sie unter [Anhang](#appendix)).

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`
   * `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`
1. Stellen Sie sicher, dass die neu hinzugefügten Dateien von Ihrem `filter.xml`.
1. Übernehmen Sie Ihre Git-Änderungen und übertragen Sie sie.
1. Führen Sie die Pipeline aus, um die Änderungen auf die Umgebung anzuwenden.

Danach sollten Sie in der Lage sein, das neue Microservice-basierte Cloud Publishing zu verwenden.

## Anhang {#appendix}

**File**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**Inhalt**:

```
{
  "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
  "private.key": "$[secret:PRIVATE_KEY]"
}
```

**File**: `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`

**Inhalt**:

```
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:jcr="http://www.jcp.org/jcr/1.0" xmlns:sling="http://sling.apache.org/jcr/sling/1.0"
          jcr:primaryType="sling:OsgiConfig"
          dxml.publish.microservice.url="https://adobeioruntime.net/api/v1/web/543112-guidespublisher/default/publishercaller.json"
          dxml.use.publish.microservice="{Boolean}true"
/>
```
