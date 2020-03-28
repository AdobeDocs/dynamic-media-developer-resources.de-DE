---
description: Dekormaterialien umfassen Bekleidungskonstrukte wie Bekleidungsstücke, T-Shirt-Abdrücke, bestickte oder gedruckte Logos sowie nicht wiederholbare, flache Objekte, die in Innen- oder Außenanwendungen verwendet werden, wie z. B. Flächentrogs, Wand-Hing-Kunst, Schilder usw.
seo-description: Dekormaterialien umfassen Bekleidungskonstrukte wie Bekleidungsstücke, T-Shirt-Abdrücke, bestickte oder gedruckte Logos sowie nicht wiederholbare, flache Objekte, die in Innen- oder Außenanwendungen verwendet werden, wie z. B. Flächentrogs, Wand-Hing-Kunst, Schilder usw.
seo-title: Dezimalstellen
solution: Experience Manager
title: Dezimalstellen
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Dezimalstellen{#decals}

Dekormaterialien umfassen Bekleidungskonstrukte wie Bekleidungsstücke, T-Shirt-Abdrücke, bestickte oder gedruckte Logos sowie nicht wiederholbare, flache Objekte, die in Innen- oder Außenanwendungen verwendet werden, wie z. B. Flächentrogs, Wand-Hing-Kunst, Schilder usw.

Ein Material gilt als dekalisch, wenn es in einem dekalen MSS angegeben ist. Ein Abruf ist normalerweise ein RGBA-Bild, wobei der Alpha-Kanal die Form des Abrufs definiert.

Auf jedes Flachobjekt, jede Fließlinie, jede Skizze, jede Ebene oder jedes Wandobjekt kann ein Dekorationszeichen angewendet werden (es sei denn, das Flag &quot;Keine Textur&quot;ist gesetzt). Dezimalstellen werden auf das Objekt angewendet, indem die Dezimalstellen an der `anchor=` Dezimalstelle des Vignettenobjekts ausgerichtet werden. Die Position kann weiter angepasst werden `pos=`.

Ein Schlagschatten wird gerendert, wenn das Dekormaterial eine Stärke definiert und das Vignettenobjekt einen Lichtvektor definiert.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Bild (normalerweise mit Alpha); erforderlich. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size= </span></a> </p> </td> 
   <td colname="col2"> <p>Dezimalbreite, -höhe und -dicke (für Schlagschatten). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Texturauflösung (ignoriert, wenn size= angegeben ist). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span></a> </p> </td> 
   <td colname="col2"> <p>Dezimalausrichtungspunkt </p> </td> 
   <td colname="col3"> <p>Bildmitte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span></a> </p> </td> 
   <td colname="col2"> <p>Relative Abstandsposition. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span></a> </p> </td> 
   <td colname="col2"> <p>Decale Deckkraft. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </td> 
   <td colname="col2"> <p>Scharfzeichnen. </p> </td> 
   <td colname="col3"> <p>0 (kein Scharfzeichnen) </p> </td> 
  </tr> 
 </tbody> 
</table>

