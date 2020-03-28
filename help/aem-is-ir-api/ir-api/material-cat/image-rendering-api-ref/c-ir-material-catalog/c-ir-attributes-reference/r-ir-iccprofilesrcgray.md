---
description: Graustufen-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für Graustufenbilder verwendet werden soll, die kein Profil einbetten.
seo-description: Graustufen-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für Graustufenbilder verwendet werden soll, die kein Profil einbetten.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

Graustufen-Standardeingabefarben-Profil. Gibt den Namen des ICC-Profils an, das für Graustufenbilder verwendet werden soll, die kein Profil einbetten.

## Eigenschaften {#section-97923d8561b845309442d57d017d91a4}

Textzeichenfolge. Ist dies der Fall, muss es sich um einen gültigen `icc::Name` Wert aus der ICC-Profil-Map dieses Bildkatalogs oder des Standardkatalogs handeln oder um einen Dateipfad relativ zu `attribute::RootPath`. Das referenzierte ICC-Profil muss ein Graustufen-Profil sein.

## Standard {#section-02c52805ee13483dba7878aeab51f889}

Vererbt von, `default::IccProfileSrcGray` wenn nicht definiert oder leer. Wenn `attribute::IccProfileSrcGray` nicht auf ein gültiges Profil aufgelöst wird, `attribute::IccProfileGray` wird stattdessen verwendet.

## Verwandte Themen {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
