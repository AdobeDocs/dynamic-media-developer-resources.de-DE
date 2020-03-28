---
description: Ebene spiegeln. Spiegelt die Ebene horizontal, vertikal oder beides nach dem Anwenden von "Beschneiden="und vor "Drehen="und "Erweitern=".
seo-description: Ebene spiegeln. Spiegelt die Ebene horizontal, vertikal oder beides nach dem Anwenden von "Beschneiden="und vor "Drehen="und "Erweitern=".
seo-title: flip
solution: Experience Manager
title: flip
topic: Scene7 Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# flip{#flip}

Ebene spiegeln. Spiegelt die Ebene horizontal, vertikal oder beides nach dem Anwenden von &quot;Beschneiden=&quot;und vor &quot;Drehen=&quot;und &quot;Erweitern=&quot;.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Ebene horizontal spiegeln (links nach rechts). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Ebene vertikal spiegeln (nach unten). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Horizontal und vertikal spiegeln </p> </td> 
 </tr> 
</table>

Kann auch auf Textebenen angewendet werden.

Einige Befehle, darunter `extend=`auch, gelten implizit für Ebene 0 anstelle der Composite-Ebene, wenn ausgewählt `layer=comp` wird. In solchen Szenarien werden alle Befehle, die automatisch der Ebene 0 zugewiesen werden, vor den Befehlen angewendet, die für `layer=comp`die Ebene gelten. So, wann `layer=comp`, `extend=` wird vor `flip=`.

>[!NOTE]
>
>Die umgedrehte Ebene wird basierend auf dem Ebenenanker positioniert. unterschiedliche Werte für &quot;flip=&quot;führen zu unterschiedlichen Ebenenpositionen, wenn sich der Anker nicht in der Mitte der Ebene befindet.

## Eigenschaften {#section-294da2af7be746b5adfc35e29ee68217}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, falls `layer=comp`dies der Fall ist. Von Effektebenen ignoriert.

## Standard {#section-502044f81a89492198d5f12a738459ea}

Keine.

## Verwandte Themen {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
