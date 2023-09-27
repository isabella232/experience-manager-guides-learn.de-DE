---
title: PDF
description: Generieren und konfigurieren Sie die PDF-Ausgabe für FrameMaker-Dokumente in AEM Guides.
exl-id: ece004ed-5233-460b-889d-94e693ceed93
source-git-commit: 8504a0a52d381044bf1f0d6e7de3585ebecf3a7b
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

---

# PDF {#id205BB0T20RH}

Die folgenden Optionen sind für die PDF-Ausgabe verfügbar:

>[!NOTE]
>
> Um Ausgabevorgaben für PDF zu öffnen, klicken Sie auf eine FrameMaker \(`.fm` oder `.book`\), klicken Sie auf &quot;Ausgabevorgaben&quot;und dann auf die Option &quot;PDF-Ausgabe&quot;.

| PDF-Optionen | Beschreibung |
|-----------|-----------|
| Ausgabetyp | Der Typ der Ausgabe, die Sie generieren möchten. Um eine PDF-Ausgabe zu generieren, wählen Sie die Option PDF . |
| Einstellungsname | Geben Sie einen beschreibenden Namen für die PDF-Ausgabeeinstellungen ein, die Sie erstellen. Sie können beispielsweise *Interne Kundenausgabe* oder *Ausgabe der Endbenutzer*. |
| **Auftragseinstellungen** |
| Optionen | Wählen Sie die PDF-Vorgabe aus, die Sie zum Generieren der PDF-Ausgabe verwenden möchten. |
| Tagged-PDF generieren | Wählen Sie diese Option, um getaggte PDF zu generieren, die Informationen zum Dokumentinhalt und zur Dokumentstruktur enthalten. Diese Informationen werden von den Bildschirmlesehilfen verwendet. |
| PDF für jede Datei im Buch generieren | Wenn Sie die Ausgabe für eine Buchdatei generieren, wählen Sie diese Option, um für jede Buchdatei eine separate PDF zu generieren. |
| PDF nur für Überprüfung generieren | Wählen Sie diese Option aus, um PDF mit aktivierter Kommentarfunktion zu generieren. |
| Erstellen eines benannten Ziels für alle Elemente und Absätze | Wählen Sie diese Option aus, um benannte Ziele basierend auf Elementen und Absätzen zu erstellen. |
| **Anzeige-Einstellungen** |
| Dokument auf Seite öffnen | Geben Sie die Seitennummer an, die beim Öffnen der PDF angezeigt werden soll. |
| Anfangszoomfaktor | Wählen Sie den Zoomfaktor des Dokuments aus. |
| Registrierungszeichen | Um ein Dokument mit Zuschnittmarkierungen und Registrierungsmarkierungen zu drucken, wählen Sie eine Option aus der Dropdownliste Registrierungsmarken aus. |
| Seitenbreite und Seitenhöhe | Geben Sie die Breite und Höhe der Seite an. |
| Seitenbereich | Wählen Sie aus, ob Sie alle Seiten im Buch oder einen Seitenbereich veröffentlichen möchten. Wenn Sie Bereich auswählen, müssen Sie den Seitenbereich Von und Bis angeben. |
| CYMK in RGB konvertieren | Wählen Sie diese Option aus, um die CYMK-Farben in der generierten PDF in RGB zu konvertieren. |
| PDF-Lesezeichen erstellen | Erstellen Sie barrierefreie PDF mit Lesezeichen. |
| Zielpfad | Der Pfad in Ihrem AEM-Repository, in dem die PDF-Ausgabe gespeichert wird. |
| Workflow &quot;Nach der Erstellung ausführen&quot; | Wenn Sie diese Option wählen, wird eine neue Dropdownliste mit dem Workflow nach der Generierung angezeigt, die alle in AEM konfigurierten Workflows enthält. Sie müssen einen Workflow auswählen, der nach Abschluss des Workflows zur Generierung der Ausgabe ausgeführt werden soll. |

**Übergeordnetes Thema:**[ Ausgabe von FrameMaker-Dokumenten generieren](fm-output-generatation.md)
