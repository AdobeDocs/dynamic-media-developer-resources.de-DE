---
description: RGB-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Antwortbilder verwendet werden soll, wenn mit icc= kein Ausgabefarbraum angegeben ist, sowie für bestimmte RGB-Farbwerte, die mit verschiedenen Bildbereitstellungsbefehlen angegeben werden, z. B. color=.
solution: Experience Manager
title: IccProfileRGB
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileRGB{#iccprofilergb}

RGB-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Antwortbilder verwendet werden soll, wenn mit icc= kein Ausgabefarbraum angegeben ist, sowie für bestimmte RGB-Farbwerte, die mit verschiedenen Bildbereitstellungsbefehlen angegeben werden, z. B. color=.

## Eigenschaften {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Text-String Falls angegeben, muss ein gültiger `icc::Name` aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein RGB sein.

## Standard {#section-dfe08dd7b851453ca816623a4179955b}

Von `default::IccProfileRgb` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
