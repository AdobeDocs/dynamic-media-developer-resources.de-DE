---
description: Vignetten können so erstellt werden, dass sie Beinahe-3D-Reflexionsdaten enthalten.
solution: Experience Manager
title: Spiegelungen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---


# Reflections{#reflections}

Vignetten können so erstellt werden, dass sie Beinahe-3D-Reflexionsdaten enthalten.

Wenn dies so verfasst wird, werden die folgenden Materialattribute zur Definition der reflektierenden Oberflächeneigenschaften des Materials verwendet:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Beschreibung </p> </th> 
   <th class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>Oberflächenglanz </p> </td> 
   <td> <p>Aus Vignette </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>Glanzvariation (Graustufenbild) </p> </td> 
   <td> <p>Keine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> raw=  </span> </a> </p> </td> 
   <td> <p>Oberflächenrauigkeit </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Materialart </p> </td> 
   <td> <p>0 (unbekannt) </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Renderer passt den Bereich der Attribute `gloss=` und `rough=` entsprechend `type=` an. Einige Werkstofftypen wie Gewebe sind im Allgemeinen weniger reflektierend als Werkstoffe wie Stein oder Metall, und die gleiche Glanzmenge, die für eines angegeben wird, führt zu einem anderen Reflexionseffekt als die andere. `gloss=`und Rauigkeit haben einen ziemlich breiten Umfang, wenn nicht angegeben oder auf 0 gesetzt  `type=` ist.

`glossmap=` kann verwendet werden, um die Glanz eines Materials Pixel für Pixel zu steuern.
