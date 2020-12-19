---
description: XMP Metadaten. Gibt die XMP Metadaten zurück, die mit dem im Anforderungspfad angegebenen Bild verknüpft sind.
seo-description: XMP Metadaten. Gibt die XMP Metadaten zurück, die mit dem im Anforderungspfad angegebenen Bild verknüpft sind.
seo-title: xmp
solution: Experience Manager
title: xmp
topic: Scene7 Image Serving - Image Rendering API
uuid: e1583ffe-531a-4334-b974-72df6fcb14ba
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---


# xmp{#xmp}

XMP Metadaten. Gibt die XMP Metadaten zurück, die mit dem im Anforderungspfad angegebenen Bild verknüpft sind.

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

Eigenschaften von Abfragen-Bilddateien.

` http:// *`Server`*/myPath/myImage.tif?req=imageprops`

Eigenschaften des Abfrage-Bildkatalogs:

` http:// *`Server`*/myRootId?req=catalogprops`

Greifen Sie von clientseitigem JavaScript, das in eine HTML-Datei eingebettet ist, auf die Eigenschaften eines Bildkatalogeintrags zu:

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

Abrufen des Maskenbilds für einen bestimmten Katalogeintrag, skaliert auf 25 % der Originalgröße:

` http:// *`Server`*/myRootId/myImageId?req=mask&scale=0.25`

Bild in achter Größe anfordern:

` http:// *`Server`*/myRootId/myImageId?scl=8`

Dies entspricht:

` http:// *`Server`*/myRootId/myImageId?req=img&scl=8`

Fordern Sie eine Miniaturansicht eines Bilds an, wobei die im Bildkatalog angegebenen Attribute für die Miniaturansicht verwendet werden:

` http:// *`Server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Senden Sie eine Textnachricht an die Serverprotokolle:

` http:// *`Server`*/myRootId?req=message&message=This%20is%20the%20message`

## Verwandte Themen {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [catalog::Zielgruppen](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md),  [Miniaturansicht](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f),  [Eigenschaften](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9),  [Imagemaps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
