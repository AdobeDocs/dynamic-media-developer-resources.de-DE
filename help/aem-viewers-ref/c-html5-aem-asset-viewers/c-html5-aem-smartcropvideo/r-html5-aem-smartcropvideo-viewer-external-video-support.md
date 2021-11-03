---
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder AEM Dynamic Media gehostet werden.
solution: Experience Manager
title: Externe Videounterstützung
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder AEM Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für HLS-Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder AEM Dynamic Media-Video oder mit externen Videos arbeiten. Wenn der Viewer mit einem Dynamic Media Classic/Dynamic Media-Video beginnt, verwenden Sie es in Zukunft mit einem solchen Asset-Typ. Es ist nicht möglich, ein externes Video mit [ `setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode. Und umgekehrt: Wenn der Viewer ursprünglich mit externen Videos geladen wurde, sollte er nur mit externen Videos funktionieren.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabe-Modifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL auf .m3u8 endet, verwendet der Viewer die HLS-Wiedergabe, andernfalls wird die progressive Wiedergabe verwendet.
