---
title: Grundlegende Fehlerbehebung
description: Erfahren Sie, wie Sie die grundlegende Fehlerbehebung durchführen.
exl-id: b5ab2618-6f11-4aaa-8471-09521f8bb512
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Grundlegende Fehlerbehebung {#id1821I0Y0G0A}

Beim Arbeiten mit AEM Guides können beim Veröffentlichen oder Öffnen eines Dokuments Fehler auftreten. Solche Fehler können in der DITA-Zuordnung, dem Thema oder im Prozess AEM Guides selbst auftreten. In diesem Abschnitt finden Sie Informationen zum Zugreifen auf und Analysieren von Informationen in der Protokolldatei zur Ausgabegenerierung. Wenn Ihr DITA-Thema zu groß ist, wird möglicherweise der JSP-Kompilierungsfehler angezeigt. In diesem Abschnitt finden Sie auch Informationen zum Beheben des JSP-Kompilierungsfehlers.

## Protokolldatei anzeigen und überprüfen {#id1822G0P0CHS}

Führen Sie die folgenden Schritte aus, um die Protokolldatei zur Ausgabegenerierung anzuzeigen und zu überprüfen:

1. Nachdem Sie den Generierungsprozess der Ausgabe gestartet haben, klicken Sie auf **Ausgaben** in der DITA-Map-Konsole.

   Die **Allgemein** Spalte **Generierte Ausgaben** zeigt die Symbole an, um einen visuellen Hinweis zum Erfolg oder Misserfolg der Ausgabegenerierung zu geben.

   ![](images/output-general-settings.png){width="300" align="left"}

   Im obigen Screenshot zeigen die ersten und dritten Symbole eine fehlgeschlagene Ausgabegenerierung an. Das zweite Symbol zeigt eine erfolgreiche Ausgabegenerierung, jedoch mit Nachrichten. Die letzte ist eine erfolgreiche Ausgabegenerierung ohne Nachricht.

1. Klicken Sie auf den Link im **Generiert bei** nach Abschluss des Auftrags.

   Die Protokolldatei wird in einer neuen Registerkarte geöffnet.

   ![](images/log-file.png){width="800" align="left"}

1. Wenden Sie die folgenden Filter an, um den Text in der Protokolldatei hervorzuheben:
   - Tödlich: Zeigt die schwerwiegenden Fehler in der Protokolldatei mit rosa Farbe an.
   - Fehler: Zeigt die Fehler in der Protokolldatei mit orangefarbener Farbe an.
   - Warnung: Markiert die Warnhinweise in der Protokolldatei mit violetter Farbe.
   - Info: Markiert die Informationsmeldungen in der Protokolldatei mit blauer Farbe.
   - Ausnahme: Die in der Protokolldatei enthaltenen Ausnahmen werden gelb hervorgehoben.
1. Verwenden Sie die Navigationstasten nach oben und unten, um zum markierten Text in der Protokolldatei zu springen.

   Alternativ können Sie durch die Protokolldatei blättern und die Meldungen überprüfen.


## Kopieren und Überprüfen der Protokolldatei in einem Texteditor

Führen Sie die folgenden Schritte aus, um die Protokolldatei zur Ausgabegenerierung in einem Texteditor zu kopieren und zu überprüfen:

1. Nachdem Sie den Generierungsprozess der Ausgabe gestartet haben, klicken Sie auf **Ausgaben** in der DITA-Map-Konsole.

1. Klicken Sie auf den Link im **Generiert bei** nach Abschluss des Auftrags.

   Die Protokolldatei wird in einer neuen Registerkarte geöffnet.

1. Klicken **Protokoll kopieren** Schaltfläche. Die Protokolldatei wird in die Zwischenablage kopiert.
1. Öffnen Sie einen Texteditor und fügen Sie die Protokolldatei in den Editor ein.

1. Scrollen Sie durch die Protokolldatei und suchen Sie nach Meldungen.

   Die folgenden Informationen helfen Ihnen dabei festzustellen, ob im DITA-Datei- oder AEM Guides-Prozess ein Fehler auftritt:

   - *Fehler im Zusammenhang mit DITA-Map-Dateien*: Wenn in der DITA-Map-Datei oder einer anderen in der DITA-Zuordnung enthaltenen Datei ein Fehler gefunden wird, enthält die Protokolldatei die Zeichenfolge &quot;BUILD FEHLGESCHLAGEN&quot;. Sie können die in der Protokolldatei angegebenen Informationen überprüfen, um die fehlerhafte Datei zu finden und das Problem zu beheben.

   Im folgenden Beispielprotokolldateiausschnitt sehen Sie die `BUILD FAILED` zusammen mit dem Grund für den Fehler.

   ![](images/dita-error-in-log-file.png){width="650" align="left"}

   - *Fehler AEM Guides-bezogen*: Der andere Fehlertyp, den Sie in der Protokolldatei identifizieren können, bezieht sich auf AEM Guides-Prozess selbst. In diesem Fall wird die DITA-Map-Datei erfolgreich analysiert, aber der Prozess zur Generierung der Ausgabe schlägt aufgrund eines internen Fehlers in AEM Guides fehl. Für solche Fehler müssen Sie sich beim technischen Support-Team um Hilfe bemühen.

   Im folgenden Beispielprotokolldateiausschnitt sehen Sie die `BUILD SUCCESSFUL` Nachricht gefolgt von einem anderen technischen Fehler.

   ![](images/process-error-in-log-file.png){width="650" align="left"}


## JSP-Kompilierungsfehler beheben

Wenn Ihr DITA-Thema zu groß ist, wird möglicherweise der JSP-Kompilierungsfehler \(`org.apache.sling.api.request.TooManyCallsException`\) in Ihrem Browser. Dieser Fehler wird möglicherweise angezeigt, wenn Sie ein Thema zum Bearbeiten, Überprüfen oder Veröffentlichen öffnen.

Führen Sie die folgenden Schritte aus, um dieses Problem zu beheben:

1. Wählen Sie in der globalen Navigation die Option Tools und dann Vorgänge > Web-Konsole aus.

   Die Seite &quot;Konfiguration der Adobe Experience Manager-Web-Konsole&quot;wird angezeigt.

1. Suchen Sie nach und klicken Sie auf *Apache Sling Main Servlet* -Komponente.

   Die konfigurierbaren Optionen für das Apache Sling Main Servlet werden angezeigt.

1. Erhöhen Sie den Wert für *Anzahl der Aufrufe pro Anforderung* -Parameter entsprechend Ihren Anforderungen.


**Übergeordnetes Thema:**[ Ausgabegenerierung](generate-output.md)
