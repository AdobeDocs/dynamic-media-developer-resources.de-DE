---
description: RGB-Standardeingabefarbe Profil. Gibt den Namen des ICC-Profils an, das für RGB-Quellbilder verwendet werden soll, die kein Profil einbetten, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-description: RGB-Standardeingabefarbe Profil. Gibt den Namen des ICC-Profils an, das für RGB-Quellbilder verwendet werden soll, die kein Profil einbetten, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB-Standardeingabefarbe Profil. Gibt den Namen des ICC-Profils an, das für RGB-Quellbilder verwendet werden soll, die kein Profil einbetten, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-3cd753196959462e9e674dab0b033d08}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name` Wert aus der ICC-Profil-Map dieses Bildkatalogs oder des Standardkatalogs handeln oder um einen Dateipfad relativ zu `attribute::RootPath`. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Vererbt von, `default::IccProfileSrcRgb` wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcRgb` nicht auf ein gültiges Profil aufgelöst wird, `attribute::IccProfileRgb` wird stattdessen verwendet.

## Verwandte Themen {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
