---
title: AEM Guides-Versionen
description: Neueste AEM Guides-Versionen und erforderliche AEM-Versionen
exl-id: 780697a9-bdc6-40c2-b258-64639fe30f88
source-git-commit: f74a9168708299d66d014dbc4bf280a1a4f07592
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---

# [!DNL AEM Guides] Versionen

[!DNL Adobe Experience Manager Guides] ist eine Anwendung, die auf AEM bereitgestellt wird. Es handelt sich dabei um eine leistungsstarke, unternehmenseigene Content-Management-Lösung (CCMS), die die native DITA-Unterstützung in Adobe Experience Manager ermöglicht und es AEM ermöglicht, die DITA-basierte Inhaltserstellung und -bereitstellung zu handhaben.

AEM Guides-Pakete sind in zwei Varianten verfügbar: UUID-Build und Nicht-UUID-Builds.

## UUID- und Nicht-UUID-Builds

Die wichtigsten Unterschiede zwischen den UUID- und Nicht-UUID-Builds lauten wie folgt:

|  | Nicht-UUID-Build | UUID-Build |
|---|---|---|
| **Asset-Identifizierung** | Alle Assets werden mithilfe des Pfads des Assets im Repository identifiziert. | Alle Assets werden anhand ihrer UUID (eindeutige ID, die vom System beim ersten Hochladen des Assets generiert wurde) identifiziert. |
| **Referenzerstellung** | Alle Inhaltsverweise werden basierend auf ihren Pfaden erstellt. | Alle Inhaltsreferenzen werden basierend auf ihrer UUID erstellt. |

### Vorteile des UUID-Builds

* Die UUID-Installation ist leistungsfähiger:
   * Verweise sind pfadunabhängig: Das Referenzverwaltungssystem kennt die Verknüpfungen, da die Verweise auf der Grundlage von UUIDs und nicht der Pfade erstellt werden.
   * Die Verschiebe-/Aktualisierungsvorgänge sind effizient: Die UUIDs bleiben auch dann gleich, wenn die Assets in einen anderen Pfad im Repository verschoben werden. Daher ist keine Verarbeitung erforderlich, um die Verweise zwischen den Assets bei Verschiebe-/Aktualisierungsvorgängen zu patchen.
* Der UUID-Build ist zukunftsorientiert, da wir dieses Framework auch für die Cloud-Einrichtung von AEM Guides verwenden.


### Wählen Sie zwischen den beiden Builds

* Wenn Sie ein neuer Kunde sind, empfehlen wir die Verwendung des UUID-Builds.
* Wenn Sie bereits Kunde sind, können Sie zum UUID-Build wechseln, da die Migration vom Build Nicht-UUID zu UUID jetzt möglich ist. Weitere Informationen finden Sie unter *Migration von Nicht-UUID-zu-UUID-Inhalten* im Abschnitt **Installieren und konfigurieren Sie Adobe Experience Manager-Handbücher.**

>[!NOTE]
>
>* Kunden müssen zum Zeitpunkt der ersten Einrichtung zwischen dem UUID- und dem Nicht-UUID-Modus entscheiden (falls Sie Hilfe benötigen, wenden Sie sich an den Customer Success Manager, um Ihnen zu helfen, die Entscheidung basierend auf Ihrem Anwendungsfall zu treffen).
>* Beim Upgrade von einer Version von AEM Guides auf eine neuere Version müssen Kunden sicherstellen, dass sie denselben Modus (UUID/Nicht-UUID) auswählen, der mit ihrem vorhandenen Modus übereinstimmt. Ein Nicht-UUID-Build sollte nicht direkt auf einen UUID-Build aktualisiert werden. Für den Wechsel vom Nicht-UUID-Build zum UUID-Build ist eine Inhaltsmigration erforderlich.


**Builds aktualisieren**

Wenn Sie von einer älteren Version auf eine neuere Version von [!DNL AEM Guides], müssen Sie möglicherweise Migrationsskripte ausführen. Aktualisierungsanweisungen finden Sie in den Versionshinweisen und der versionsspezifischen Dokumentation .

Nicht alle Aktualisierungspfade werden direkt unterstützt. Beispielsweise ist ein direktes Upgrade auf Version 4.0 nur ab Version 3.8 möglich. Wenn Sie eine Version vor Version 3.8 verwenden, finden Sie in der versionsspezifischen Dokumentation entsprechende Upgrade-Anweisungen. [Hilfe-Archiv](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).
Wenden Sie sich an Ihren Customer Success Manager, um den Aktualisierungspfad zu überprüfen.

