---
description: Attribute für Text auf Pfad.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# pathAttr{#pathattr}

Attribute für Text auf Pfad.

` pathAttr= *`Richtung`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Richtung </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> | <span class="codeph"> reverse </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Textstartposition auf Pfad (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Textende Position auf Pfad (real 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Angeben `norm` , um Text zu zeichnen, der in der Nähe des ersten Pfadvertex beginnt, und `reverse` um Text in die entgegengesetzte Richtung zu zeichnen, beginnend beim letzten Scheitelpunkt.

*`startPos`* und *`endPos`* die Anpassung der Position auf dem Pfad ermöglichen, an der der Text gezeichnet wird. 0.0 entspricht dem ersten Scheitelpunkt im Pfad und 1.0 dem letzten Scheitelpunkt; Zwischenwerte geben den Abstand zwischen dem ersten und dem letzten Scheitelpunkt an.

## Eigenschaften {#section-80f266da4e2549d89f022a3f9ff4584d}

Ebenenattribut. Wird ignoriert, wenn die Ebene nicht `textPs=` und `textPath=` Befehle.

*`startPos`* muss größer oder gleich 0 und kleiner als 1,0 sein. *`endPos`* muss größer sein als *`startPos`* und kleiner oder gleich 1,0 bei Anwendung auf einen offenen Pfad oder kleiner oder gleich ( *`startPos`* + 1,0) bei Anwendung auf einen geschlossenen Pfad.

## Standard {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Verwandte Themen {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
