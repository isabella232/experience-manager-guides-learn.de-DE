---
title: Konfigurieren globaler Profile oder Profile auf Ordnerebene
description: Erfahren Sie, wie Sie globale Profile oder Profile auf Ordnerebene konfigurieren
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '3890'
ht-degree: 0%

---


# Konfigurieren globaler Profile oder Profile auf Ordnerebene {#id181AH2003PF}

In einem Unternehmen können verschiedene Gruppen oder Produkte verschiedene Authoring-Vorlagen, Ausgabevorlagen, bedingte Attributprofile \(oder Betreffschemata\) und Web-Editor-Konfigurationen verwenden. Die Konfiguration dieser Vorlagen nur auf Unternehmensebene (oder globaler Ebene) kann die Arbeit von Autoren erschweren, da ihnen Vorlagen oder Profile angezeigt werden, die für sie nicht relevant sind.

AEM Guides ermöglichen die Konfiguration von Authoring- \(Thema- oder Zuordnungsvorlagen), Ausgabevorlagen, bedingten Attributen und Web-Editor-Konfigurationen auf Unternehmensebene \(global\) sowie auf Ordnerebene. Auf diese Weise können Sie die Konfigurationen für verschiedene Abteilungen oder Produkte in Ihrem Unternehmen trennen.

Außerdem können Sie die ordnerspezifischen Konfigurationen an eine Abteilung oder Produktadministratoren delegieren, um die Verwaltung zu dezentralisieren.

Über die Kachel Ordnerprofile in den Einstellungen für Guides können Sie Einstellungen auf den folgenden Registerkarten konfigurieren:

- **Allgemein**: Die Registerkarte &quot;Allgemein&quot;ist verfügbar, wenn Sie Einstellungen auf Ordnerebene \(oder Projekt-/Produkteinstellungen\) konfigurieren. Sie können Einstellungen wie die Ordnerpfade konfigurieren, für die die Einstellungen gelten sollen, und Benutzer, die über Administratorrechte zum Erstellen oder Aktualisieren von Konfigurationen verfügen.

- **Bedingte Attribute**: Verwenden Sie diese Registerkarte, um bedingte Attribute auf globaler oder Ordnerebene zu konfigurieren. Ein bedingtes Attribut ist eine Kombination aus Attributname und -wert und Sie können auch eine Bezeichnung dafür definieren. Sie können die standardmäßigen DITA-Attribute oder Ihre eigenen benutzerdefinierten Attribute verwenden. Die von Ihnen auf globaler Ebene definierten bedingten Attribute werden allen Benutzern projektübergreifend zur Verfügung gestellt. Wenn Sie bedingte Attribute auf Ordnerebene definiert haben, werden sie mit den global definierten bedingten Attributen zusammengeführt.

- **Authoring-Vorlage**: Verwenden Sie diese Registerkarte, um die Vorlagen zu konfigurieren, die Ihre Autoren zum Erstellen von DITA-Inhalten verwenden werden. Die folgenden Themenvorlagen sind standardmäßig verfügbar:

   - Glossar

   - Verweis

   - Thema

   - Konzept

   - Aufgabe

   - Fehlerbehebung

   - Leer

   - DITAVAL
   >[!NOTE]
   >
   > Sie können jede vorhandene Vorlage als Grundlage für die Erstellung neuer Vorlagen verwenden. Die leere DITA-Vorlage enthält keine Struktur oder Elemente wie die anderen Vorlagen. Sie können jede der OOTB-DITA-Vorlagen als Basis verwenden, Änderungen daran vornehmen und sie mit einem anderen Namen speichern. Nachdem Sie die erforderlichen Änderungen vorgenommen haben, fügen Sie die aktualisierte Vorlage zur Konfiguration der globalen oder auf Ordnerebene erstellten Authoring-Vorlagen hinzu und sie steht dann für das Authoring zur Verfügung.

   Neben Themenvorlagen können Sie auch die Zuordnungsvorlagen definieren, die Autoren zur Verfügung gestellt werden. Die folgenden Zuordnungsvorlagen sind standardmäßig verfügbar:

   - Map

   - Lesezeichen


