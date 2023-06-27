---
title: Informationen zu diesem Handbuch
description: Informationen zu diesem Handbuch
source-git-commit: e3b2fc8c96ce535bb91e7bce935720aa389a917a
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 10%

---


# Informationen zu diesem Handbuch {#id175MC0P0S5Z}

Adobe Experience Manager-Handbücher \(später bezeichnet als *AEM*\) ist eine leistungsstarke, Cloud-basierte Inhaltsverwaltungslösung auf Unternehmensebene \(CCMS\). Sie ermöglicht native DITA-Unterstützung in Adobe Experience Manager und ermöglicht AEM die Bearbeitung der DITA-basierten Inhaltserstellung und -Bereitstellung. Sie ermöglicht es Autoren, Inhalte mithilfe des benutzerfreundlichen integrierten Web-Editors zu erstellen und in verschiedenen Ausgabeformaten zu veröffentlichen.

Dieses Handbuch enthält Anweisungen zum Herunterladen, Installieren und Konfigurieren AEM Handbücher. In diesem Handbuch finden Sie detaillierte Anweisungen zum Einrichten AEM Guides gemäß Ihren Anforderungen an die Erstellung und Veröffentlichung im Unternehmen.

Dieses Handbuch richtet sich an folgende Zielgruppen:

- Administratoren, die AEM Handbücher installieren und verwalten.

- Herausgeber, die die Veröffentlichungsaufgabe ausführen, um Ausgabe in verschiedenen Formaten zu generieren.


## Inhaltsstruktur

Die Informationen in diesem Handbuch sind wie folgt organisiert:

- [Informationen zu diesem Handbuch](#id175MC0P0S5Z): Dieses Thema bietet eine Einführung in dieses Handbuch, die gewünschte Zielgruppe und die Organisation der Informationen in diesem Handbuch.

- [Herunterladen und installieren](download-install.md#): Hier wird beschrieben, wie Sie AEM Handbücher herunterladen, installieren oder aktualisieren.

- [Benutzerverwaltung und Sicherheit](user-admin-sec.md#): Hier werden das Kernkonzept der Benutzer und die Authentifizierung in AEM und die von AEM Guides erstellten Standardbenutzergruppen beschrieben.

- [Verwenden einer benutzerdefinierten DITA-OT- und DITA-Spezialisierung](dita-ot-specialization.md#): In diesem Thema wird beschrieben, wie Sie benutzerdefinierte DITA-OT-Plug-ins konfigurieren und DITA-Spezialisierung verwenden.

- [Dokumentstatus konfigurieren](customize-doc-state.md#): In diesem Thema wird erläutert, wie Sie benutzerdefinierte Status für Ihre DITA-Dokumente konfigurieren.

- [Migrieren vorhandener Inhalte](migrate-content.md#): Hier wird beschrieben, wie Sie vorhandenen Inhalt in AEM Repository integrieren.

- [Dateinamen konfigurieren](conf-file-names.md#): In diesem Thema wird erläutert, wie Sie Einstellungen konfigurieren, um automatisch Dateinamen zuzuweisen und einen Regex für gültige Dateinamenzeichen zu definieren.

- [Konfigurieren von Themen- und Zuordnungsvorlagen](conf-template-tags.md#): Hier wird beschrieben, wie Sie Themen- und Zuordnungsvorlagen konfigurieren, um Ihren Authoring-Anforderungen zu entsprechen. Erfahren Sie mehr über das Tagging-System in AEM und wie Sie Tags für die Verwendung mit AEM Handbüchern konfigurieren.

- [Anpassen des Web-Editors](conf-web-editor.md#): In diesem Thema werden die verschiedenen Anpassungen erläutert, die Sie im Web Editor vornehmen können, um die Funktionalität zu verbessern.

- [Standardmäßig Attribut @navtitle einschließen](auto-add-navtitle.md#): In diesem Thema wird erläutert, wie Sie die `@navtitle` -Attribut einer Referenzdatei in einer Zuordnung standardmäßig hinzugefügt.

- [Konfigurieren globaler Profile oder Profile auf Ordnerebene](conf-folder-level.md#): In diesem Thema wird der Prozess zum Erstellen von Ordnerprofilen und zum Gewähren von Berechtigungen für bestimmte Benutzer erläutert.

- [Versionsverwaltung](version-management.md#): Hier wird beschrieben, wie Sie das automatische Auschecken von Dateien konfigurieren, die zur Bearbeitung im Web Editor geöffnet sind.

- [Ausgabegenerierungseinstellungen konfigurieren](conf-output-generation.md#): In diesem Thema werden die verschiedenen Konfigurationen beschrieben, die Sie vornehmen können, um den standardmäßigen Generierungsprozess für die Ausgabe anzupassen.

- [Workflows konfigurieren und anpassen](customize-workflows.md#): Hier werden verschiedene Konfigurationen beschrieben, um die standardmäßigen Workflows anzupassen, die in den AEM-Handbüchern enthalten sind.

- [Inhalt übersetzen](translation.md#): Dieses Thema enthält Links zu den entsprechenden Hilfeartikeln in AEM Dokumentation, die Ihnen helfen, das Übersetzungs-Framework zu verstehen und zu konfigurieren. Erfahren Sie außerdem, wie Sie einen komponentenbasierten Übersetzungs-Workflow aktivieren.

- [Konfigurieren der Suche in der AEM Assets-Benutzeroberfläche](conf-dita-search.md#): Hier wird beschrieben, wie Sie die DITA-Inhaltssuche in der Assets-Benutzeroberfläche konfigurieren und Ihre benutzerdefinierten Attribute bei der Suche hinzufügen.


## Überblick über Adobe Experience Manager \(AEM\)

[Adobe Experience Manager \(AEM\)](https://business.adobe.com/de/products/experience-manager/adobe-experience-manager.html) ist eine umfassende Content-Management-Lösung zum Erstellen von Websites, mobilen Apps und Formularen. AEM hilft Ihnen bei der Verwaltung Ihrer Marketing-Inhalte und -Assets. AEM ist as a Cloud Service verfügbar. AEM as a Cloud Service hilft Ihnen, Ihren Kunden personalisierte, inhaltsgesteuerte Erlebnisse bereitzustellen, indem Sie die Leistungsfähigkeit des AEM Content Management Systems mit AEM Digital Asset Management kombinieren. Einige der wichtigsten Ressourcen, die Ihnen bei den ersten Schritten und der Bereitstellung für AEM as a Cloud Service helfen können, sind:

- [as a Cloud Service Übersicht über Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=de)
- [Erste Schritte auf der Migrationstour zu Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/migration-journey/getting-started.html?lang=en)
- [Starten Sie den Einstieg in den Experience Manager as a Cloud Service .](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/onboarding/home.html?lang=enhttps://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/home.html?lang=en)
- [Implementieren von Programmen für AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/home.html?lang=de)
- [Bereitstellen in AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/overview.html?lang=de)
- [Handbuch zu Assets as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/home.html?lang=de)

## Zusätzliche Ressourcen

Im Folgenden finden Sie eine Liste weiterer hilfreicher Ressourcen AEM Handbücher, die im Abschnitt [Lernen und Support](https://helpx.adobe.com/support/xml-documentation-for-experience-manager.html) Seite:

- Benutzerhandbuch
- API-Referenzhandbuch

