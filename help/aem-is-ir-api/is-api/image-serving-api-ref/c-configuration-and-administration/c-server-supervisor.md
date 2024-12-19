---
description: Bildbereitstellungskomponenten werden vom Server-Supervisor verwaltet, der ein Linux-Daemon oder Windows-Service ist (S7Supervisor.exe, in der Systemsteuerung unter "Dynamic Media-Bildbereitstellung“ aufgeführt).
solution: Experience Manager
title: Server-Verantwortlicher
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# Server-Verantwortlicher{#server-supervisor}

Bildbereitstellungskomponenten werden vom Server-Supervisor verwaltet, der ein Linux-Daemon oder Windows-Service ist (S7Supervisor.exe, in der Systemsteuerung unter &quot;Dynamic Media-Bildbereitstellung“ aufgeführt).

Zusätzlich zum Starten und Beenden anderer Bildbereitstellungskomponenten ist der Server-Supervisor dafür verantwortlich, den Zustand dieser anderen Komponenten sicherzustellen. Sollte eine Komponente abstürzen, wird sie automatisch neu gestartet, um Service-Unterbrechungen zu minimieren.

## Starten und Anhalten {#section-061d28d74e034a30adc39ea3e2031cd0}

Der Server Supervisor wird mit dem Skript des Image-Serving-Dienstprogramms gestartet, gestoppt und neu gestartet. Weitere Informationen finden Sie [Utilities-](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)).

Beim Starten und Anhalten von Server Supervisor werden automatisch alle anderen Image-Serving-Komponenten gestartet und angehalten.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
