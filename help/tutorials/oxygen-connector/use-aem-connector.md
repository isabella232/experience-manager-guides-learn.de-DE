---
title: Sauerstoff-Plug-in für Adobe Experience Manager-Handbücher
description: Erfahren Sie, wie Sie mit dem Oxygen-Plug-in für Adobe Experience Manager-Handbücher Inhalte erstellen und verwalten können.
hide: true
hidefromtoc: true
exl-id: 2db9a34e-2efa-47ad-ba6b-02afc5197669
source-git-commit: 23c1dfb405643bd9f5906807dddc4fff3f2e8535
workflow-type: tm+mt
source-wordcount: '6120'
ht-degree: 0%

---


# Sauerstoff-Plug-in für Adobe Experience Manager-Handbücher {#id1645H6010Q5}

Mit dem Sauerstoff-Plug-in für Adobe Experience Manager-Handbücher \(später als &quot;Sauerstoff-Plug-in für AEM Guides&quot;im Handbuch\) können Sie die XML-Autoreninstanz mit dem Adobe Experience Manager \(AEM\)-Repository verbinden, um Inhalte zu erstellen und zu verwalten. Mit dem Plug-in können Sie Dateien durchsuchen, durchsuchen und öffnen, Dateien auschecken und einchecken sowie Ordner und Dateien in AEM Repository hochladen. Mit dem Bedienfeld &quot;AEM Guides&quot;in der Desktop-Applikation können Sie die gewünschten Ordner \(aus AEM Repository\) zur Liste der bevorzugten Ordner markieren, damit Sie schnell darauf zugreifen können. Darüber hinaus können Sie ein Paket in AEM Web-Oberfläche installieren und Ihre DITA-Dateien in der Oxygen XML Author direkt über die AEM Web-Oberfläche öffnen.

## Herunterladen und installieren {#id1826M0L0PUI}

