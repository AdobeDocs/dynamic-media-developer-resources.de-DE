---
title: Auswahlbefehle
description: Mit diesen Befehlen können Sie Vignettengruppen, Objekte, Unterbereiche von Gruppen oder Objekten auswählen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43f6ec6e-e4eb-468d-9c66-841af5e0a8a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# Auswahlbefehle{#selection-commands}

Mit diesen Befehlen können Sie Vignettengruppen, Objekte, Unterbereiche von Gruppen oder Objekten auswählen.

Der Befehl bzw. das Material oder beides wird nach diesem Auswahlbefehl und vor dem nächsten Auswahlbefehl (oder dem Ende der Anforderung) auf das ausgewählte Element festgelegt. Auswahlbefehle trennen Materialspezifikationssegmente (MSS).

<table id="simpletable_028957E516644FE8A7B1BC056A32FCD1"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a" type="reference" format="dita" scope="local"> OBJ</a> </span> </p></td> 
  <td class="stentry"> <p>Wählen Sie eine Vignettengruppe oder ein Objekt nach Namen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b" type="reference" format="dita" scope="local"> SEL</a></span> </p></td> 
  <td class="stentry"> <p>Wählen Sie eine Vignettengruppe oder ein Objekt nach Pixelposition aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-decal.md#reference-3a5f1adc7fe24c91aa5655d64038e857" type="reference" format="dita" scope="local"> Aufkleber</a></span> </p></td> 
  <td class="stentry"> <p>Wählen Sie den Abziehbildbereich des ausgewählten Objekts aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sub.md#reference-3cedba817f3c401495ba32bd1bf9b383" type="reference" format="dita" scope="local"> Unter</a></span> </p></td> 
  <td class="stentry"> <p>Einen Unterbereich der ausgewählten Gruppe oder des ausgewählten Objekts auswählen. </p></td> 
 </tr> 
</table>
