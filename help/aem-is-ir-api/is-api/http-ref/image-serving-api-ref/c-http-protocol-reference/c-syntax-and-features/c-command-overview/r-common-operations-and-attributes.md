---
description: Diese Befehle gelten für Bild-, Text- und einfarbige Ebenen. Sie sind auch im Allgemeinen für zusammengesetzte Bilder und einfache Bildanforderungen ohne Ebenen nützlich.
solution: Experience Manager
title: Gemeinsame Aktionen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f30a9653-7aed-4233-8361-18ca6561d420
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Gemeinsame Aktionen{#common-operations}

Diese Befehle gelten für Bild-, Text- und einfarbige Ebenen. Sie sind auch im Allgemeinen für zusammengesetzte Bilder und einfache Bildanforderungen ohne Ebenen nützlich.

<table id="simpletable_996969D618C94BE8B81FAED512B5B7BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>Blendet die Ebene aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a" type="reference" format="dita" scope="local"> op_brightness</a> </p></td> 
  <td class="stentry"> <p>Passt die Ebenenhelligkeit an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-colorbalance.md#reference-fb6af4ecf0f842d3adfdda342834a8fd" type="reference" format="dita" scope="local"> op_colorbalance</a> </p></td> 
  <td class="stentry"> <p>Passt unabhängig Rot, Grün, Blau an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-colorize.md#reference-50399231d6dc4c15b3ab5b93c32c458a" type="reference" format="dita" scope="local"> op_colorize</a> </p></td> 
  <td class="stentry"> <p>Colorisiert die Ebenendaten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d" type="reference" format="dita" scope="local"> op_contrast</a> </p></td> 
  <td class="stentry"> <p>Passt den Kontrast an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-hue.md#reference-4d97f5e206114db8b09132fd6e55ec00" type="reference" format="dita" scope="local"> op_hue</a> </p></td> 
  <td class="stentry"> <p>Verschiebt den Farbton aller Farben. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-invert.md#reference-5e3a8e9882a74a52acfd503cd7987828" type="reference" format="dita" scope="local"> op_invert</a> </p></td> 
  <td class="stentry"> <p>Farben umkehren. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_geräusch</a> </p></td> 
  <td class="stentry"> <p>Fügt der Ebene Rauschen hinzu. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-saturation.md#reference-6b7ee05a462f4f01b1fb7108230d90d9" type="reference" format="dita" scope="local"> op_sättigung</a> </p></td> 
  <td class="stentry"> <p>Passt die Farbsättigung an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541" type="reference" format="dita" scope="local"> op_sharpen</a> </p></td> 
  <td class="stentry"> <p>Wendet einfache Scharfzeichnung an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm</a> </p></td> 
  <td class="stentry"> <p>Wendet die Unschärfemaske an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-flip.md#reference-f8568a61b77c41569d382a3147964ce3" type="reference" format="dita" scope="local"> flip</a> </p></td> 
  <td class="stentry"> <p>Spiegelt die Ebene horizontal und/oder vertikal. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096" type="reference" format="dita" scope="local"> rotate</a> </p></td> 
  <td class="stentry"> <p>Dreht die Ebene. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-perspective.md#reference-c941f3bb1eee4dd29abf3824c0b0bc8e" type="reference" format="dita" scope="local"> perspektive</a> </p></td> 
  <td class="stentry"> <p>Umwandlung der Ebene in Perspektive. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d" type="reference" format="dita" scope="local"> clipPath</a> </p></td> 
  <td class="stentry"> <p>Gibt die Clipform(en) für die Ebene an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53" type="reference" format="dita" scope="local"> clipXPath</a> </p></td> 
  <td class="stentry"> <p>Gibt die invertierte(n) Clipform(en) für die Ebene an. </p></td> 
 </tr> 
</table>
