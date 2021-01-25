---
description: Filter für statischen Inhaltstyp. Gibt eine Filterzeichenfolge für statischen Inhalt an, der über "/is/content"bereitgestellt wird.
seo-description: Filter für statischen Inhaltstyp. Gibt eine Filterzeichenfolge für statischen Inhalt an, der über "/is/content"bereitgestellt wird.
seo-title: Typ
solution: Experience Manager
title: Typ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---


# Typ{#type}

Filter für statischen Inhaltstyp. Gibt eine Filterzeichenfolge für statischen Inhalt an, der über &quot;/is/content&quot;bereitgestellt wird.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Geben Sie die Filterzeichenfolge ein. </p></td> 
 </tr> 
</table>

Der Server vergleicht das Feld mit dem Wert von `catalog::Type` des angeforderten statischen Inhaltselements. Das Element wird an den Client zurückgegeben, wenn die Werte übereinstimmen (Groß-/Kleinschreibung beachten). Andernfalls wird ein Fehler zurückgegeben.

## Eigenschaften {#section-529b088434a44a9f86a64ef548d2925b}

Wird nur für statische Inhaltsanforderungen (nicht Bildanforderungen) unterstützt, die über bereitgestellt werden. Wird ignoriert, wenn `catalog::Type` leer ist oder nicht definiert ist.

## Standard {#section-e9e8f51d0a01452183ccb510efd87d46}

Es wird keine Typübereinstimmung angewendet, wenn `type=` nicht angegeben ist oder leer ist.

## Verwandte Themen {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Bereitstellen von statischen (Nicht-Bild-)Inhalten](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da),  [Katalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
