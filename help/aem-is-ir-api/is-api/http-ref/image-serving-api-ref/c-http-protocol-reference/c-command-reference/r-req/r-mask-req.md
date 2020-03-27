---
description: Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.
seo-description: Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.
seo-title: Maske
solution: Experience Manager
title: Maske
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.

`req=mask`

Unterstützt dieselben Befehle wie `req=img`und wird auf dieselbe Weise vom Server verarbeitet. Anstatt jedoch die RGB- oder RGBA-Daten zurückzugeben, verwirft der Server die Farbinformationen und gibt nur die Daten zur Maske (Alpha-Kanal) zurück. Das Antwortdatenformat und der AntwortmIME-Typ werden von `fmt=`festgelegt.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.
