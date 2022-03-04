---
description: CMYK-Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für CMYK-Materialbilder verwendet werden soll, die kein Farbprofil einbetten.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK-Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für CMYK-Materialbilder verwendet werden soll, die kein Farbprofil einbetten.

## Eigenschaften {#section-0cee77438d914c319ec876edb3490821}

Textzeichenfolge. Wenn angegeben, muss eine gültige sein. `icc::Name` Wert aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder einen Dateipfad relativ zu `attribute::RootPath`. Das referenzierte ICC-Profil muss ein CMYK-Profil sein.

## Standard {#section-11f6239e0dd14827abf4a95c1b30161c}

Vererbt von `default::IccProfileSrcCmyk` wenn nicht definiert oder leer ist. Wenn `attribute::IccProfileSrcCmyk` wird nicht in ein gültiges Profil aufgelöst; `attribute::IccProfileCmyk` stattdessen verwendet.

## Verwandte Themen {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
