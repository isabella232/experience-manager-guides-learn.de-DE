---
title: Inhalte übersetzen
description: Erfahren Sie, wie Sie Inhalte übersetzen
source-git-commit: 4d54c52b8771b0c5a40018cfec3a6586029af2fb
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 16%

---


# Inhalte übersetzen {#id181GB0400UI}

Automatisieren Sie die Übersetzung von Seiteninhalten, Assets und benutzergenerierten Inhalten, um mehrsprachige Websites zu erstellen und zu verwalten. Um Übersetzungs-Workflows zu automatisieren, integrieren Sie Übersetzungsanbieter in AEM und erstellen Sie Projekte für die Übersetzung von Inhalten in mehrere Sprachen. AEM unterstützt Workflows für menschliche und maschinelle Übersetzungen.

- Menschliche Übersetzung: Inhalte werden an Ihren Übersetzungsdienstleister gesendet und von professionellen Übersetzern übersetzt. Wenn die Inhalte übersetzt wurden, werden sie zurückgesendet und in AEM importiert. Wenn Ihr Übersetzungsanbieter in AEM integriert ist, werden Inhalte automatisch zwischen AEM und dem Übersetzungsanbieter ausgetauscht

- Maschinelle Übersetzung: Der maschinelle Übersetzungs-Service übersetzt sofort Ihre Inhalte


Die Übersetzung der Inhalte umfasst die folgenden Schritte:

1. AEM mit Ihrer [Übersetzungsdienstleister](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en) und erstellen Sie Framework-Konfigurationen für die Übersetzungsintegration.

1. Verknüpfen Sie die Seiten Ihres Sprachstamms mit dem Übersetzungsdienstleister und den Framework-Konfigurationen.

1. Identifizieren Sie den Typ von [zu übersetzende Inhalte](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/rules.html?lang=en).

1. [Bereiten Sie die Inhalte für die Übersetzung vor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html?lang=en), indem Sie den Sprachstamm und die Stammseiten der Sprachkopien erstellen.

1. Erstellen [Übersetzungsprojekte](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=de) , um die zu übersetzenden Inhalte zu sammeln und den Übersetzungsprozess vorzubereiten.

1. Verwenden Sie Übersetzungsprojekte, um [Verwalten der Inhaltsübersetzung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/managing-projects.html?lang=de) -Prozess.


Wenn Ihr Übersetzungsanbieter keinen Connector zur Integration mit AEM bereitstellt, unterstützt AEM den manuellen Export und Import von übersetzten Inhalten im XML-Format.

>[!TIP]
>
> Siehe *Übersetzung* im Leitfaden zu Best Practices Best Practices für die Übersetzung von Inhalten.

## Konfigurieren der Registerkarte &quot;Übersetzung&quot;im DITA-Map-Dashboard

So blenden Sie die Registerkarte Übersetzung im DITA Map-Dashboard aus:

1. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen.
1. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die Registerkarte &quot;Übersetzung&quot;im Zuordnungs-Dashboard zu konfigurieren:

   | PID | Eigenschaftenschlüssel | Eigenschaftswert |
   |---|------------|--------------|
   | `com.adobe.fmdita.config.ConfigManager` | `tabs.translation` | Boolesch \( true/false\).<br> **Standardwert**: `true` |

   >[!NOTE]
   >
   > Diese Konfiguration ist standardmäßig aktiviert und die Registerkarte &quot;Übersetzung&quot;ist nicht im Landkarten-Dashboard verfügbar.


## Konfigurieren des komponentenbasierten Übersetzungs-Workflows

Wenn der Connector für den Übersetzungsanbieter keine DITA-Inhalte unterstützt, muss der komponentenbasierte Übersetzungs-Workflow aktiviert werden. Nach der Aktivierung wird der übersetzbare Inhalt als Asset-Metadaten gesendet. Der Connector muss jedoch die Übersetzung von Asset-Metadaten unterstützen, damit dieser Workflow funktioniert.

Basierend auf dem in Ihrem Setup verwendeten Übersetzungs-Workflow sollte die Option für komponentenbasierte Übersetzungs-Workflows konfiguriert werden. Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um den komponentenbasierten Übersetzungs-Workflow zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `component.translation` | Boolesch: <br> - Wenn Sie eine menschliche Übersetzung verwenden, dann *Deaktivieren* \( `false`\) die **Komponentenbasierter Übersetzungs-Workflow** -Option. <br> - Wenn Sie maschinelle Übersetzung verwenden, dann *Aktivieren \( `true`\)* die **Komponentenbasierter Übersetzungs-Workflow** -Option. |

>[!NOTE]
>
> Wenn Sie Übersetzungs-Connector verwenden, stellen Sie sicher, dass Sie den Connector wie im Abschnitt *[Konfigurieren des Übersetzungsintegrations-Frameworks](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en)* Thema in AEM Dokumentation.

>[!IMPORTANT]
>
> Nachdem Sie die Übersetzungskonfigurationen eingerichtet haben, stellen Sie sicher, dass Sie die entsprechende Cloud-Konfiguration für die Sprachordner einrichten.

## Konfigurieren der Nachbearbeitung temporärer Sprachkopien

Wenn Sie den Übersetzungs-Workflow starten, erstellt das System temporäre Sprachkopien des Quellinhalts. Sie können die Nachbearbeitung für diese temporären Dateien aktivieren oder deaktivieren. Im Anschlussvorgang werden die eingehenden und ausgehenden Verweise aus den Dateien aufgelöst, der Dokumentstatus wird zusammen mit anderen Vorgängen festgelegt. Wenn Sie die Nachbearbeitung für diese temporären Dateien aktivieren, kann es länger dauern, bis der Übersetzungsprozess abgeschlossen ist. Daher wird empfohlen, die Option &quot;Nachbearbeitung&quot;deaktiviert zu lassen.

Verwenden Sie die Anweisungen unter [Konfigurationsüberschreibungen](download-install-additional-config-override.md#) , um die Konfigurationsdatei zu erstellen. Geben Sie in der Konfigurationsdatei die folgenden \(Eigenschaft\)-Details an, um die Nachbearbeitung temporärer Sprachkopien zu konfigurieren:

| PID | Eigenschaftenschlüssel | Eigenschaftswert |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `postprocess.temporary.langcopies` | Boolesch: <br> - Wenn Sie die Nachbearbeitung nicht für die temporären Dateien ausführen möchten, dann *Deaktivieren* \( false\) die **Sprachkopien nach der Verarbeitung** -Option.<br> - Wenn Sie die Nachbearbeitung für die temporären Dateien ausführen möchten, dann *Aktivieren* \( true\) die **Sprachkopien nach der Verarbeitung** -Option.<br> **Standardwert**: false |

