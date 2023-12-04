---
title: Recommendations zur Leistungsoptimierung
description: Recommendations zur Leistungsoptimierung kennenlernen
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Recommendations zur Leistungsoptimierung {#id213BD0JG0XA}

## Datenspeicher konfigurieren \(erforderlich\)

**Was ist die Veränderung?**
Legen Sie die `minRecordLength` -Eigenschaft auf einen Wert von `100` unter der Konfiguration `org.apache.jackrabbit.oak.plugins.blob.datastore.FileDataStore.` Weitere Informationen zum Dateidatumsspeicher und zum S3-Datenspeicher finden Sie unter [Konfigurieren von Knotenspeichern und Datenspeichern in AEM 6](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html) Artikel.

>[!NOTE]
>
> Bei S3-Datenspeichern hängen die Kosten für die Pflege von Inhalten im Datenspeicher auch von der Anzahl der Anfragen ab. Daher sollten bei dieser Einstellung mit S3 die Einrichtungskosten pro Anfrage und die Cachegröße ebenfalls berücksichtigt werden.

**Wann sollte konfiguriert werden?**
Nach der Ersteinrichtung, aber vor der Migration von Inhalten. Sie müssen diese Änderung auch auf einem vorhandenen System durchführen, wodurch sichergestellt wird, dass alle neuen Inhalte im Datenspeicher und nicht im Segmentspeicher gespeichert werden.

**Ergebnis dieser Änderung**
Die DITA-Dateien werden im Datenspeicher und nicht im Segmentspeicher gespeichert. Dadurch bleibt die Größe des Segmentspeichers unter den empfohlenen Grenzen, was die Reaktionsfähigkeit des Systems verbessert.

## Lucene-Index aktualisieren \(erforderlich\)

**Was ist die Veränderung?**
Schließen Sie /var/dxml aus oak:index/lucene aus.

>[!NOTE]
>
> AEM Guides verwenden niemals Lucene-Indizes, um im Knoten /var/dxml nach Inhalten zu suchen.

**Wann sollte konfiguriert werden?**
Wenn Sie diese Änderung auf einem neuen System vornehmen, bevor Sie Inhalte migrieren, ist nur eine Aktualisierung von oak:index/lucene erforderlich. Andernfalls erstellen Sie in einem vorhandenen System, in dem der Inhalt bereits migriert ist, nach der Änderung in oak:index/lucene Indizes für Lucene \(*Dies kann einige Stunden dauern*\).

**Ergebnis dieser Änderung**
Diese Änderung verhindert, dass der Knoten /var/dxml indiziert und im Segmentspeicher gespeichert wird.

## Java-Speicheroptimierung \(erforderlich\)

**Was ist die Veränderung?**
Die JVM-Startparameter sollten entsprechend der Infrastruktur und der Festplattengröße sorgfältig angepasst werden. Es wird empfohlen, den Adobe-Support zu konsultieren, um Hilfe beim Zugriff auf die ideale Konfiguration zu erhalten. Sie können jedoch die folgenden Konfigurationen selbst ausprobieren:

- Setzen Sie die JVM-Heap-Größe auf ein Minimum von 1/4 des gesamten verfügbaren Speichers. Verwenden des Parameters `-Xmx<size>` , um die Heap-Speichergröße festzulegen. Legen Sie den Wert für fest:`Xms` gleich `-Xmx`.

- Aktivieren `-XX:+HeapDumpOnOutOfMemoryError` und legen Sie den Pfad für `-XX:HeapDumpPath=</path/to/folder``>`.

- Aktivieren Sie das Java GC-Protokoll als:

`* -XX:+PrintGCDateStamps`

`* -verbose:gc`

`* -XX:+PrintGCDetails`

`* -XX:+PrintTenuringDistribution`

`* -Xloggc:</path/to/gc.log>`

- Im Allgemeinen für Java 11 verwenden Sie G1GC \(`-XX:+UseG1GC`\) und für Java 8 verwenden Sie CMS \(-`XX:+UseConcMarkSweepGC`\).

- Verwendung `-XX:NewRatio` um die Größe des Speicherplatzes der jungen Generation zu steuern. Der Standardwert ist 2, was bedeutet, dass 1/3 des Speichers für junge Generation verwendet wird. Da viele Objekte schnell erstellt und zerstört werden, wird mit dem Wert 1 1/2 des Speichers der jungen Generation zugewiesen.

- Steuern Sie die Anzahl der Objekte, die mit der `-XX:MaxTenuringThreshold`. Verwenden Sie den Wert 15 \(Standard\), um zu verzögern, wenn Objekte zur alten Generation weitergeleitet werden.

**Wann sollte konfiguriert werden?**
Wenn Sie diese Änderung an einem vorhandenen System vornehmen, müssen Sie das System neu starten. Bei einer Neuinstallation sollte diese Änderung in der Datei mit dem Startskript \(.bat oder .sh\) vorgenommen werden, bevor das System gestartet wird.

**Ergebnis dieser Änderung**
Dies führt zu einer optimalen Heap-Größe und einer regulierten Ausführung von GC.

## Minimierung der Client-Bibliothek in der Autoreninstanz \(optional\)

**Was ist die Veränderung?**
Die Client-Bibliotheken sollten in den Authoring-Instanzen auf minimiert eingestellt werden. Dadurch wird sichergestellt, dass beim Durchsuchen des Systems von verschiedenen Speicherorten weniger Bytes heruntergeladen werden müssen. Um diese Änderung vorzunehmen, legen Sie die Konfiguration in **HTML Library Manager** über die Felix-Konsole.

**Wann sollte konfiguriert werden?**
Dies kann zur Laufzeit über die Felix-Konsole oder über die Code-Implementierung erfolgen.

**Ergebnis dieser Änderung**
Diese Änderung verbessert die Ladezeit von Seiten in der -Autoreninstanz, da weniger Bytes zum Laden der Client-Bibliotheken übertragen werden.

## Konfigurieren von Threads für gleichzeitige Veröffentlichung \(Erforderlich, je nach Anwendungsfall\)

**Was ist die Veränderung?**
Diese Änderung ist erforderlich, wenn Sie DITA-OT zum Veröffentlichen der Ausgabe verwenden und eine Reihe von gleichzeitigen Veröffentlichungs-Threads ebenfalls definiert ist.

Standardmäßig stellt AEM Guides die Veröffentlichungs-Threads auf die Anzahl der CPUs+1 ein. Es wird jedoch empfohlen, diesen Wert auf die Hälfte \(1/2\) oder ein Drittel \(1/3\) der Gesamtanzahl der CPUs festzulegen. Legen Sie dazu die **Erstellungspoolgröße** -Eigenschaft unter der Konfiguration `com.adobe.fmdita.publish.manager.PublishThreadManagerImpl` gemäß den Empfehlungen.

**Wann sollte konfiguriert werden?**
Dies kann zur Laufzeit über die Felix-Konsole oder über die Code-Implementierung erfolgen.

**Ergebnis dieser Änderung**
Diese Änderung stellt sicher, dass in einer laufenden Autoreninstanz nicht alle Ressourcen für die Veröffentlichungsvorgänge zugewiesen werden. Dadurch bleiben die Systemressourcen auch für Autoren verfügbar, was zu einem besseren Benutzererlebnis führt.

## Konfigurieren der Batch-Größe von Knoten für die Generierung AEM Site-Ausgabe \(Erforderlich, je nach Anwendungsfall\)

**Was ist die Veränderung?**
Diese Änderung ist erforderlich, wenn Sie die AEM Sites-Ausgabe generieren.

Legen Sie die **Beschränken AEM Site-Seiten in Heap** Eigenschaft unter `com.adobe.fmdita.config.ConfigManager` auf eine Zahl, die auf der Konfiguration Ihres Systems basiert. Diese Eigenschaft definiert die Batch-Größe der Knoten, die bei der Erstellung der Site-Seiten übertragen werden sollen. Auf einem System mit einer größeren Anzahl von CPUs und Heap-Größe können Sie beispielsweise den Standardwert von `500` auf eine größere Zahl. Sie müssen die Ausführung mit dem geänderten Wert testen, um zu einem optimalen Wert für diese Eigenschaft zu gelangen.

**Wann sollte konfiguriert werden?**
Dies kann zur Laufzeit über die Felix-Konsole oder über die Code-Implementierung erfolgen.

**Ergebnis dieser Änderung**
Eine erhöhte Anzahl von **Beschränken AEM Site-Seiten in Heap** -Eigenschaft optimiert den Generierungsprozess der AEM Site-Ausgabe.

## Anzahl der Nachbearbeitungs-Threads optimieren \(je nach Anwendungsfall obligatorisch\)

**Was ist die Veränderung?**
Diese Änderung ist erforderlich, wenn Sie DITA-Inhalte stapelweise hochladen.

Legen Sie die **Nachbearbeitungs-Threads** Eigenschaft unter `com.adobe.fmdita.config.ConfigManager` nach `1`.

**Wann sollte konfiguriert werden?**
Dies kann zur Laufzeit erfolgen.

**Ergebnis dieser Änderung**
Durch diese Änderung wird die Nachbearbeitungszeit beim Massen-Upload von DITA-Dateien verkürzt.

**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)
