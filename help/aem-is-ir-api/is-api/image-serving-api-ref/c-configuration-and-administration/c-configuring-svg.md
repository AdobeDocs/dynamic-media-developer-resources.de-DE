---
description: Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.
seo-description: Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.
seo-title: SVG konfigurieren
solution: Experience Manager
title: SVG konfigurieren
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG konfigurieren{#configuring-svg}

Die SvgRender-Komponente ist eine unabhängige Java-Anwendung.

Die SVG-Konfigurationseinstellungen befinden sich in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml]und [!DNL ServerSupervisorRegistry.xml].

Eine Socketverbindung wird verwendet, um zwischen SvgRender und dem Image-Server zu kommunizieren. Die Anschlussnummer ist 27346. Bei Bedarf können Sie sie ändern, indem Sie `SVGRender.port` in [!DNL svg.conf] und `<SVGTcpPort>` in einen neuen Wert einstellen [!DNL ImageServerRegistry.xml] .

## Verwandte Themen {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-Konfigurationseinstellungen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
