---
description: Mit diesen Befehlen können Sie Ebeneneffekte wie Schlagschatten- oder Schein-Effekte definieren. Effektebenen ignorieren alle anderen Befehle.
seo-description: Mit diesen Befehlen können Sie Ebeneneffekte wie Schlagschatten- oder Schein-Effekte definieren. Effektebenen ignorieren alle anderen Befehle.
seo-title: Ebeneneffekt, Befehle
solution: Experience Manager
title: Ebeneneffekt, Befehle
topic: Scene7 Image Serving - Image Rendering API
uuid: 5fef90d1-0507-497b-9187-869672996852
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Ebeneneffekt, Befehle{#layer-effect-commands}

Mit diesen Befehlen können Sie Ebeneneffekte wie Schlagschatten- oder Schein-Effekte definieren. Effektebenen ignorieren alle anderen Befehle.

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p></td> 
  <td class="stentry"> <p>Gibt den Übergangsmodus für Ebenen an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> color</a> </p></td> 
  <td class="stentry"> <p>Gibt die Farbe und Deckkraft des Haupteffekts an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> effect</a> </p></td> 
  <td class="stentry"> <p>Beginn des Effekteebenensegments und gibt die Z-Reihenfolge an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>Gibt an, wie die Ebenenmaske des übergeordneten Elements (Alpha-Kanal) verwendet wird. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>Federn Sie den Effekt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_large</a> </p></td> 
  <td class="stentry"> <p>Vergrößert oder verkleinert den Ebeneneffekt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_geräusch</a> </p></td> 
  <td class="stentry"> <p>Fügt dem Effekt Rauschen hinzu. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>Reduziert die Deckkraft der Ebene. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>Positioniert die Effektebene relativ zur übergeordneten Ebene. </p></td> 
 </tr> 
</table>
