---
title: Konfigurieren eines Datenquellen-Connectors
description: Erfahren Sie, wie Sie einen Datenquellen-Connector konfigurieren
source-git-commit: 2e7f9fb0a5932cc6fa5852ba8d9b9bf13ab12aed
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 1%

---


# Konfigurieren eines Datenquellen-Connectors

AEM Guides bietet vordefinierte Connectoren für JIRA-, SQL-Datenbanken (MySQL, PostgreSQL, Microsoft SQL Server, SQLite, MariaDB, H2DB), AdobeCommerce- und Elasticsearch-Datenbanken. Sie können auch andere Connectoren hinzufügen, indem Sie die Standardschnittstellen erweitern. Die folgende Konfiguration hilft Ihnen, die verschiedenen Datenquellen einfach hinzuzufügen. Nach dem Hinzufügen können Sie die Datenquellen im Web Editor anzeigen.

Führen Sie die folgenden Schritte aus, um einen Datenquellen-Connector zu konfigurieren und ihn dann im Web Editor zu verwenden:

## Connector konfigurieren

Sie können einen vordefinierten Connector konfigurieren, indem Sie eine JSON-Datei hochladen. Sie können die folgenden Beispielkonfigurationsdateien verwenden, um Connectoren für JIRA-, SQL-Datenbanken (MySQL, PostgreSQL, Microsoft SQL Server, SQLite, MariaDB, H2DB), AdobeCommerce- und Elasticsearch-Datenbanken einzurichten.

Eine Beispielsetup-Datei für die grundlegende Authentifizierung von Jira mit Benutzername und Kennwort:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.JiraConnector",
	"configName": "Jira",
	"templateFolders": ["/content/dam/dita-templates/konnect/jira"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthUserNamePasswordRestConfig",
		"configData": {
			"username": "jirausername",
			"password": "jirapassword",
			"url": "https://jira.corp.adobe.com/rest/api/latest/search"
		}
	}
}
```

Speichern Sie beispielsweise als `jira.json`.

Eine Beispielsetup-Datei für die grundlegende Authentifizierung von Jira mit Token:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.JiraConnector",
	"configName": "Jira",
	"templateFolders": ["/content/dam/dita-templates/konnect/jira"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthTokenRestConfig",
		"configData": {
			"token": "jiraauthtoken",
			"url": "https://jira.corp.adobe.com/rest/api/latest/search"
		}
	}
}
```

Speichern Sie beispielsweise als `jira.json`.

Eine Beispielsetup-Datei für die grundlegende Authentifizierung von Jira mit dem Token, in dem das Keyword &quot;Einfach&quot;enthalten ist:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.JiraConnector",
	"configName": "Jira",
	"templateFolders": ["/content/dam/dita-templates/konnect/jira"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthTokenRestConfig",
		"configData": {
			"token": "Basic jiraauthtoken",
			"url": "https://jira.corp.adobe.com/rest/api/latest/search"
		}
	}
}
```

Speichern Sie beispielsweise als `jira.json`.

Eine Beispielsetup-Datei für die einfache Authentifizierung von MySql:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.MySqlConnector",
	"configName": "MySQL",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
		"configData": {
			"username": "admin",
			"password": "admin",
			"driver": "com.mysql.jdbc.Driver",
			"connectionString": "jdbc:mysql://host.corp.adobe.com:3306/plm"
		}
	}
}
```

Speichern Sie beispielsweise als `mysql.json`.

Eine Beispielsetup-Datei für die einfache Authentifizierung von PostgreSQL:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.PostgreSqlConnector",
	"configName": "PostgreSQL",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
		"configData": {
			"username": "admin",
			"password": "admin",
			"driver": "org.postgresql.Driver",
			"connectionString": "jdbc:postgresql://host:port/database"
		}
	}
}
```

Speichern Sie beispielsweise als `postgres.json`.

Eine Beispielsetup-Datei für die grundlegende Authentifizierung von Microsoft SQL Server:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.MsSqlServerConnector",
	"configName": "MSSQLServer",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
		"configData": {
			"username": "admin",
			"password": "admin",
			"driver": "com.microsoft.sqlserver.jdbc.SQLServerDriver",
			"connectionString": "jdbc:sqlserver://10.10.10.10\\SQLEXPRESS01:1433;database=TutorialDB;encrypt=false;trustServerCertificate=true"
		}
	}
}
```

