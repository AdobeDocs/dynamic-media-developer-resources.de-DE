---
title: Unterstützung externer Videos
description: Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 0%

---

# Unterstützung externer Videos{#external-video-support}

Der Viewer unterstützt die Wiedergabe von Videos, die außerhalb von Dynamic Media Classic oder Adobe Experience Manager - Dynamic Media gehostet werden.

Unterstützte Formate für das externe Video sind entweder MP4 im H.264-Format oder M3U8 Manifest für HLS Stream.

Der Viewer kann entweder mit Dynamic Media Classic oder Experience Manager - Dynamic Media-Videos oder mit externen Videos verwendet werden. Wenn der Viewer mit Dynamic Media Classic/Dynamic Media-Videos beginnt, diese ab jetzt mit einem solchen Asset-Typ verwendet werden, ist es nicht mehr möglich, ein externes Video mit in diesen Viewer zu laden [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)-Methode. Und umgekehrt: Wenn der Viewer zunächst mit externen Videos geladen wurde, sollte er nur mit externen Videos arbeiten.

Beim Arbeiten mit externen Videos ignoriert der Viewer den Wert des Wiedergabemodifikators und erkennt den Wiedergabetyp aus der externen Videoerweiterung. Wenn die externe Video-URL auf endet, `.M3U8` der Viewer die HLS-Wiedergabe verwendet, wird andernfalls die progressive Wiedergabe verwendet.
