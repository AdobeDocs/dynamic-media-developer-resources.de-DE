---
description: RGB - Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Quellbilder verwendet werden soll, die kein Farbprofil einbetten, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB - Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Quellbilder verwendet werden soll, die kein Farbprofil einbetten, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-3cd753196959462e9e674dab0b033d08}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `icc::Name` -Wert aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Wird von `default::IccProfileSrcRgb` übernommen, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcRgb` nicht in ein gültiges Profil aufgelöst wird, wird stattdessen `attribute::IccProfileRgb` verwendet.

## Verwandte Themen {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
