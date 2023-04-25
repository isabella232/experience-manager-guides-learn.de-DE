---
title: Versionshinweise | Adobe Experience Manager-Handbücher as a Cloud Service, Version April 2022
description: April-Version der Adobe Experience Manager-Handbücher as a Cloud Service
exl-id: c735ba24-a803-454b-8723-57dacf90061b
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 3%

---

# April-Version der Adobe Experience Manager-Handbücher as a Cloud Service

## Aktualisierung auf die Version vom April

Aktuelles Upgrade durchführen [!DNL Adobe Experience Manager Guides] as a Cloud Service (später genannt) *[!DNL AEM Guides]as a Cloud Service*) einrichten, indem Sie die folgenden Schritte ausführen:
1. Sehen Sie sich den Git-Code des Cloud Services an und wechseln Sie zu der Verzweigung, die in der Cloud Services-Pipeline entsprechend der Umgebung konfiguriert ist, die Sie aktualisieren möchten.
1. Aktualisieren `<dox.version>` -Eigenschaft in `/dox/dox.installer/pom.xml` -Datei Ihres Cloud Services-Git-Codes auf 2022.4.133.
1. Übertragen Sie die Änderungen und führen Sie die Cloud Services-Pipeline aus, um auf die April-Version von zu aktualisieren. [!DNL AEM Guides] as a Cloud Service.

## Kompatibilitätsmatrix

In diesem Abschnitt wird die Kompatibilitätsmatrix für die von [!DNL AEM Guides] as a Cloud Service Version April 2022.

### FrameMaker und FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Nicht kompatibel | Aktualisierung 4 und höher für 2020 |
|  |  |


### Sauerstoffanschluss

| Cloud-Version für AEM Guides | Sauerstoff Connector Windows | Sauerstoff Connector Mac |
| --- | --- | --- |
| 2022.4.0 | 2.5.6 | 2.5.6 |
|  |  |  |

*Die in AEM erstellten Grundlinien und Bedingungen werden in FMPS-Versionen ab 2020.2 unterstützt.

## Neue Funktionen und Erweiterungen

Im Web-Editor wurden viele Verbesserungen und neue Funktionen hinzugefügt:

### Verbesserte Schlüsselauflösung

Ein DITA-Inhaltsschlüsselverweis fügt einen Teil des Inhalts von einem Thema in ein anderes. Es verwendet einen Schlüssel zum Suchen des Inhalts. Die Schlüsselverweise, die mit einem DITA-Thema verknüpft sind, müssen aufgelöst werden. Die ausgewählte Stammzuordnung hat die höchste Priorität, um Schlüsselverweise aufzulösen.

![Dialogfeld &quot;Benutzereinstellungen&quot;](assets/user-preferences.png)

Jetzt werden die Schlüsselverweise auf der Grundlage der in der folgenden Prioritätsreihenfolge festgelegten Stammzuordnung aufgelöst:

1. Benutzereinstellungen
1. Bedienfeld &quot;Landkartenansicht&quot;
1. Ordnerprofil

Weitere Informationen finden Sie unter *Schlüsselverweise auflösen* im Benutzerhandbuch.

### Hinzufügen eines benutzerdefinierten Bedienfelds im linken Bereich

Jetzt können Sie ein benutzerdefiniertes Bedienfeld im linken Bereich des Web-Editors hinzufügen. Sie können ein benutzerdefiniertes Bedienfeld für verschiedene Zwecke verwenden, z. B. Hilfe bereitstellen oder Tests für ein Projekt durchführen. Wenn ein benutzerdefiniertes Bedienfeld konfiguriert wurde, wird es auch in der Liste der Bedienfelder innerhalb der **Editor-Einstellungen**. Sie können den Schalter umschalten, um das benutzerdefinierte Bedienfeld ein- oder auszublenden.

### Möglichkeit, den Dokumentstatus von Themen in einer DITA-Zuordnung zu ändern

Jetzt können Sie den Dokumentstatus ausgewählter Themen in einer DITA-Zuordnung einfach ändern. Sie können die Eigenschaften ausgewählter Themen auch in einer DITA-Zuordnung über die **Weitere Optionen** Menü unten im Bedienfeld &quot;Kartenansicht&quot;.

