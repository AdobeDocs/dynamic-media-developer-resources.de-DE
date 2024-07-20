---
description: Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.
solution: Experience Manager
title: SVG konfigurieren
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# SVG konfigurieren{#configuring-svg}

Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.

Die SVG-Konfigurationseinstellungen befinden sich unter [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] und [!DNL ServerSupervisorRegistry.xml].

Eine Socketverbindung wird verwendet, um zwischen SvgRender und dem Image-Server zu kommunizieren. Die Portnummer ist 27346. Falls nötig, kann es geändert werden, indem `SVGRender.port` in [!DNL svg.conf] und `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] auf einen neuen Wert gesetzt werden.

## Verwandte Themen {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-Konfigurationseinstellungen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