Speichern Sie beispielsweise als `mssqlserver.json`.

Eine Beispielsetup-Datei für die grundlegende Authentifizierung von SQLite:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.SqliteConnector",
	"configName": "SQLiteServer",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
		"configData": {
			"username": "admin",
			"password": "admin",
			"driver": "org.sqlite.JDBC",
			"connectionString": "jdbc:sqlite:sample.db"
		}
	}
}
```

Speichern Sie beispielsweise als `sqqlite.json`.



Eine Beispielsetup-Datei für H2DB:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.sql.H2DBConnector",
	"configName": "H2DBConnector",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
		"configData": {
			"username": "admin",
			"password": "admin",
			"driver": "org.h2.Driver",
			"connectionString": "jdbc:h2:file:D:/h2db/db"
		}
	}
}
```

Speichern Sie beispielsweise als `sqqlite.json`.



Eine Beispielsetup-Datei für die grundlegende Authentifizierung von MariaDb:

```
{
	"connectorClazz": "com.adobe.guides.sample.konnect.connector.MariaDBConnector",
	"configName": "SampleMariaDbConnector",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.sql.UserPassSqlConfig",
		"configData": {
			"username": "admin",
			"password": "admin",
			"driver": "org.mariadb.jdbc.Driver",
			"connectionString": "jdbc:mariadb://no1010042073107.corp.adobe.com:3308/mysql"
		}
	}
}
```

Speichern Sie beispielsweise als `mariadb.json`.


Eine Beispielsetup-Datei für die grundlegende Authentifizierung von Elasticsearch:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.rest.ElasticsearchConnector",
	"configName": "SampleES",
	"templateFolders": ["/content/dam/dita-templates/konnect/sql"],
	"connectionConfig": {
		"configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.BasicAuthUserNamePasswordRestConfig",
		"configData": {
			"username": "admin",
			"password": "admin",    	
			"url": "https://testsearch-1370045986.us-east-1.bonsaisearch.net:443"   }
	}
}
```

Speichern Sie beispielsweise als `ES.json`.

Die Abfrage der Elastic Search sollte den Index und die Abfrage enthalten:

```
{
"index": "kibana_sample_data_ecommerce",
"queryString":{
    "query": {
        "match_all": {}
    }
}
}
```



Eine Beispielsetup-Datei für AdobeCommerce NoAuth:

```
{
	"connectorClazz": "com.adobe.guides.konnect.definitions.ootb.connector.graphql.AdobeCommerceConnector",
	"configName": "SampleCommerce",
	"templateFolders": ["/content/dam/dita-templates/konnect"],
	"connectionConfig": {   "configClazz": "com.adobe.guides.konnect.definitions.ootb.config.rest.NoAuthRestConfig",
   "configData": {
   			"url": "http://host/graphql"   
		}
	}
}
```

Speichern Sie beispielsweise als `commerce.json`.

### Connector-Konfiguration anpassen

Mit AEM Guides können Sie einige Werte in der Konfigurationsdatei an die Bedürfnisse des Benutzers anpassen.

| Eigenschaftsname | Beschreibung |
|---|---|
| configName | Der Benutzer kann einen Konfigurationsnamen angeben, um den Connector zu identifizieren |
| templateFolders | Liste der Ordner, aus denen Vorlagen abgerufen werden |

Andere Felder werden basierend auf der Konfigurationsklasse angepasst, die zum Ausführen des Connectors ausgewählt wurde.

## Laden Sie die Datei an einen Speicherort in AEM hoch.

Laden Sie die Datei an einen Speicherort in AEM Assets hoch.

Zum Beispiel: `/var/dxml/konnect/jira.json`

## Erstellen einer Konfiguration mithilfe der REST-API

Sie können die Konfiguration mithilfe der REST-API registrieren. Weitere Informationen finden Sie unter *REST-API zur Registrierung eines Datenquellen-Connectors* in der API-Referenz für Adobe Experience Manager-Handbücher.

Nachdem Sie die Datenquelle konfiguriert haben, wird der Connector im Web Editor im Bereich &quot;Data Sources&quot;aufgeführt. Anschließend können Sie eine Verbindung zur Datenquelle herstellen und ein Inhaltsfragment in Ihre Themen einfügen. Weitere Informationen finden Sie unter [Inhaltsfragment aus Ihrer Datenquelle einfügen](../user-guide/web-editor-content-snippet.md).

