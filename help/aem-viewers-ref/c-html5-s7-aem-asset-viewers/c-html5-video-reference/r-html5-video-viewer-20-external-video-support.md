---
title: Unterstützung externer Videos
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Unterstützung externer Videos{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8 Manifest für HLS Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder Experience Manager - Dynamic Media-Videos oder mit externen Videos verwendet werden. Wenn der Viewer mit Dynamic Media Classic/Dynamic Media-Videos beginnt, diese ab jetzt mit einem solchen Asset-Typ verwendet werden, ist es nicht mehr möglich, mit [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) -Methode ein externes Video in diesen Viewer zu laden. Und umgekehrt: Wenn der Viewer zunächst mit externen Videos geladen wurde, sollte er nur mit externen Videos arbeiten.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabemodifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL auf endet, `.m3u8` der Viewer die HLS-Wiedergabe verwendet, wird andernfalls die progressive Wiedergabe verwendet.
