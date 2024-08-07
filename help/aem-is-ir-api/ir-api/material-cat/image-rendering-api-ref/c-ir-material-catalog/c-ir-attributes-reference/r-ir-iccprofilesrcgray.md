---
title: IccProfileSrcGray
description: Graustufen-Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für Graustufenbilder verwendet werden soll, die kein Farbprofil einbetten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Graustufen-Standardeingabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für Graustufenbilder verwendet werden soll, die kein Farbprofil einbetten.

## Eigenschaften {#section-97923d8561b845309442d57d017d91a4}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `icc::Name` -Wert aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein Graustufenprofil sein.

## Standard {#section-02c52805ee13483dba7878aeab51f889}

Wird von `default::IccProfileSrcGray` übernommen, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcGray` nicht in ein gültiges Profil aufgelöst wird, wird stattdessen `attribute::IccProfileGray` verwendet.

## Verwandte Themen {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
