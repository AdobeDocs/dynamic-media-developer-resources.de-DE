---
title: rau
description: Rauhigkeit der Materialoberfläche. Gibt die relative Rauigkeit der Materialoberfläche an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: 'https://experienceleague.adobe.com/FhLagzJwQodPihSxkEyBl8zSnEU0gDq0zevixYMApUY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 182
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
