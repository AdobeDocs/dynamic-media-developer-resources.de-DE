---
description: Vignetten können so erstellt werden, dass sie nahezu 3D-Reflexionsdaten enthalten.
solution: Experience Manager
title: Spiegelungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 4%

---

# Spiegelungen{#reflections}

Vignetten können so erstellt werden, dass sie nahezu 3D-Reflexionsdaten enthalten.

Wenn dies so festgelegt ist, werden die folgenden Materialattribute verwendet, um die Eigenschaften der reflektierenden Oberfläche des Materials zu definieren:

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
   <td> <p>Glanzvariante (Graustufenbild) </p> </td> 
   <td> <p>Keine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> raw=  </span> </a> </p> </td> 
   <td> <p>Oberflächenrauigkeit </p> </td> 
   <td> <p>40 % </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Materialart </p> </td> 
   <td> <p>0 (unbekannt) </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Renderer passt den Bereich der Attribute `gloss=` und `rough=` gemäß `type=` an. Einige Materialarten wie Gewebe sind im Allgemeinen weniger reflektierend als Materialarten wie Stein oder Metall, und die gleiche Glanzmenge, die für eine der beiden Typen angegeben ist, führt zu einer anderen Reflexion als die andere. `gloss=`und Rauigkeit haben einen ziemlich großen Spielraum, wenn nicht angegeben  `type=` ist oder auf 0 gesetzt ist.

`glossmap=` kann verwendet werden, um die Glanz eines Materials Pixel für Pixel zu steuern.