**[!DNL AEM Guides]Builds**

Die folgende Liste enthält die neuesten [!DNL AEM Guides] Pakete, die für die Installation auf AMS oder On-Prem verfügbar sind, entsprechende AEM (Voraussetzungen), Downloadlinks von Paketen und weitere hilfreiche Informationen. Es wird empfohlen, nur den aktuellen Build von [!DNL AEM Guides]. Wenn Sie aus irgendeinem Grund Zugriff auf ältere Builds benötigen, stellen Sie bitte eine Verbindung zum Customer Success Manager Ihres Kontos her.

>[!NOTE]
>
>Wenden Sie sich an Ihren Customer Success Manager, um Zugriff auf [!DNL AEM Guides] Builds für AEM as a Cloud Service.

| [!DNL AEM Guides]Version  | Versionshinweise | AEM Voraussetzung | Downloadlinks erstellen |
|---|---|---|---|
| **AEM Guides 4.1** | [4.1.x - Versionshinweise](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html) | **Nicht-UUID und UUID 4.1.2**<br><br> AEM 6.5 SP13, SP12, SP11 oder SP10 <br>Java: 11 oder 8 <br><br>**Nicht-UUID und UUID 4.1**<br><br> AEM 6.5 SP13, SP12, SP11 oder SP10 | **Nicht-UUID**: <br> **AEM 6.5** <br>[4,1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-non-uuid%2Fcom.adobe.fmdita-6.5-4.1.159.zip)<br>[4.1.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-2%2F4-1-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.1.2.11.zip)<br>[4.1.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-3%2F4-1-3-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.1.3.2.zip)<br><br> **UUID** <br>**AEM 6.5** <br>[4,1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-uuid%2Fcom.adobe.fmdita-6.5-uuid-4.1.159.zip)<br>[4.1.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-2%2F4-1-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.1.2.11.zip)<br>[4.1.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-3%2F4-1-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.1.3.2.zip) |
| **AEM Guides 4.0** | [4.0.x - Versionshinweise](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html) | **Nicht-UUID und UUID 4.0.3**<br> AEM 6.5 SP12, SP11, SP10 oder SP9 <br>Java: 11 oder 8 <br><br> <br>**Nicht-UUID und UUID 4.0.2** <br> AEM 6.5 SP12, SP11, SP10 oder SP9 <br>Java: 11 oder 8 <br><br> **Nicht-UUID und UUID 4.0** <br> AEM 6.5 SP11, SP10 oder SP9 | **Nicht-UUID**: <br> **AEM 6.5** <br>[4,0,3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-hotfix-4.0.3.1.zip)<br>[4,0,2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.0.2.10.zip)  <br> [4.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-non-uuid/com.adobe.fmdita-6.5-4.0.70.zip)  <br><br> **UUID** <br>**AEM 6.5**  <br>[4,0,3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-hotfix-4.0.3.1.zip) <br>[4,0,2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.0.2.10.zip)<br> [4.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-uuid/com.adobe.fmdita-6.5-uuid-4.0.70.zip) |
| **AEM Guides 3.8.5** <br> 3.8.5 ist eine SP-Version, die auf Version 3.8 basiert. <br>Version 3.8 darf nicht eigenständig installiert werden, da Version 3.8.5 SP eine kritische Fehlerbehebung enthält. <br>Kunden müssen zuerst 3.8 und dann SP 3.8.5 installieren. | [3.8.x - Versionshinweise](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-3-8.html) | **Nicht-UUID** <br> AEM 6.5 SP9 oder SP8 <br> AEM 6.4 SP8 <br> AEM 6.3 SP3 <br><br> **UUID** <br> AEM 6.5 SP9 oder SP8 | **Nicht-UUID**: <br> **AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.5-hotfix-3.8.5.2.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.5-3.8.166.zip)<br> **AEM 6.4** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.4-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.4-3.8.166.zip) <br> **AEM 6.3** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.3-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.3-3.8.166.zip) <br><br> **UUID** <br>**AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5uuid/com.adobe.fmdita.uuid-6.5-hotfix-3.8.5.2.zip) <br> [3.8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8uuid/com.adobe.fmdita.uuid-6.5-3.8.168.zip) |
