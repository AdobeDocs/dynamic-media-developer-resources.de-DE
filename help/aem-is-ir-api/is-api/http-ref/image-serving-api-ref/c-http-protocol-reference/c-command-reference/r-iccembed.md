---
description: Profil "Farbe einbetten". Gibt an, ob das funktionierende ICC-Profil oder das mit icc= angegebene Profil in das Antwortbild eingebettet werden soll.
seo-description: Profil "Farbe einbetten". Gibt an, ob das funktionierende ICC-Profil oder das mit icc= angegebene Profil in das Antwortbild eingebettet werden soll.
seo-title: iccEmbed
solution: Experience Manager
title: iccEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: ccd3fd2f-6f73-4725-a51a-9daf643d71af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# iccEmbed{#iccembed}

Profil &quot;Farbe einbetten&quot;. Gibt an, ob das funktionierende ICC-Profil oder das mit icc= angegebene Profil in das Antwortbild eingebettet werden soll.

`iccEmbed=0|1`

## Eigenschaften {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Anforderungsattribut. Wird ignoriert, wenn kein Profil zum Einbetten verfügbar ist.

## Standard {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, um keine Einbettung von ICC-Profilen in Ausgabebilder vorzunehmen. Wird ignoriert, wenn das Ausgabebildformat die Einbettung von ICC-Profilen nicht unterstützt.

Weitere Informationen finden Sie unter [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a).

## Verwandte Themen {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
