---
title: Abziehbilder
description: Zu den Abziehmaterialien gehören Bekleidungskonstrukte wie Applikationen, T-Shirt-Prints und gestickte oder gedruckte Logos. Dazu gehören auch nicht wiederholbare, flache Objekte, die in Innen- oder Außenanwendungen verwendet werden, wie z. B. Flächenteppiche, an der Wand aufgehängte Kunstwerke und Schilder.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# Abziehbilder{#decals}

Zu den Abziehmaterialien gehören Bekleidungskonstrukte wie Applikationen, T-Shirt-Prints und gestickte oder gedruckte Logos. Dazu gehören auch nicht wiederholbare, flache Objekte, die in Innen- oder Außenanwendungen verwendet werden, wie z. B. Flächenteppiche, an der Wand aufgehängte Kunstwerke und Schilder.

Ein Material gilt als Abziehbild, wenn es in einem Abziehbild angegeben ist. Ein Abziehbild ist normalerweise ein RGBA-Bild, wobei der Alphakanal die Form des Abziehbilds definiert.

Ein Aufkleber kann auf jede Ebene, Fließlinie, Skizze, Ebene oder jedes Wandobjekt angewendet werden (es sei denn, die Markierung „Keine Textur“ ist festgelegt). Abziehbilder werden auf das Objekt angewendet, indem die `anchor=` des Abziehbilds am Abziehursprungspunkt des Vignettenobjekts ausgerichtet wird. Die Position kann mit `pos=` weiter eingestellt werden.

Ein Schlagschatten wird gerendert, wenn das Abziehbildmaterial eine Dicke definiert und das Vignettenobjekt einen Lichtvektor definiert.

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
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
   <td colname="col2"> <p>Bild (normalerweise mit Alpha); erforderlich. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size= </span> </a> </p> </td> 
   <td colname="col2"> <p>Abziehbildbreite, -höhe und -dicke (für Schlagschatten). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturauflösung (wird ignoriert, wenn Größe= angegeben ist). </p> </td> 
   <td colname="col3"> <p> <span class="codeph">::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> Anker= </span> </a> </p> </td> 
   <td colname="col2"> <p>Abziehbildpunkt </p> </td> 
   <td colname="col3"> <p>Bildmitte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> POS= </span> </a> </p> </td> 
   <td colname="col2"> <p>Relative Abziehposition. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> OPAC= </span> </a> </p> </td> 
   <td colname="col2"> <p>Deckkraft des Abziehbilds. </p> </td> 
   <td colname="col3"> <p>100 % </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp= </span> </a> </td> 
   <td colname="col2"> <p>Scharfzeichnen. </p> </td> 
   <td colname="col3"> <p>0 (keine Scharfzeichnung) </p> </td> 
  </tr> 
 </tbody> 
</table>
