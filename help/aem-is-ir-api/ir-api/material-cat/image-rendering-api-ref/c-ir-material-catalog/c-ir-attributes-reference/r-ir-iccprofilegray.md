---
title: IccProfileGray
description: Graustufen-Standardfarbraum. Gibt den Namen des ICC-Farbprofils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

Graustufen-Standardfarbraum. Gibt den Namen des ICC-Farbprofils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit `icc=` angegeben ist.

## Eigenschaften {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Textzeichenfolge. Falls angegeben, muss ein gültiger `icc::Name` -Wert aus der ICC-Profilzuordnung dieses Materialkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein Graustufenprofil sein.

## Standard {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Wird von `default::IccProfileGray` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
