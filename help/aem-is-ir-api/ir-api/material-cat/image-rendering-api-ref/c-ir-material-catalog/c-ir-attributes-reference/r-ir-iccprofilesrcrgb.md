---
title: IccProfileSrcRgb
description: RGB - Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Materialbilder und Vignetten verwendet werden soll, die kein Farbprofil einbetten. Auch für RGB-Farbwerte, die mit verschiedenen Image Rendering-Befehlen angegeben werden, wie bgc= und color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB - Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Materialbilder und Vignetten verwendet werden soll, die kein Farbprofil einbetten. Auch für RGB-Farbwerte, die mit verschiedenen Image Rendering-Befehlen angegeben werden, wie z. B. `bgc=` und `color=`.

## Eigenschaften {#section-c22966bba03e43c08e9d3fb91bfdd465}

Textzeichenfolge. Wenn angegeben, muss eine gültige sein. `icc::Name` Wert aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder einen Dateipfad relativ zu `attribute::RootPath`. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-0171cd6680284bfa9844b9cc3644ca61}

Vererbt von `default::IccProfileSrcRgb` wenn nicht definiert oder leer ist. Wenn `attribute::IccProfileSrcRgb` wird nicht in ein gültiges Profil aufgelöst; `attribute::IccProfileRgb` stattdessen verwendet.

## Verwandte Themen {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
