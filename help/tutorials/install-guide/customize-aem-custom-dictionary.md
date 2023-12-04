---
title: AEM Standardwörterbuch anpassen
description: Erfahren Sie, wie Sie AEM Standardwörterbuch anpassen
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# AEM Standardwörterbuch anpassen {#id209SD8000WU}

Der Web Editor kann so konfiguriert werden, dass er AEM Rechtschreibprüfung oder die Rechtschreibprüfung des Browsers verwendet. Wenn Sie sich dafür entscheiden, mit AEM Rechtschreibprüfung zu arbeiten, erhalten Sie die Flexibilität, Ihre benutzerdefinierte Wortliste zu definieren. Diese benutzerdefinierten Wörter werden dann zum AEM Wörterbuch hinzugefügt und diese Wörter werden im Web Editor nicht als \(falsch\) gekennzeichnet.

Führen Sie die folgenden Schritte aus, um Ihre benutzerdefinierte Wortliste zu erstellen, die AEM Wörterbuch hinzugefügt wird:

1. Melden Sie sich bei AEM an und öffnen Sie den CRXDE Lite-Modus.

1. Navigieren Sie zum folgenden Knoten:

   /apps/fmdita/config

1. Erstellen Sie eine neue Datei mit dem Namen user\_dictionary.txt.

1. Öffnen Sie die Datei und fügen Sie eine Liste von Wörtern hinzu, die Sie in Ihrem benutzerdefinierten Wörterbuch definieren möchten.

   Der folgende Screenshot zeigt die Liste der benutzerdefinierten Wörter, die der Datei &quot;user\_dictionary.txt&quot;hinzugefügt wurden:

   ![](assets/custom-words-list-dictionary.png){width="650" align="left"}

1. Speichern und schließen Sie die Datei.


Autoren müssen ihre Web-Editor-Sitzung neu starten, damit die benutzerdefinierte Wörterbuchliste im AEM Wörterbuch aktualisiert wird.

**Übergeordnetes Thema:**[ Anpassen des Web-Editors](conf-web-editor.md)
