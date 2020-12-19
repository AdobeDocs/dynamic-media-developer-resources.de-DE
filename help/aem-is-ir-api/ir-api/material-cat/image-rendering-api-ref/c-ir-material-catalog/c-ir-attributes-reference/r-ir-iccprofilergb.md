---
description: RGB-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für RGB-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Rendering-Befehlen wie bgc= und color= angegeben wurden.
seo-description: RGB-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für RGB-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Rendering-Befehlen wie bgc= und color= angegeben wurden.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

RGB-Standard-Ausgabefarbe-Profil. Gibt den Namen des ICC-Profils an, das für RGB-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde, und für bestimmte RGB-Farbwerte, die mit verschiedenen Image Rendering-Befehlen wie bgc= und color= angegeben wurden.

## Eigenschaften {#section-b4a1bd92e99047479a5036413525a6d9}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `icc::Name`-Wert aus der ICC-Profil-Map dieses Materialkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-5809772f8e96438ab7626d323c66a4ba}

Vererbt von `default::IccProfileRgb`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
