---
title: Glosskarte
description: Glanzkarte Bild. Bietet eine pixelweise Steuerung des Glanzes einer wiederholbaren Textur, eines Hintergrundbilds/Rahmens oder eines Abziehbilds.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# Glosskarte {#glossmap}

Glanzkarte Bild. Bietet eine pixelweise Steuerung des Glanzes einer wiederholbaren Textur, eines Hintergrundbilds/Rahmens oder eines Abziehbilds.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss Map Image File (Graustufen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Anfrage an Image-Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ForeignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Anfrage an einen Fremdserver. </p></td> 
 </tr> 
</table>

Anwendbar für Materialien wie metallische Lackeffekte, gestanzte Folientapeten und -rahmen sowie metallische Fadengewebe.

Das Gloss-Map-Bild muss 8-Bit-Graustufen aufweisen und dieselbe Größe wie das mit `src=` angegebene Primärbild haben. Weitere Informationen finden Sie in der Beschreibung von [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Eigenschaften {#section-26375672d69849be9b026cc93c3bc558}

Materialattribut. Unterstützt durch wiederholbare Texturen, Tapeten und Rahmen und Abziehbilder. Wird von einfarbigen Materialien, Schränken und Fensterabdeckungen ignoriert. Weitere Informationen finden Sie unter [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Standard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Keine.

## Verwandte Themen {#section-33953fc1be82452da37141f2e541e00c}

[Gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
