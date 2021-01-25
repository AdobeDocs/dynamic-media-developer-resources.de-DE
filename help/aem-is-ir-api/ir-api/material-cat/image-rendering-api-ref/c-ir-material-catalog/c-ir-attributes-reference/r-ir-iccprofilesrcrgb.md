---
description: RGB-Standardeingabefarbe Profil. Gibt den Namen des ICC-Profils an, das für RGB-Materialbilder und -Vignetten verwendet werden soll, die kein Profil einbetten, sowie für RGB-Farbwerte, die mit verschiedenen Bildwiedergabebefehlen wie bgc= und color= angegeben wurden.
seo-description: RGB-Standardeingabefarbe Profil. Gibt den Namen des ICC-Profils an, das für RGB-Materialbilder und -Vignetten verwendet werden soll, die kein Profil einbetten, sowie für RGB-Farbwerte, die mit verschiedenen Bildwiedergabebefehlen wie bgc= und color= angegeben wurden.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9657e296-0d2a-4b05-9be7-5a54d3277f90
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB-Standardeingabefarbe Profil. Gibt den Namen des ICC-Profils an, das für RGB-Materialbilder und -Vignetten verwendet werden soll, die kein Profil einbetten, sowie für RGB-Farbwerte, die mit verschiedenen Bildwiedergabebefehlen wie bgc= und color= angegeben wurden.

## Eigenschaften {#section-c22966bba03e43c08e9d3fb91bfdd465}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name`-Wert aus der ICC-Profil-Map entweder dieses Bildkatalogs oder des Standardkatalogs oder um einen Dateipfad relativ zu `attribute::RootPath` handeln. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-0171cd6680284bfa9844b9cc3644ca61}

Vererbt von `default::IccProfileSrcRgb`, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcRgb` nicht in ein gültiges Profil aufgelöst wird, wird stattdessen `attribute::IccProfileRgb` verwendet.

## Verwandte Themen {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
