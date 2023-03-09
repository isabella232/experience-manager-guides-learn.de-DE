---
title: FMPS- und AEM-Handbücher
description: Veröffentlichen mit FMPS mithilfe von AEM
source-git-commit: 5c53f89a811571c2193769bb4821657df3212dc0
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# Handbücher für FrameMaker Publishing Server (FMPS) und AEM

**AEM Guides-Integration mit FrameMaker Publishing Server könnte Ihre Lösung sein, wenn Sie nach einer qualitativ hochwertigen automatisierten Veröffentlichung suchen.\
Der folgende Artikel hilft Ihnen beim Einrichten und Ausführen von FMPS mit AEM Guides.**

## Kompatibilität von FMPS mit AEM Guides:

- Kompatibilität mit 4.1 AEM Guides: [Link](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
- Kompatibilität mit 4.0 AEM Guides: [Link](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Zukünftige Version: [Link](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Installation:

### AEM:

Installation und Konfiguration siehe: [Link](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS:

Informationen zur FMPS-Installation finden Sie unter [Video-Link](https://www.youtube.com/watch?v=2deelyM5VA8&amp;t) oder [Dokumentation](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&amp;rhtocid=_2)

## Erforderliche Konfigurationen:

Ihre DITA-Inhalte können mit FrameMaker Publishing Server (FMPS) ausgegeben werden. Sie können die Ausgabe in allen von FMPS unterstützten Formaten erstellen. Ändern Sie in der Web-Konsole die folgenden Eigenschaften des Pakets com.adobe.fmdita.config.ConfigManager , um AEM Guides zur Verwendung von FMPS einzurichten.

Um die Web-Konsole zu öffnen, navigieren Sie zum URL-Zugriff http://\&lt;server name=&quot;&quot;>:\&lt;port>/system/console/configMgr.

**Konfigurationseigenschaften und ihre Beschreibung:** [Link](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Laufender Test:

Mithilfe von FMPS können Sie automatisch veröffentlichen **PDF, Responsive HTML5** und **Epub** für Ihre DITA- und FM-Assets.

Wählen Sie im Menü &quot;PDF mithilfe generieren&quot;die Option &quot;FrameMaker Publishing Server&quot;.

Der Benutzer kann &quot;settings File(.sts)&quot;und &quot;ditaval&quot;angeben. Die Filterung erfolgt mithilfe eines Ditavars, das auf den von Ihnen angegebenen Bedingungen basiert.

- **Festlegen der Datei**: Veröffentlichungseinstellung für FrameMaker/FMPS , die alle Einstellungen enthält, die FMPS beim Veröffentlichen berücksichtigen soll. Beispiel: Generieren der Ausgabe mit der benutzerdefinierten Vorlage, Generieren von Marken und Anschnitten (PDF), Generieren von PDF mit Inhaltsverzeichnis, Index usw.
- **FMPS vorhanden:** Vordefinierte Kombination aus Ditaval und Einstellungsdatei, anstatt separate Ditaval- und Einstellungsdateien bereitzustellen, kann der Benutzer eine FMPS-Vorgabe vorab erstellen, die für Veröffentlichungsanforderungen wiederverwendet werden kann.

**Hinweis:** Wenn Sie keine der Einstellungen oder FMPS-Vorgaben auswählen, wird FMPS mit der Standardsystemeinstellung veröffentlicht.

Wenn Sie die FMPS-Vorgabe ausgewählt und auch die Einstellungen/Ditaval-Datei aus AEM bereitgestellt haben, tritt ein Konflikt auf und die FMPS-Vorgabe hat Vorrang vor benutzerdefinierten Einstellungen/Ditaval-Dateien.

### Grundlegende Veröffentlichung mit FMPS:

Sie können Ihre bereits erstellten Grundlinien mit FMPS2020.0.2 oder höher veröffentlichen.

**Beispiel für eine FMPS-Einstellungsdatei (.sts-Datei) zum Einstieg:** [Link](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (Entpacken Sie diese Datei)

## Häufig gestellte Fragen und Fehlerbehebung:

- Die FMPS-Veröffentlichung schlägt mit &quot;Timeout Exception&quot;fehl.

Überprüfen und erhöhen Sie den Wert von &quot;FMPS timeout&quot;(Seconds) in /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;

- Die FMPS-Vorgabe kann nicht in der Dropdown-Liste abgerufen werden.

Stellen Sie sicher, dass auf dem Server eine vordefinierte FMPS-Vorgabe erstellt wurde und dass Ihre Verbindungseinstellungen korrekt sind.

- Ich bekomme beim Veröffentlichen leere PDF.

Wenn Sie UUID verwenden, stellen Sie sicher, dass Sie in den FrameMaker-Bearbeitungseinstellungen die Option &quot;UUID-basierte Referenzierung verwenden&quot;aktiviert haben und umgekehrt bei Nicht-UUID-AEM.

- Meine Einstellungen/Einstellungen werden in der endgültigen veröffentlichten Ausgabe nicht angewendet.

Stellen Sie sicher, dass Sie nicht beide Einstellungen/Ditaval-Dateien und FMPS-Vorgaben parallel auswählen. Überprüfen Sie die Ausgabe manuell mit FrameMaker.

- Die Grundlinie wird nicht über FMPS veröffentlicht.

Die grundlegende Veröffentlichung ist mit der FMPS-Version 2020.0.2 oder höher kompatibel.\
Vergewissern Sie sich, dass die Grundlinie ordnungsgemäß erstellt wurde, gehen Sie zur Karte Dashboard-Themen-Download-Karte zuordnen und wählen Sie &quot;Grundlinie verwenden &quot;.

- Die Veröffentlichung von Aufgaben über FMPS dauert länger als andere Engines.

Es wird einen idealen festen Header von ca. 3-4 Minuten nur beim Veröffentlichen aus FMPS als aus anderen Engines, wenn Sie glauben, dass dies mehr ist, wenden Sie sich an Ihren FMPS-Administrator oder an den Support für die Adobe.

## Sonstige -Ressourcen:

[FMPS - Schulung und Support](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[AEM Lernen und Support](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[FrameMaker- und FMPS-Community](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&amp;sort=latest_replies&amp;lang=all&amp;tabid=all)

[AEM Guides Community](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)
