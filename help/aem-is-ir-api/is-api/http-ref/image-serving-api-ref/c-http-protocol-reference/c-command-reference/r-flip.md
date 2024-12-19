---
title: leicht schlagen
description: Ebene spiegeln. Spiegelt die Ebene horizontal, vertikal oder beides nach dem Anwenden von Zuschnitt= und vor dem Drehen= und Dehnen=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---

# leicht schlagen{#flip}

Ebene spiegeln. Spiegelt die Ebene horizontal, vertikal oder beides nach dem Anwenden von Zuschnitt= und vor dem Drehen= und Dehnen=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> LR-</span> </p> </td> 
  <td class="stentry"> <p>Spiegelt die Ebene horizontal (links-rechts). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Ebene vertikal kippen (nach oben und unten). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Lrud </span> </p> </td> 
  <td class="stentry"> <p>Sowohl horizontal als auch vertikal kippen. </p> </td> 
 </tr> 
</table>

Sie kann auch auf Textebenen angewendet werden.

Einige Befehle, einschließlich `extend=`, gelten implizit für Ebene 0 anstelle der zusammengesetzten Ebene, wenn `layer=comp` ausgewählt ist. In solchen Szenarien werden alle Befehle, die automatisch Ebene 0 zugeordnet sind, vor den Befehlen angewendet, die für `layer=comp` gelten. Daher wird `extend=` beim `layer=comp` vor der `flip=` angewendet.

>[!NOTE]
>
>Die gespiegelte Ebene wird basierend auf dem Ebenenanker positioniert. Unterschiedliche `flip=` führen zu unterschiedlichen Ebenenpositionen, wenn sich der Anker nicht in der Mitte der Ebene befindet.

## Eigenschaften {#section-294da2af7be746b5adfc35e29ee68217}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-502044f81a89492198d5f12a738459ea}

Keine.

## Verwandte Themen {#section-47f6484deccd420983df15ec163b4a83}

[Drehen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [Anker=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
