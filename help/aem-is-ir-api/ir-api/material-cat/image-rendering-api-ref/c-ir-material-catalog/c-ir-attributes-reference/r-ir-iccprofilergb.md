---
title: IccProfileRGB
description: RGB-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Antwortbilder verwendet werden soll, wenn mit icc= kein Ausgabefarbraum angegeben ist. Auch für bestimmte RGB-Farbwerte, die mit verschiedenen Image-Rendering-Befehlen angegeben werden, z. B. bgc= und color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
TQID: 'https://experienceleague.adobe.com/dyjS9FzJYrC4VXHr2olLvTUEXj-fjKwC1lIkCDc5D2E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 2%

---

# IccProfileRGB{#iccprofilergb}

RGB-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für RGB-Antwortbilder verwendet werden soll, wenn bei `icc=` kein Ausgabefarbraum angegeben ist. Dies gilt auch für bestimmte RGB-Farbwerte, die mit verschiedenen Image-Rendering-Befehlen wie `bgc=` und `color=` festgelegt werden.

## Eigenschaften {#section-b4a1bd92e99047479a5036413525a6d9}

Text-String Falls angegeben, muss ein gültiger `icc::Name` aus der ICC-Profilzuordnung dieses Materialkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein RGB-Profil sein.

## Standard {#section-5809772f8e96438ab7626d323c66a4ba}

Von `default::IccProfileRgb` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
