---
title: Externe Videounterstützung
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager oder Dynamic Media gehostet werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager oder Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für HLS-Stream.

Der Viewer kann entweder Dynamic Media Classic- oder Experience Manager Dynamic Media-Videos oder externe Videos verwenden. Wenn der Viewer mit Dynamic Media Classic/AEM Dynamic Media-Video beginnt, sollte er in Zukunft mit einem solchen Asset-Typ verwendet werden. Es ist nicht möglich, ein externes Video mit der [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode in diesen Viewer zu laden und umgekehrt. Das heißt, wenn der Viewer ursprünglich mit externen Videos geladen wurde, funktioniert er nur mit externen Videos.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert eines beliebigen Wiedergabe-Modifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit `.m3u8` endet, verwendet der Viewer die HLS-Wiedergabe. Andernfalls wird die progressive Wiedergabe verwendet.
