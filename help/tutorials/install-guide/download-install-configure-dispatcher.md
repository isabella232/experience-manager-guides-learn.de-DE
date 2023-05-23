---
title: Konfiguration des Dispatchers
description: Erfahren Sie, wie Sie den Dispatcher konfigurieren
source-git-commit: 9fe396dcfd2e3570ec386c958d7d4efdb4d608e5
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 9%

---


# Konfiguration des Dispatchers {#id213BCM0M05U}

Wenn Sie planen, einen Dispatcher in der AEM-Autoreninstanz zusammen mit AEM Guides zu verwenden, müssen Sie die folgenden zusätzlichen Konfigurationen durchführen, um das Setup abzuschließen:

>[!NOTE]
>
> Dispatcher ist ein Tool von Adobe Experience Manager für das Zwischenspeichern und/oder den Lastenausgleich. Weitere Informationen zur Verwendung des Dispatchers finden Sie unter [Dispatcher-Übersicht](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=de).

## AllowEncodedSlashes in URLs aktivieren

URLs mit kodierten Schrägstrichen sind in AEM Dispatcher-Einrichtung nicht standardmäßig aktiviert. Bei der Arbeit mit AEM Handbüchern müssen Sie dies jedoch aktivieren. Dazu müssen Sie den Parameter AllowEncodedSlashes in der Apache-Konfiguration auf Ein setzen, wie im folgenden Snippet gezeigt:

```XML
<VirtualHost *:80>
                ServerName www.geometrixx-outdoors.com
                **AllowEncodedSlashes On**
                <Directory />
                <IfModule disp_apache2.c>
                SetHandler dispatcher-handler
                </IfModule>
                Options FollowSymLinks
                AllowOverride None
                </Directory>
                </VirtualHost>
            
```

## Datei &quot;mime.types&quot;für DITA konfigurieren

Wenn Sie einen Dispatcher mit AEM Guides verwenden, müssen Sie sicherstellen, dass die DITA-Map- und Themendateien als HTML gerendert werden, damit Autoren den Inhalt erwartungsgemäß anzeigen können (anstelle des Rohtextformats\).

Führen Sie die folgenden Schritte aus, um die Datei &quot;mime.types&quot;zu aktualisieren:

1. Stellen Sie mithilfe von SSH eine Verbindung zum Dispatcher-Server her und navigieren Sie zur Datei &quot;httpd.conf&quot;.

1. Überprüfen Sie den Pfad der Datei &quot;mime.types&quot;.

1. Öffnen Sie die Datei &quot;mime.types&quot;und suchen Sie nach &quot;text/html&quot;. Die Standardzuordnung für &quot;text/html&quot;lautet:

   `text/html html htm`

1. Aktualisieren Sie die Zuordnung, indem Sie Ditamap- und Dia-Erweiterungen wie folgt hinzufügen:

   `text/html html htm ditamap dita`

1. Speichern und schließen Sie die Datei.


Diese Konfigurationsaktualisierung stellt sicher, dass die vom Dispatcher gerenderten DITA-Zuordnungs- und Themendateien in der Assets-Benutzeroberfläche als HTML angezeigt werden.

## URL der Anfrage &quot;Benutzereinstellungen zulassen&quot;

Wenn Sie einen Dispatcher mit AEM Guides verwenden und Ihre Autoreninstanz über einen Dispatcher verfügt, nehmen Sie die folgenden beiden Änderungen vor:

- Setzen Sie die URL der POST-Anfrage auf die Whitelist. Beispiel &quot; `/filters`&quot; Regel wird unten angegeben - Fügen Sie diese Regel zur Dispatcher-Konfigurationsdatei hinzu:

```json
/xxxx {/type "allow" /method "POST" /url "/home/users/*/preferences"}
```

- Stellen Sie sicher, dass das URL-Muster &quot; /libs/cq/security/userinfo.json&quot;nicht im Autoren-Dispatcher zwischengespeichert ist. Fügen Sie daher eine Regel \(wie unten\) in author\_dispatcher.any hinzu.

```json
/xxxx {
                /glob "/libs/cq/security/userinfo.json"
                /type "deny"
                }
```

**Übergeordnetes Thema:**[ Herunterladen und installieren](download-install.md)

