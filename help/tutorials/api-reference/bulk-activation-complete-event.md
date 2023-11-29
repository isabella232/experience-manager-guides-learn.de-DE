---
title: Ereignis-Handler für Massenaktivierung
description: Erfahren Sie mehr über den Massen-Aktivierungsabschließen-Ereignishandler
source-git-commit: 4b0e3f7cf777d2b98eb394fd89235acddef4769a
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# Ereignis-Handler für Massenaktivierung

Experience Manager-Handbücher verfügbar machen `com/adobe/fmdita/replication/complete` -Ereignis, das verwendet wird, um alle Vorgänge nach Abschluss eines Massenaktivierungsprozesses durchzuführen. Dieses Ereignis wird ausgelöst, wenn ein Massenaktivierungsprozess abgeschlossen ist. Wenn Sie beispielsweise die Massenaktivierung einer AEM Site-Vorgabe einer Zuordnung ausführen, wird dieses Ereignis nach dem Ende des Aktivierungsprozesses aufgerufen.


Sie müssen einen AEM Ereignishandler erstellen, um die in diesem Ereignis verfügbaren Eigenschaften zu lesen und eine weitere Verarbeitung durchzuführen.

Ereignisdetails werden nachfolgend erläutert:

**Ereignisname**:

```
com/adobe/fmdita/replication/complete 
```

**Parameter**: |Name|Typ|Beschreibung| |—|—|—| |`path`|String|Der Pfad der Datei, die dieses Ereignis ausgelöst hat. <br> Beispiel, `/content/output/sites/ditamap1-ditamap`. <br> Dies ist eine Liste von Pfaden, die als JSON-Array serialisiert wurden.| |`messageType`|Zeichenfolge|Der Typ einer Nachricht. <br>Mögliche Option : `REPLICATION`| |`action`|String|Dies ist die ausgeführte Aktion. <br>Mögliche Option : `BulkReplicate`| |`user`|String|Der Benutzer, der den Vorgang gestartet hat.| |`result`|Zeichenfolge|Das Ergebnis der Massenaktivierung. Es handelt sich um ein serialisiertes JSON-Objekt: <br>`{"success":boolean,"code":integer,"message":"" }`| |`agentId`|String|Die in der Replikation verwendete agentId. Zum Beispiel: `"publish"`.| |`importMode`|String|Importmodus, der in der Aktivierung verwendet wird. Die möglichen Optionen sind: <br>`REPLACE, MERGE, UPDATE`.|


**Beispiel-Ereignis-Listener**:

```XML
@Component(service = EventHandler.class,
        immediate = true,
        property = {
                EventConstants.EVENT_TOPIC + "=" + "com/adobe/fmdita/replication/complete",
        })
 
public class SampleEventHandler implements EventHandler {
 
    protected final Logger log = LoggerFactory.getLogger(this.getClass());
 
    @Override
    public void handleEvent(final Event event) {
        Map<String, String> properties = new HashMap<>();
        properties.put("paths", (String) event.getProperty("paths"));
        properties.put("messageType", (String) event.getProperty("messageType"));
        properties.put("action", (String) event.getProperty("action"));
        properties.put("result", (String) event.getProperty("result"));
        properties.put("user", (String) event.getProperty("user"));
        properties.put("agentId", (String) event.getProperty("agentId"));
        properties.put("importMode", (String) event.getProperty("importMode"));
 
        String eventTopic = event.getTopic();
        log.debug("eventTopic {}", eventTopic);
        for(Map.Entry entry:properties.entrySet()) {
            log.debug(entry.getKey() + " : " + entry.getValue());
        }
 
    }
}
```
