---
title: Reflexionen
description: Vignetten können so verfasst werden, dass sie nahezu 3D-Reflexionsdaten enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# Reflexionen{#reflections}

Vignetten können so verfasst werden, dass sie nahezu 3D-Reflexionsdaten enthalten.

Wenn dies der Fall ist, werden die folgenden Materialattribute verwendet, um die reflektierenden Oberflächeneigenschaften des Materials zu definieren:

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
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> Glanz=</span> </a> </p> </td> 
   <td> <p>Oberflächenglanz </p> </td> 
   <td> <p>Aus Vignette </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> Glossmap= </span> </a> </p> </td> 
   <td> <p>Glanzvariation (Graustufenbild) </p> </td> 
   <td> <p>Keine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> grob= </span> </a> </p> </td> 
   <td> <p>Oberflächenrauheit </p> </td> 
   <td> <p>40 % </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Materialart </p> </td> 
   <td> <p>0 (unbekannt) </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Renderer passt den Bereich des `gloss=`- und `rough=` entsprechend den `type=` an. Einige Materialtypen wie Gewebe sind weniger reflektierend als Materialtypen wie Stein oder Metall. Außerdem führt die gleiche für eine bestimmte Glanzmenge oft zu einem anderen Reflexionseffekt als die andere. Das Attribut `gloss=` und die Rauigkeit haben einen ziemlich breiten Farbraum, wenn `type=` nicht angegeben oder auf `0` gesetzt ist.

`glossmap=` Wird verwendet, um den Glanz eines Materials Pixel für Pixel zu steuern.
