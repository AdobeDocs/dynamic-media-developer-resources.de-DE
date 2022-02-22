---
title: glossmap
description: Gloss-Map-Bild. Ermöglicht die pixelweise Steuerung des Glanzes einer wiederholbaren Textur, eines Hintergrundbilds/einer Hintergrundfarbe oder eines Decals.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 3%

---

# glossmap {#glossmap}

Gloss-Map-Bild. Ermöglicht die pixelweise Steuerung des Glanzes einer wiederholbaren Textur, eines Hintergrundbilds/einer Hintergrundfarbe oder eines Decals.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss-Map-Bilddatei (Graustufen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Anforderung an Image-Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ForeignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Anfrage an einen ausländischen Server. </p></td> 
 </tr> 
</table>

Gilt für Materialien wie metallische Farbeffekte, gestrichelte Folienhintergrund und Rahmen sowie metallische Gewinde.

Das Glossardiagramm muss in 8-Bit-Graustufen vorliegen und die gleiche Größe wie das mit `src=`. Siehe Beschreibung von [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) für weitere Informationen.

## Eigenschaften {#section-26375672d69849be9b026cc93c3bc558}

Materialattribut. Unterstützt durch wiederholbare Texturen, Wallpaper, Rahmen und Decals. Ignoriert von Materialien mit fester Farbe, Schrank und Fensterbezug. Siehe [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) für weitere Informationen.

## Standard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Keine.

## Verwandte Themen {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
