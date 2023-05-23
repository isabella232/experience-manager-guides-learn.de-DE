---
title: Verwenden einer benutzerdefinierten DITA-OT- und DITA-Spezialisierung
description: Erfahren Sie, wie Sie benutzerdefinierte DITA-OT- und DITA-Spezialisierung verwenden.
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '2075'
ht-degree: 0%

---


# Verwenden einer benutzerdefinierten DITA-OT- und DITA-Spezialisierung {#id181GAJ0005Z}

Das DITA Open Toolkit \(DITA-OT\) ist ein Satz von Java-basierten Open-Source-Tools, die die Verarbeitung von DITA-Maps und Themeninhalten ermöglichen. Mit AEM Guides können Sie benutzerdefinierte DITA-OT-Plug-ins einfach importieren und verwenden. Nach dem Import können AEM Guides so konfiguriert werden, dass das benutzerdefinierte DITA-OT-Plug-in verwendet wird, um Ausgaben in jedem beliebigen Format zu generieren. Wählen Sie zum Zeitpunkt der Generierung der Ausgabe einfach die DITA-OT-Option aus und AEM Guides verwenden das benutzerdefinierte DITA-OT-Plug-in, um die erforderliche Ausgabe zu generieren.

Wenn Sie Ant-Parameter beim Veröffentlichen einer Ausgabe verarbeiten möchten, können Sie dies mithilfe AEM Handbüchern einfach tun. Sie können angeben, welche Ant-Parameter Sie verwenden möchten und dieselben dann vom Veröffentlichungsprozess verarbeitet werden.

