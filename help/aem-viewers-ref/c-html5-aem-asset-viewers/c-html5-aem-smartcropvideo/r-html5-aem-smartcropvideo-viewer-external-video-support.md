---
title: Unterstützung externer Videos
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Unterstützung externer Videos{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8 Manifest für HLS Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder Experience Manager - Dynamic Media oder mit einem externen Video arbeiten. Wenn der Viewer mit einem Dynamic Media Classic/Dynamic Media-Video beginnt, es ab sofort mit einem solchen Asset-Typ verwenden soll, ist es nicht möglich, mit [`setVideo`] ein externes Video in diesen Viewer zu laden
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode. Und umgekehrt: Wenn der Viewer zunächst mit externen Videos geladen wurde, sollte er nur mit externen Videos arbeiten.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabemodifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL auf endet, `.M3U8` der Viewer die HLS-Wiedergabe verwendet, wird andernfalls die progressive Wiedergabe verwendet.
