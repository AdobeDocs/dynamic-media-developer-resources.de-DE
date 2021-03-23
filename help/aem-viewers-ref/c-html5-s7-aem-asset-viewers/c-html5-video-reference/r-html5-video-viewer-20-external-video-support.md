---
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder AEM Dynamic Media gehostet werden.
solution: Experience Manager
title: Externe Videounterstützung
feature: Dynamic Media Classic, Viewer, SDK/API, Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder AEM Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für den HLS-Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder AEM Dynamic Media oder mit externen Videos arbeiten. Wenn der Viewer mit Dynamic Media Classic/Dynamic Media-Beginn fortfahren und diesen Asset-Typ verwenden sollte, ist es nicht möglich, ein externes Video mit der [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode in diesen Viewer zu laden. Und umgekehrt: Wenn der Viewer zunächst mit externen Videos geladen wurde, sollte er nur mit externen Videos funktionieren.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Modifikators &quot;Wiedergabe&quot;und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit .m3u8 endet, verwendet der Viewer die HLS-Wiedergabe, andernfalls wird die progressive Wiedergabe verwendet.