>[!NOTE]
>
> AEM Guides werden mit DITA-OT Version 3.3.2 geliefert. AEM Guides unterstützen jedoch DITA-OT Version 1.7 und höher. Eine vollständige Liste der DITA-OT-Versionen finden Sie unter [DITA-OT-Versionen](http://www.dita-ot.org/download).

>[!TIP]
>
> Siehe *DITA-OT-Profilkonfiguration* und *Verwenden benutzerdefinierter DITA-OT* Abschnitte des Best Practices-Handbuchs zu Best Practices für die Verwendung benutzerdefinierter DITA-OT-Plug-ins.

## Verwenden benutzerdefinierter DITA-OT-Plug-ins {#id181NH1020L7}

Es gibt zwei Möglichkeiten, das benutzerdefinierte DITA-OT-Plug-in für die Veröffentlichung zu verwenden. Die erste Methode besteht darin, das benutzerdefinierte DITA-OT-Plug-in in das AEM-Repository hochzuladen. Die andere Methode besteht darin, das benutzerdefinierte DITA-OT-Plug-in auf Ihrem Server zu speichern, ein Profil zu erstellen und den Speicherort des benutzerdefinierten DITA-OT-Plug-ins in Ihrem Profil anzugeben.

Standardmäßig enthalten AEM Guides ein vorkonfiguriertes Profil, das die Konfigurationen für die Standardvorlagen enthält, die zum Bearbeiten und Veröffentlichen von Inhalten verwendet werden sollen. Sie können benutzerdefinierte Profile mit benutzerdefinierten Vorlagen erstellen, die beim Bearbeiten von Dokumenten und benutzerdefinierten DITA-OT-Plug-ins zum Veröffentlichen von Inhalten verwendet werden.

Das standardmäßige DITA-OT-Paket, das mit AEM Guides verfügbar ist, wird mit dem Apache FOP XSL-FO-Prozessor geliefert, der das Rendering von MathML-Gleichungen nicht unterstützt. Wenn Sie MathML-Gleichungen in Ihrem Inhalt verwenden, stellen Sie sicher, dass Sie ein MathML-Rendering-Engine-Plug-in für Apache FOP integriert haben oder einen anderen XSL-FO-Prozessor verwenden.

>[!IMPORTANT]
>
> Wenn Sie AEM Guides von Version 2.2 auf 2.5.1 oder 2.6 aktualisiert haben, werden alle über den Konfigurationsmanager vorgenommenen Änderungen automatisch ausgewählt und im Standardprofil gespeichert.

Führen Sie die folgenden Schritte aus, um das benutzerdefinierte DITA-OT-Plug-in in das AEM-Repository hochzuladen:

1. Melden Sie sich bei AEM an und öffnen Sie den Modus CRXDE Lite .

1. Laden Sie die `DITA-OT.ZIP` -Datei.

   Der Speicherort der `DITA-OT.ZIP` Datei ist `/libs/fmdita/dita_resources/DITA-OT.zip`.

   ![](assets/dita-ot-zip-in-crx.png)

1. Extrahieren Sie den Inhalt der ZIP-Datei auf Ihrem Server.

1. Verwenden Sie einen DITA-OT-Plug-in-Integrationsmechanismus, um die neue Version von DITA-OT in Ihr benutzerdefiniertes DITA-OT-Plug-in zu integrieren.

   >[!NOTE]
   >
   > Das Klassenpfadtrennzeichen in der Plug-in-ZIP-Datei ist vom Betriebssystem abhängig. Wenn Ihr Server unter Windows gehostet wird, unterscheidet sich das Klassenpfadtrennzeichen von dem unter Linux verwendeten. Weitere Informationen zur manuellen Integration von Plug-ins finden Sie unter *Manuelles Installieren von Plug-ins* Thema in der DITA-OT-Dokumentation.

1. Erstellen Sie die ZIP-Datei erneut und behalten Sie dabei denselben Namen \(`DITA-OT.ZIP`\) und die Ordnerstruktur.

1. Laden Sie die aktualisierte ZIP-Datei wieder in das AEM-Repository hoch.

   Stellen Sie vor dem Hochladen der ZIP-Datei die folgenden Prüfungen sicher:

   - Führen Sie den Integrator \(zur Installation des benutzerdefinierten Plug-ins\) auf einem Mac/Linux-Betriebssystem aus, um Probleme mit Dateiseparatoren zu vermeiden. Da Windows und Linux OS unterschiedliche Dateiseparatoren haben, ist das in Mac/Linux OS integrierte Plug-in sowohl mit dem Windows- als auch dem Linux-Setup kompatibel.
   - Stellen Sie sicher, dass `DITA-OT.ZIP` enthält einen Ordner mit dem Namen &quot;DITA-OT&quot;, der alle relevanten Plug-ins und Dateien enthält.
   - Vergewissern Sie sich, dass `DITA-OT.ZIP` Die erstellte Datei hat mimeType: &quot;nt:file&quot; \(entspricht dem primären Typ der ZIP-Datei beim Hochladen in AEM\). Verwenden Sie ein WebDAV-Tool oder eine Codebereitstellung, um diese ZIP-Datei in den gewünschten Pfad in AEM hochzuladen. \(Verwenden Sie AEM Paketmanager nicht, um diese ZIP-Datei bereitzustellen, da diese ZIP kein AEM Inhaltspaket, sondern nur eine Archivdatei ist.\)

   >[!NOTE]
   >
   > Es wird empfohlen, das standardmäßige DITA-OT-Paket nicht zu überschreiben. Sie sollten Ihr benutzerdefiniertes DITA-OT-Paket mit Ihrem Plug-in an einem anderen Speicherort unter dem `apps` Ordner.

1. Öffnen Sie das standardmäßige DITA-Profil zur Bearbeitung und speichern Sie es \(ohne Aktualisierungen vorzunehmen\), damit die Änderungen wirksam werden.


Führen Sie die folgenden Schritte aus, um ein neues Profil zu erstellen und es so zu konfigurieren, dass das auf Ihrem Server gespeicherte benutzerdefinierte DITA-OT-Plug-in verwendet wird:

1. Speichern Sie das benutzerdefinierte DITA-OT-Plug-in auf Ihrem Server.

   >[!NOTE]
   >
   > Die Ordnerstruktur zum Speichern des benutzerdefinierten DITA-OT-Plug-ins sollte wie folgt lauten: `\*<parent-folder\>*\DITA-OT`.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools.

1. Klicken Sie auf **DITA-Profile** Kachel.

   >[!NOTE]
   >
   > Die Informationen zum Standardprofil werden auf der Seite Profile angezeigt. Wenn Sie AEM Guides von Version 2.2 auf 2.5.1 oder 2.6 aktualisiert haben, werden alle über den Konfigurationsmanager vorgenommenen Änderungen automatisch ausgewählt und im Standardprofil gespeichert.

1. Sie können das Standardprofil bearbeiten, ein neues Profil erstellen oder Einstellungen aus dem Standardprofil duplizieren, um ein neues Profil zu erstellen.

   >[!NOTE]
   >
   > Sie können das Standardprofil aktualisieren, es jedoch nicht löschen. Alle neuen Profile, die Sie erstellen, können jedoch bearbeitet und gelöscht werden.

1. Konfigurieren Sie die folgenden Eigenschaften für die Verwendung des benutzerdefinierten DITA-OT-Plug-ins:

   | Eigenschaftsname | Beschreibung |
   |-------------|-----------|
   | **Profileigenschaften** |
   | Profilname | Geben Sie einen eindeutigen Namen für dieses Profil an. |
   | Ausgabe wiederverwenden | *\(Optional\)* Wenn Ihr Profil auf einem vorhandenen Profil basiert, wählen Sie diese Option aus. Wenn Sie diese Option auswählen, wird sichergestellt, dass AEM Guides den Inhalt des DITA-OT-Pakets nicht erneut extrahieren und das vorhandene DITA-OT-Paket wiederverwenden. |
   | Profilextraktionspfad | *\(Optional\)* Geben Sie den Pfad an, unter dem DITA-OT auf der Festplatte gespeichert wird. Standardmäßig bündelt AEM Guides ein DITA-OT-Paket in seinem Repository und wird unter diesem Pfad auf dem Datenträger extrahiert.<br>**Hinweis** Sie können diesen Pfad mit einer beliebigen vorhandenen Systemvariable oder -eigenschaft definieren. Siehe Beschreibung [DITA-OT-Umgebungsvariablen](#id181NH0YN0AX) -Eigenschaft für weitere Informationen. |
   | Zugewiesener Pfad | \(*Optional*\) Geben Sie den Pfad in Ihrem Inhalts-Repository an, für den dieses Profil gilt. Sie können mehrere Orte angeben. |
   | **DITA-OT-Eigenschaften** |
   | DITA-OT-Timeout | \(*Optional*\) Geben Sie die Zeit \(in Sekunden\) an, für die AEM Guides auf eine Antwort vom DITA-OT-Plug-in warten. Wenn keine Antwort in der angegebenen Zeit empfangen wurde, beendet AEM Guides die Veröffentlichungsaufgabe und die Aufgabe wird als fehlgeschlagen gekennzeichnet. Außerdem werden die Fehlerprotokolle in der Protokolldatei zur Generierung der Ausgabe verfügbar gemacht. <br>Standardwert: 300 Sekunden \(5 Minuten\) |
   | DITA-OT-PDF-Argumente | Geben Sie die Befehlszeilenargumente an, die vom benutzerdefinierten DITA-OT-Plug-in zum Generieren der PDF-Ausgabe verarbeitet werden. Geben Sie für alle benutzerdefinierten DITA-OT-Profile das folgende Befehlszeilenargument an:`-lib plugins/org.dita.pdf2.fop/lib/` |
   | DITA-OT AEM Arguments | \(*Optional*\) Geben Sie die benutzerdefinierten Befehlszeilenargumente an, die vom benutzerdefinierten DITA-OT-Plug-in zum Generieren der AEM Site-Ausgabe verarbeitet werden. |
   | DITA-OT-Bibliothekspfade | \(*Optional*\) Geben Sie die zusätzlichen Bibliothekspfade des DITA-OT-Plug-ins an. |
   | DITA-OT Build XML | \(*Optional*\) Geben Sie den Pfad des benutzerdefinierten Ant-Build-Skripts an, das mit dem angepassten DITA-OT-Plug-in gebündelt wird. Dieser Pfad ist relativ zum DITA-OT-Ordner auf Ihrem Dateisystem. |
   | DITA-OT-Ant-Skript-Ordner | \(Optional\) Geben Sie den Pfad des Skriptordners DITA-OT Ant an. Dieser Pfad ist relativ zum DITA-OT-Ordner auf Ihrem Dateisystem. |
   | DITA-OT-Umgebungsvariablen | *\(Optional\)* Geben Sie Umgebungsvariablen an, die an den DITA-OT-Prozess übergeben werden sollen. Standardmäßig fügt AEM Guides vier Variablen hinzu: `ANT_OPTS`, `ANT_HOME`, `PATH`und `CLASSPATH`. <br> Sie können alle vorhandenen Systemumgebungsvariablen oder Eigenschaften zum Erstellen neuer Umgebungsvariablen wiederverwenden. Wenn Sie beispielsweise `JAVA_HOME` -Systemvariable, die in Ihrem System definiert ist, und Sie möchten eine neue Umgebungsvariable mit dem Namen `JAVA_BIN` , die mit `JAVA_HOME`. Anschließend können Sie die Definition von `JAVA_BIN` as:<br> `JAVA_BIN= ${JAVA_HOME}/bin` <br> **Hinweis** Sie können auch Java-Systemeigenschaften verwenden, um Umgebungsvariablen zu erstellen. Wenn AEM Startskript beispielsweise eine Java-Systemeigenschaft definiert `java.io.tmpdir` in einen temporären Ordner zu verweisen, können Sie diese Eigenschaft verwenden, um eine neue Variable wie folgt zu definieren: `${java.io.tmpdir}/fmdita/dita_ot`. <br> **Wichtig** Um eine vorhandene Systemvariable oder -eigenschaft wiederzuverwenden, muss sie in `${}`. |
   | DITA-OT-Ausgabe überschreiben | *\(Optional\)* Wenn diese Option aktiviert ist, können Sie das DITA-OT-Paket angeben, das auf Ihrem lokalen System verfügbar ist, um die Ausgabe mithilfe von DITA-OT zu generieren. Diese Konfiguration wird bei Aktivierung des ConfigManager festgelegt. <br> Wenn Sie den Pfad eines DITA-OT-Pakets angeben möchten, das auf AEM Server gespeichert ist, deaktivieren Sie diese Option. |
   | AEM DITA-OT-ZIP-Pfad/lokaler DITA-OT-Ordnerpfad | Geben Sie je nach Ihrer Auswahl in der DITA-OT-Ausgabe überschreiben den vollständigen Pfad an, in dem die benutzerdefinierte DITA-OT.zip-Datei gespeichert ist. Dies kann der Pfad in Ihrem AEM-Repository oder lokalen System sein. |
   | DITA-OT-Plug-in-Pfad | Pfad des benutzerdefinierten Plug-ins. Dieses Plug-in wird automatisch in das Haupt-DITA-OT-Paket integriert. |
   | Kataloge integrieren | \(*Optional*\) Pfad der benutzerdefinierten DTD- und XSD-catalog.xml-Dateien im AEM-Repository. Dies sollte nur bereitgestellt werden, wenn die Kataloge im DITA-OT-Paket fehlen. Diese Kataloge werden automatisch als Plug-in in das DITA-OT integriert. |
   | System-ID-Katalog hinzufügen | \(*Optional*\) Wählen Sie diese Option nur aus, wenn im Katalog fehlende Öffentliche ID-Einträge vorhanden sind oder die DITA-Dateien nur die System-IDs verwenden, die relativ zum Serverpfad sind, von dem aus sie hochgeladen werden. |
   | Temporärer DITA-OT-Pfad | *\(Optional\)* Geben Sie einen temporären Speicherort an, an den DITA-Dateien zur Verarbeitung kopiert werden. Bevor DITA-OT Dateien verarbeitet, werden sie an diesen temporären Speicherort kopiert. Standardmäßig lautet der Speicherort für temporäre Datenspeicherung: <br> **Hinweis** Sie können diesen Pfad mit einer beliebigen vorhandenen Systemvariable oder -eigenschaft definieren. Siehe Beschreibung [DITA-OT-Umgebungsvariablen](#id181NH0YN0AX) -Eigenschaft für weitere Informationen. |

   >[!NOTE]
   >
   >  Das Installationsprogramm für AEM Guides erstellt zwei Umgebungsvariablen, mit denen Sie den Pfad der benutzerdefinierten DITA-OT-Plug-in-Dateien angeben können. Diese Umgebungsvariablen sind: DITAOT\_DIR, das den Pfad des Ordners DITA-OT im Dateisystem enthält; und DITAMAP\_DIR, die den Pfad enthält, in den der DITA-Map-Inhalt im Dateisystem extrahiert wird.

1. Klicken **Fertig** , um das Profil zu speichern.


>[!NOTE]
>
> Sie können das benutzerdefinierte DITA-Profil als Paket exportieren und auf die anderen AEM Guides-Instanzen hochladen, um Zeit zu sparen. Weitere Informationen finden Sie unter [Anhang](appendix.md).

## Integrieren der DITA-Spezialisierung {#id211MB0E00XA}

Bei der DITA-Spezialisierung werden neue DITA-Strukturen erstellt, indem neue Elemente hinzugefügt oder vorhandene Elemente entfernt werden. Um ein neues DITA-Element zu erstellen, können Sie ein vorhandenes DITA-Element als Grundlage nehmen und es gemäß Ihren Authoring-Anforderungen ändern. Im Wesentlichen ermöglicht Ihnen die DITA-Spezialisierung die Erstellung benutzerdefinierter Informationsmodelle, die Ihren Geschäftsanforderungen entsprechen und gleichzeitig die Vorteile der vorhandenen DITA-Architektur erhalten.

Sie können die Profilfunktion verwenden, um benutzerdefinierte DITA-Spezialisierungseinstellungen zu speichern. Diese Einstellungen können dann zum Zeitpunkt der Bearbeitung und Veröffentlichung von benutzerdefinierten DITA-Inhalten verwendet werden. Mit AEM Guides können Sie die öffentliche ID und die System-ID in Ihren benutzerdefinierten DTDs/XSDs verwenden.

>[!NOTE]
>
> AEM Guides Web Editor unterstützt keine XSDs.

Führen Sie die folgenden Schritte aus, um ein neues Profil zu erstellen und es für die Verwendung spezialisierter DTDs und XSDs AEM Handbücher zu konfigurieren:

1. Erstellen Sie auf Ihrem lokalen Computer einen Spezialisierungsordner, der die spezialisierten DTDs und XSDs enthält.

1. Geben Sie die DTD-Details im `catalog.xml` -Datei, die auch im Spezialisierungsordner enthalten sein muss.

   >[!NOTE]
   >
   > Im Fall von DITA 1.3 ist der Standardspeicherort für DTD `catalog.xml` -Datei im AEM-Repository lautet: `/libs/fmdita/dita_resources/DITA-1.3/dtd/catalog.xml`.

1. Geben Sie die XSD-Details im `catalog.xml` -Datei, die auch im Spezialisierungsordner enthalten sein muss.

   >[!NOTE]
   >
   > Im Fall von DITA 1.3 lautet der Standardspeicherort für die XSD-Datei catalog.xml im AEM-Repository: `/libs/fmdita/dita_resources/DITA-1.3/xsd/catalog.xml`.

1. Laden Sie den Ordner an den folgenden Speicherort hoch:

   `/libs/fmdita/dita_resources`

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools.

1. Klicken Sie auf **DITA-Profile** Kachel.

   >[!NOTE]
   >
   > Die Informationen zum Standardprofil werden auf der Seite Profile angezeigt. Wenn Sie AEM Guides von Version 2.2 auf 2.5.1 oder 2.6 aktualisiert haben, werden alle über den Konfigurationsmanager vorgenommenen Änderungen automatisch ausgewählt und im Standardprofil gespeichert.

1. Sie können das Standardprofil bearbeiten, ein neues Profil erstellen oder Einstellungen aus dem Standardprofil duplizieren, um ein neues Profil zu erstellen.

   >[!NOTE]
   >
   > Das Standardprofil kann nicht gelöscht werden. Alle neuen Profile, die Sie erstellen, können jedoch bearbeitet und gelöscht werden.

1. Im **Schema** \> **Katalog** Einstellungen festlegen, geben Sie den Pfad der benutzerdefinierten DTD und XSD an `catalog.xml` -Dateien in Ihrem AEM-Repository.

1. Wählen Sie die **System-ID-Katalog hinzufügen** -Option.

   >[!NOTE]
   >
   > Wählen Sie diese Option nur aus, wenn im Katalog fehlende Öffentliche ID-Einträge vorhanden sind oder die DITA-Dateien nur die System-IDs verwenden, die relativ zum lokalen Dateipfad sind, von dem aus sie hochgeladen werden.

   Weitere Informationen zu anderen Eigenschaften auf der Seite &quot;Profile&quot;finden Sie in der Tabelle &quot;Eigenschaften&quot;unter [Schritt 6](#id17A9F0D075Z) des [Verwenden benutzerdefinierter DITA-OT-Plug-ins](#id181NH1020L7) Abschnitt.

1. Klicken **Fertig** , um das Profil zu speichern.


>[!NOTE]
>
> Sie können das benutzerdefinierte DITA-Profil als Paket exportieren und auf die anderen AEM Guides-Instanzen hochladen, um Zeit zu sparen. Weitere Informationen finden Sie unter [Anhang.md](appendix.md).

