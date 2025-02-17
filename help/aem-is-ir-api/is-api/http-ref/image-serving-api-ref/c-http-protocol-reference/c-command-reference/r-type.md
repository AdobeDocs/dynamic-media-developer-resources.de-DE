---
title: Typ
description: Filter für statischen Inhaltstyp. Gibt eine Filterzeichenfolge für statische Inhalte an, die über /is/content bereitgestellt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# Typ{#type}

Filter für statischen Inhaltstyp. Gibt eine Filterzeichenfolge für statische Inhalte an, die über /is/content bereitgestellt werden.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Val</span> </p> </td> 
  <td class="stentry"> <p>Filterzeichenfolge eingeben. </p></td> 
 </tr> 
</table>

Der Server vergleicht `val` mit dem Wert von `catalog::Type` des angeforderten statischen Inhaltselements. Das Element wird an den Client zurückgegeben, wenn die Werte übereinstimmen (Groß-/Kleinschreibung wird beachtet). Andernfalls wird ein Fehler zurückgegeben.

## Eigenschaften {#section-529b088434a44a9f86a64ef548d2925b}

Wird nur für statische Inhaltsanfragen (Nicht-Bild) unterstützt, die über bereitgestellt werden. Ignoriert, wenn `catalog::Type` leer oder nicht definiert ist.

## Standard {#section-e9e8f51d0a01452183ccb510efd87d46}

Es wird keine Typübereinstimmung angewendet, wenn `type=` nicht angegeben oder leer ist.

## Verwandte Themen {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Statische Inhalte (keine Bilder) werden bereitgestellt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [Katalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
