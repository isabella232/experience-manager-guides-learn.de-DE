---
title: Benutzerverwaltung und Sicherheit
description: Erfahren Sie, wie die Benutzerverwaltung und Sicherheit funktionieren.
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 13%

---


# Benutzerverwaltung und Sicherheit {#id181AED00G5Z}

Um auf Funktionen in AEM Handbüchern zugreifen und diese konfigurieren zu können, müssen Sie Benutzer erstellen. Diesen Benutzern können dann Berechtigungen für den Zugriff auf alle oder bestimmte Funktionen in AEM Handbüchern zugewiesen werden. Erfahren Sie, wie Sie die Benutzerautorisierung konfigurieren und verwalten und verstehen Sie auch die Theorie, die dahinter steckt, wie Authentifizierung und Autorisierung in AEM funktioniert.

Die folgenden Themen in AEM Dokumentation helfen Ihnen dabei, die Konzepte und Funktionen der Benutzerverwaltung sowie sicherheitsrelevante Aspekte zu verstehen:

- [Benutzer und Gruppen in AEM](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#UsersandGroupsinAEM)

- [Berechtigungen in AEM](https://helpx.adobe.com/de/experience-manager/6-5/sites/administering/using/security.html#PermissionsinAEM)

- [Verwalten von Benutzenden und Gruppen](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#ManagingUsersandGroups)

- [Verwalten von Berechtigungen](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/security.html#ManagingPermissions)


## Von AEM Guides erstellte Benutzergruppen {#id181TF0K0MHT}

AEM Guides bieten drei native Gruppen zur Verwaltung verschiedener Aufgaben in einem DITA-Projekt. Diese Gruppen sind: *Autoren*, *Überprüfer* und *Herausgeber*. Abhängig von der Gruppe, der ein Benutzer zugeordnet ist, können er bestimmte Aufgaben ausführen. Beispielsweise kann eine Veröffentlichungsaufgabe nur von einem Herausgeber, aber nicht von einem Autor oder Überprüfer ausgeführt werden. Auf ähnliche Weise kann ein Autor ein neues Thema erstellen und ein Überprüfer kann nur ein Thema überprüfen.

>[!TIP]
>
> Siehe *Berechtigungen* im Handbuch Best Practices für Best Practices zum Festlegen von Benutzerberechtigungen.

In der folgenden Tabelle sind verschiedene Aufgaben und die Gruppen aufgeführt, die diese Aufgaben ausführen können:

| Aufgabe | Autoren | Prüfer | Herausgeber |
|----|-------|---------|----------|
| DITA-Thema erstellen | Ja |   | Ja |
| DITA Map erstellen | Ja |   | Ja |
| Sammlungen zuordnen | Ja |   | Ja |
| Bewertungsaufgabe erstellen | Ja |   | Ja |
| Thema überprüfen[1](#fntarg_1) | Ja | Ja | Ja |
| Schlüsselauflösung | Ja |   | Ja |
| Öffnen in FrameMaker | Ja |   | Ja |
| Auschecken/Einchecken | Ja |   | Ja |
| Thema bearbeiten | Ja |   | Ja |
| Verschieben-Thema | Ja |   | Ja |
| Eigenschaften von Themen bearbeiten | Ja |   | Ja |
| Kopieren | Ja |   | Ja |
| Löschen | Ja |   | Ja |
| Link freigeben | Ja |   | Ja |
| **Dokumentstatus** |
| Dokumentstatusprofil erstellen/bearbeiten |   |   | Ja |
| Dokumentstatus ändern[2](#fntarg_2) | Ja | Ja | Ja |
| **In der DITA Map Console verfügbare Funktionen \(Registerkarte &quot;Ausgabevorgaben&quot;\)** |
| Generieren |   |   | Ja |
| Bearbeiten |   |   | Ja |
| Duplizieren |   |   | Ja |
| Erstellen |   |   | Ja |
| Vorgabe löschen |   |   | Ja |
| **In der DITA Map Console verfügbare Funktionen \(Registerkarte &quot;Ausgaben&quot;\)** |
| Anzeigen der generierten Ausgabe | Ja |   | Ja |
| **In der DITA-Map-Konsole verfügbare Funktionen \(Registerkarte &quot;Themen&quot;\)** |
| Bewertungsaufgabe erstellen | Ja |   | Ja |
| Bearbeiten | Ja |   | Ja |
| **In der DITA Map Console verfügbare Funktionen \(Registerkarte &quot;Grundlinien&quot;\)** |
| Erstellen |   |   | Ja |
| Bearbeiten |   |   | Ja |
| Duplizieren |   |   | Ja |
| Remove |   |   | Ja |
| DITA-Map-Konsole \(Registerkarte &quot;Berichte&quot;\) | Ja |   | Ja |
| **In der DITA-Zuordnungskonsole verfügbare Funktionen \(Bedingungsvorgaben\)** |
| Bedingungsvorgabe erstellen/bearbeiten |   |   | Ja |

## Zusätzliche Hinweise zu Benutzergruppen

Die folgende Liste enthält einige Empfehlungen und Punkte, die sich auf Benutzergruppen und entsprechende Berechtigungen beziehen:

- Wenn Sie möchten, dass ein Benutzer den Übersetzungs- oder Überprüfungs-Workflow startet, stellen Sie sicher, dass der Benutzer Mitglied der *Herausgeber* und *Gruppe &quot;projects-administrators&quot;*.

- Benutzer müssen über die Lese-, Erstellungs-, Lösch- und Änderungsberechtigungen für die Ordner mit den Quell- und Zielsprachen verfügen, an denen sie arbeiten müssen.

- Wenn Sie ein Projekt erstellen, sind Sie der Eigentümer des Projekts mit *Herausgeber* Berechtigungen. Damit andere Benutzer in einem Projekt ihre Teammitglieder sehen, Aufgaben erstellen oder Workflows erstellen können, müssen sie Lesezugriff auf `/home/users` und `/home/groups` Knoten. Eine Möglichkeit, Lesezugriff auf `/home/users` und `/home/groups` -Knoten erhalten Lesezugriff auf die `projects-users` hinzugefügt.

- *Überprüfer* Sie können über die Projektkonsole oder über den Benachrichtigungslink im Posteingang auf Überprüfungskommentare zu einem Thema zugreifen und diese hinzufügen. Außerdem ist dieser Zugriff nur verfügbar, bis die Prüfungsaufgabe geöffnet ist.

- Standardmäßig *Herausgeber* erhalten Zugriff und Berechtigungen für die folgenden Ordner in DAM:

   - ``/var/dxml``–\> Lesen und Schreiben

   - `/content/dam/fmdita-outputs` –\> Lesen und Schreiben

   - `/content/output/sites` –\> Lesen und Schreiben

   Sie müssen Ihrem Herausgeber explizite Lese- und Schreibberechtigungen erteilen, wenn Sie neben den oben genannten standardmäßigen Veröffentlichungsorten einen anderen Speicherort verwenden.

- Alle Benutzer unter *Autoren*, *Überprüfer* und *Herausgeber* Gruppen haben Lesezugriff auf alle Inhalte in DAM.

- Berechtigungen auf Ordnerebene müssen Benutzern über die Benutzerverwaltungsseite zugewiesen werden.

- Wenn Sie möchten, dass Ihre Benutzer Suchvorgänge in DAM ausführen können, müssen Sie Ihre Benutzer zum Mitglied der *dam-users* hinzugefügt.

- Wenn Sie jedem Benutzer Administratorrechte gewähren möchten, können Sie ihm Zugriff über AEM Standardgruppen gewähren, z. B. *Administratoren*, *projects-administrators*, oder die OSGi-Konfiguration \(Felix Console\).

- Um Benutzern Berechtigungen zum Ändern des Dokumentstatus zu geben, stellen Sie sicher, dass Sie den Benutzer im Abschnitt Statusübergang des Dokumentstatusprofils hinzufügen.

[1](#fnsrc_1) Wenn *Autoren* und *Herausgeber* werden zur Überprüfung aufgefordert.[2](#fnsrc_2) Abhängig von den Berechtigungen, die dem Benutzer im Dokumentstatusprofil zugewiesen wurden.

