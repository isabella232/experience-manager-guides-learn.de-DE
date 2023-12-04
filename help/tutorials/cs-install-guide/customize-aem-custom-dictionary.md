---
title: AEM Standardwörterbuch anpassen
description: Erfahren Sie, wie Sie AEM Standardwörterbuch anpassen
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# AEM Standardwörterbuch anpassen {#id209SD8000WU}

Der Web Editor kann so konfiguriert werden, dass er AEM Rechtschreibprüfung oder die Rechtschreibprüfung des Browsers verwendet. Wenn Sie sich dafür entscheiden, mit AEM Rechtschreibprüfung zu arbeiten, erhalten Sie die Flexibilität, Ihre benutzerdefinierte Wortliste zu definieren. Diese benutzerdefinierten Wörter werden dann zum AEM Wörterbuch hinzugefügt und diese Wörter werden im Web Editor nicht als \(falsch\) gekennzeichnet.

Führen Sie die folgenden Schritte aus, um Ihre benutzerdefinierte Wortliste zu erstellen, die AEM Wörterbuch hinzugefügt wird:

1. Erstellen Sie die Datei &quot;user\_dictionary.txt&quot;mit einer Liste von Wörtern, die Sie in Ihrem benutzerdefinierten Wörterbuch definieren möchten.

   >[!NOTE]
   >
   > Jedes benutzerdefinierte Wort muss in einer neuen Zeile definiert werden.

1. Speichern Sie die Datei unter dem folgenden Speicherort im Git-Repository von Cloud Manager:

   /apps/fmdita/config

1. Speichern Sie die Datei.

   Übertragen Sie die Änderungen und führen Sie die Cloud Manager- \(CI/CD\)-Pipeline aus, um Konfigurationsänderungen bereitzustellen.


Autoren müssen ihre Web-Editor-Sitzung neu starten, damit die benutzerdefinierte Wörterbuchliste im AEM Wörterbuch aktualisiert wird.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
