---
description: CMYK-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Materialbilder verwendet werden soll, die kein Profil einbetten.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für CMYK-Materialbilder verwendet werden soll, die kein Profil einbetten.

## Eigenschaften {#section-0cee77438d914c319ec876edb3490821}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name`-Wert aus der ICC-Profil-Map entweder dieses Bildkatalogs oder des Standardkatalogs oder um einen Dateipfad relativ zu `attribute::RootPath` handeln. Das referenzierte ICC-Profil muss ein CMYK-Profil sein.

## Standard {#section-11f6239e0dd14827abf4a95c1b30161c}

Vererbt von `default::IccProfileSrcCmyk`, wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcCmyk` nicht in ein gültiges Profil aufgelöst wird, wird stattdessen `attribute::IccProfileCmyk` verwendet.

## Verwandte Themen {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
