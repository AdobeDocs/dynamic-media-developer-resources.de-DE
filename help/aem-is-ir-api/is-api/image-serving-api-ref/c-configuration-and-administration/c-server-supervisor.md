---
description: Image Serving-Komponenten werden vom Server Supervisor verwaltet, einem Linux-Daemon oder Windows-Dienst (S7Supervisor.exe, in der Systemsteuerung als "Scene7 Image Serving"aufgeführt).
seo-description: Image Serving-Komponenten werden vom Server Supervisor verwaltet, einem Linux-Daemon oder Windows-Dienst (S7Supervisor.exe, in der Systemsteuerung als "Scene7 Image Serving"aufgeführt).
seo-title: Server Supervisor
solution: Experience Manager
title: Server Supervisor
topic: Scene7 Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Server Supervisor{#server-supervisor}

Image Serving-Komponenten werden vom Server Supervisor verwaltet, einem Linux-Daemon oder Windows-Dienst (S7Supervisor.exe, in der Systemsteuerung als &quot;Scene7 Image Serving&quot;aufgeführt).

Der Server Supervisor ist nicht nur dafür verantwortlich, andere Image Serving-Komponenten zu starten und zu beenden, sondern auch dafür verantwortlich, den Zustand dieser anderen Komponenten zu gewährleisten. Bei einem Absturz einer Komponente wird sie automatisch neu gestartet, um alle Dienstunterbrechungen zu minimieren.

## Starten und Beenden von {#section-061d28d74e034a30adc39ea3e2031cd0}

Der Server Supervisor wird mit dem Image Serving-Dienstprogrammskript gestartet, beendet und neu gestartet. Weitere Informationen finden Sie in der [Dienstprogrammdokumentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f).

Der Server Supervisor wird automatisch gestartet und beendet, und alle anderen Image Serving-Komponenten werden angehalten.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
