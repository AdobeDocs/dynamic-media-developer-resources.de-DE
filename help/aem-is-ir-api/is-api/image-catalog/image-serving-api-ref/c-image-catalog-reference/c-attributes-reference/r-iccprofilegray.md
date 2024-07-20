---
title: IccProfileGray
description: Graustufen-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben ist, und für bestimmte Graustufenfarbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

Graustufen-Standardausgabefarbprofil. Gibt den Namen des ICC-Farbprofils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn kein Ausgabefarbraum mit icc= angegeben ist, und für bestimmte Graustufenfarbwerte, die mit verschiedenen Image Serving-Befehlen wie color= angegeben werden.

## Eigenschaften {#section-03f090ee2acf4537b83f78840d23ecab}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `icc::Name` -Wert aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein Graustufenprofil sein.

## Standard {#section-95ba3ab15edc4259b657c6ebf8783d61}

Wird von `default::IccProfileGray` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
