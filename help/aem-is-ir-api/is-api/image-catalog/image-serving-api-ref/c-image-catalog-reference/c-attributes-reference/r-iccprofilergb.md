---
description: RGB-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für RGB-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-description: RGB-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für RGB-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 40606151-d5fa-4ae5-b6f0-e811bfea4691
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileRgb{#iccprofilergb}

RGB-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für RGB-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name` Wert aus der ICC-Profil-Map dieses Bildkatalogs oder des Standardkatalogs handeln oder um einen Dateipfad relativ zu `attribute::RootPath`. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-dfe08dd7b851453ca816623a4179955b}

Vererbt von, `default::IccProfileRgb` wenn nicht definiert oder leer.

## Verwandte Themen {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
