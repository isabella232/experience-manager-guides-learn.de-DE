---
title: Weitere Funktionen im Map-Editor
description: Erfahren Sie, wie Sie andere Funktionen in den Map-Editoren verwenden.
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Weitere Funktionen im Map-Editor {#id1942D0T0HUI}

Einige allgemeine Funktionen im Basic- und Advanced Map Editor sind:

## Schlüsselverweise auflösen {#id176GD01H05Z}

einen DITA-Inhaltsschlüsselverweis oder `conkeyref` ist ein Mechanismus zum Einfügen eines Teils des Inhalts von einem Thema in ein anderes. Dieser Mechanismus verwendet den Schlüssel zum Auffinden des wiederzuverwendenden Inhalts anstelle des Mechanismus für die direkte Inhaltsreferenz. Weitere Informationen zu direkten und indirekten Verweisen in DITA finden Sie unter *DITA-Adressierung* in OASIS DITA Language Specification.

Wenn das DITA-Thema mit Schlüsselverweisen verknüpft ist, müssen diese vor der Vorschau, Bearbeitung oder Überprüfung eines Themas aufgelöst werden.

Die Schlüsselreferenzen werden auf der Grundlage der in der folgenden Prioritätsreihenfolge festgelegten Stammzuordnung aufgelöst:

1. Benutzereinstellungen
1. Bedienfeld &quot;Landkartenansicht&quot;
1. Ordnerprofil

Die in den Benutzereinstellungen ausgewählte Stammzuordnung hat die höchste Priorität, um Schlüsselverweise aufzulösen, gefolgt vom Bedienfeld Kartenansicht und der Stammzuordnung des Ordnerprofils. Wenn also in den Benutzereinstellungen keine Zuordnung festgelegt ist, wird die im Bedienfeld Kartenansicht geöffnete Karte verwendet. Wenn keine Zuordnung im Bereich &quot;Map View&quot;geöffnet ist, wird die in den Ordnerprofilen festgelegte Zuordnung verwendet, um die Schlüsselverweise aufzulösen.

Die Schlüsselreferenzen können in einer DITA-Map-Datei oder einer separaten DITA-Datei gespeichert werden. In AEM Handbüchern können Sie Schlüsselreferenzen entweder auf Projektebene oder auf Sitzungsebene angeben. Wenn bereits eine Stammzuordnung für die Benutzersitzung definiert ist, wird sie zum Auflösen der Schlüssel verwendet. Andernfalls wird die standardmäßige Stammzuordnung für diesen Ordner verwendet. Wenn keine standardmäßige Stammzuordnung konfiguriert ist, werden die fehlenden Schlüsselverweise für den Benutzer hervorgehoben.

Es gibt mehrere Möglichkeiten, wichtige Verweise in einem DITA-Thema zu lösen, indem die DITA-Zuordnung definiert wird, die an den folgenden Stellen verwendet werden soll:

**Projekteigenschaften** - Sie können eine Stammzuordnung zum Auflösen von Schlüsselverweisen beim Erstellen eines Projekts im Abschnitt Projekteigenschaften definieren.

Diese Stammzuordnung gilt für alle Assets \(Ordner und Unterordner\), die mit diesem Projekt verknüpft sind. Für Inhalte, die in mehreren Projekten referenziert werden, wird eine alphabetische Liste von Projekten verwaltet und die Standardstammkarte, die dem ersten Projekt zugeordnet ist, wird verwendet. Sie können auch die DITA-Zuordnung auswählen, die in der Liste zum Auflösen von Schlüsselverweisen verwendet werden soll.

**Themenvorschau** - Klicken Sie im Vorschaumodus &quot;Thema&quot;auf das Symbol Schlüsselauflösung in der Symbolleiste und wählen Sie die DITA-Datei aus, die für Schlüsselverweise verwendet werden soll.

**Ansicht &quot;Themenbearbeitung&quot;** - Klicken Sie beim Bearbeiten eines DITA-Themas auf das Symbol Schlüsselauflösung und wählen Sie die DITA-Datei aus, die zum Auflösen der Schlüsselverweise verwendet werden soll.

**Übergeordnetes Thema:**[ Arbeiten mit dem Map Editor](map-editor.md)