Das Sauerstoff-Plugin für AEM Guides wird über Ihr Adobe Software Distribution-Portal bereitgestellt. Suchen Sie auf der Registerkarte &quot;Experience Manager&quot;nach &quot;Sauerstoff&quot;und laden Sie dann das Plug-in-Installationsprogramm von Ihrem [Adobe Software Distribution-Portal](https://experience.adobe.com/#/downloads/content/software-distribution/en/general.html).

>[!NOTE]
>
>Überprüfen Sie in den Versionshinweisen für die jeweiligen Adobe Experience Manager-Handbücher auf die Kompatibilität der Adobe-Connector-Version.

Nachdem Sie das Installationsprogramm installiert haben, installieren Sie es auf Ihrem lokalen Computer, auf dem die Oxygen XML Author installiert ist. Bevor Sie mit der Installation beginnen, müssen Sie sicherstellen, dass Ihr System die technischen Anforderungen für die Installation des Oxygen Plugins für AEM Guides erfüllt.

### Technische Anforderungen

- Sauerstoff-XML-Autorenversion 25.1

- Adobe Experience Manager-Handbücher Version 4.3 oder höher

- Adobe Experience Manager-Version 6.5 mit Service Pack 14, 15, 16 und 17

- Von Oxygen XML Author Version 25.1 unterstütztes Betriebssystem

- Java Development Kit
   - Oracle SE 8 JRE 1.8

### Installieren des Plug-ins unter Windows

>[!IMPORTANT]
>
>Wenn Sie eine ältere Version des Plug-ins auf Ihrem System installiert haben, stellen Sie sicher, dass Sie es deinstallieren, bevor Sie den Installationsprozess starten. Siehe **Deinstallieren von Paketen** im Abschnitt [Arbeiten mit Paketen](https://helpx.adobe.com/de/experience-manager/6-4/sites/administering/using/package-manager.html) Artikel für Anweisungen zur Deinstallation.

Führen Sie die folgenden Schritte für das System aus, auf dem Oxygen XML Author installiert ist:

1. Starten des Installationsprogramms `.exe` -Datei.

   Der Willkommensbildschirm des Installationsassistenten wird angezeigt.

1. Klicks **Nächste** und navigieren Sie zu dem Speicherort, an dem die .exe-Datei der Oxygen XML Author verfügbar ist.

1. Wählen Sie die Datei aus und klicken Sie auf **Öffnen**.

   Der Speicherort der ausgewählten Datei wird im Installationsassistenten hinzugefügt.

1. Klicken Sie auf **Weiter**.

1. Klicken Sie auf **Installieren**.

1. Klicks **Beenden** um den Installationsassistenten zu schließen.
1. Starten Sie die XML-Autoreninstanz Oxygen.

   Das Bedienfeld AEM Guides wird im XML-Autor von Sauerstoff angezeigt.

   ![AEM](images/oxygen-aem-connector.png){width="800" align="left"}

   >[!NOTE]
   >
   >Wenn das Bedienfeld AEM Guides nicht angezeigt wird, finden Sie die Problemumgehungen im Abschnitt zur Fehlerbehebung .—[Bedienfeld AEM Guides fehlt](#id192BH200ZAX).


### Installieren des Plug-ins in Mac

>[!IMPORTANT]
>
>Wenn Sie eine ältere Version des Plug-ins auf Ihrem System installiert haben, stellen Sie sicher, dass Sie es deinstallieren, bevor Sie den Installationsprozess starten. Siehe **Deinstallieren von Paketen** im Abschnitt [Arbeiten mit Paketen](https://helpx.adobe.com/de/experience-manager/6-4/sites/administering/using/package-manager.html) Anweisungen zur Deinstallation des Artikels.

Führen Sie die folgenden Schritte für das System aus, auf dem Oxygen XML Author installiert ist:

1. Suchen Sie die .dmg-Datei des Plug-ins auf Ihrem System.

1. Doppelklicken Sie auf die Datei &quot;.dmg&quot;, um den Dateiinhalt zu öffnen.

   Die .dmg-Datei enthält einen Ordner aem-connector-x.x und eine Datei aem-connector-x.x-setup .

   >[!NOTE]
   >
   >x.x in den Dateinamen ist die Versionsnummer des Plug-ins.

1. Kopieren Sie den Ordner aem-connector-x.x in den Ordner plugins von Oxygen XML Author.
1. Doppelklicken Sie auf die Datei aem-connector-x.x-setup , um das Installationsprogramm zu starten.

1. Starten Sie die XML-Autoreninstanz Oxygen.

   Das Bedienfeld AEM Guides wird im XML-Autor von Sauerstoff angezeigt.

   ![AEM Connector Mac](images/oxygen-aem-connector-mac.png) {width="800" align="left"}

   >[!NOTE]
   >
   >Wenn das Bedienfeld AEM Guides nicht angezeigt wird, finden Sie die Problemumgehungen im Abschnitt zur Fehlerbehebung .—[Bedienfeld AEM Guides fehlt](#id192BH200ZAX).


### Installieren Sie das Paket für die Aktivierung der Dokumentbearbeitungsfunktion über AEM Web-Oberfläche {#id182CE0Q0TY4}

Als Autor können Sie Ihre DITA-Maps oder -Themen in der Oxygen XML Author direkt über die AEM Web-Oberfläche öffnen und bearbeiten. Um diese Funktion in AEM Web-Oberfläche zu aktivieren, muss Ihr AEM-Administrator ein Paket in Ihrer AEM-Authoring-Instanz installieren.

Als AEM Administrator führen Sie die folgenden Schritte aus, um das Paket zu installieren:

1. Rufen Sie die ZIP-Datei des Pakets von Ihrem IT-Team ab.
1. Melden Sie sich bei Ihrer AEM an *\(als Administrator\)* und navigieren Sie zum CRX Package Manager. Die Standard-URL für den Zugriff auf den Paketmanager lautet

   `http://<server name>:<port>/crx/packmgr/index.jsp`

   Der Package Manager verwaltet die Pakete in Ihrer lokalen AEM-Installation. Weitere Informationen zum Arbeiten mit Package Manager finden Sie unter [Arbeiten mit Paketen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developer-tools/package-manager.html?lang=en) in AEM Dokumentation.

   ![Package Manager](images/package-manager.png) {width="650" align="left"}

1. Um das Sauerstoffpaket hochzuladen, klicken Sie auf **Paket hochladen**.
1. Navigieren Sie im Dialogfeld &quot;Paket hochladen&quot;zur Sauerstoffpaketdatei, die Sie in Schritt 1 heruntergeladen haben, und klicken Sie auf OK.

   Das Paket wird in Ihre AEM-Instanz hochgeladen.

1. Um den Installationsprozess zu starten, klicken Sie auf **Installieren**.

   ![Sauerstoffverpackung](images/oxygen-package.png){width="650" align="left"}

1. Klicken Sie im Dialogfeld Paket installieren auf **Installieren**.
1. Klicken Sie nach Abschluss der Installation auf die Schaltfläche Home in der oberen linken Ecke des CRX Package Manager.
1. Wählen Sie eine DITA-Datei im Ordner &quot;Assets&quot;aus.

   **In Sauerstoff bearbeiten** ist in der Symbolleiste verfügbar. Weitere Informationen zur Verwendung dieser Option finden Sie unter [Öffnen Sie das DITA-Thema in der Oxygen XML Author über AEM Web-Oberfläche.](#id182CE0I905Z).

   >[!NOTE]
   >
   >Die **In Sauerstoff bearbeiten** angezeigt, wenn Sie ein DITA-Thema auswählen. Wenn Sie mehrere Themen auswählen, ist die Option nicht sichtbar.


## Konfigurieren des Sauerstoffplugins für AEM Guides {#id1826KF00AHS}

Nachdem Sie das Plug-in heruntergeladen und installiert haben, müssen Sie Folgendes konfigurieren, damit es mit dem Plug-in funktioniert:

- **Webauthentifizierungseinstellungen**: Einstellungen für die SSO-Authentifizierung im Plug-in für AEM Handbücher.
- **Allgemeine Einstellungen**: Verbindungsparameter für das Plug-in, z. B. AEM Server-URL, Anmeldedaten usw.
- **Voreinstellung für die Profilattributanpassung und Dateinamen in Querverweisen**: Diese Konfiguration ist für die Profilattributschemata für die Dokumentationssätze erforderlich.

### Webauthentifizierungseinstellungen

JxBrowser wird für die SSO-Authentifizierung durch das Oxygen-Connector-Plug-in verwendet. Es handelt sich um einen Chromium-basierten Browser. Für Java 9+ ist der Zugriff auf nicht öffentliche APIs erforderlich und Sie müssen diesen Zugriff explizit auf JxBrowser gewähren. Weitere Informationen finden Sie unter [JxBrowser-Fehlerbehebung](https://jxbrowser-support.teamdev.com/docs/guides/troubleshooting/issues.html).

Aktualisieren Sie die angegebenen Dateien, um die Web-Authentifizierungseinstellungen im Oxygen-Plug-in für AEM Guides zu konfigurieren:

>[!NOTE]
>
>Erstellen Sie eine Sicherungskopie der Datei, bevor Sie sie aktualisieren.

**Für Mac und Sauerstoff 25.1**

Fügen Sie die folgenden Zeilen in env.sh hinzu:

```java
--illegal-access=permit\
--add-opens=java.desktop/javax.swing.plaf.basic=ALL-UNNAMED\
--add-exports=javafx.controls/com.sun.javafx.scene.control=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.stage=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED\
--add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED\
--add-opens=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED\
--add-opens=javafx.graphics/javafx.stage=ALL-UNNAMED\
--add-opens=javafx.graphics/com.sun.javafx.tk.quantum=ALL-UNNAMED\
--add-exports=java.desktop/sun.awt=ALL-UNNAMED\
--add-opens javafx.swing/javafx.embed.swing=ALL-UNNAMED
```

Fügen Sie die folgenden Zeilen in die Datei SauerstoffAuthor.sh ein.

```java
-Djdk.module.illegalAccess=permit\-Djava.ipc.external=true\
```

**Windows und Sauerstoff 25.1**

Fügen Sie die folgenden Zeilen in env.bat hinzu

```java
--illegal-access=permit --add-opens=java.desktop/javax.swing.plaf.basic=ALL-UNNAMED --add-exports=javafx.controls/com.sun.javafx.scene.control=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.stage=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --add-opens=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --add-opens=javafx.graphics/javafx.stage=ALL-UNNAMED --add-opens=javafx.graphics/com.sun.javafx.tk.quantum=ALL-UNNAMED --add-exports=java.desktop/sun.awt=ALL-UNNAMED --add-opens javafx.swing/javafx.embed.swing=ALL-UNNAMED
```

Fügen Sie die folgenden Zeilen in die Datei SauerstoffAuthor.bat ein

```java
-Djdk.module.illegalAccess=permit -Djava.ipc.external=true
```

>[!NOTE]
>
>Als Administrator müssen Sie Sauerstoff von SauerstoffAuthor.sh für Mac und SauerstoffAuthor.bat für Windows ausführen.

### Allgemeine Einstellungen

Führen Sie die folgenden Schritte aus, um die Verbindungseinstellungen im Sauerstoff-Plug-in für Adobe Experience Manager-Handbücher zu konfigurieren:

1. Klicken Sie im Bedienfeld AEM Guides auf das Einstellungssymbol und wählen Sie dann **Einstellungen**.

   ![Verbindungsparameter ](images/settings.png){width="800" align="left"}

1. Geben Sie die folgenden Details an:
   - **Server-URL**: URL des AEM-Servers, beispielsweise:

     ```http
     http[s]://<host>:<port>
     ```

     Geben Sie in der obigen URL den Hostnamen und Port des Servers an, auf dem AEM Server bereitgestellt wird.

     >[!IMPORTANT]
     >
     >Wenn Ihr AEM-Server an Port 80 oder 443 bereitgestellt wird, müssen Sie ihn nicht in der URL angeben.

   - **Authentifizierung:** Wählen Sie aus **Einfach \(Benutzername/Kennwort\)** oder **Webauthentifizierung**. Wenn Sie **Allgemein** Authentifizierung müssen Sie die **Benutzername** und **Passwort** im Dialogfeld &quot;Voreinstellungen&quot;.

     Wenn Sie Webauthentifizierung auswählen, wird der Bildschirm AEM Anmeldung angezeigt. Geben Sie Ihre Anmeldedaten ein und klicken Sie auf **Anmelden** Schaltfläche. Bei erfolgreicher Anmeldung wird der Bildschirm AEM Anmeldung geschlossen und im Bedienfeld AEM Handbücher wird die Dateiliste vom AEM-Server angezeigt.

   - **Verbindungs-Timeout**: Geben Sie die Zeit in Sekunden an, die der Client auf eine Antwort vom AEM-Server wartet. Wenn innerhalb der angegebenen Zeit keine Antwort vom Server empfangen wird, wird die Anfrage beendet. Der Standardwert ist 20 Sekunden.

   - **Lokaler Ordner**: Speicherort auf Ihrem lokalen Computer, an dem die Dateien aus AEM Repository nach dem Auschecken gespeichert werden. Wenn Sie einen Speicherort angeben, der nicht auf dem Laufwerk vorhanden ist, erstellt das Plug-in diesen Speicherort.
   - **Datei beim Auschecken öffnen**: Wenn diese Option aktiviert ist, werden die Dateien beim Auschecken geöffnet.
   - **Datei beim Einchecken schließen**: Wenn ausgewählt, werden die Dateien beim Einchecken geschlossen. Vor dem Schließen der Datei wird ein Popup angezeigt, in dem Sie die Versionskommentare angeben können.
   - **Dialogfeld &quot;Einchecken&quot;beim Schließen der Datei anzeigen**: Wenn diese Option aktiviert ist, wird beim Schließen einer Datei ein Popup-Fenster angezeigt. Im Popup-Fenster können Sie auswählen, ob Sie die Datei einchecken oder die Datei schließen möchten, ohne sie einzuchecken.
   - **Datei für automatisches Auschecken beim Öffnen**: Wenn diese Option aktiviert ist, wird sie durch Doppelklicken auf eine Datei automatisch ausgecheckt und zur Bearbeitung geöffnet. Wenn die Datei bereits ausgecheckt ist, wird sie einfach zur Bearbeitung geöffnet. Wenn diese Option nicht ausgewählt ist, wird eine Datei, für die Sie keine Sperre haben, im schreibgeschützten Modus geöffnet.
1. Klicken Sie auf **OK**.

### Voreinstellung für die Profilattributanpassung und Dateinamen in Querverweisen {#id1827K0D0OHT}

Sie müssen die Voreinstellungen in der Oxygen XML Author konfigurieren, um das Profilattribut zu verwenden, das den DITA-Themen im AEM Repository zugeordnet ist. Außerdem müssen Sie die Voreinstellung so konfigurieren, dass Dateinamen anstelle von GUIDs in den Querverweisen angezeigt werden.

Führen Sie die folgenden Schritte aus, um Profilattribute und Querverweise zu konfigurieren:

1. Klicken Sie in Oxygen XML Author auf **Optionen** \> **Voreinstellungen**.
1. Im **Dokumenttyp-Zuordnung** Registerkarte auswählen **DITA** und klicken Sie anschließend auf **Erweitern**.

   ![Dokumenttyp-Zuordnung](images/document_type_association.png){width="650" align="left"}

1. Im **Klassenpfad** Wählen Sie com.adobe.o2.connector im **Übergeordnete Klassenlader vom Plug-in mit ID verwenden** angezeigt.

   ![Registerkarte &quot;Klassenpfad&quot;](images/dita-extension.png){width="650" align="left"}

1. Im **Erweiterungen** -Tab, nehmen Sie die folgenden Änderungen vor:
   - Klicks **Auswählen** neben dem **Listener für Autorenerweiterungsstatus** under **Individuelle Erweiterungen** und wählen Sie CustomAuthorExtensionStateListener - com.adobe.o2.framework.extn im **Klasse** Liste. Klicken Sie auf **OK**.
   - Klicks **Auswählen** neben dem **Autor des benutzerdefinierten Attributwert-Editors** under **Individuelle Erweiterungen** und wählen Sie CustomValueEditor - com.adobe.o2.framework.extn im **Klasse** Liste. Klicken Sie auf **OK**.
Der folgende Screenshot zeigt die konfigurierte **Erweiterung** Registerkarte für DITA-Themen:

     ![Konfigurierte Erweiterung für DITA-Themen](images/dita-topic-extension-tab.png){width="650" align="left"}

   - Klicks **Auswählen** neben dem **Erweiterungspaket** und wählen Sie LinkResolverExtensionBundle - com.adobe.o2.framework.extn im **Klasse** Liste. Klicken Sie auf **OK**.

     ![Konfigurierte Erweiterung für DITA-Themen](images/dita-map-extenstion-link-resolve.png) {width="650" align="left"}


1. Klicks **OK** in allen Dialogfeldern, um Ihre Änderungen zu speichern.

### Konfigurieren der DITA Map-Erweiterung

Die Konfiguration der DITA-Map-Erweiterung ist erforderlich, um das Öffnen von Zuordnungsdateien in der Oxygen XML-Autoreninstanz direkt über die AEM Web-Oberfläche zu ermöglichen. Diese Konfigurationen ähneln den Konfigurationen für Profilattribute, die im vorherigen Verfahren vorgenommen wurden.

Führen Sie die folgenden Schritte aus, um die DITA Map-Erweiterung zu konfigurieren:

1. Klicken Sie in Oxygen XML Author auf **Optionen** \> **Voreinstellungen**.
1. Im **Dokumenttyp-Zuordnung** Registerkarte auswählen **DITA Map** und klicken Sie anschließend auf **Erweitern**.
1. Im **Klassenpfad** Wählen Sie com.adobe.o2.connector im **Übergeordnete Klassenlader vom Plug-in mit ID verwenden** angezeigt.
1. Im **Erweiterungen** -Tab, nehmen Sie die folgenden Änderungen vor:
1. 
   - Klicks **Auswählen** neben dem **Listener für Autorenerweiterungsstatus** under **Individuelle Erweiterungen** und wählen Sie CustomDITAMapAuthorExtensionStateListener - com.adobe.o2.framework.extn im **Klasse** Liste. Klicken Sie auf **OK**.
- Klicks **Auswählen** neben dem **Autor des benutzerdefinierten Attributwert-Editors** under **Individuelle Erweiterungen** und wählen Sie CustomValueEditor - com.adobe.o2.framework.extn im **Klasse** Liste. Klicken Sie auf **OK**.
- *\(Optional\)* Wenn Sie beim Öffnen einer Zuordnungsdatei keine Verweise auflösen möchten, müssen Sie die folgende zusätzliche Konfiguration durchführen:

  Klicks **Auswählen** neben dem **Referenzen-Resolver** under **Individuelle Erweiterungen** und wählen Sie CustomDITAMapReferenceResolver - com.adobe.o2.framework.extn im **Klasse** Liste. Klicken Sie auf **OK**.

  Der folgende Screenshot zeigt die konfigurierte **Erweiterung** tab:

  ![Konfigurierte Erweiterung für DITA Map](images/dita-map-extension-tab.png){width="650" align="left"}

1. Klicks **OK** in allen Dialogfeldern, um Ihre Änderungen zu speichern.

## Arbeiten mit dem Sauerstoff-Plug-in für AEM Guides {#id1826JG00WY4}

### Bedienfeld &quot;AEM Guides&quot;

Der folgende Bildschirm zeigt das Bedienfeld AEM Guides .

![Connector-Bereich](images/connector-panel.png){width="550" align="left"}

**A**\) Zeigt die Suchleiste an.

**B**\) Zeigt den Ordner Favoriten an. Standardmäßig ist sie leer. Sie können Ordner aus dem AEM-Repository als Favoriten hinzufügen. Die bevorzugten Ordner werden hier angezeigt.

**C**\) Der DAM-Ordner zeigt das AEM Repository an. Sie können die Ordneransicht erweitern und reduzieren.

**D**\) Das Symbol Einstellungen \(Zahnrad\) mit den folgenden Optionen:

- **Verbinden**: Wählen Sie diese Option, um eine Verbindung zum AEM-Server herzustellen. Die Option ist deaktiviert, wenn die XML-Autoreninstanz mit dem AEM Server verbunden ist.
- **Aktualisieren**: Wählen Sie diese Option, um den aktuellen Status der Dateien und Ordner aus dem AEM Repository abzurufen.

  >[!NOTE]
  >
  >Achten Sie darauf, die Dateien zu speichern, bevor Sie sie aktualisieren. Wenn Sie **Aktualisieren** -Option, erhalten Sie eine Warnung, um Ihre Dateien zu speichern, bevor Sie sie aktualisieren. Wenn Sie Ihre Dateien nicht gespeichert haben, können Sie auf **Abbrechen** und speichern Sie sie.

- **Einstellungen**: Sie können diese Option verwenden, um das Dialogfeld &quot;Allgemeine Voreinstellungen&quot;des Plug-ins zu öffnen.
- **Abmelden**: Wählen Sie diese Option, um die AEM Serververbindung zu schließen. Diese Option ist nur verfügbar, wenn Sie den Webauthentifizierungsmodus verwenden.

### Kontextmenüfunktionen

Die Funktionen des SauerstoffPlugins für AEM Guides sind verfügbar, wenn Sie mit der rechten Maustaste auf einen Ordner oder eine Datei im AEM-Repository klicken. Die für die Ordner verfügbaren Funktionen unterscheiden sich von den Dateien. Im Folgenden finden Sie eine vollständige Liste der Funktionen im Oxygen Plugin für AEM Guides-Kontextmenü:

- **Öffnen**: Öffnet die ausgewählte Datei oder erweitert den ausgewählten Ordner.
- **Öffnen in**: Sie können die ausgewählte Datei im Web Editor für AEM Handbücher, im Map Dashboard oder im Map Editor öffnen. Weitere Informationen zu diesen Optionen finden Sie unter [Öffnen Sie die Datei im Editor AEM Guides .](#id195GH0V30KX).
- **Auschecken**: Prüft eine Datei aus AEM Repository. Weitere Informationen finden Sie unter [Auschecken von Dateien](#id195HC020TS4).
- **Checkout mit abhängigen Elementen**: Prüft eine Datei mit ihren direkten Verweisen. Weitere Informationen finden Sie unter [Auschecken von Dateien](#id195HC020TS4).
- **Checkout mit schreibgeschützten abhängigen Elementen**: Prüft die ausgewählte Datei mit den abhängigen Elementen. Sie können keine Änderungen an den abhängigen Dateien vornehmen. Weitere Informationen finden Sie unter [Auschecken von Dateien](#id195HC020TS4).
- **Abbrechen des Auscheckens**: Bricht die ausgecheckte Datei ab, schließt die Datei aus dem Editor und setzt die Änderungen auf die letzte Version der auf dem Server gespeicherten Datei zurück.
- **Aktualisieren**: Ruft bei einer Datei die neueste Kopie der Datei aus dem AEM-Repository ab. Für einen Ordner ruft er die Ordnerstruktur und den Status der Datei ab. Das bedeutet, dass eine Datei hinzugefügt wird und sie dann in der AEM Guides-Ansicht angezeigt wird. Wenn eine Datei auf AEM Server ausgecheckt wurde, zeigt die Aktualisierung in der Sauerstoffverfassungs-Autoreninstanz die Datei als ausgecheckt an. Dies aktualisiert jedoch nicht die Dateiliste im *In AEM Handbüchern ausgecheckte Dateien* Ansicht.
- **Ausgecheckte Dateien aktualisieren**: Aktualisiert die Liste der ausgecheckten Dateien im *In AEM Handbüchern ausgecheckte Dateien* Ansicht. Wenn eine Datei auf AEM Server ausgecheckt wurde, wird durch eine Aktualisierung die Liste der ausgecheckten Dateien im *In AEM Handbüchern ausgecheckte Dateien* Ansicht. Wenn jedoch eine neue Datei hinzugefügt wurde oder sich der Status einer Datei geändert hat, wird sie nicht in der Baumstruktur der AEM Guides aktualisiert. Um den Status von Dateien auf AEM zu aktualisieren, müssen Sie eine Aktualisierung durchführen.
- **Einchecken**: Prüft eine Datei, die Sie ausgecheckt haben. Weitere Informationen finden Sie unter [Einchecken einer Datei](#id182CF0J0FHS).
- **Einchecken mit abhängigen Elementen**: Wenn Sie Dateien mit abhängigen Elementen ausgecheckt haben, checkt diese Option die Hauptdatei zusammen mit den abhängigen Elementen ein. Weitere Informationen finden Sie unter [Einchecken einer Datei](#id182CF0J0FHS).
- **Ordner erstellen**: Erstellt einen Ordner im AEM-Repository. Diese Option ist nur auf Ordnerebene verfügbar.
- **Datei hochladen\(en\)**: Lädt einzelne oder mehrere Dateien hoch. Weitere Informationen finden Sie unter [Dateien und Ordner hochladen](#id195HC03F03J).
- **Hochladen mit abhängigen Elementen**: Lädt DITA-Dateien \(XML, DITA, Book Map oder DITA Map\) mit den abhängigen Elementen hoch. Weitere Informationen finden Sie unter [Dateien und Ordner hochladen](#id195HC03F03J).
- **Ordner hochladen**: Lädt einen Ordner in das AEM-Repository hoch. Weitere Informationen finden Sie unter [Dateien und Ordner hochladen](#id195HC03F03J).
- **Zu Favoriten hinzufügen**: Fügt einen Ordner zum *Favoriten* Ordner im Bedienfeld &quot;AEM Guides&quot;. Es wird empfohlen, Ihren Arbeitsordner hier hinzuzufügen, was die Synchronisierung von Dateien und den Dateistatus von AEM erleichtert.
- **Aus Favoriten entfernen**: Entfernt einen Ordner aus *Favoriten*. Weitere Informationen finden Sie unter [Favoriten hinzufügen oder entfernen](#id195HC04405P).
- **Anzeigen von Metadaten**: Zeigt die Metadaten wie die DITA-Klasse, den Titel, den Typ, die UUID und andere mit einer Datei verknüpfte Informationen an. Weitere Informationen finden Sie unter [Metadaten einer Datei anzeigen](#id195GHN0H05C).
- **Versionen anzeigen**: Zeigt den Versionsverlauf einer Datei an. Weitere Informationen finden Sie unter [Versionsverlauf einer Datei anzeigen](#id195GI000D5Q).

### Öffnen einer Datei in der XML-Autoreninstanz von Oxygen {#id195GHJ0A0UB}

Nachdem Sie eine Verbindung zum AEM-Repository hergestellt haben, können Sie Dateien zur Bearbeitung in der XML-Autoreninstanz öffnen. Führen Sie die folgenden Schritte aus, um eine Datei zur Bearbeitung im Oxygen XML Author zu öffnen:

1. Klicken Sie mit der rechten Maustaste auf eine Datei im Bedienfeld AEM Guides , die Sie zur Bearbeitung öffnen möchten.

1. Auswählen **Öffnen** aus dem Kontextmenü aus.

   Die Datei wird im Editor der XML-Autoreninstanz von Oxygen geöffnet.

   ![Anleitung in Datei-Tab](images/guid-in-file-tab.png) {width="800" align="left"}

   Wenn Sie den Mauszeiger über die Registerkarte einer Datei bewegen, wird Ihnen der Serverpfad zusammen mit der UUID angezeigt. Im obigen Screenshot wird die UUID des Dokuments hervorgehoben.


Wenn Sie die **Datei für automatisches Auschecken beim Öffnen** Option \(im Dialogfeld Voreinstellungen\), wird die Datei beim Öffnen automatisch ausgecheckt und steht zur Bearbeitung zur Verfügung. Um eine Datei zu öffnen, können Sie entweder auf einen Dateinamen doppelklicken oder mit der rechten Maustaste auf den Dateinamen klicken und **Öffnen** aus dem Kontextmenü aus. Wenn diese Option nicht ausgewählt ist, wird die Datei im schreibgeschützten Modus geöffnet.

>[!NOTE]
>
>Sie können auch auf eine Datei doppelklicken, um sie zu öffnen.

### Öffnen Sie die Datei im Editor AEM Guides . {#id195GH0V30KX}

Wenn Sie die in AEM Handbüchern verfügbaren Editoren verwenden möchten, wählen Sie die gewünschte Option im Kontextmenü aus. Führen Sie die folgenden Schritte aus, um den Editor AEM Guides anstelle des Oxygen XML Author-Editors zu verwenden:

1. Klicken Sie mit der rechten Maustaste auf eine Datei im Bedienfeld AEM Guides , die Sie zur Bearbeitung öffnen möchten.

1. Auswählen **Öffnen in** Wählen Sie im Kontextmenü eine der folgenden Optionen aus:

   - **Web-Themen-Editor**: Wenn es sich bei der Datei, die Sie öffnen, um eine .xml - oder .dita -Datei handelt, können Sie sie zur Bearbeitung im Web Editor öffnen. Wählen Sie die **Web-Themen-Editor** -Option, um die ausgewählte Datei zur Bearbeitung im Web-Editor zu öffnen.

   - **Zuordnungs-Dashboard**: Sie können eine .ditamap-Datei im Dashboard der Karte bearbeiten, in der Sie verschiedene Vorgänge für die Zuordnungsdatei ausführen können. Diese Vorgänge hängen von der Rolle/Gruppe ab, zu der Sie gehören.

   - **Web DITA Map Editor**: Wenn Sie die .ditamap-Datei zur Bearbeitung im Map Editor öffnen möchten, wählen Sie diese Option. Mit der Option &quot;DITA Map Editor&quot;können Sie Themen hinzufügen oder entfernen, Beziehungstabellen hinzufügen und andere Vorgänge auf Ihrer Zuordnung durchführen.


### Auschecken von Dateien {#id195HC020TS4}

Wenn Sie eine Datei auschecken, wird sie lokal auf Ihrem System gespeichert und zur Bearbeitung im AEM Repository gesperrt. Führen Sie die folgenden Schritte aus, um eine Datei auszuchecken:

1. Sie können Ihre Dateien auf eine der folgenden Arten auschecken:
   - Klicken Sie im Bereich &quot;AEM Handbücher&quot;mit der rechten Maustaste auf eine Datei.
   - Klicken Sie mit der rechten Maustaste auf die Registerkarte &quot;Zuordnung&quot;im Bereich &quot;DITA Maps Manager&quot;.
   - Klicken Sie mit der rechten Maustaste auf eine Datei im Bereich &quot;DITA Maps Manager&quot;.
   - Klicken Sie mit der rechten Maustaste auf die Registerkarte &quot;Datei&quot;, wenn Sie eine Zuordnung oder ein Thema im Editor öffnen.

1. Wählen Sie eine der folgenden Optionen aus:
   - **Checkout:** Checkt eine Datei aus AEM Repository aus und stellt sie zur Bearbeitung bereit.
   - **Checkout mit abhängigen Elementen**: Prüft eine Datei mit ihren direkten Verweisen. Mit dieser Option können Sie Änderungen an übergeordneten und untergeordneten Seiten vornehmen. Das Sauerstoff-Plug-in für AEM Guides unterstützt das Auschecken einer Ebene von abhängigen Elementen. Beispiel: Zuordnung A verweist auf Thema A und Thema A verweist auf Thema B. Wenn Sie Karte A auschecken, wird Thema A unabhängig von der Ebene in der TOC-Hierarchie ausgecheckt. Themen B wird jedoch nicht überprüft, da es nicht direkt von Karte A aus verknüpft ist.
   - **Checkout mit schreibgeschützten abhängigen Elementen**: Prüft eine Datei und lädt ihre abhängigen Elemente als schreibgeschützte Kopien auf Ihren lokalen Computer herunter. Sie können keine Änderungen an den abhängigen Dateien vornehmen.

Wenn Sie die **Dateien beim Auschecken öffnen** Option \(im Dialogfeld Voreinstellungen\), wird die Datei beim Auschecken einer Datei automatisch zur Bearbeitung geöffnet.

Wenn Sie die **Datei für automatisches Auschecken beim Öffnen** Option \(im Dialogfeld Voreinstellungen\), wird die Datei beim Öffnen automatisch ausgecheckt und zur Bearbeitung zur Verfügung gestellt. Um eine Datei zu öffnen, können Sie entweder auf einen Dateinamen doppelklicken oder mit der rechten Maustaste auf den Dateinamen klicken und **Öffnen** aus dem Kontextmenü aus.

Wenn eine Datei ausgecheckt wird, ändert sich das Symbol der Datei, um den Sperrstatus anzuzeigen.

![Auschecken einer Datei](images/check-out-file.png){width="650" align="left"}

Im obigen Screenshot wird eine von einem anderen Benutzer ausgecheckte Datei mit einem schwarzen Sperrsymbol \(A\) angezeigt. Die vom aktuellen Benutzer ausgecheckte Datei wird mit einem grünen Schloss \(B\) angezeigt.

>[!NOTE]
>
>Wenn die ausgecheckte Datei gelöscht oder in einen anderen Ordner in AEM verschoben wird, erhalten Sie beim Einchecken der Datei eine Fehlermeldung. Vergewissern Sie sich, dass die ausgecheckte Datei nicht über die AEM Web-Oberfläche verschoben oder gelöscht wird.

### Einchecken einer Datei {#id182CF0J0FHS}

Wenn Sie eine Datei einchecken, wird die lokale Kopie von Ihrem System im AEM-Repository gespeichert und die Sperre in der Datei wird entfernt. Führen Sie die folgenden Schritte aus, um eine Datei einzuchecken:

1. Speichern Sie die Datei, indem Sie auf **Datei** \> **Speichern**.

1. Klicken Sie mit der rechten Maustaste auf eine ausgecheckte Datei oder Zuordnung an einem der folgenden Speicherorte:
   - Bedienfeld &quot;AEM Guides&quot;
   - Bedienfeld &quot;DITA Maps Manager&quot;
   - Registerkarte &quot;Datei&quot;, wenn Sie eine Zuordnung oder ein Thema im Editor öffnen.
   - Die Registerkarte &quot;Zuordnung&quot;im Bereich &quot;DITA Maps Manager&quot;.

1. Wählen Sie aus den folgenden beiden Optionen:

   - **Einchecken**: Checkt die ausgewählte Datei aus Ihrem lokalen System in AEM Repository ein.
   - **Einchecken mit abhängigen Personen:** Wenn Sie eine Datei zusammen mit den abhängigen Elementen ausgecheckt haben, verwenden Sie diese Option, um alle abhängigen Dateien in einem Vorgang einzuchecken. Bei Auswahl dieser Option wird das Dialogfeld &quot;Einchecken&quot;mit allen abhängigen Dateien angezeigt. Klicken Sie auf OK , um alle Dateien gleichzeitig einzuchecken.

   Wenn Sie die abhängigen Dateien nicht ausgecheckt haben und diese Option wählen, werden nur die abhängigen Dateien eingecheckt, die \(separat\) ausgecheckt haben. Ihnen wird eine Liste der Dateien angezeigt, die nicht eingecheckt werden konnten:

   ![Fehler einchecken](images/check-in-error.png){width="800" align="left"}

   Es wird dringend empfohlen, keine ausgecheckte Datei zu verschieben. Wenn jedoch eine ausgecheckte Datei an einen anderen Speicherort verschoben wird, müssen Sie den Checkout für diese Datei abbrechen. Wenn Sie Aktualisierungen an dieser Datei vornehmen möchten, checken Sie die Datei erneut aus, nehmen Sie Änderungen vor und checken Sie sie dann wieder ein. Wenn Sie versuchen, eine Datei einzuchecken, die von ihrem ursprünglichen Speicherort verschoben wurde, wird ein Fehler ausgegeben.

   Wenn eine abhängige Datei in AEM ausgecheckt ist, wird die abhängige Datei beim Einchecken nicht im Dialogfeld &quot;Einchecken&quot;angezeigt. Um eine Liste der abhängigen Dateien zu erhalten, die in AEM ausgecheckt wurden, müssen Sie einen Ordner aktualisieren.

   Wenn Sie über AEM eine abhängige Datei eingecheckt haben, wird die Dateiliste in der Sauerstoff-Autoreninstanz erst aktualisiert, wenn Sie den Ordner &quot;Aktualisierte und ausgecheckte Dateien aktualisieren&quot;erstellt haben. Wenn Sie ein Check-in mit abhängigen Personen durchführen und einige Dateien über AEM einchecken, erhalten Sie eine Fehlerliste mit den Dateien, die nicht eingecheckt werden konnten.

1. \(Optional\) Im **Einchecken** oder **Einchecken mit abhängigen Personen** Dialogfeld, Kommentar hinzufügen in **Versionskommentare** Textfeld.

   >[!NOTE]
   >
   >Dieser Kommentar wird im AEM Versionsverlauf der Datei angezeigt.

1. Fügen Sie Titel im **Titel** Textfeld in der **Einchecken** oder **Einchecken mit abhängigen Personen** Dialogfeld . Geben Sie einen Titel ein und drücken Sie die Eingabetaste. Beispiel: *Version 2307*.

   Wenn Ihr Administrator eine vordefinierte Liste von Bezeichnungen verwendet und diese in die `label.json` -Datei, werden diese Beschriftungen als Dropdown-Liste angezeigt. Sie können eine oder mehrere Beschriftungen aus der Dropdown-Liste auswählen.

   ![Dialogfeld &quot;Einchecken&quot;](images/checkin-dropdown-labels.png){width="550" align="left"}

   Sie können derselben Version eines Themas mehrere Bezeichnungen (durch Kommas getrennt) hinzufügen.  Beispiel: *Adobe*, *AEM*,*Handbücher*
Sie können jedoch nicht dieselbe Bezeichnung zu den verschiedenen Versionen eines Themas hinzufügen. Wenn Sie eine Bezeichnung hinzufügen, die Sie bereits zu einer früheren Version hinzugefügt haben, wird diese der neuesten Version hinzugefügt und aus der früheren Version entfernt.

   >[!NOTE]
   > 
   > Diese Beschriftungen werden im AEM Versionsverlauf der Datei angezeigt.


1. Klicken Sie auf **OK**.

>[!NOTE]
>
>Wenn die ausgecheckte Datei gelöscht oder in einen anderen Ordner in AEM verschoben wird, erhalten Sie beim Einchecken der Datei eine Fehlermeldung. Vergewissern Sie sich, dass die ausgecheckte Datei nicht über die AEM Web-Oberfläche verschoben oder gelöscht wird.

### Ausgecheckte Dateien in AEM Guides-Ansicht

Wenn Sie mehrere Ordner haben, ist es nicht einfach herauszufinden, wie viele Dateien in einer Ansicht ausgecheckt werden. AEM Guides bieten die Option &quot;Ausgecheckte Dateien&quot;in AEM Guides-Ansicht, die eine vollständige Momentaufnahme der derzeit ausgecheckten Dateien liefert. Mithilfe dieser Ansicht können Sie mithilfe von AEM Handbüchern einfach herausfinden, welche Dateien von Ihnen in AEM Repository überprüft wurden. Führen Sie die folgenden Schritte aus, um auf diese Ansicht zuzugreifen und sie zu verwenden:

1. Klicks **Fenster** \> **Anzeigen-Ansicht** \> **In AEM Handbüchern ausgecheckte Dateien**.

   Die Ansicht Dateien, die in AEM Guides ausgecheckt wurden, wird angezeigt.

   ![ausgecheckte Dateien](images/files-checkedout-view.png){width="550" align="left"}

1. Klicken Sie mit der rechten Maustaste auf eine Datei in dieser Ansicht, um die folgenden Optionen zu erhalten:

   - [Öffnen](#id195GH0V30KX)
   - [Öffnen in](#id195GH0V30KX)
   - Abbrechen des Auscheckens
   - [Einchecken](#id182CF0J0FHS)
   - [Einchecken mit abhängigen Personen](#id182CF0J0FHS)
   - [Anzeigen von Metadaten](#id195GHN0H05C)
   - [Versionen anzeigen](#id195GI000D5Q)

**Hinweise zu ausgecheckten Dateien in AEM Guides-Ansicht:**

- Die *In AEM Handbüchern ausgecheckte Dateien* In der Ansicht werden die Sitzungen des Benutzers verwaltet. Das bedeutet, dass Dateien, die vom aktuellen Benutzer ausgecheckt wurden, in der Ansicht über die Sitzungen desselben Benutzers hinweg gespeichert und gepflegt werden \(oder Cache\).

- Wenn der Benutzer die Anmeldedaten oder den AEM-Server ändert, werden die Daten der ausgecheckten Datei \(oder Cache\) in der Ansicht zurückgesetzt. Der Benutzer muss manuell eine *Ausgecheckte Dateien aktualisieren* -Befehl für jeden Ordner, aus dem die Dateien zuvor ausgecheckt wurden. Um dies zu vereinfachen, wird empfohlen, Ihre Arbeitsordner zu *Favoriten* von wo aus Sie schnell eine Ordneraktualisierung durchführen können.

- Sie können die Dateiliste nach Dateinamen, Titel oder Pfad sortieren. Wenn eine neue Datei ausgecheckt ist, wird die Datei in der Ansicht in sortierter Reihenfolge angezeigt.


### Hochladen von Dateien und Ordnern {#id195HC03F03J}

Führen Sie die folgenden Schritte aus, um Dateien oder Ordner hochzuladen:

1. Klicken Sie mit der rechten Maustaste auf einen Ordner im Bedienfeld AEM Handbücher .
1. Wählen Sie eine der folgenden Optionen aus:
   - **Datei hochladen\(en\)**: Wählen Sie diese Option, um einzelne oder mehrere Dateien in den ausgewählten Ordner im AEM-Repository hochzuladen. Wählen Sie im Dialogfeld Zu ladende Dateien auswählen die Dateien aus und klicken Sie auf **Öffnen**.
   - **Hochladen mit abhängigen Elementen**: Wählen Sie diese Option, um eine DITA-Datei mit den abhängigen Elementen hochzuladen. Wählen Sie im Dialogfeld Zu ladende Datei auswählen die Dateien aus und klicken Sie auf **Öffnen**.
   - **Ordner hochladen**: Wählen Sie diese Option, um einen Ordner in das AEM-Repository hochzuladen. Wählen Sie im Dialogfeld Auswählen den Ordner aus und klicken Sie auf **Auswählen**.

**Zusätzliche Hinweise zum Arbeiten mit UUID-basierten Dateien**:

Beim Verschieben oder Kopieren von Inhalten aus Ihrem lokalen System in AEM Repository müssen die folgenden Punkte berücksichtigt werden:

- Beim Hochladen einer oder mehrerer Dateien wird für Dateien ohne UUID eine neue UUID generiert. Diese UUID wird im `topic id` einer DITA-Datei.

- Beim Kopieren eines Ordners werden die Verweise auf die Dateien \(im Ordner\) automatisch in allen DITA-Maps aktualisiert, die auf Dateien in diesem Ordner verweisen.

- Beim Kopieren einer DITA-Map-Datei werden die UUID-Verweise in der Map-Datei nicht geändert.

- Wenn eine Datei oder ein Ordner einen Konflikt oder ein Duplikat aufweist, wird ein eindeutiger Dateiname für die neue Datei generiert, die kopiert oder verschoben wird.

- Keine zwei Dateien können dieselbe UUID aufweisen. Allen neuen Dateien wird eine eindeutige UID zugewiesen.

- Wenn eine Datei von zwei verschiedenen Benutzern gleichzeitig hochgeladen wird, überschreibt die später verarbeitete Datei die frühere Datei. Eine solche Praxis sollte jedoch vermieden werden.

- Wenn Sie Inhalte aus AEM Repository auschecken und Änderungen auf Ihrem lokalen System vornehmen, stellen Sie sicher, dass der Dateiname zum Zeitpunkt des Hochladens der Datei nicht geändert wird.

- Wenn Sie einen Verweis in den DITA Maps Manager einfügen, wird der Titel der Datei und nicht die UUID angezeigt. Wenn der Titel nicht vorhanden ist, wird der Dateiname angezeigt.

### Favoriten hinzufügen oder entfernen {#id195HC04405P}

Führen Sie die folgenden Schritte aus, um einen Ordner zum Ordner Favoriten im Bedienfeld AEM Handbücher hinzuzufügen oder zu entfernen:

- Klicken Sie mit der rechten Maustaste auf einen Ordner und wählen Sie **Zu Favoriten hinzufügen**. Sie können einen Ordner zu Favoriten hinzufügen, wenn er nicht zu Favoriten gehört.
- Sie können Ordner auf folgende Weise aus Favoriten entfernen:
   - Rechtsklicken Sie auf einen Ordner im **Favoriten** Ordner und auswählen **Aus Favoriten entfernen**.
   - Klicken Sie mit der rechten Maustaste auf einen Ordner im AEM-Repository unter **DAM** Ordner, der bereits als Favorit hinzugefügt wurde, und wählen Sie **Aus Favoriten entfernen**.

### Versionsverlauf einer Datei anzeigen {#id195GI000D5Q}

Führen Sie die folgenden Schritte aus, um den Versionsverlauf einer Datei anzuzeigen:

1. Klicken Sie mit der rechten Maustaste auf eine Datei im Bedienfeld AEM Guides .

1. Auswählen **Versionen anzeigen** aus dem Kontextmenü aus.

   Der Versionsverlauf der Datei wird im Dialogfeld Versionen angezeigt.

   ![Versionsverlauf](images/version-history.png){width="550" align="left"}


### Metadaten einer Datei anzeigen {#id195GHN0H05C}

Führen Sie die folgenden Schritte aus, um die Metadaten einer Datei anzuzeigen:

1. Klicken Sie mit der rechten Maustaste auf eine Datei im Bedienfeld AEM Guides .

1. Auswählen **Anzeigen von Metadaten** aus dem Kontextmenü aus.

   Die Metadaten der Datei wie DITA-Klasse, Dokumentstatus, Änderungsdatum, Größe, Titel und UUID werden im Dialogfeld Metadaten angezeigt.

   ![Anzeigen von Metadaten](images/metadata.png){width="550" align="left"}


## Suchen nach einem Thema im AEM Repository {#id1826J20405Z}

Sie können über die Suchleiste im Bedienfeld AEM Handbücher nach Themen im AEM Repository suchen. Sie können im gesamten DAM-Ordner suchen oder einen Ordner auswählen und dann nach einem Thema in diesem Ordner suchen. Das Suchergebnis zeigt die Themen an, deren Text mit Ihrer Suchabfrage übereinstimmt.

Führen Sie die folgenden Schritte aus, um Themen zu suchen:

1. Wählen Sie einen Ordner im AEM-Repository aus, in dem Sie nach einem Thema suchen möchten.
1. Geben Sie die Suchabfrage ein \(z. B. `introduction`\) in der Suchleiste des Oxygen Plugins für AEM Guides.
1. Klicken Sie auf die Suchschaltfläche oder drücken Sie die Eingabetaste.

   Das Ergebnis wird auf der Registerkarte Suchergebnisse als Liste mit dem Dateipfad angezeigt. Wenn für Ihre Suchanfrage kein passendes Ergebnis vorliegt, werden in &lt;path of=&quot;&quot; the=&quot;&quot; selected=&quot;&quot; folder=&quot;&quot;> angezeigt.

   ![Ergebnisse der Suche](images/search.png){width="550" align="left"}

1. \(Optional\) Doppelklicken Sie auf eine Datei im Suchergebnis, um sie in der XML-Autoreninstanz von Oxygen zu öffnen.
1. Führen Sie einen der folgenden Schritte aus, um zur AEM Repository-Ansicht zurückzukehren:
   - Um die AEM Repository-Ansicht anzuzeigen, ohne die Suchergebnisse zu löschen, klicken Sie auf **Durchsuchen** Registerkarte.
   - Um die Suchergebnisse zu löschen und das AEM Repository anzuzeigen, klicken Sie auf das Symbol Suche löschen .

## Öffnen Sie das DITA-Thema in der Oxygen XML Author über AEM Web-Oberfläche. {#id182CE0I905Z}

Sie können Ihr DITA-Thema in der Oxygen XML Author über die AEM Web-Oberfläche öffnen und bearbeiten. Sie müssen ein Package in AEM installieren, um diese Option zu aktivieren. Weitere Informationen zur Paketinstallation finden Sie unter [Installieren Sie das Paket für die Aktivierung der Dokumentbearbeitungsfunktion über AEM Web-Oberfläche](#id182CE0Q0TY4).

>[!NOTE]
>
>Die **In Sauerstoff bearbeiten** kann von verschiedenen Stellen in AEM aus aufgerufen werden: bei Auswahl eines Themas, bei der Vorschau eines Themas oder über die Registerkarte Themen und Berichte der DITA-Map-Konsole. Wenn Sie mehrere Themen auswählen, ist die Option nicht in der Symbolleiste sichtbar.

**DITA-Thema öffnen**

Führen Sie die folgenden Schritte aus, um ein DITA-Thema in der XML-Autoreninstanz von Oxygen zu öffnen:

1. Wählen Sie ein Thema in Ihren Assets aus und klicken Sie auf **In Sauerstoff bearbeiten** in der Symbolleiste.

   >[!NOTE]
   >
   >Wenn das Thema nicht ausgecheckt ist, wird es zunächst ausgecheckt und dann im Bearbeitungsmodus in Sauerstoff geöffnet.

1. Wählen Sie Oxygen XML Author *&lt;version>* im **Launch-Anwendung** Meldungsfeld. Sie können **Meine Auswahl an AEM-Links speichern** -Option, um Ihre Voreinstellung zu speichern.

**Bearbeiten eines DITA-Themas**

Führen Sie die folgenden Schritte aus, um ein DITA-Thema in der Oxygen XML Author zu bearbeiten:

1. Auswählen und Auschecken eines Themas in Ihren Assets.
1. Klicks **In Sauerstoff bearbeiten** in der Symbolleiste.

   >[!NOTE]
   >
   >Wenn das Thema nicht ausgecheckt ist, wird es zunächst ausgecheckt und dann im Bearbeitungsmodus in Sauerstoff geöffnet.

1. Wählen Sie Oxygen XML Author *&lt;version>* im **Launch-Anwendung** Meldungsfeld. Sie können **Meine Auswahl an AEM-Links speichern** -Option, um Ihre Voreinstellung zu speichern.
1. Bearbeiten Sie das Thema in der Oxygen XML Author.
1. Checken Sie das Thema aus dem Oxygen-Plug-in für AEM Guides ein.

   Weitere Informationen zum Einchecken eines Themas mit dem Sauerstoff-Plug-in für AEM Guides finden Sie unter [Einchecken einer Datei](#id182CF0J0FHS).

   >[!NOTE]
   >
   >Stellen Sie sicher, dass Sie das Thema mit dem Sauerstoff-Plug-in für AEM Guides einchecken. Wenn Sie über die AEM Web-Oberfläche einchecken, werden die Änderungen, die Sie in der Sauerstoff-XML-Autoreninstanz vornehmen, nicht in der eingecheckten Version des Themas gespeichert.


## Arbeiten mit Attributprofilen {#id1827JA002YK}

Mit AEM Guides können Sie bedingte Attribute mithilfe der relevanten DITA-Attribute einfach erstellen und zuordnen. Sie können bedingte Attribute auf globaler Ebene oder auf Ordnerebene definieren. Die global definierten Bedingungen sind für alle Projekte sichtbar und die Bedingungen auf Ordnerebene sind nur in Projekten sichtbar, die innerhalb des angegebenen Ordners erstellt wurden. Inhaltsautoren können diese bedingten Attribute verwenden, um Inhalte in ihren DITA-Themen oder -Maps, die sie erstellen oder verwenden, an Bedingungen zu knüpfen. Weitere Informationen zum Erstellen von bedingten Attributen in AEM mithilfe der AEM-Handbücher finden Sie unter *Bedingte Attribute für globale Profile oder Profile auf Ordnerebene konfigurieren* unter Installieren und Konfigurieren von Adobe Experience Manager-Handbüchern.

>[!NOTE]
>
>Stellen Sie sicher, dass Sie die bedingten Attribute in AEM hinzugefügt und [Voreinstellung für die Profilattributanpassung](#id1827K0D0OHT) bevor Sie bedingte Attribute zu Ihrem Inhalt hinzufügen.

Führen Sie die folgenden Schritte aus, um Ihrem Inhalt in der XML-Autoreninstanz Bedingungsattribute hinzuzufügen:

1. Checken Sie ein Thema aus und öffnen Sie es über *Sauerstoff-Plug-in für AEM Guides*.
1. Wählen Sie den Teil des Inhalts aus, auf den Sie die bedingten Attribute anwenden möchten.
1. Doppelklicken Sie auf das bedingte Attribut im Bereich &quot;Attribute&quot;der XML-Autoreninstanz Oxygen .

   ![Attributbedienfeld](images/attribute-panel.png){width="300" align="left"}

1. Im **Verfügbar** im Dialogfeld &quot;Attribut bearbeiten&quot;das Attribut\(s\) auswählen und auf **Hinzufügen**.

   Der folgende Bildschirm zeigt `audience` -Attribute.

   ![Dialogfeld &quot;Attribute bearbeiten&quot;](images/edit-attributes.png){width="550" align="left"}

1. Klicken Sie auf **OK**.

   Die Attribute werden dem Inhalt hinzugefügt.


## Fehlerbehebung bei allgemeinen Problemen {#id188ABC00RY4}

In diesem Thema werden einige der häufigsten Probleme behandelt, die bei der Arbeit mit dem Plug-in auftreten können, sowie deren Lösungen.

### Bedienfeld AEM Guides fehlt {#id192BH200ZAX}

**Problem** - Wenn das Bedienfeld &quot;AEM Guides&quot;in der XML-Autoreninstanz nicht angezeigt wird, versuchen Sie die folgenden Lösungen:

Lösung 1:

1. Aktivieren Sie in der XML-Autoreninstanz Oxygen das Plug-in.

   Klicks **Optionen** \> **Voreinstellungen** \> **Plugins** und wählen **Sauerstoff-Plug-in für Adobe Experience Manager-Handbücher.**

1. Starten Sie die XML-Autoreninstanz von Oxygen neu.


Lösung 2:

1. Wenn das Bedienfeld &quot;AEM Guides&quot;immer noch nicht angezeigt wird, aktivieren Sie das Fenster AEM Guides .

   Klicken Sie in Oxygen XML Author auf **Fenster** \> **Anzeigen-Ansicht** \> **AEM**.

Lösung 3:

1. Deinstallieren Sie das Oxygen-Plug-in für Adobe Experience Manager-Handbücher und installieren Sie es erneut.

   - Deinstallieren Sie unter Windows das Plug-in von **Programme hinzufügen oder entfernen** Liste. Installieren Sie dann das Plug-in neu.

   - Rufen Sie in Mac den Ordner aem-connector-x.x im Ordner &quot;plugins&quot;von Oxygen XML Author auf und verschieben Sie ihn in **Papierkorb**. Leeren Sie dann die **Papierkorb** Ordner.


### Anschluss für DITA-OT-Transformation konfigurieren

**Problem** - Wenn Sie eine DITA-OT-Transformation für Dateien ausführen, die vom Plug-in verarbeitet werden, schlägt die Transformation mit dem folgenden Fehler fehl:

![Fehler bei DITA-OT-Transformation](images/proxy-server-path-error-new.png){width="800" align="left"}

**Lösung** - Dieses Problem wurde behoben, indem ein Proxy-Server zwischen DITA-OT und dem Plug-in hinzugefügt wurde. Dieser Proxy-Server verarbeitet und gibt alle Dateien weiter, die von DITA-OT für Umwandlungen angefordert werden. Der Standardanschluss, für den dieser Server konfiguriert wurde, ist: `5972`. Wenn Sie diesen Anschluss für einen anderen Server verwenden, können Sie einen anderen Anschluss für den Proxyserver angeben.

Führen Sie die folgenden Schritte aus, um den Standardanschluss des Proxyservers zu ändern:

1. Navigieren Sie zum Basisverzeichnis Ihres Benutzers (Benutzer\).
1. Erstellen Sie eine Datei mit dem Namen aem\_connector\_proxy.
1. Öffnen Sie die Datei in einem beliebigen Texteditor und fügen Sie in der ersten Zeile der Datei eine verfügbare Anschlussnummer hinzu.
1. Speichern und schließen Sie die Datei.
1. Starten Sie die XL-XML-Autoreninstanz neu und führen Sie die DITA-OT-Transformation aus.


### AEM Bedienfeld &quot;Guides&quot;navigiert nicht zum Speicherort der geöffneten Datei

Problem: Wenn Sie eine Datei zum Bearbeiten in der XML-Autoreninstanz von AEM Server aus öffnen, wird die Datei zur Bearbeitung in der XML-Autoreninstanz geöffnet. Das Bedienfeld AEM Guides zeigt jedoch nicht den Speicherort der Datei in der Navigationsstruktur an.

Lösung: Dieses Problem wurde in Szenarien beobachtet, in denen der Dateipfad /content/dam zweimal enthält. Standardmäßig werden alle Assets in AEM im Ordner /content/dam gespeichert. Wenn Sie eine Ordnerstruktur hochladen oder erstellen, die auch /content/dam enthält, wird dieses Problem beobachtet. Sie können alle normalen Vorgänge für diese Dateien ausführen, ihr Speicherort innerhalb der Navigationsstruktur wird jedoch nicht standardmäßig angezeigt. Um auf diese Datei in der Navigationsstruktur zuzugreifen, müssen Sie manuell zum Speicherort der Datei navigieren. Beachten Sie, dass in der Navigationsstruktur der doppelte Pfad /content/dam durch /content/assets ersetzt wird.

### Protokollierung konfigurieren

Problem: Das Sauerstoff-Plug-in für AEM Guides generiert standardmäßig keine Protokolle, was das Debuggen von Fehlerszenarien erschwert.

Lösung: Führen Sie die folgenden Schritte aus, um die Logger für Adobe Xygen und JxBrowser einzurichten:

1. Oxygen XML Author schließen

1. Erstellen Sie eine Datei mit dem Namen `logback.xml` mit folgendem Inhalt:

   ```xml
   <configuration>
       <appender name="R2" class="ch.qos.logback.core.rolling.RollingFileAppender">
           <file>${user.home}/Desktop/oxygenLog/oxygen.log</file>
           <rollingPolicy class="ch.qos.logback.core.rolling.FixedWindowRollingPolicy">
               <fileNamePattern>${user.home}/Desktop/oxygenLog/oxygen%i.log.gz</fileNamePattern>
               <minIndex>1</minIndex>
               <maxIndex>20</maxIndex>
           </rollingPolicy>
           <triggeringPolicy class="ch.qos.logback.core.rolling.SizeBasedTriggeringPolicy">
               <maxFileSize>100MB</maxFileSize>
           </triggeringPolicy>
           <encoder>
               <pattern>%r %marker %p [ %t ] %c - %m%n</pattern>
           </encoder>
       </appender> 
   
       <root level="debug">
           <appender-ref ref="R2" />
       </root>
   </configuration>   
   ```

1. Speichern Sie die Datei im `Oxygen Author 25` Verzeichnis. (Der Pfad lautet beispielsweise: `C:\Program Files\Oxygen XML Author 25\logback.xml`)

1. Schließen Sie die Datei. Dadurch werden Xygen-Protokolle aktiviert, die unter dem Pfad verfügbar sind: `${user.home}/Desktop/oxygenLog/oxygen.log`
1. Öffnen Sie die `oxygenAuthor.bat` in einem Texteditor.
1. Richten Sie JxBrowser-bezogene Protokolle ein, indem Sie den Parameter hinzufügen
   `-Denable.aem.jx.log=true`. Dies ermöglicht JxBrowser-bezogene Protokolle, die Sie unter dem Pfad anzeigen können: `${user.home}\AppData\Local\Temp\Oxygen_Plugin_Javax_Log.log`:




   ```java
   SET OXYGEN_JAVA=java.exe
   if exist "%JAVA_HOME%\bin\java.exe" set OXYGEN_JAVA="%JAVA_HOME%\bin\java.exe"
   if exist "%~dp0\jre\bin\java.exe" SET OXYGEN_JAVA="%~dp0\jre\bin\java.exe"
   rem Set environment variables
   call "%~dp0\env.bat"
   %OXYGEN_JAVA% -XX:-OmitStackTraceInFastThrow -XX:SoftRefLRUPolicyMSPerMB=10 -Djdk.module.illegalAccess=permit -Djava.ipc.external=true 
   -Denable.aem.jx.log=true -Dsun.java2d.noddraw=true -Dsun.awt.nopixfmt=true -Dsun.java2d.dpiaware=true -Dsun.io.useCanonCaches=true -Dsun.io.useCanonPrefixCache=true 
   -Dsun.awt.keepWorkingSetOnMinimize=true -Dcom.oxygenxml.app.descriptor=ro.sync.exml.AuthorFrameDescriptor
    -Dcom.oxygenxml.ApplicationDataFolder="%APPDATA%" -cp %CP% ro.sync.exml.Oxygen %*
   ```


Mit den vorherigen Schritten werden die Protokolle aktiviert und Sie können sie zur Problembehebung verwenden.


