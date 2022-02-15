---
title: Externe Videounterstützung
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für HLS-Stream.

Der Viewer kann entweder Dynamic Media Classic oder Experience Manager - Dynamic Media-Video oder mit externen Videos verwenden. Wenn der Viewer mit einem Dynamic Media Classic/Dynamic Media-Video beginnt, verwenden Sie es in Zukunft mit einem solchen Asset-Typ. Es ist nicht möglich, ein externes Video mit [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) -Methode. Und umgekehrt: Wenn der Viewer ursprünglich mit externen Videos geladen wurde, sollte er nur mit externen Videos funktionieren.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabe-Modifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit `.m3u8` Der Viewer verwendet die HLS-Wiedergabe, andernfalls wird die progressive Wiedergabe verwendet.
