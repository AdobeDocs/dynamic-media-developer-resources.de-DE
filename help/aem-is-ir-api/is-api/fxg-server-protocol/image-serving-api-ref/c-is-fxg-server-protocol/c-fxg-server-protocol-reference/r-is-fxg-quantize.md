---
title: quanteln
description: Farbquantisierung. Legt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# quanteln{#quantize}

Farbquantisierung. Legt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung fest.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Typ </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Wählen Sie ' <span class="codeph"> Web </span>' oder ' <span class="codeph"> mac </span>', um eine vordefinierte Palette zu wählen, oder setzen Sie auf ' <span class="codeph"> adaptive </span>', um eine optimale Palette für das Bild zu berechnen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> Dithering-Optionen </p> <p>Wählen Sie 'Diffuse' für Floyd-Steinberg-Fehlerdiffusion oder 'off', um Dithering zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Anzahl der in der Palette ' <span class="codeph"> adaptiven </span>' enthaltenen Ausgabefarben (Ganzzahl). </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> muss zwischen 2 und 256 liegen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Durch Kommas getrennte Liste erzwungener RGB-Farben im Hex6-Format. Hier können Sie erzwungene Farben angeben, die in die Palette "<span class="codeph"> adaptive </span>" aufgenommen werden sollen. Wenn die Anzahl der angegebenen Farben kleiner als <span class="codeph"> numColors-</span> ist, werden zusätzliche Farben anhand des Bildinhalts berechnet. </p> <p>Wird nur verwendet, wenn <span class="codeph"> fmt=gif </span> oder <span class="codeph"> fmt=gif-alpha </span>. Andernfalls ignoriert. Die mit <span class="codeph"> <span class="varname"> colorList </span> </span> angegebenen Farben müssen RGB-Werte im Hex6-Format sein (siehe <span class="codeph">-</span>); andere Farbspezifikatoren sind nicht zulässig. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-b3a979dc9ae3459baa093bf17310988f}

Generieren eines GIF-Miniaturbilds mit der Palette &quot;`web`&quot; ohne Dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Konvertieren Sie das Bild in eine zweifarbige GIF mit Key-Color-Transparenz und erzwingen Sie Farben in Schwarzweiß:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
