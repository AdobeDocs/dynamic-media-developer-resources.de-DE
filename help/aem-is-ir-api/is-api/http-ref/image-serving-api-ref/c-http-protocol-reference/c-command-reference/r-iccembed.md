---
description: Farbprofil einbetten. Gibt an, ob das funktionierende ICC-Farbprofil oder das mit icc= angegebene Profil in das Antwortbild eingebettet werden soll.
solution: Experience Manager
title: iccEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# iccEmbed{#iccembed}

Farbprofil einbetten. Gibt an, ob das funktionierende ICC-Farbprofil oder das mit icc= angegebene Profil in das Antwortbild eingebettet werden soll.

`iccEmbed=0|1`

## Eigenschaften {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Anforderungsattribut. Wird ignoriert, wenn kein Profil zum Einbetten verfügbar ist.

## Standard {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, damit keine ICC-Profile in Ausgabebilder eingebettet werden. Wird ignoriert, wenn das Einbetten von ICC-Profilen im Ausgabebildformat nicht unterstützt wird.

Weitere Informationen finden Sie unter [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) .

## Verwandte Themen {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
