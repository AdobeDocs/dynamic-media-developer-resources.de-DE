---
title: Externe Videounterstützung
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für HLS-Stream.

Der Viewer kann entweder Dynamic Media Classic oder Experience Manager - Dynamic Media-Video oder mit externen Videos verwenden. Wenn der Viewer mit einem Dynamic Media Classic/Dynamic Media-Video beginnt, verwenden Sie es in Zukunft mit einem solchen Asset-Typ. Es ist nicht möglich, ein externes Video mit [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode. Und umgekehrt: Wenn der Viewer ursprünglich mit externen Videos geladen wurde, sollte er nur mit externen Videos funktionieren.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabe-Modifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit `.M3U8` Der Viewer verwendet die HLS-Wiedergabe, andernfalls wird die progressive Wiedergabe verwendet.
