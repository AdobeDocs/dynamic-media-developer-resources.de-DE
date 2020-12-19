---
description: Diese Befehle gelten für Bild-, Text- und Vollfarbebenen. Die meisten sind für das Composite-Bild und für einfache Anforderungen ohne Ebenen nicht aussagekräftig. Sie gelten nicht für Effektebenen.
seo-description: Diese Befehle gelten für Bild-, Text- und Vollfarbebenen. Die meisten sind für das Composite-Bild und für einfache Anforderungen ohne Ebenen nicht aussagekräftig. Sie gelten nicht für Effektebenen.
seo-title: Allgemeine Ebenenbefehle
solution: Experience Manager
title: Allgemeine Ebenenbefehle
topic: Scene7 Image Serving - Image Rendering API
uuid: f11da6ba-18f2-42d6-8257-cb8ebef8c7d8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# Allgemeine Ebenenbefehle{#common-layer-commands}

Diese Befehle gelten für Bild-, Text- und Vollfarbebenen. Die meisten sind für das Composite-Bild und für einfache Anforderungen ohne Ebenen nicht aussagekräftig. Sie gelten nicht für Effektebenen.

<table id="simpletable_8A74E965537D4E8CB91E95AEAE9673E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p> </td> 
  <td class="stentry"> <p>Gibt den Übergangsmodus für Ebenen an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab" type="reference" format="dita" scope="local"> bgColor</a> </p></td> 
  <td class="stentry"> <p>Gibt eine Hintergrundfarbe und Deckkraft der Ebene an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac" type="reference" format="dita" scope="local"> erweitern</a> </p></td> 
  <td class="stentry"> <p>Erweitert (oder schneidet) das Rechteck der Ebene. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> color</a> </p></td> 
  <td class="stentry"> <p>Legt die Farbe und Deckkraft der Ebene fest. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d" type="reference" format="dita" scope="local"> layer</a> </p></td> 
  <td class="stentry"> <p>Wählt die Ebene aus und gibt die z-Reihenfolge an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06" type="reference" format="dita" scope="local"> Karte</a> </p></td> 
  <td class="stentry"> <p>Definiert eine Imagemap für diese Ebene. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>Reduziert die Deckkraft der Ebene. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138" type="reference" format="dita" scope="local"> herkunft</a> </p></td> 
  <td class="stentry"> <p>Legt den Herkunft-Punkt der Ebene fest. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>Positioniert die Ebene relativ zur Ebene 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-size-reference.md#reference-04d383f32c7b4003bed9978cb854747b" type="reference" format="dita" scope="local"> Größe</a> </p></td> 
  <td class="stentry"> <p>Legt die Beschränkung der Ebenengröße fest. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-hide.md#reference-e336facb21a644eea78c2c84c1c4576e" type="reference" format="dita" scope="local"> ausblenden</a> </p></td> 
  <td class="stentry"> <p>Blenden Sie die Ebene aus. </p></td> 
 </tr> 
</table>

