---
description: Glanz-Map-Bild. Ermöglicht eine Pixel-für-Pixel-Steuerung des Glanzlichts einer wiederholbaren Textur, eines Hintergrundbilds/Randes oder eines Dezimalbereichs.
seo-description: Glanz-Map-Bild. Ermöglicht eine Pixel-für-Pixel-Steuerung des Glanzlichts einer wiederholbaren Textur, eines Hintergrundbilds/Randes oder eines Dezimalbereichs.
seo-title: glossmap
solution: Experience Manager
title: glossmap
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# glossmap{#glossmap}

Glanz-Map-Bild. Ermöglicht eine Pixel-für-Pixel-Steuerung des Glanzlichts einer wiederholbaren Textur, eines Hintergrundbilds/Randes oder eines Dezimalbereichs.

`glossmap={ *``*| *`glossMapFileEmbeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> EmbeddedReq</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}'}|{'{'<span class="varname"> ForeignReq</span>'}' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span></span> </p></td> 
  <td class="stentry"> <p>Glänzende Imagemap-Bilddatei (Graustufen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span></span> </p></td> 
  <td class="stentry"> <p>Anforderung an den Image-Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Foreign Req </span></span> </p></td> 
  <td class="stentry"> <p>Anforderung an einen ausländischen Server. </p></td> 
 </tr> 
</table>

Gilt für Materialien wie metallische Lackeffekte, gestanzte Folienhintergründe und Rahmen, metallische Gewebe usw.

Das Bild für die Glossarkarte muss 8-Bit-Graustufen aufweisen und die exakt gleiche Größe haben wie das mit `src=`dem primären Bild angegebene Bild. Weitere Informationen finden Sie in der Beschreibung der [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Eigenschaften {#section-26375672d69849be9b026cc93c3bc558}

Materialattribut. Unterstützt durch wiederholbare Texturen, Hintergrundbilder, Rahmen und Dekore. Durch feste Farbe, Schrank und Fensterbedeckungsmaterialien ignoriert. See [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) for additional information.

## Standard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Keine.

## Verwandte Themen {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
