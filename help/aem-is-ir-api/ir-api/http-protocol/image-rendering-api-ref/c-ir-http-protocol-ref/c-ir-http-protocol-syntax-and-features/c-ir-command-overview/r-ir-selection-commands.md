---
description: Mit diesen Befehlen werden Vignettengruppen, Objekte, Unterbereiche von Gruppen oder Objekten ausgewählt.
seo-description: Mit diesen Befehlen werden Vignettengruppen, Objekte, Unterbereiche von Gruppen oder Objekten ausgewählt.
seo-title: Auswahlbefehle
solution: Experience Manager
title: Auswahlbefehle
topic: Scene7 Image Serving - Image Rendering API
uuid: fac4080b-3b7e-46ac-a564-3a7eff80c9eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Auswahlbefehle{#selection-commands}

Mit diesen Befehlen werden Vignettengruppen, Objekte, Unterbereiche von Gruppen oder Objekten ausgewählt.

Der Befehl bzw. das Material bzw. beide werden nach diesem Auswahlbefehl und vor dem nächsten Auswahlbefehl (bzw. dem Ende der Anforderung) auf das ausgewählte Element festgelegt. Auswahlbefehle begrenzen Materialspezifikationssegmente (MSS).

<table id="simpletable_028957E516644FE8A7B1BC056A32FCD1"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a" type="reference" format="dita" scope="local"> obj</a> </span> </p></td> 
  <td class="stentry"> <p>Wählen Sie anhand des Namens eine Vignettengruppe oder ein Objekt aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b" type="reference" format="dita" scope="local"> sel</a></span> </p></td> 
  <td class="stentry"> <p>Wählen Sie eine Vignettengruppe oder ein Objekt nach Pixelposition aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-decal.md#reference-3a5f1adc7fe24c91aa5655d64038e857" type="reference" format="dita" scope="local"> dekal</a></span> </p></td> 
  <td class="stentry"> <p>Wählen Sie den Dezimalbereich des ausgewählten Objekts aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sub.md#reference-3cedba817f3c401495ba32bd1bf9b383" type="reference" format="dita" scope="local"> sub</a></span> </p></td> 
  <td class="stentry"> <p>Wählen Sie einen Unterbereich der ausgewählten Gruppe oder des ausgewählten Objekts aus. </p></td> 
 </tr> 
</table>

