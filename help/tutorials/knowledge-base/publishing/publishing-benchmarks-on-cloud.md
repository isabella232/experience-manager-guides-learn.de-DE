---
title: Anleitungen zur Veröffentlichung von Benchmarks auf AEMaaCS
description: Machen Sie sich mit den Systembeschränkungen bei der Veröffentlichung in AEM Cloud vertraut.
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 8%

---

# AEM Anleitungen zur Veröffentlichung von Benchmarks auf AEMaaCS

Derzeit AEM Guides-Cloud-Service hat einige Einschränkungen bei der Größe von Veröffentlichungskarten, die das Guides-Team aktiv lösen möchte.

Das Guides-Team hat einen skalierbaren Publishing-Microservice eingeführt, um große Karten und mehrere gleichzeitige Veröffentlichungen zu unterstützen. Weitere Informationen zum neuen Veröffentlichungs-Microservice finden Sie unter [Architektur von Publishing-Microservices](publish-microservice-architecture-and-performance.md)

Informationen zum Konfigurieren des neuen Veröffentlichungsdienstes für AEM Cloud-Umgebung finden Sie unter [Neue mikrodienstbasierte Veröffentlichung konfigurieren](configure-microservices.md)


## Ausführungsumgebung

    AEM: 2023.5.11983.20230511T173830Z
    Guide Add on Release: 2023.6.0
    AEM Site-Vorlage: OOTB-Vorlage für AEM Guides
    DITA-OT-Version: 3.5.4
    Veröffentlichungs-Workflow-Typ: Veröffentlichungs-Workflow aufteilen
    Vom Microservice unterstützte Ausgabe: Native PDF, PDF (Dita-OT)

## Generierungsnummern der Ausgabe

| Ausgabetyp | Zuordnungsgröße (Themenverweise) | Ausführungsdauer (in Sekunden) | Publishing-Microservice |
|---------------|------------------------------|----------------------------|-----------------------|
| AEM Site | 3500 | 5220 | Nein |
| Native PDF | 3500 | 780 | Ja |
| PDF (DITA-OT) | 11000 | 960 | Ja |
| HTML5 | 3500 | 240 | Nein |
| Benutzerdefiniert | 300 | 300 | Nein |

## Wichtige Hinweise

- AEM Site erstellt viele cq:Page -Knoten und reduziert sie, indem sie sie während der Generierungszeit einzeln rendert. Aus diesem Grund ist es ratsam, zu vermeiden, dass mehrere gleichzeitige AEM Site-Veröffentlichungen ausgeführt werden, da dies das System überlasten kann.
- AEM die Zeit der Site-Erstellung hängt von der verwendeten Vorlage ab. Die Ausführungszeit kann sich bei Verwendung komplexer Vorlagen erhöhen.
- Die Ausführungszeit der benutzerdefinierten Veröffentlichung ist für eine benutzerdefinierte Beispielausgabe vorgesehen. Die benutzerdefinierte Veröffentlichungszeit hängt ausschließlich von der eigenen Transformationslogik des Kunden ab.
