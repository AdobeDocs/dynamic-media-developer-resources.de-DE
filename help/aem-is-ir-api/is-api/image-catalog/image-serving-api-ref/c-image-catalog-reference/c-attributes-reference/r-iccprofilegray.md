---
description: Graustufen-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte Graustufen-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-description: Graustufen-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte Graustufen-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileGray{#iccprofilegray}

Graustufen-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte Graustufen-Farbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben wurden.

## Eigenschaften {#section-03f090ee2acf4537b83f78840d23ecab}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name` Wert aus der ICC-Profil-Map dieses Bildkatalogs oder des Standardkatalogs handeln oder um einen Dateipfad relativ zu `attribute::RootPath`. Das referenzierte ICC-Profil muss ein Graustufen-Profil sein.

## Standard {#section-95ba3ab15edc4259b657c6ebf8783d61}

Vererbt von, `default::IccProfileGray` wenn nicht definiert oder leer.

## Verwandte Themen {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
