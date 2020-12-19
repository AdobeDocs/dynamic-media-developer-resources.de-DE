---
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von SPS oder AEM Dynamic Media gehostet werden.
seo-description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von SPS oder AEM Dynamic Media gehostet werden.
seo-title: Externe Videounterstützung
solution: Experience Manager
title: Externe Videounterstützung
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von SPS oder AEM Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für den HLS-Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder AEM Dynamic Media oder mit externen Videos arbeiten. Wenn der Viewer mit Dynamic Media Classic/AEM Dynamic Media-Videos Beginn hat, sollte er in Zukunft mit einem solchen Asset-Typ verwendet werden. Es ist nicht möglich, ein externes Video mit der [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode in diesen Viewer zu laden und umgekehrt. Das heißt, wenn der Viewer zunächst mit externen Videos geladen wurde, funktioniert er weiterhin nur mit externen Videos.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert eines beliebigen Wiedergabeschutzmodifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit `.m3u8` endet, verwendet der Viewer die HLS-Wiedergabe; Andernfalls wird die progressive Wiedergabe verwendet.
