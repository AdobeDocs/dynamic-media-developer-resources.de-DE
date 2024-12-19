---
title: rau
description: Rauhigkeit der Materialoberfläche. Gibt die relative Rauigkeit der Materialoberfläche an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# rau{#rough}

Rauhigkeit der Materialoberfläche. Gibt die relative Rauigkeit der Materialoberfläche an.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Val </span> </p> </td> 
  <td class="stentry"> <p>Oberflächenrauigkeit (0…100 Prozent) oder -1 zur Auswahl der Standardrauigkeit. </p> </td> 
 </tr> 
</table>

Wird zur Steuerung des Render-Effekts der 3D-Reflexion verwendet. Niedrigere Raueitswerte erzeugen typischerweise glattere Reflexionseffekte; höhere Werte bewirken Randomisierung und Streuung des reflektierten Bildes.

Jeder Materialtyp (`type=`) definiert einen minimalen und einen maximalen Reflexions-Rendereffekt basierend auf der Rauigkeit. Bei einigen Materialtypen (z. B. Wandpapier) hat `rough=` nur minimale Auswirkungen auf das Aussehen der Reflexion, während bei anderen Materialtypen (z. B. Stein oder Keramik) der Effekt wesentlich ausgeprägter ist.

`rough=-1` Setzt die Raueit auf einen serverinternen Standardwert (40% für typische Materialtypen).

## Eigenschaften {#section-515375758b254c80af576271bdb61bb8}

Materialattribut. Wird ignoriert, wenn die Vignette keine 3D-Reflexionsfähigkeit hat, wenn dem Zielobjekt keine 3D-Geometrie zugeordnet ist oder wenn das Zielobjekt keine anderen Objekte in der Szene reflektiert.

## Standard {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Wenn das Material auf einem Katalogeintrag basiert, ansonsten ca. 40%.

## Verwandte Themen {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
