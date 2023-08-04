---
title: AEM Umgebung für native PDF-Veröffentlichung konfigurieren
description: AEM Umgebung für native PDF-Veröffentlichung konfigurieren
exl-id: 40266ca0-0b0b-4418-b606-f70270addbaa
source-git-commit: 45dfe6078039001327e91ae85ea2a5beeacb2d59
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 1%

---

# AEM Umgebung für native PDF-Veröffentlichung konfigurieren

AEM Guides enthalten eine native PDF-Publishing-Engine, mit der Benutzer Inhalte im PDF-Format entwerfen, entwickeln und veröffentlichen können.

Es bietet die Möglichkeit, verschiedene Seitenlayouts und CSS-Vorlagen zu erstellen und die PDF-Vorlagen in Verbindung mit den Seitenlayouts und CSS zu entwerfen.

Die Schritte zum Konfigurieren dieser nativen PDF in AEM Guides unterscheiden sich je nach Betriebssystem. Führen Sie die folgenden Konfigurationsschritte basierend auf dem Betriebssystem aus, auf dem AEM installiert ist.

## Voraussetzungen

Mindestanforderungen für die Einrichtung der nativen PDF:

- Installierte Java Platform, Standard Edition 8 oder 11 JDK (Java SE Development Kit) und JRE (Java SE Runtime Environment)
- AEM 6.5 SP13, SP12, SP11 oder SP10
- Guides 4.1 und höher (UUID oder UUID)

Die native PDF-Publishing-Engine benötigt Oracle JDK, um die Knotenmodule im Ordner AEM crx-quickstart zu generieren. Standardmäßig werden die folgenden Betriebssysteme unterstützt:

- Windows 10, Windows 2019 Server und höher.
- Linux - (RHEL 8 und höher, CentOS 7 und höher, Ubuntu 18 und höher)
- Mac OS (Intel-basiert)

## Konfigurationsschritte für Windows Server (JAVA 11/8)

1. Stellen Sie sicher, dass AEM Server ausfällt.
2. Klicken Sie in der Windows-Taskleiste mit der rechten Maustaste auf das Windows-Symbol und wählen Sie System.
3. Klicken Sie im Fenster &quot;Einstellungen&quot;unter &quot;Verwandte Einstellungen&quot;auf Erweiterte Systemeinstellungen.
4. Klicken Sie auf der Registerkarte Erweitert auf Umgebungsvariablen .
5. Klicken Sie im Abschnitt Systemvariablen auf &quot;_Neu_&quot;, um eine neue Umgebungsvariable zu erstellen.
6. Geben Sie als Variablennamen JAVA_HOME ein.
7. Geben Sie im Wertefeld den Pfad zur Java-Installation an und klicken Sie auf OK.

   Beispiel:

   JAVA 11

   C:\Program Files\JAVA\jdk-11.0.15.1

   JAVA 8

   C:\Program Files\JAVA\ jdk1.8.0_144

8. Fügen Sie Pfad aus Systemvariablen hinzu und klicken Sie auf Bearbeiten.

9. Jetzt geben die Pfadvariablen den Wert des Serverpfads an und klicken auf OK.

   Beispiel:

   JAVA 11

   %JAVA_HOME%\bin\server\

   JAVA 8

   %JAVA_HOME%\jre\bin\server\

10. Klicken Sie erneut im Dialogfeld Umgebungsvariablen auf &quot;OK&quot;.
11. Klicken Sie erneut auf &quot;OK&quot;im Dialogfeld &quot;Systemeigenschaften&quot;.
12. Starten Sie nun den AEM-Server.
13. Erstellen Sie nativen PDF aus Vorgaben im Web-Editor.

## Konfigurationsschritte für Linux-Server (RHEL7/centOS 7)

1. Stellen Sie sicher, dass der AEM Server ausfällt.
2. Überprüfen Sie die Variable JAVA_HOME , indem Sie echo $JAVA_HOME ausführen.
3. Wenn die Variable JAVA_HOME nicht festgelegt ist, führen Sie Schritt 4 aus. Wechseln Sie andernfalls direkt zu Schritt 5.
4. Variable JAVA_HOME mithilfe der folgenden Befehle festlegen, die auf der installierten Java-Version basieren

   Beispiel:

   JAVA 11

   1. export JAVA\_HOME=/usr/lib/jvm/java-11.0.15.1
   2. export PATH=$PATH: $JAVA\_HOME/bin
   3. export LD\_LIBRARY\_PATH=/usr/lib/jvm/jdk-11.0.15.1/lib/server:/usr/java/jdk-11.0.15.1/lib/server

   JAVA 8

   1. export JAVA\_HOME=/usr/lib/jvm/java-11.0.15.1
   2. export PATH=$PATH: $JAVA\_HOME/bin

