---
description: CMYK-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für CMYK-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben ist, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für CMYK-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben ist, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-d8b6102cc1c744d482f99808ccfcaa24}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `icc::Name` -Wert aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein CMYK-Profil sein.

## Standard {#section-62442df09a724950bfbdd0640b3e6678}

Wird von `default::IccProfileCmyk` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
