---
description: CMYK-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Quellbilder verwendet werden soll, die kein Profil einbetten, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-description: CMYK-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Quellbilder verwendet werden soll, die kein Profil einbetten, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Quellbilder verwendet werden soll, die kein Profil einbetten, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name`-Wert aus der ICC-Profil-Map entweder dieses Bildkatalogs oder des Standardkatalogs oder um einen Dateipfad relativ zu `attribute::RootPath` handeln. Das referenzierte ICC-Profil muss ein CMYK-Profil sein.

## Standard {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Vererbt von `default::IccProfileSrcCmyk`, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcCmyk` nicht in ein gültiges Profil aufgelöst wird, wird stattdessen `attribute::IccProfileCmyk` verwendet.

## Verwandte Themen {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
