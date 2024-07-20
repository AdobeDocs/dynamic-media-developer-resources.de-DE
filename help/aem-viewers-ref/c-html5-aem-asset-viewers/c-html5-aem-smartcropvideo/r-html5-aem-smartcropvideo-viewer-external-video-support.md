---
title: Externe Videounterstützung
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

# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für HLS-Stream.

Der Viewer kann entweder Dynamic Media Classic oder Experience Manager - Dynamic Media-Video oder mit externen Videos verwenden. Wenn der Viewer mit Dynamic Media Classic/Dynamic Media-Video beginnt, verwenden Sie es in Zukunft mit einem solchen Asset-Typ, es ist nicht möglich, ein externes Video mit [`setVideo`] in diesen Viewer zu laden.
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode. Umgekehrt: Wenn der Viewer ursprünglich mit externen Videos geladen wurde, sollte er nur mit externen Videos funktionieren.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabe-Modifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit `.M3U8` endet, verwendet der Viewer die HLS-Wiedergabe, andernfalls wird die progressive Wiedergabe verwendet.
