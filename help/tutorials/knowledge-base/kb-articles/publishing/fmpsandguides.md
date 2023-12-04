---
title: Veröffentlichen mithilfe von FrameMaker Publishing Server (FMPS) in AEM Guides
description: Veröffentlichen mit FMPS mithilfe von AEM
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Veröffentlichen mithilfe von FrameMaker Publishing Server (FMPS) in AEM Guides

AEM Guides-Integration mit FrameMaker Publishing Server könnte Ihre Lösung sein, wenn Sie nach einer qualitativ hochwertigen automatisierten Veröffentlichung suchen.\
Artikel hilft Ihnen beim Einrichten und Ausführen von FMPS mit AEM Guides.

## Kompatibilität von FMPS mit AEM Guides

- Kompatibilität mit 4.1 AEM Guides: [4.1 Kompatibilitätsmatrix](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
- Kompatibilität mit 4.0 AEM Guides: [Kompatibilitätsmatrix 4.0](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Neueste Version: [Neueste Versionsinformationen](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Installation

Weitere Informationen zur Installation und Konfiguration von AEM und FMPS finden Sie im Folgenden.

### AEM

Installation und Konfiguration siehe: [4.1 Installation und Konfigurationen](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS

Informationen zur FMPS-Installation finden Sie unter [YouTube-Link](https://www.youtube.com/watch?v=2deelyM5VA8&amp;t) oder [FMPS-Installation und -Konfiguration](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&amp;rhtocid=_2)

## Erforderliche Konfigurationen

Mit FrameMaker Publishing Server (FMPS) können Sie Ihren DITA-Inhalt generieren. FMPS unterstützt eine breite Palette von Ausgabeformaten. Ändern Sie die folgenden Eigenschaften des Bundles &quot;com.adobe.fmdita.config.ConfigManager&quot;in der Web-Konsole, um AEM Guides für die Verwendung von FMPS zu konfigurieren.

Um die Web-Konsole zu öffnen, navigieren Sie zum URL-Zugriff http://\&lt;server name=&quot;&quot;>:\&lt;port>/system/console/configMgr.

**Konfigurationseigenschaften und ihre Beschreibung** [4.1 Installation und Konfiguration](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Laufender Test:

Mithilfe von FMPS können Sie automatisch veröffentlichen **PDF, Responsive HTML5**, und **Epub** für Ihre DITA- und FM-Assets.

Wählen Sie im Menü &quot;PDF mithilfe generieren&quot;die Option FrameMaker Publishing Server.

Der Benutzer kann &quot;settings File(.sts)&quot;und &quot;ditaval&quot;angeben. Das Filtern erfolgt mithilfe eines Ditavings, das auf den von Ihnen angegebenen Bedingungen basiert.

- **Datei festlegen**: Eine Einstellungsdatei für die FrameMaker-/FMPS-Veröffentlichung, die alle Einstellungen enthält, die FMPS bei der Veröffentlichung berücksichtigen soll. Erstellen Sie beispielsweise eine Ausgabe mit einer benutzerdefinierten Vorlage, erstellen Sie Markierungen und Anschnitte (PDF) und erstellen Sie PDF mit dem Inhaltsverzeichnis.
- **FMPS-Vorgabe:** Es handelt sich um eine vordefinierte Kombination aus Ditaval und Einstellungsdatei. Anstatt separate Ditaval- und Einstellungsdateien bereitzustellen, kann der Benutzer eine FMPS-Vorgabe erstellen, die für Veröffentlichungsanforderungen wiederverwendet werden kann.

**Hinweis:** Die Standardsystemeinstellung wird von FMPS zur Veröffentlichung verwendet, wenn Sie keine der Einstellungen oder die FMPS-Vorgabe auswählen.

Es handelt sich um einen Konflikt, wenn Sie die FMPS-Vorgabe auswählen und auch benutzerdefinierte Einstellungen oder eine Ditaval-Datei aus AEM bereitgestellt haben. In diesem Fall hat die FMPS-Vorgabe Vorrang vor den benutzerdefinierten Einstellungen oder der Ditaval-Datei.

### Grundlegende Veröffentlichung mit FMPS:

Sie können Ihre bereits erstellten Grundlinien mit FMPS2020.0.2 oder höher veröffentlichen.

**Beispiel für eine FMPS-Einstellungsdatei (.sts-Datei) zum Einstieg:** [Beispieldatei für FMPS-Einstellungen](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (Entpacken Sie diese Datei)

## Häufig gestellte Fragen und Fehlerbehebung:

- ### FMPS-Veröffentlichung schlägt mit &quot;Timeout Exception&quot;fehl

>Überprüfen und erhöhen Sie den Wert von &quot;FMPS timeout&quot;(Seconds) in /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;

- ### FMPS-Vorgabe kann nicht in der Dropdown-Liste abgerufen werden

>Stellen Sie sicher, dass auf dem Server eine vordefinierte FMPS-Vorgabe erstellt wurde und dass Ihre Verbindungseinstellungen korrekt sind.

- ### Ich erhalte beim Veröffentlichen leere PDF

>Wenn Sie UUID verwenden, stellen Sie sicher, dass Sie in den FrameMaker-Bearbeitungseinstellungen die Option &quot;UUID-basierte Referenzierung verwenden&quot;aktiviert haben, und umgekehrt bei AEM Handbüchern ohne UUID.

- ### Meine Einstellungen/Einstellungen werden in der endgültigen veröffentlichten Ausgabe nicht angewendet

>Vergewissern Sie sich, dass Sie nicht gleichzeitig die FMPS-Vorgabe und die Einstellungen-/Diaval-Datei auswählen. Verwenden Sie FrameMaker, um die Ausgabe manuell zu überprüfen.

- ### Die Grundlinie wird nicht über FMPS veröffentlicht

>FMPS2020.0.2 oder neuere Versionen sind mit Grundlinien-Publishing kompatibel.
>Vergewissern Sie sich, dass Ihre Grundlinie ordnungsgemäß erstellt wurde. Gehen Sie zur Prüfung zum Map-Dashboard - Themen - Karte herunterladen und wählen Sie &quot;Grundlinie verwenden&quot;.
- ### Veröffentlichungsaufgaben aus FMPS benötigen mehr Zeit als andere Engines

>Bei der Veröffentlichung über FMPS beträgt die optimale feste Header-Zeit ca. 3-4 Minuten. Wenn Sie glauben, dass die Header länger ist, wenden Sie sich an Ihren FMPS-Administrator oder kontaktieren Sie den Adobe Support.

## Weitere Ressourcen:

[FMPS - Schulung und Support](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[AEM Handbücher - Schulung und Support](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[FrameMaker- und FMPS-Community](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&amp;sort=latest_replies&amp;lang=all&amp;tabid=all)

[AEM Guides Community](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)
