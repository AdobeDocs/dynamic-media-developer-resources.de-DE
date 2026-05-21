---
title: pathAttr
description: Text-auf-Pfad-Attribute.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
TQID: 'https://experienceleague.adobe.com/A7uOgsYtOH6AmVOtbUfQDVJHwJEkCSXqBYavY9CbRkw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 1%

---

# pathAttr{#pathattr}

Text-auf-Pfad-Attribute.

` pathAttr= *`direction`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> <span class="varname"> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Norm </span> | <span class="codeph"> umgekehrte </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos-</span> </p> </td> 
  <td class="stentry"> <p>Text-Startposition auf Pfad (real 0.0…1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Text-Endposition auf Pfad (real 0.0…&lt;2.0). </p> </td> 
 </tr> 
</table>

Geben Sie `norm` an, um Text beginnend beim ersten Pfadscheitelpunkt und `reverse` zu zeichnen, um Text in die entgegengesetzte Richtung beginnend beim letzten Scheitelpunkt zu zeichnen.

*`startPos`* und *`endPos`* ermöglichen die Anpassung der Position des Textes auf dem Pfad. 0,0 entspricht dem ersten Scheitelpunkt im Pfad und 1,0 dem letzten Scheitelpunkt; Zwischenwerte geben den Abstand entlang des Pfads zwischen dem ersten und dem letzten Scheitelpunkt an.

## Eigenschaften {#section-80f266da4e2549d89f022a3f9ff4584d}

Ebenenattribut. Wird ignoriert, wenn die Ebene keine `textPs=`- und `textPath=` enthält.

*`startPos`* muss größer oder gleich 0 und kleiner als 1,0 sein. *`endPos`* muss größer als *`startPos`* und kleiner oder gleich 1,0 sein, wenn es auf einen offenen Pfad angewendet wird, oder kleiner oder gleich ( *`startPos`* + 1,0), wenn es auf einen geschlossenen Pfad angewendet wird.

## Standard {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Verwandte Themen {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
