---
description: Image Serving-Komponenten werden vom Server Supervisor verwaltet, der ein Linux-Daemon oder Windows-Dienst ist (S7Supervisor.exe, im Dienste-Control Panel als "Dynamic Media Image Serving"aufgeführt).
solution: Experience Manager
title: Server-Supervisor
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Server-Supervisor{#server-supervisor}

Image Serving-Komponenten werden vom Server Supervisor verwaltet, der ein Linux-Daemon oder Windows-Dienst ist (S7Supervisor.exe, im Dienste-Control Panel als &quot;Dynamic Media Image Serving&quot;aufgeführt).

Zusätzlich zum Starten und Beenden anderer Image Serving-Komponenten ist der Server Supervisor dafür verantwortlich, den Zustand dieser anderen Komponenten sicherzustellen. Wenn eine Komponente abstürzt, wird sie automatisch neu gestartet, um Dienstunterbrechungen zu minimieren.

## Starten und Beenden {#section-061d28d74e034a30adc39ea3e2031cd0}

Der Server Supervisor wird mit dem Image Serving-Dienstprogrammskript gestartet, angehalten und neu gestartet. Weitere Informationen finden Sie in der [Dienstprogrammdokumentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) .

Der Server Supervisor wird automatisch gestartet und beendet, und alle anderen Image Serving-Komponenten werden angehalten.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
