---
description: Attribute für Text auf Pfad.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---


# pathAttr{#pathattr}

Attribute für Text auf Pfad.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Richtung </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> |  <span class="codeph"> umgekehrt  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>Textposition auf Beginn (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>Textendposition auf Pfad (real 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Geben Sie `norm` an, um Text beginnend beim ersten Pfadscheitelpunkt und `reverse` zu zeichnen, um den Text in die entgegengesetzte Richtung, beginnend beim letzten Scheitelpunkt, zu zeichnen.

*`startPos`* und  *`endPos`* ermöglichen die Anpassung an die Stelle auf dem Pfad, an der der Text gezeichnet wird. 0.0 entspricht dem ersten Scheitelpunkt im Pfad und 1.0 dem letzten Scheitelpunkt; Zwischenwerte geben den Abstand zwischen dem ersten und dem letzten Scheitelpunkt an.

## Eigenschaften {#section-80f266da4e2549d89f022a3f9ff4584d}

Ebenenattribut. Wird ignoriert, wenn die Ebene keine `textPs=`- und `textPath=`-Befehle enthält.

*`startPos`* muss größer als oder gleich 0 und kleiner als 1,0 sein.  *`endPos`* muss größer  *`startPos`* und kleiner als 1,0 sein, wenn sie auf einen offenen Pfad angewendet wird, oder kleiner gleich (  *`startPos`* + 1,0), wenn sie auf einen geschlossenen Pfad angewendet wird.

## Standard {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Verwandte Themen {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
