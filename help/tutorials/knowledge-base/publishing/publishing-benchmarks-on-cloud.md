---
title: Anleitungen zur Veröffentlichung von Benchmarks auf AEMaaCS
description: Machen Sie sich mit den Systembeschränkungen bei der Veröffentlichung in AEM Cloud vertraut.
source-git-commit: e64430bb968b18090c3981cc2d21ebe6593ba933
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 7%

---


# AEM Anleitungen zur Veröffentlichung von Benchmarks auf AEMaaCS

Derzeit AEM Guides-Cloud-Service hat einige Einschränkungen bei der Größe von Veröffentlichungskarten, die das Guides-Team aktiv lösen möchte.

Das Guides-Team hat bereits eine skalierbare [Publishing-Microservice](publish-microservice-architecture-and-performance.md) zur Unterstützung von großen Karten und mehreren gleichzeitigen Veröffentlichungen. Derzeit unterstützt dieser Microservice eine Untergruppe von Ausgabetypen und die Unterstützung für andere Typen befindet sich in der aktiven Entwicklung.

Informationen zum Konfigurieren des neuen Veröffentlichungsdienstes für AEM Cloud-Umgebung finden Sie unter [Neue mikrodienstbasierte Veröffentlichung konfigurieren](configure-microservices.md)

## Ausführungsumgebung

    AEM: 2023.5.11983.20230511T173830Z
    Guide Add On Release: 2023.6.0
    AEM Site-Vorlage: OOTB-Vorlage für AEM Guides
    DITA-OT-Version: 3,5,4
    Veröffentlichungs-Workflow-Typ: Veröffentlichungsarbeitsablauf aufteilen
    Vom Microservice unterstützte Ausgabe: Native PDF, PDF (Dita-OT)

## Generierungsnummern der Ausgabe

| Ausgabetyp | Zuordnungsgröße (Themenverweise) | Ausführungsdauer (in Sekunden) | Publishing-Microservice |
|---------------|------------------------------|----------------------------|-----------------------|
| AEM Site | 3500 | 5220 | Nein |
| Native PDF | 3500 | 780 | Ja |
| PDF (DITA-OT) | 11000 | 960 | Ja |
| HTML 5 | 3500 | 240 | Nein |
| Benutzerdefiniert | 300 | 300 | Nein |

## Wichtige Hinweise

- AEM Site erstellt viele cq:Page -Knoten und reduziert sie, indem sie sie während der Generierungszeit einzeln rendert. Aus diesem Grund ist es ratsam, zu vermeiden, dass mehrere gleichzeitige AEM Site-Veröffentlichungen ausgeführt werden, da dies das System überlasten kann.
- AEM die Zeit der Site-Erstellung hängt von der verwendeten Vorlage ab. Die Ausführungszeit kann sich bei Verwendung komplexer Vorlagen erhöhen.
- Die Ausführungszeit der benutzerdefinierten Veröffentlichung ist für eine benutzerdefinierte Beispielausgabe vorgesehen. Die benutzerdefinierte Veröffentlichungszeit hängt ausschließlich von der eigenen Transformationslogik des Kunden ab.
