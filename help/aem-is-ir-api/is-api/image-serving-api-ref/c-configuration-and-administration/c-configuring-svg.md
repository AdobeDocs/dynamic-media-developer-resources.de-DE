---
description: Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.
seo-description: Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.
seo-title: SVG konfigurieren
solution: Experience Manager
title: SVG konfigurieren
uuid: f6e131af-283e-4649-b349-123489c0838d
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 2%

---


# Konfigurieren von SVG{#configuring-svg}

Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.

Die SVG-Konfigurationseinstellungen befinden sich in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] und [!DNL ServerSupervisorRegistry.xml].

Eine Socketverbindung wird verwendet, um zwischen SvgRender und dem Image-Server zu kommunizieren. Die Anschlussnummer ist 27346. Falls erforderlich, kann sie geändert werden, indem `SVGRender.port` in [!DNL svg.conf] und `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] auf einen neuen Wert eingestellt wird.

## Verwandte Themen {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-Konfigurationseinstellungen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
