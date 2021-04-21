---
description: CMYK-Standardausgabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK-Standardausgabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte CMYK-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-d8b6102cc1c744d482f99808ccfcaa24}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name`-Wert aus der ICC-Profil-Map entweder dieses Bildkatalogs oder des Standardkatalogs oder um einen Dateipfad relativ zu `attribute::RootPath` handeln. Das referenzierte ICC-Profil muss ein CMYK-Profil sein.

## Standard {#section-62442df09a724950bfbdd0640b3e6678}

Vererbt von `default::IccProfileCmyk`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
