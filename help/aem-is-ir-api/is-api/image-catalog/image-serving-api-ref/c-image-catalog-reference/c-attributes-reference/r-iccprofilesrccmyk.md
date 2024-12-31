---
title: IccProfileSrcCmyk
description: CMYK-Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für CMYK-Quellbilder verwendet werden soll, die kein Farbprofil einbetten, sowie für bestimmte CMYK-Farbwerte, die mit verschiedenen Bildbereitstellungsbefehlen angegeben werden, z. B. color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK-Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für CMYK-Quellbilder verwendet werden soll, die kein Farbprofil einbetten, sowie für bestimmte CMYK-Farbwerte, die mit verschiedenen Bildbereitstellungsbefehlen angegeben werden, z. B. color=.

## Eigenschaften {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Text-String Falls angegeben, muss ein gültiger `icc::Name` aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein CMYK-Profil sein.

## Standard {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Von `default::IccProfileSrcCmyk` geerbt, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcCmyk` nicht zu einem gültigen Profil aufgelöst wird, wird stattdessen `attribute::IccProfileCmyk` verwendet.

## Verwandte Themen {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
