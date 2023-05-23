---
title: Übersetzen von Inhalten in AEM Handbüchern
description: Erfahren Sie, wie Sie Inhalte übersetzen
source-git-commit: 9fe396dcfd2e3570ec386c958d7d4efdb4d608e5
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 10%

---


# Inhalte übersetzen {#id181GB0400UI}

Automatisieren Sie die Übersetzung von Seiteninhalten, Assets und benutzergenerierten Inhalten, um mehrsprachige Websites zu erstellen und zu verwalten. Um Übersetzungs-Workflows zu automatisieren, integrieren Sie Übersetzungsanbieter in AEM und erstellen Sie Projekte für die Übersetzung von Inhalten in mehrere Sprachen. AEM unterstützt Workflows für menschliche und maschinelle Übersetzungen.

- Menschliche Übersetzung: Inhalte werden an Ihren Übersetzungsdienstleister gesendet und von professionellen Übersetzern übersetzt. Wenn die Inhalte übersetzt wurden, werden sie zurückgesendet und in AEM importiert. Wenn Ihr Übersetzungsanbieter in AEM integriert ist, werden Inhalte automatisch zwischen AEM und dem Übersetzungsanbieter ausgetauscht

- Maschinelle Übersetzung: Der maschinelle Übersetzungs-Service übersetzt sofort Ihre Inhalte


Die Übersetzung der Inhalte umfasst die folgenden Schritte:

1. AEM mit Ihrer [Übersetzungsdienstleister](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html#ConnectingtoaTranslationServiceProvider) und erstellen [Framework-Konfigurationen für die Übersetzungsintegration](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html#CreatingaTranslationIntegrationConfiguration).

1. Verknüpfen Sie die Seiten Ihrer Übergeordneten Sprache mit dem [Übersetzungsdienst- und Framework-Konfigurationen](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html#ConfiguringPagesforTranslation).

1. Identifizieren Sie den Typ von [zu übersetzende Inhalte](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-rules.html).

1. [Bereiten Sie die Inhalte für die Übersetzung vor](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-prep.html), indem Sie den Sprachstamm und die Stammseiten der Sprachkopien erstellen.

1. Erstellen [Übersetzungsprojekte](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-manage.html) , um die zu übersetzenden Inhalte zu sammeln und den Übersetzungsprozess vorzubereiten.

1. Verwenden Sie Übersetzungsprojekte, um [Verwalten der Inhaltsübersetzung](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-manage.html) Prozess.


Wenn Ihr Übersetzungsanbieter keinen Connector zur Integration mit AEM bereitstellt, unterstützt AEM den manuellen Export und Import von übersetzten Inhalten im XML-Format.

>[!TIP]
>
> Siehe *Übersetzung* s Abschnitt im Handbuch mit Best Practices für Best Practices zur Übersetzung von Inhalten.

## Konfigurieren der Registerkarte &quot;Übersetzung&quot;im DITA-Map-Dashboard

Die Option Übersetzungsregisterkarte ausblenden ist standardmäßig nicht aktiviert und muss über configMgr aktiviert werden. So blenden Sie die Registerkarte Übersetzung im DITA Map-Dashboard aus:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Wählen Sie die **Registerkarte &quot;Übersetzung ausblenden&quot;** -Option, um die Registerkarte &quot;Übersetzung&quot;im Landkarten-Dashboard auszublenden.

   >[!NOTE]
   >
   > Diese Eigenschaft ist standardmäßig deaktiviert und die Registerkarte &quot;Übersetzung&quot;ist im Landkarten-Dashboard verfügbar.

1. Klicken Sie auf **Speichern**.

## Konfigurieren des komponentenbasierten Übersetzungs-Workflows

Wenn der Connector für den Übersetzungsanbieter keine DITA-Inhalte unterstützt, muss der komponentenbasierte Übersetzungs-Workflow aktiviert werden. Nach der Aktivierung wird der übersetzbare Inhalt als Asset-Metadaten gesendet. Der Connector muss jedoch die Übersetzung von Asset-Metadaten unterstützen, damit dieser Workflow funktioniert.

Basierend auf dem in Ihrer Einrichtung verwendeten Übersetzungs-Workflow sollte die Option für einen komponentenbasierten Übersetzungs-Workflow wie folgt konfiguriert werden:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Konfigurieren Sie die **Komponentenbasierter DITA-Übersetzungs-Workflow** -Option entsprechend Ihrer Einrichtung:

   - Wenn Sie menschliche Übersetzung verwenden, dann *Deaktivieren* die **Komponentenbasierter Übersetzungs-Workflow** -Option.

   - Wenn Sie maschinelle Übersetzung verwenden, dann *Aktivieren* die **Komponentenbasierter Übersetzungs-Workflow** -Option.
   >[!NOTE]
   >
   > Wenn Sie Übersetzungs-Connector verwenden, stellen Sie sicher, dass Sie den Connector wie im Abschnitt *[Konfigurieren des Framework für die Übersetzungsintegration](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-tic.html)* Thema in AEM Dokumentation.

1. Klicken Sie auf **Speichern**.


>[!IMPORTANT]
>
> Nachdem Sie die Übersetzungskonfigurationen eingerichtet haben, stellen Sie sicher, dass Sie die entsprechende Cloud-Konfiguration für die Sprachordner einrichten.

## Konfigurieren der Nachbearbeitung temporärer Sprachkopien

Wenn Sie den Übersetzungs-Workflow starten, erstellt das System temporäre Sprachkopien des Quellinhalts. Sie können die Nachbearbeitung für diese temporären Dateien aktivieren oder deaktivieren. Im Anschlussvorgang werden die eingehenden und ausgehenden Verweise aus den Dateien aufgelöst, der Dokumentstatus wird zusammen mit anderen Vorgängen festgelegt. Wenn Sie die Nachbearbeitung für diese temporären Dateien aktivieren, kann es länger dauern, bis der Übersetzungsprozess abgeschlossen ist. Daher wird empfohlen, die Option &quot;Nachbearbeitung&quot;deaktiviert zu lassen.

Standardmäßig ist die Option Nachbearbeitung temporärer Dateien deaktiviert. Sie können diese Option konfigurieren, indem Sie die folgenden Schritte ausführen:

1. Öffnen Sie die Seite Adobe Experience Manager Web Console Configuration .

   Die Standard-URL für den Zugriff auf die Konfigurationsseite lautet:

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Suchen Sie nach und klicken Sie auf **com.adobe.fmdita.config.ConfigManager** Bundle.

1. Konfigurieren Sie die **Sprachkopien nach der Verarbeitung** -Option entsprechend Ihrer Einrichtung:

   - \(*Standard*\) Wenn Sie die Nachbearbeitung nicht für die temporären Dateien ausführen möchten, dann *Deaktivieren* die **Sprachkopien nach der Verarbeitung** -Option.

   - Wenn Sie die Nachbearbeitung für die temporären Dateien ausführen möchten, dann *Aktivieren* die **Sprachkopien nach der Verarbeitung** -Option.

1. Klicken Sie auf **Speichern**.


