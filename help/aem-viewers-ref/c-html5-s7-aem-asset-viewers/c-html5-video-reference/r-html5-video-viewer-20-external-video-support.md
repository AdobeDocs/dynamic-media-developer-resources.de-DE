---
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb des Scene7 Publishing Systems oder von AEM Dynamic Media gehostet werden.
seo-description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb des Scene7 Publishing Systems oder von AEM Dynamic Media gehostet werden.
seo-title: Externe Videounterstützung
solution: Experience Manager
title: Externe Videounterstützung
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Externe Videounterstützung{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb des Scene7 Publishing Systems oder von AEM Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8-Manifest für den HLS-Stream.

Der Viewer kann entweder Scene7- oder Dynamic Media-Videos oder externe Videos verwenden. Wenn der Viewer mit Scene7/Dynamic Media-Beginn fortfahren und diesen Asset-Typ verwenden sollte, ist es nicht möglich, ein externes Video mit der [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) Methode in diesen Viewer zu laden. Und umgekehrt: Wenn der Viewer zunächst mit externen Videos geladen wurde, sollte er nur mit externen Videos funktionieren.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Modifikators &quot;Wiedergabe&quot;und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL mit .m3u8 endet, verwendet der Viewer die HLS-Wiedergabe, andernfalls wird die progressive Wiedergabe verwendet.
