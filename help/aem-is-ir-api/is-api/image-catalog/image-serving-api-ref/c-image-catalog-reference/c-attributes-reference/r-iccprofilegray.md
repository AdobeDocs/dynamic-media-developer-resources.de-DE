---
title: IccProfileGray
description: Graustufen-Standardfarbprofil für die Ausgabe. Gibt den Namen des ICC-Farbprofils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn mit icc= kein Ausgabefarbraum angegeben wurde, sowie für bestimmte Graustufen-Farbwerte, die mit verschiedenen Bildbereitstellungsbefehlen festgelegt wurden, z. B. color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
TQID: 'https://experienceleague.adobe.com/brb4FvAJ9aMt3FylkuDbuRMEGabGuRqWBVD2Yu1y4os'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

Graustufen-Standardfarbprofil für die Ausgabe. Gibt den Namen des ICC-Farbprofils an, das für Graustufen-Antwortbilder verwendet werden soll, wenn mit icc= kein Ausgabefarbraum angegeben wurde, sowie für bestimmte Graustufen-Farbwerte, die mit verschiedenen Bildbereitstellungsbefehlen festgelegt wurden, z. B. color=.

## Eigenschaften {#section-03f090ee2acf4537b83f78840d23ecab}

Text-String Falls angegeben, muss ein gültiger `icc::Name` aus der ICC-Profilzuordnung dieses Bildkatalogs oder des Standardkatalogs oder ein Dateipfad relativ zu `attribute::RootPath` sein. Das referenzierte ICC-Profil muss ein Graustufenprofil sein.

## Standard {#section-95ba3ab15edc4259b657c6ebf8783d61}

Von `default::IccProfileGray` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
