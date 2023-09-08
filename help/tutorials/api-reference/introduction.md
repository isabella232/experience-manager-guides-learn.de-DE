---
title: Einführung
description: Einführung in das API-Referenzhandbuch für AEM Handbücher
source-git-commit: 4dcd90422f02f3b45aa74137fe58609962b09b49
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---


# Einführung {#id1761C0007W7}

Adobe Experience Manager-Handbücher \(später bezeichnet als *AEM*\) ist eine End-to-End-Unternehmenslösung, mit der Adobe Experience Manager \(AEM\) über Funktionen zur Komponenteninhaltsverwaltung \(CCMS\) für die DITA-basierte Inhaltserstellung und -bereitstellung verfügen kann. Kunden können programmgesteuert über die AEM Guides-APIs auf AEM Guides-Workflows zugreifen, um sie in andere Unternehmensanwendungen zu integrieren. Diese APIs können auch von Adobe-Partnern verwendet werden, um das Wertversprechen von AEM Guides zu verbessern, indem deren Funktionalität erweitert oder in andere Anwendungen oder Dienste integriert wird.

## AEM Guides-APIs

Die AEM Guides-APIs sind in zwei Formaten verfügbar: HTTP und Java. Diese APIs stellen Anwendungsentwicklern wichtige Funktionen von AEM Handbüchern zur Verfügung. Mit diesen Funktionen können Entwickler eigene Plug-ins erstellen, um die vordefinierten Workflows zu erweitern. Die APIs stehen zur Verwaltung von Ausgaben für DITA-Inhalte, zum Arbeiten mit DITA-Maps, zum Hinzufügen bedingter Attribute zu Profilen auf Ordnerebene und zum Konvertieren von HTML- und Words-Dokumenten in das DITA-Format zur Verfügung.

## Installieren der JARs auf Ihrem lokalen Apache Maven-Repository {#install-jar-local}

Um die JAR-Dateien verwenden zu können, die von AEM Guides bereitgestellt werden, müssen Sie sie in Ihrem lokalen Apache Maven-Repository installieren. Führen Sie die folgenden Schritte aus, um die JARs auf Ihrem Maven-Repository zu installieren:

1. Extrahieren Sie den Inhalt der AEM Guides-Package \(.zip\) auf Ihrem lokalen System.

2. Navigieren Sie in der Eingabeaufforderung zum folgenden Ordner im Pfad des extrahierten Inhalts:

   ```
   \jcr_root\libs\fmdita\osgi-bundles\install
   ```

3. Führen Sie den folgenden Befehl aus, um das API-Bundle in Ihrem lokalen Maven-Repository zu installieren:

   ```
   mvn install:install-file -Dfile=api-X.x.jar -DgroupId=com.adobe.fmdita -DartifactId=api -Dversion=X.x -Dpackaging=jar**
   ```

   >[!NOTE]
   >
   > Im obigen Befehl sollte X.x durch die tatsächliche Versionsnummer in den Dfile - und Dversion -Parametern ersetzt werden.

4. \(*Optional*\) Installieren Sie die Abhängigkeit im Repository Ihres lokalen Maven-Projekts. Sie können dies erreichen, indem Sie einen Ordner in Ihrem Maven-Projekt erstellen und dann die `mvn install` -Befehl, der im vorherigen Schritt mit dem folgenden zusätzlichen Parameter gegeben wurde:

   ```
   -DlocalRepositoryPath=<path_to_project_repository>
   ```

   Um als Nächstes den lokalen Repository-Ordner des Projekts für den Maven-Build-Prozess verfügbar zu machen, fügen Sie eine `repository` -Element in der übergeordneten pom.xml-Datei wie unten gezeigt:

   ```XML
   <repositories>
      <repository>
         <id>project-repository</id>
         <url>file://${project.basedir}/repository</url>
      </repository>
   </repositories>
   ```


Durch diesen Prozess werden die API-JARs im lokalen Maven-Repository installiert.

## Verwenden der Dienst-API-JAR-Datei in einem Maven-Projekt

Führen Sie nach der Installation der API-JARs in Ihrem lokalen Maven-Repository die folgenden Schritte aus, um die JAR-Datei in Ihren Projekten zu verwenden:

1. Fügen Sie die JAR-Datei zu Ihrer Codebasis hinzu und übertragen Sie sie in das Code-Basis-Repository unter einem Ordner, z. B. &quot;Abhängigkeiten&quot;. Beachten Sie, dass der Ordnername von Ihrer Code-Basis-Hierarchie abhängt.

