---
description: Graustufen-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für Graustufen-Quellbilder verwendet werden soll, die kein Profil einbetten, sowie für bestimmte Graustufen-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-description: Graustufen-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für Graustufen-Quellbilder verwendet werden soll, die kein Profil einbetten, sowie für bestimmte Graustufen-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Graustufen-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für Graustufen-Quellbilder verwendet werden soll, die kein Profil einbetten, sowie für bestimmte Graustufen-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-8cbb316df6eb463aaca7b308d3568086}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name`-Wert aus der ICC-Profil-Map entweder dieses Bildkatalogs oder des Standardkatalogs oder um einen Dateipfad relativ zu `attribute::RootPath` handeln. Das referenzierte ICC-Profil muss ein Graustufen-Profil sein.

## Standard {#section-bcc7250715884412bd0780f60d1cce7b}

Vererbt von `default::IccProfileSrcGray`, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcGray` nicht in ein gültiges Profil aufgelöst wird, wird stattdessen `attribute::IccProfileGray` verwendet.

## Verwandte Themen {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
