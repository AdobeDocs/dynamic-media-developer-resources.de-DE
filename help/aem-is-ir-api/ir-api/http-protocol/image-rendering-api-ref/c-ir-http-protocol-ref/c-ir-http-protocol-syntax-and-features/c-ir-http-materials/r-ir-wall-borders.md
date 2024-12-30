---
title: Wandränder
description: Ein Material gilt als Wandumrandung, wenn es in einer Wandumrandung MSS angegeben ist (eingeführt mit sub=3..5).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e11c38d0-8255-4363-ae60-f47be37a1495
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# Wandränder{#wall-borders}

Ein Material gilt als Wandumrandung, wenn es in einer Wandumrandung MSS angegeben ist (eingeführt mit sub=3..5).

Die Texturbilder der Wandränder können einen Alphakanal enthalten, um die Form des Rahmens zu definieren. Wandränder können nur auf Wandobjekte angewendet werden.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Wiederholbares Texturbild; erforderlich </p> </td> 
   <td colname="col3"> <p>Keine </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturauflösung </p> </td> 
   <td colname="col3"> <p> <span class="codeph">::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> Anker= </span> </a> </p> </td> 
   <td colname="col2"> <p>Horizontale Texturausrichtung (y-Wert wird ignoriert) </p> </td> 
   <td colname="col3"> <p>0 (linker Bildrand) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Scharfzeichnen </p> </td> 
   <td colname="col3"> <p>0 (keine Scharfzeichnung) </p> </td> 
  </tr> 
 </tbody> 
</table>
