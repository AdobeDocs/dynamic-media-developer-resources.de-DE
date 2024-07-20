---
description: XMP Metadaten. Gibt die XMP Metadaten zurück, die mit dem im Anfragepfad angegebenen Bild verknüpft sind.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---

# xmp{#xmp}

XMP Metadaten. Gibt die XMP Metadaten zurück, die mit dem im Anfragepfad angegebenen Bild verknüpft sind.

`req=xmp`

Andere Befehle werden ignoriert. Es gilt die UTF-8-Kodierung. Die Antwort wird als XML mit dem MIME-Typ `text/xml` formatiert.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

## Eigenschaften {#section-0d26b6a56c844153ae5cea4880370d00}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Wenn die URL keinen Bildpfad oder keine Modifikatoren enthält, dann:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Andernfalls `req=img`

## Beispiele {#section-34213692deab4a0f9037d5844132ee14}

Eigenschaften der Bilddatei abfragen.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Eigenschaften des Abfragebildkatalogs:

` http:// *`server`*/myRootId?req=catalogprops`

Greifen Sie von der clientseitigen JavaScript aus, die in eine HTML-Datei eingebettet ist, auf die Eigenschaften eines Bildkatalogeintrags zu:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Rufen Sie das Maskenbild für einen bestimmten Katalogeintrag ab, skaliert auf 25 % der Originalgröße:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Bild mit achter Größe anfordern:

` http:// *`server`*/myRootId/myImageId?scl=8`

Dies entspricht:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Fordern Sie eine Miniaturansicht eines Bildes an, indem Sie auf die im Bildkatalog angegebenen Attribute für Miniaturansichten zurückgreifen:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Senden Sie eine Textnachricht an die Serverprotokolle:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Verwandte Themen {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md), [Miniaturbildskalierung](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f), [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), [Imagemaps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
