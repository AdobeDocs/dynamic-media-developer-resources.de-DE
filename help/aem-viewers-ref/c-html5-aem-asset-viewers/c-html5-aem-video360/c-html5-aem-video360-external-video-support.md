---
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder AEM Dynamic Media gehostet werden.
solution: Experience Manager
title: Externe Videounterstützung
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder AEM Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für den HLS-Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder AEM Dynamic Media oder mit externen Videos arbeiten. Wenn der Viewer mit Dynamic Media Classic/AEM Dynamic Media-Videos Beginn hat, sollte er in Zukunft mit einem solchen Asset-Typ verwendet werden. Es ist nicht möglich, ein externes Video mit der [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode in diesen Viewer zu laden und umgekehrt. Das heißt, wenn der Viewer zunächst mit externen Videos geladen wurde, funktioniert er weiterhin nur mit externen Videos.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert eines beliebigen Wiedergabeschutzmodifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit `.m3u8` endet, verwendet der Viewer die HLS-Wiedergabe; Andernfalls wird die progressive Wiedergabe verwendet.