2. Konfigurieren Sie die Projektdateien &quot;pom.xml&quot;wie folgt:

   Datei &quot;pom.xml&quot;des übergeordneten Projekts:

   >[!IMPORTANT]
   >
   > Im folgenden Codefragment sollte X.x durch die tatsächliche Versionsnummer und den Dateinamen der API-JAR-Datei ersetzt werden. Diese Informationen entsprechen den Angaben in Schritt 3 der [Installationsprozess](#install-jar-local).

   ```XML
   <plugin>
   
       <groupId>org.apache.maven.plugins</groupId>
   
      <artifactId>maven-install-plugin</artifactId>
   
       <version>2.5.2</version>
   
       <configuration>
   
               <groupId>com.adobe.fmdita</groupId>
   
               <artifactId>api</artifactId>
   
               <version>X.x</version>
   
               <file>${basedir}/dependencies/fmdita/api-X.x.jar</file>
   
               <packaging>jar</packaging>
   
               <generatePom>true</generatePom>
   
       </configuration>
   
       <executions>
   
           <execution>
   
               <id>inst_fmdita</id>
   
                   <goals>
   
                       <goal>install-file</goal>
   
                   </goals>
   
                   <phase>clean</phase>
   
           </execution>
   
       </executions>
   </plugin>
   ```

   Datei pom.xml des untergeordneten Moduls:

   ```XML
   <plugin>
      <groupId>org.apache.maven.plugins</groupId>
   
      <artifactId>maven-install-plugin</artifactId>
   
      <configuration>
   
         <groupId>com.adobe.fmdita</groupId>
   
         <artifactId>api</artifactId>
   
         <version>3.6</version>
   
         <file>${basedir}/../dependencies/fmdita/api-3.6.jar</file>
   
         <packaging>jar</packaging>
   
         <generatePom>true</generatePom>
   
      </configuration>
   
      <executions>
   
         <execution>
   
            <id>inst_fmdita</id>
   
            <goals>
   
               <goal>install-file</goal>
   
            </goals>
   
            <phase>clean</phase>
   
         </execution>
   
      </executions>
   
   </plugin>
   ```


## Dienst-API-JAR aus öffentlichem Maven-Repository konfigurieren und verwenden

Führen Sie die folgenden Schritte aus, um die Service-API-JARs aus dem öffentlichen Maven-Repository in Ihren Projekten zu konfigurieren und zu verwenden:

1. Um die Dienst-API-JAR in einem Projekt zu verwenden, konfigurieren Sie AEM Guides das öffentliche Maven-Repository in Ihrer pom.xml-Datei.
2. Konfigurieren Sie das öffentliche Maven-Repository in der Maven-Datei settings.xml wie folgt:

   ```XML
   <repository>
      <id>fmdita-public</id>
      <name>fmdita-public</name>
      <url>https://repo.xmldocumentation.com/repository/fmdita-public</url>
   </repository>
   ```

3. Nachdem das Repository eingerichtet wurde, fügen Sie die JAR-Datei für die Dienst-API als Projektabhängigkeit in der Datei &quot;pom.xml&quot;des Projekts hinzu.

   >[!NOTE]
   >
   > Verwenden Sie dieselbe Version der API-JAR-Datei wie das AEM Guides-Paket, das Sie auf dem Server installiert haben.

4. Konfigurieren Sie die Maven-Abhängigkeit wie unten dargestellt:

   ```XML
   <dependency>
      <groupId>com.adobe.fmdita</groupId>
      <artifactId>api</artifactId>
      <version>4.0</version>
   </dependency>
   ```


Sobald die Service-API-JAR-Datei als Projektabhängigkeit in der Datei &quot;pom.xml&quot;des Projekts hinzugefügt wurde, können Sie AEM Guides-Java-APIs in Ihrem Projekt erstellen und verwenden.

## Verwenden von API JAR aus dem zentralen Maven-Repository für AEM Handbücher as a Cloud Service

Für AEM Guides as a Cloud Service wurde die API-JAR-Datei in Maven Central bereitgestellt. Sie können die API-JAR-Datei ohne Einrichtung verwenden.

>[!NOTE]
>
> Die Namenskonvention der API-JAR-Datei wurde gemäß der Namenskonvention für Cloud-Add-ons aktualisiert.

Um die API-JAR-Datei zu verwenden, müssen Sie die Abhängigkeit zur pom.xml Ihres Projekts hinzufügen, wie unten dargestellt:

```XML
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-guides-sdk-api</artifactId>
   <version>2022.5</version>
</dependency>
```

>[!NOTE]
>
> Da die Pakete innerhalb der API-JAR immer noch dieselben sind, ist keine Codeänderung erforderlich, um diese API-JAR in den vorhandenen Cloud-Projekten zu verwenden.

## Zusätzliche Ressourcen

Im Folgenden finden Sie eine Liste weiterer hilfreicher Ressourcen AEM Handbücher, die im Abschnitt [Lernen und Support](https://helpx.adobe.com/support/xml-documentation-for-experience-manager.html) Seite:

- Benutzerhandbuch
- Handbuch zur Installation und Konfiguration
- Schnellstartanleitung
- [Hilfeseite](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html) \(Zugriff auf die Dokumentation zu älteren Versionen\)

