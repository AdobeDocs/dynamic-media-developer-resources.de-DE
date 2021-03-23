---
description: Graustufen-Standardfarbraum. Gibt den Namen des ICC-Profils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde.
seo-description: Graustufen-Standardfarbraum. Gibt den Namen des ICC-Profils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
uuid: 064be242-d964-4fb8-99ea-78bb5599e70f
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

Graustufen-Standardfarbraum. Gibt den Namen des ICC-Profils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben wurde.

## Eigenschaften {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `icc::Name`-Wert aus der ICC-Profil-Map dieses Materialkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein Graustufen-Profil sein.

## Standard {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Vererbt von `default::IccProfileGray`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