![ausgewählte Themeneigenschaften](assets/map-view-properties.png)

### Im Vorschaumodus angezeigte Versionsinformationen

Der Web Editor hilft Ihnen bei der Verwaltung Ihrer Versionen. Jetzt können Sie auch die Version des aktiven Themas oder der DITA-Zuordnung oben rechts auf der Registerkarte &quot;Datei&quot;des Themas im Vorschaumodus eines Themas sehen.

![Vorschau Version](assets/preview-version.png)

## Behobene Probleme

Die in verschiedenen Bereichen behobenen Fehler sind unten aufgeführt:

* Neue Beschriftungen werden nicht automatisch im Dropdown-Menü &quot;Beschriftung hinzufügen/entfernen&quot;angezeigt. Stattdessen muss die Grundlinie aktualisiert werden. (9249)
* Der Grundlinientitel kann nicht bearbeitet werden, wenn eine Grundlinie durch Beschriftungskriterien erstellt wurde. (9171)
* Veröffentlichungsaufträge mit einer Grundlinie werden im Status &quot;Warten&quot;festgehalten, wenn der Grundlinienstatus zu &quot;Fehlgeschlagen&quot;geändert wird. (9194)
* Wenn Sie Beschriftungen für direkte Verweise entfernen, werden die Beschriftungen auch aus indirekten Verweisen entfernt. (9257)
* Die Suche während der Eingabe führt zu unerwünschten Suchanfragen in der Repository-Ansicht. (9307)
* Probleme treten auf, wenn ein beliebiger Suchbegriff im Titel für die Registerkarte verwendet wird. (9318)
* Die Grundlinie schlägt beim Hinzufügen einer Bezeichnung mit Leerzeichen fehl. (9362)
* AEM Site-Ausgabe zeigt das Glossarverwendungselement nicht korrekt an. (8936)
* Konsolenfehler tritt beim Öffnen der **Ausgabe** im Web Editor. (8715)
* Die Fehlermeldung, die bei der Veröffentlichung eines manuellen Datensatztyps über Salesforce angezeigt wird, ist nicht intuitiv. (8952)
* Die Einstellung Mit Bedingungsattributen validieren wird nicht sofort geöffnet. Stattdessen muss der Benutzer die Datei erneut öffnen, um die Validierungen anzuzeigen. (9300)
* Metadaten können nicht entfernt werden, nachdem eine DITA-Zuordnung mit Metadaten veröffentlicht wurde.  (9178)
* Das Übersetzungsfenster ist auch beim Öffnen der DITA-Karte im Map Editor sichtbar. (9053)
* Benutzerdefinierte DTD, die vom Benutzer definiert wird, hat keinen Vorrang vor standardmäßiger DITA-DTD, die in DITA-OT eingebettet ist. (9104)
* In der Funktion Native PDF schlägt der Upload in die Vorlagen bei Nicht-DITA- und Nicht-Bilddateien fehl. (9070)
* Der Autorisierungsmechanismus führt in einigen spezialisierten Szenarien zwei Abfragen anstelle einer aus. (9221)
* Das Veröffentlichen der AEM Site-Ausgabe schlägt bei der Verwendung der benutzerdefinierten DTD fehl. (9243)
* Die Fußnote &quot;Verwendung nach Referenz&quot;scrollt nicht zum Fußnote-Abschnitt in AEM Site-Ausgabe. (9234)

## Bekannte Probleme

Adobe hat das folgende bekannte Problem im [!DNL AEM Guides] as a Cloud Service April-Version.

* Der Web Editor meldet keinen Fehler, wenn zwei oder mehr Grundlinien mit demselben Namen erstellt werden, jedoch Unterschiede bei Leerzeichen oder Groß-/Kleinschreibung bestehen. Beispielsweise &quot;adobe&quot;und &quot;Adobe&quot;oder &quot;Adobe&quot;.
* Der Sauerstoff-Connector hängt zwischenzeitlich beim häufigen Anmelden, Abmelden oder Wechseln zwischen verschiedenen Authentifizierungstypen.