5. Starten Sie AEM Server neu und wechseln Sie zu Schritt 12, wenn Sie Guides der Version 4.2 und höher verwenden.
6. Kopieren Sie &quot;_node_modules.zip_&quot; am Ende dieses Artikels an das Verzeichnis crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166/ angehängt.
7. Öffnen Sie das Terminal im Verzeichnis crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166/.
8. Löschen Sie den Ordner &quot;node_modules&quot;mithilfe des folgenden Befehls

   **rm -rf node_modules**

9. Entpacken Sie node_modules.zip mithilfe des folgenden Befehls

   **unzip node_modules.zip**

10. Wenn der Befehl &quot;Entpacken&quot;nicht installiert/erkannt wurde, kann er mit folgendem Befehl installiert werden

   **yum install unzip**

11. Installieren Sie das Paket fontconfig .
Befehl: yum install fontconfig
12. Erstellen Sie nativen PDF aus Vorgaben im Web-Editor.

**NOTE** : Das Paket node_modules.zip kann heruntergeladen werden. [here](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:295d8f03-41e1-429b-8465-2761ce3c2fb3).

Der manuelle Import der heruntergeladenen Knotenmodule für das Linux-Betriebssystem ist eine Problemumgehung für Benutzer, die sich in Guides 4.1 oder früheren Versionen befinden (Schritt 6-12).

## Konfigurationsschritte für den Mac-Computer (JAVA 11/8)

1. Installieren Sie Oracle JAVA 11 oder Oracle JAVA 8.
2. Setzen Sie die Umgebungsvariable JAVA_HOME auf den installierten JAVA-Ordner.
3. Öffnen Sie eine Unix-Shell.
(Hier wird der Bash zum Einrichten der Konfiguration verwendet.)

   Befehl: nano ~/.bashrc

4. Variable JAVA_HOME mithilfe der folgenden Befehle festlegen, die auf der installierten Java-Version basieren

   Beispiel:

   JAVA 11

   export JAVA\_HOME= /Library/Java/JavaVirtualMachines/jdk-11.0.15.1.jdk/Contents/Home

5. Grundlinie neu laden

   Befehl: source ~/.bashrc.

6. Stellen Sie sicher, dass JAVA_HOME mit dem Befehl echo $JAVA_HOME eingestellt ist.

7. Führen Sie die folgenden drei Befehle aus AEM Installationspfad aus.

   C:/{aem-installation-folder}/crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166

   i) Suchen Sie . -type d -exec chmod 0755 {} \; ii) finden Sie . -Typ f -exec chmod 0755 {} \; iii) .node-darwin/lib/node_modules/npm/bin/npm-cli.js —prefix . install —unsafe-perm —scripts-prepend-node-path

8. Überprüfen Sie mithilfe des folgenden Befehls, ob Java installiert ist.

   i) Ausführen **./node-darwin/bin/node** Befehl aus dem Ordner /crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166

   ![Mac](../assets/publishing/mac.png)

   ii) a = require(&#39;java&#39;)

9. Installieren Sie das Paket fontconfig .
Befehl: apt install fontconfig

10. Erstellen Sie nativen PDF aus Vorgaben im Web-Editor.

## Fehlerbehebung

Im Folgenden finden Sie die häufigen Fehler, die während der PDF-Erstellung auftreten können, wenn Umgebungsvariablen nicht ordnungsgemäß festgelegt sind.

### Nullzeiger-Ausnahme in Windows/Mac OS

![Null-Zeiger-Ausnahme](../assets/publishing/null-pointer-exception.png)

Wenn das Problem auch nach der Korrektur der Java-Umgebungseinstellungen weiter besteht, überprüfen Sie Folgendes erneut:

1. Überprüfen Sie, ob die Ausgabevorgabe richtig definiert ist, oder erstellen Sie eine neue Ausgabevorgabe ohne Leerzeichen.

2. Überprüfen Sie das Verzeichnis der Knotenressourcen unter /libs/fmdta/node_resources , um sicherzustellen, dass alle erforderlichen Bibliotheken während der Installation installiert sind.

### Fehlende Bibliotheken in RHEL 7 Linux OS

![fehlende Bibliotheken](../assets/publishing/missing-libraries.png)

### Zeitüberschreitung beim Veröffentlichungsprozess. Der Prozess wurde nicht in der angegebenen Zeit von 0ms abgeschlossen.

![Veröffentlichungs-Prozess-Timeout](../assets/publishing/publish-process-timeout.png)

Überprüfen Sie den Wert der Zeitüberschreitungseigenschaft für den Knoten nodejs in /var/dxml/profiles/b1aad0a7-9079-e56c-1ed8-6fcababe8166/nodejs im CRX-Repository. Der Standardwert ist 300.



Wenn bei der Durchführung eines der oben genannten Schritte Probleme auftreten, posten Sie Ihre Frage in der AEM Guides-Community. [Forum](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation) Hilfe.