- **Ausgabevorgabe**: Ähnlich wie bei Authoring-Vorlagen gibt es fünf vorkonfigurierte Ausgabevorgaben:

   - AEM Site

   - PDF

   - HTML 5

   - EPUB

   - Benutzerdefiniert
   Herausgeber können diese vordefinierten Ausgabevorgaben verwenden, um Inhalte zu veröffentlichen. Diese Vorgaben können von einem Administrator des Profils auf globaler oder Ordnerebene konfiguriert werden. Nach der Konfiguration stehen die Veröffentlichungsvorgaben den Herausgebern für neu erstellte DITA-Maps zur Verfügung. Sie können Veröffentlichungsvorgaben auch auf vorhandene DITA-Maps anwenden, siehe [Vorgabenänderungen anwenden](#id18AGD0K0OHS) für weitere Details.

- **XML-Editor-Konfigurationen**: Verwenden Sie diese Registerkarte, um das Erscheinungsbild und die verschiedenen Funktionen des Web-Editors anzupassen. Die folgenden konfigurierbaren Einstellungen sind für den Web Editor verfügbar:

   - Konfiguration der Benutzeroberfläche des XML-Editors
   - CSS-Vorlagenlayout
   - XML-Editor-Snippets
   - Beschriftungen der XML-Inhaltsversion
   - Rootmap \(nur auf Ordnerebene\)

Sie können sowohl globale Profile als auch Profile auf Ordnerebene konfigurieren. In einem Profil auf Ordnerebene können Sie die Ordner definieren, für die die Einstellungen gelten sollen. Zu diesen Einstellungen gehören die bedingten Attribute, Bearbeitungsvorlagen, Ausgabevorgaben und Einstellungen des XML-Editors. Die Konfigurationen für bedingte Vorgaben, Authoring-Vorlagen und XML-Editor werden dann Autoren zur Verfügung gestellt, die in den konfigurierten Ordnern arbeiten. Auf ähnliche Weise haben Herausgeber Zugriff auf die konfigurierten Ausgabevorgaben, die in den konfigurierten Ordnern definiert sind.

Ein Profil auf Ordnerebene überschreibt die im globalen Profil konfigurierten Einstellungen. Anders ausgedrückt: Wenn ein Ordner über ein Profil auf Ordnerebene verfügt, werden die Authoring-Vorlagen, Ausgabevorlagen und XML-Editor-Einstellungen angezeigt, die im entsprechenden Ordnerprofil konfiguriert sind. Die im globalen Profil konfigurierten Einstellungen werden nicht angezeigt. Dies gilt jedoch nicht für die bedingten Attribute. Bei bedingten Attributen werden die bedingten Attribute auf globaler Ebene und auf Ordnerebene zusammengeführt.

Die folgenden Abschnitte führen Sie durch den Prozess der Konfiguration globaler Profile auf Profil- und Ordnerebene.

## Globales Profil konfigurieren

Führen Sie die folgenden Schritte aus, um das globale Profil zu konfigurieren:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die Schaltfläche **Ordnerprofile**.

   Zum ersten Mal wird die Seite Ordnerprofile nur mit der Kachel Globales Profil angezeigt.

1. Klicken Sie auf **Globales Profil** Kachel.

1. So konfigurieren Sie **Bedingte Attribute**, siehe [Bedingte Attribute für globale Profile oder Profile auf Ordnerebene konfigurieren](#id1889D0I305Z).

1. So konfigurieren Sie **Authoring-Vorlage**, siehe [Bearbeitungsvorlagen konfigurieren](#id1889D0IL0Y4).

1. So konfigurieren Sie **Ausgabevorgaben**, siehe [Konfigurieren von Ausgabevorgaben](#id18AGD0IH0Y4).

1. Informationen zum Konfigurieren der XML-Editor-Konfiguration finden Sie unter [Konfigurieren und Anpassen des XML-Web-Editors](#id2065G300O5Z).

1. Nachdem Sie alle erforderlichen Aktualisierungen vorgenommen haben, speichern und schließen Sie die **Globales Profil**.


## Erstellen und Konfigurieren eines Profils auf Ordnerebene

Führen Sie die folgenden Schritte aus, um ein Profil auf Ordnerebene zu konfigurieren:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die **Ordnerprofile** Kachel.

   Zum ersten Mal wird die Seite Ordnerprofile nur mit der Standardkachel Globales Profil angezeigt.

1. Klicken Sie auf **Erstellen**.

1. Geben Sie die folgenden Details in die **Ordnerprofil erstellen** dialog:
   - Name des Ordnerprofils.
   - Pfad des Ordners, in dem das Profil anwendbar sein soll.

      >[!NOTE]
      >
      > Sie können nicht mehrere Ordnerprofile auf einen Ordner anwenden. Stellen Sie sicher, dass auf den Ordner, den Sie hier auswählen, kein anderes Profil angewendet wird. Im Fall von über- und untergeordneten Ordnern mit eigenen spezifischen Profilen verwendet der untergeordnete Ordner die Konfigurationen aus seinem eigenen Profil. Die Konfigurationen aus dem übergeordneten Ordner überschreiben nicht die Konfigurationen eines untergeordneten Ordners.

1. Klicken Sie auf **Erstellen**.

   Auf der Seite Ordnerprofile wird eine neue Kachel mit dem Namen des Ordnerprofils erstellt

1. Klicken Sie auf die Kachel Ordnerprofil , um sie zu bearbeiten.

   Es wird eine Registerkarte Allgemein mit dem Namen des Ordnerprofils und den konfigurierten Ordnerinformationen angezeigt.

1. Klicken **Bearbeiten** , um mehrere Ordner und Benutzer hinzuzufügen, die Administratorzugriff haben, um das Ordnerprofil zu ändern.

   >[!NOTE]
   >
   > Benutzer, die Sie hier hinzufügen, verfügen über die Administratorrechte zum Aktualisieren der bedingten Attribute, der Bearbeitungsvorlage und der für dieses Ordnerprofil konfigurierten Ausgabevorgaben.

1. Um einen Ordner hinzuzufügen, klicken Sie auf das Symbol Durchsuchen im Ordnerpfad, navigieren Sie zu einem Ordner, wählen Sie ihn aus und klicken Sie auf Hinzufügen , um ihn diesem Profil hinzuzufügen.

   >[!NOTE]
   >
   > Stellen Sie sicher, dass dem Ordner, den Sie hier auswählen, kein anderes Profil auf Ordnerebene zugeordnet ist.

1. Um einen Benutzer hinzuzufügen, wählen Sie einen Benutzer aus der **Admin-Benutzer** Dropdown-Liste und klicken Sie auf **Hinzufügen**.

   >[!NOTE]
   >
   > Sie können dem Ordnerprofil aus der Dropdownliste mehrere Benutzer hinzufügen. Sie können auch einen vorhandenen Administrator aus der Liste entfernen, indem Sie auf das Löschsymbol neben der Benutzer-ID klicken.

1. Nachdem Sie alle erforderlichen Ordner und Benutzer zum Ordnerprofil hinzugefügt haben, klicken Sie auf **Speichern**.


Jetzt können Sie die bedingten Attribute, Bearbeitungsvorlagen, Ausgabevorgaben und den XML-Editor konfigurieren.

>[!IMPORTANT]
>
> Wenn Sie ein Ordnerprofil erstellen, enthält es standardmäßig keine Authoring-Vorlagen. Sie müssen die erforderlichen Authoring-Vorlagen zum Ordnerprofil hinzufügen, damit sie für Ihre Autoren verfügbar sind.

## Bedingte Attribute für globale Profile oder Profile auf Ordnerebene konfigurieren {#id1889D0I305Z}

Führen Sie die folgenden Schritte aus, um standardmäßige DITA-unterstützte bedingte Attribute auf globaler oder Ordnerebene zu konfigurieren:

1. Melden Sie sich bei Adobe Experience Manager als Administrator oder Benutzer mit Administratorrechten für ein Profil auf Ordnerebene an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die **Ordnerprofile** Kachel.

1. Klicken Sie auf die Profilkachel, die Sie konfigurieren möchten.

   >[!NOTE]
   >
   > Sie können bedingte Attribute im Profil &quot;Global&quot;oder in einem Profil auf Ordnerebene konfigurieren.

1. Klicken Sie auf der Profilseite auf die **Bedingte Attribute** Registerkarte.

1. Klicken Sie auf **Bearbeiten**.

1. Klicken Sie auf **Hinzufügen**.

1. Geben Sie die **Name**, **Wert** und **Titel** für das bedingte Attribut.

   Sie können ein Profil mit nur dem Attributnamen speichern. Ein Attribut kann jedoch nur verwendet werden, wenn dafür ein Wert angegeben ist. Wenn Sie für ein Attribut - Wert und Titel angeben, zeigt der Web Editor die Bezeichnung des bedingten Attributs an. Außerdem wird der Titel dem Publishing-Administrator zum Zeitpunkt der Erstellung einer bedingten Vorgabe angezeigt.

   Der folgende Screenshot zeigt die Definition der `platform` -Attribut mit möglichen Werten und Bezeichnungen.

   ![](assets/add_profile.png){width="650" align="left"}

1. Wenn Sie weitere Werte für dasselbe Attribut hinzufügen möchten, klicken Sie auf die **+** und geben Sie den zusätzlichen Wert und die Bezeichnung ein.

1. Wenn Sie weitere Attribute hinzufügen möchten, klicken Sie auf **Hinzufügen**.

1. Klicken Sie auf **Speichern**.


**Verwenden benutzerdefinierter Attribute**

Wenn Sie ein benutzerdefiniertes Attribut verwenden, muss es sich um ein gültiges DITA-Attribut handeln, das von der DTD unterstützt wird. Wenn Sie ein beliebiges Attribut verwenden möchten, das kein standardmäßiges DITA-Attribut ist, führen Sie die folgenden zusätzlichen Schritte aus:

1. Fügen Sie das benutzerdefinierte Attribut zur DTD-Datei hinzu. Wenn Ihre DTD-Datei beispielsweise &quot;commonElements.mod&quot;ist, müssen Sie diese Datei im DTD-Ordner suchen. Der Standardpfad der System-DTD-Datei lautet:

   /libs/fmdita/dita\_resources/DITA-1.3/dtd/base/dtd/commonElements.mod

   >[!IMPORTANT]
   >
   > Die spezielle DTD-Datei sollte Teil der Bereitstellung von benutzerspezifischem Code sein. DTDs unter /etc sind Teil der Produktbereitstellung und werden daher bei der Installation neuer Versionen überschrieben. Es wird empfohlen, spezialisierte DTD unter /apps im Projektordner hinzuzufügen und den DTD/Katalogpfad in das DITA-Profil einzuschließen. Weitere Informationen finden Sie unter [Integrieren der DITA-Spezialisierung](dita-ot-specialization.md#id211MB0E00XA).

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

1. Suchen Sie nach und klicken Sie auf *com.adobe.fmdita.config.ConfigManager* Bundle.

1. Speichern Sie die Konfiguration.

   Dadurch wird der System-Cache gelöscht.

1. Navigieren Sie zur Datei &quot;condAttrList.xml&quot;, die unter folgendem Speicherort verfügbar ist:

   /libs/fmdita/config/condAttrList.xml

1. Erstellen Sie einen Überlagerungsknoten des `config` -Ordner in `apps` Knoten.

1. Navigieren Sie zur Datei &quot;condAttrList.xml&quot;und fügen Sie sie der Datei &quot;condAttrList.xml&quot;im `apps` node:

   `/apps/fmdita/config/condAttrList.xml`

1. Speichern Sie die Datei.

1. Fügen Sie benutzerdefinierte Attribute zum Profil auf globaler Ebene oder auf Ordnerebene hinzu.


## Bearbeitungsvorlagen konfigurieren {#id1889D0IL0Y4}

AEM Guides sind mit 7 nativen Bearbeitungsvorlagen und 2 DITA-Zuordnungsvorlagen ausgestattet. Sie können festlegen, dass nur einige Vorlagen für Ihre Autoren verfügbar sind. Wenn Sie eine benutzerdefinierte Vorlage verwenden, kann diese konfiguriert und für das Authoring bereitgestellt werden. Auf der Registerkarte &quot;Authoring-Vorlage&quot;in der Konfiguration von Ordnerprofilen können Sie Themen- oder Zuordnungsvorlagen aus globalen Profilen oder Profilen auf Ordnerebene hinzufügen oder entfernen.

Sie können auch vor dem Konfigurieren der Themen- oder Zuordnungsvorlagen auf globaler oder Ordnerebene einen Speicherort für Ihre benutzerdefinierten Authoring-Vorlagen definieren. Informationen zum Konfigurieren eines benutzerdefinierten Speicherorts zum Speichern von Bearbeitungsvorlagen finden Sie unter [Benutzerdefinierten DITA-Vorlagenordnerpfad konfigurieren](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z).

Führen Sie die folgenden Schritte aus, um das Thema oder die Zuordnungsvorlagen zu einem Ordnerprofil hinzuzufügen:

1. Melden Sie sich bei Adobe Experience Manager als Administrator oder Benutzer mit Administratorrechten für ein Profil auf Ordnerebene an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die **Ordnerprofile** Kachel.

1. Klicken Sie auf die Profilkachel, die Sie konfigurieren möchten.

   >[!NOTE]
   >
   > Sie können die Authoring-Vorlage im Profil &quot;Global&quot;oder in einem Profil auf Ordnerebene konfigurieren.

1. Klicken Sie auf der Profilseite auf die **Authoring-Vorlage** Registerkarte.
1. Klicken Sie auf **Bearbeiten**.

   Sie erhalten die Optionen zum Hinzufügen von Themen- und Zuordnungsvorlagen, indem Sie vom Standardspeicherort aus suchen oder nach ihnen suchen.

   >[!NOTE]
   >
   > Standardmäßig werden alle Authoring-Vorlagen im Ordner /content/dam/dita-templates gespeichert. Die `dita-templates` Ordner enthält `topics` und `maps` Unterordner zum Speichern der Themen- und Zuordnungsvorlagen. Sie können Ihre benutzerdefinierten Vorlagen \(.dita,.xml oder .ditamapfiles\) in die Standardordner für Vorlagen einfügen. Nachdem Sie Ihre Vorlage im Standardordner hinzugefügt haben, können Sie sie dem globalen Ordner oder dem Ordnerprofil hinzufügen. Weitere Informationen zum Erstellen benutzerdefinierter Vorlagen mit dem Web Editor finden Sie unter [Benutzerdefinierte Authoring-Vorlage erstellen](#id1917D0EG0HJ).

   ![](assets/search-author-temp.png){width="550" align="left"}

1. Fügen Sie Ihrem Profil das erforderliche Thema hinzu und ordnen Sie ihm Vorlagen zu.

   Um eine Vorlage hinzuzufügen, führen Sie einen der folgenden Schritte aus:

   - Auswählen **Suche oder Typ** und geben Sie den Namen einer Vorlage ein oder wählen Sie ihn aus der Dropdown-Liste aus. Die Dropdown-Liste enthält alle Standardvorlagen und alle neuen Vorlagen, die Sie erstellt haben.

      ![](assets/default-template-list.png){width="350" align="left"}

   - Klicken **Durchsuchen** und wählen Sie eine Vorlage aus DAM aus.

1. Klicken Sie auf **Hinzufügen**.

   Die ausgewählten Vorlagen werden der Vorlagenliste hinzugefügt.

   ![](assets/author-templ-added-list.png){width="550" align="left"}

   >[!NOTE]
   >
   > Sie können die Reihenfolge der Vorlagen ändern, indem Sie sie an die gewünschte Position in der Liste ziehen. Die Position von Vorlagen steuert die Reihenfolge, in der sie auf der Blueprint-Seite im Workflow für die Themen- oder Zuordnungserstellung angezeigt werden.

1. Klicken Sie auf **Speichern**.


Falls Sie die Vorlagen für ein Profil auf Ordnerebene konfiguriert haben, werden die konfigurierten Vorlagen dem konfigurierten Ordner zugeordnet. Alle im konfigurierten Ordner erstellten Projekte haben Zugriff auf nur die Vorlagen, die im Profil auf Ordnerebene konfiguriert sind.

## Benutzerdefinierte Authoring-Vorlage erstellen {#id1917D0EG0HJ}

AEM Guides bieten eine einfache Möglichkeit, Authoring-Vorlagen zu erstellen. Als Systemadministrator können Sie den Web Editor verwenden, um von Grund auf Bearbeitungsvorlagen zu erstellen. Anschließend können Sie die neue Vorlage im globalen Profil hinzufügen oder sie mithilfe des ordnerspezifischen Profils einem bestimmten Ordner zuweisen.

Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Authoring-Vorlage zu erstellen:

1. Melden Sie sich bei Adobe Experience Manager als Administrator an.

1. Navigieren Sie in der Assets-Benutzeroberfläche zu dem Ordner, der zum Speichern der Vorlagendateien konfiguriert ist. Standardmäßig werden alle Themenvorlagen im Ordner /content/dam/dita-templates/topics gespeichert.

   >[!NOTE]
   >
   > Informationen zum Konfigurieren eines benutzerdefinierten Speicherorts zum Speichern von Themen oder Zuordnungsvorlagen finden Sie unter [Benutzerdefinierten DITA-Vorlagenordnerpfad konfigurieren](conf-template-tags-custom-dita-topic-template.md#id191LCF0095Z)

1. Klicken **Erstellen** \> **DITA-Vorlage**.

1. Wählen Sie auf der Blueprint-Seite den Typ der DITA-Themenvorlage aus, die Sie erstellen möchten.

   >[!NOTE]
   >
   > Sie können die Vorlage &quot;Leer&quot;von Grund auf verwenden. Die leere Vorlage enthält keine Struktur oder Elemente.

1. Klicken Sie auf **Weiter**.

1. Geben Sie auf der Seite mit den neuen Vorlageneigenschaften eine **Titel**, **Name** und **Beschreibung** für die Vorlage.

   >[!NOTE]
   >
   > Der Name wird basierend auf dem Titel der Vorlage automatisch vorgeschlagen. Wenn Sie den Namen manuell angeben möchten, stellen Sie sicher, dass der Name keine Leerzeichen, Apostroph oder Klammern enthält und mit .dita endet.

1. *\(Optional\)* Klicken Sie auf **Miniatur hinzufügen** zum Browser für und wählen Sie eine Miniaturansicht aus, die mit Ihrer Vorlage verknüpft werden soll.

1. Klicken Sie auf **Erstellen**.

   Die Meldung Thema erstellt wird angezeigt.

   Sie können die Vorlage zur Bearbeitung im Web-Editor öffnen oder die Vorlagendatei im Vorlagenspeicherort speichern. Nachdem die Vorlage erstellt wurde, können Sie den Web Editor verwenden, um die Vorlage entsprechend Ihren Authoring-Anforderungen anzupassen. Nachdem eine Vorlage erstellt wurde, stellen Sie sicher, dass Sie sie entweder mit einem globalen Profil oder einem Profil auf Ordnerebene verknüpfen.


## Konfigurieren von Ausgabevorgaben {#id18AGD0IH0Y4}

In einer typischen Unternehmensumgebung können für verschiedene Produkte oder Benutzerhandbücher unterschiedliche Ausgabevorlagen verwendet werden. Es kann auch einige gängige Prozesse zur Generierung von Ausgaben geben, die von allen Herausgebern verwendet werden sollten, sowie eine Reihe spezifischer Prozesse zur Generierung von Ausgaben für eine bestimmte Gruppe von Herausgebern oder Projekten.

Mit AEM Guides kann der Administrator Ausgabevorgaben mit bestimmten Einstellungen erstellen, die dann von allen oder einem bestimmten Satz von Herausgebern zum Generieren der Ausgabe verwendet werden können. Beispielsweise kann der Administrator eine Ausgabevorgabe erstellen, um ein Benutzerhandbuch zu generieren, das für alle Herausgeber gleich ist. Und eine andere, um die Programmier-Benutzer-Handbücher zu erstellen, die für eine Reihe von Herausgebern spezifisch sind. Beide Vorgaben können für die Verwendung verschiedener Ausgabevorlagen konfiguriert werden. In diesem Beispiel kann die allgemeine Veröffentlichungsvorgabe für die Generierung des Benutzerhandbuchs auf globaler Ebene konfiguriert werden. Außerdem kann die Ausgabevorgabe zum Generieren des Programmierhandbuchs auf Ordnerebene konfiguriert werden.

Nachdem die standardmäßigen Ausgabevorgaben im System erstellt wurden, verwenden alle DITA-Maps, die danach erstellt wurden, die Standardvorgaben, um die Ausgabe zu generieren. Alle vorhandenen DITA-Maps verwenden jedoch weiterhin die Ausgabevorgaben, die zuvor mit ihnen konfiguriert wurden. Wenn Sie die neue Ausgabevorgabe auf alle vorhandenen DITA-Maps anwenden möchten, müssen Sie den Workflow Vorgabenänderungen anwenden ausführen.

Zusätzlich zu den auf globaler oder Unternehmensebene konfigurierten Vorgaben hätte ein Herausgeber weiterhin die Berechtigung, mehr Ausgabevorgaben zu erstellen. Diese Vorgaben sind jedoch an die DITA-Map gebunden, für die sie erstellt werden. Weitere Informationen zum Erstellen regulärer Ausgabevorgaben für eine DITA-Zuordnung finden Sie unter *Ausgabevorgabe erstellen, bearbeiten, duplizieren oder entfernen* im *Verwenden von Adobe Experience Manager-Handbüchern*.

Führen Sie die folgenden Schritte aus, um globale oder ordnerspezifische Ausgabevorgaben zu konfigurieren:

1. Melden Sie sich bei Adobe Experience Manager als Administrator oder Benutzer mit Administratorrechten für ein ordnerspezifisches Profil an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die **Ordnerprofile** Kachel.

1. Klicken Sie auf die Profilkachel, die Sie konfigurieren möchten.

   >[!NOTE]
   >
   > Sie können Ausgabevorgaben im globalen Profil oder in einem ordnerspezifischen Profil konfigurieren.

1. Auf der Profilseite. Klicken Sie auf **Ausgabevorgaben** Registerkarte.

   Es wird eine Liste mit vordefinierten Ausgabevorgaben angezeigt, die AEM Site, PDF, HTML5, EPUB und benutzerdefiniertes Modell umfasst.

1. Führen Sie einen der folgenden Schritte aus, um eine Ausgabevorgabe zu erstellen oder zu bearbeiten:

   - Klicken **Erstellen** , um eine neue Ausgabevorgabe von Grund auf neu zu erstellen.
   - Klicken Sie auf Duplizieren , um eine Kopie der ausgewählten Ausgabevorgabe zu erstellen. Sie können Änderungen an der duplizierten Vorgabe vornehmen und sie speichern.

   - Klicken **Bearbeiten** , um die Konfiguration der ausgewählten Vorgabe zur Bearbeitung zu öffnen.

      Weitere Informationen zu den Ausgabevorgabeneinstellungen finden Sie unter *Grundlegendes zu den Ausgabevorgaben* in den Benutzerhandbüchern zu Adobe Experience Manager.

1. Klicken **Speichern** , um die voreingestellten Einstellungen zu speichern.


Alle DITA-Maps, die danach erstellt oder hochgeladen wurden, verfügen über die neue oder aktualisierte Ausgabevorgabe.

## Vorgabenänderungen anwenden {#id18AGD0K0OHS}

Eine neue, auf globaler Ebene erstellte Ausgabevorgabe wird allen neuen DITA-Maps zur Verfügung gestellt, die Sie in Zukunft erstellen. Wenn eine neue Ausgabevorgabe auf Ordnerebene erstellt wird, wird diese Vorgabe für alle Maps verfügbar gemacht, die im konfigurierten Ordner erstellt werden. Standardmäßig wird eine neue Ausgabevorgabe für keine vorhandene DITA-Zuordnung verfügbar gemacht.

Wenn Sie eine vorhandene Ausgabevorgabe aktualisiert haben oder eine neue Ausgabevorgabe für vorhandene DITA-Maps verfügbar machen möchten, führen Sie die folgenden Schritte aus:

1. Melden Sie sich bei Adobe Experience Manager als Administrator oder Benutzer mit Administratorrechten für ein ordnerspezifisches Profil an.

1. Klicken Sie oben auf den Adobe Experience Manager-Link und wählen Sie **Instrumente**.

1. Auswählen **Handbücher** aus der Liste der Tools und klicken Sie auf die **Ordnerprofile** Kachel.

1. Klicken Sie auf die Profilkachel, die Sie konfigurieren möchten.

   >[!NOTE]
   >
   > Sie können Ausgabevorgaben im globalen Profil oder in einem ordnerspezifischen Profil konfigurieren.

1. Auf der Profilseite. Klicken Sie auf **Ausgabevorgaben** Registerkarte.

   Es wird eine Liste mit vordefinierten Ausgabevorgaben angezeigt, die AEM Site, PDF, HTML5, EPUB und benutzerdefiniertes Modell umfasst.

1. Wählen Sie die Ausgabevorgabe aus, die Sie auf vorhandene DITA-Maps anwenden möchten.

1. Klicken **Vorgabenänderungen anwenden** in der Hauptsymbolleiste.

1. Im Dialogfeld Vorgabenänderungen anwenden können Sie aus folgenden Optionen auswählen:

   - **Auswählen der Option &quot;Vorhandene Vorgabe überschreiben&quot;**: Wenn Sie diese Option auswählen, überschreiben alle Aktualisierungen, die Sie in den vorhandenen Ausgabevorgaben vorgenommen haben, die Einstellungen in allen vorhandenen DITA-Maps, in denen diese Vorgabe verwendet wird. Dies führt jedoch zum Verlust vorhandener bedingter Vorgabe- und Basisinformationen, die mit der Zuordnung verknüpft sind.

   - **Nicht auswählen Option &quot;Vorhandene Vorgabe überschreiben&quot;**: Wenn Sie diese Option nicht auswählen, wirken sich die Aktualisierungen, die Sie in den vorhandenen Ausgabevorgaben vorgenommen haben, nicht auf die vorhandenen DITA-Maps aus. Nur die neu hinzugefügten Vorgaben werden zu den vorhandenen DITA-Maps hinzugefügt. Beachten Sie, dass die neu erstellte DITA-Zuordnung sowohl die aktualisierten Ausgabevorgaben als auch die neu hinzugefügten Vorgaben erhält.

1. Klicken **OK** , um Änderungen aus den ausgewählten Ausgabevorgaben auf alle vorhandenen DITA-Maps anzuwenden.


## Konfigurieren und Anpassen des XML-Web-Editors {#id2065G300O5Z}

Standardmäßig enthält der XML-Web-Editor eine Vielzahl von Funktionen, die Ihren Autoren beim Erstellen von DITA-Dokumenten helfen. Wenn Sie in einer restriktiven Umgebung arbeiten, können Sie auswählen, welche Funktionen Ihren Autoren zur Verfügung stehen. Auf der Registerkarte &quot;Konfiguration des XML-Editors&quot;können Sie die Funktionen einfach steuern und auch das Erscheinungsbild Ihres Web-Editors ändern. Als Administrator können Sie die folgenden Komponenten des Web-Editors anpassen:

**Konfiguration der Benutzeroberfläche des XML-Editors**

Diese Einstellung steuert die Symbolleiste und die anderen Elemente der Benutzeroberfläche des Web Editors. Klicken Sie auf **Download** -Symbol, um die neueste Datei ui\_config.json auf Ihr lokales System herunterzuladen. Anschließend können Sie Änderungen an der Datei vornehmen und die Datei hochladen. Klicken Sie auf **Download-Standard**-Symbol, um die Standarddatei ui\_config.json auf Ihr lokales System herunterzuladen. Sie können die Standarddatei jederzeit herunterladen, Änderungen daran vornehmen und sie hochladen. Abhängig davon, wo Sie die Datei hochladen, ob es sich um ein globales Profil oder ein Profil auf Ordnerebene handelt, werden die Änderungen entsprechend angewendet. Weitere Informationen zum Anpassen des XML-Editors mithilfe der Datei ui\_config.json finden Sie unter [Symbolleiste anpassen](conf-web-editor-customize-toolbar.md#).

**CSS-Vorlagenlayout**

Laden Sie die in diesem Abschnitt verfügbare Datei herunter, um das Erscheinungsbild Ihres Dokuments bei der Vorschau oder beim Öffnen zur Bearbeitung im Web Editor anzupassen. Die standardmäßige CSS-Datei, die heruntergeladen werden kann, ist nur eine Testdatei, die nicht für die Anpassung verwendet werden sollte. Sie können eine CSS-Datei mit Anpassungen für den Web-Editor erstellen und diese hochladen. Sie können beispielsweise eine .css-Datei mit folgendem Code erstellen:

```css
.title {    font-size: 9em;}
```

Speichern Sie diese Datei und laden Sie sie im Abschnitt CSS-Vorlagenlayout hoch. Wenn Sie die Datei das nächste Mal herunterladen, erhalten Sie die neueste CSS-Datei, die im Web Editor verwendet wird.

**XML-Editor-Snippets**

Mithilfe der Konfigurationsdatei in diesem Abschnitt können Sie einige standardmäßige Snippets erstellen und sie für Ihre Autoren freigeben. Die Standardstruktur der Datei ist unten angegeben:

```css
{
   "snippetID": {
      "name": "snippet Name",
      "description": "snippet Description",
      "value": "<i>this is snippet value</i>"
  }
}
```

Die folgenden Details sind zum Erstellen eines Snippets erforderlich:

- **snippetID:**   Eine eindeutige ID für das Snippet. Es kann einen alphanumerischen Wert annehmen.

- **name:**   Ein beschreibender Name zur Identifizierung des Codeausschnitts. Dieser Name wird im Bedienfeld &quot;Snippets&quot;angezeigt.

- **description:**   Fügen Sie eine beschreibende Information für das Snippet hinzu.

- **Wert:**   Geben Sie den XML-Code des Snippets an.

>[!NOTE]
>
> Sie können weitere Snippets hinzufügen, indem Sie am Ende Ihrer Snippet-Definition ein Komma \(,\) hinzufügen und dieselbe Struktur für das nächste Snippet wiederholen.

**Beschriftungen der XML-Inhaltsversion**

Autoren können standardmäßig Titel ihrer Wahl erstellen und sie mit ihren Themendateien verknüpfen. Dies kann jedoch zu vielen Variationen derselben Beschriftung führen, z. B. könnte eine Beschriftung mit den Bezeichnungen &quot;Version 1.0&quot;, &quot;Version 1.0&quot;, &quot;Version 1&quot; verwendet werden, um die gleiche Stufe eines Themas zu identifizieren. Um eine solche inkonsistente Beschriftung im System zu vermeiden, können Sie eine vordefinierte Liste von Bezeichnungen erstellen, aus der Autoren dann eine Auswahl treffen können. Eine konsistente Beschriftung hilft bei einer besseren Verwaltung von Dateien in Ihrem System.

Mithilfe der Konfiguration der Versionsbezeichnung können Sie eine Liste gültiger Beschriftungen für Ihr Unternehmen hochladen. Laden Sie die standardmäßige Datei label.json herunter und ändern Sie sie wie unten gezeigt:

```css
{
"label1":"Draft",
"label2":"PM-Review",
"label3":"Engg-Review",
"label4":"QE-Review",
"label5":"Ready for Loc",
"label6":"Ready for Publish"
}
```

Im obigen Beispiel ist &quot;label1&quot;der Bezeichner für die Bezeichnungsreihenfolge und wird an den Titel angehängt, der den Autoren überall dort angezeigt wird, wo eine Bezeichnung erforderlich ist. Speichern Sie diese Datei und laden Sie sie im Abschnitt &quot;Beschriftungen der XML-Inhaltsversion&quot;hoch.

>[!IMPORTANT]
>
> Damit Konfigurationen auf Ordnerebene wirksam werden, müssen Benutzer das Profil unter ihren Benutzereinstellungen im Web Editor auswählen.

**Rootmap**

Wenn Ihre Autoren mit einer bestimmten Stammkarte arbeiten, können Sie diese hier durchsuchen und auswählen. Beachten Sie, dass Sie die Rootmap nur für ein Profil auf Ordnerebene definieren können.

