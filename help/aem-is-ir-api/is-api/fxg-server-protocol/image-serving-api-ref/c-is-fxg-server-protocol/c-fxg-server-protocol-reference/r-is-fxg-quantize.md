---
title: quanteln
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die Konvertierung der GIF-Ausgabe an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# quanteln{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die Konvertierung der GIF-Ausgabe an.

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
  <td class="stentry"> <p>Kommagetrennte Liste erzwungener RGB-Farben im Hex6-Format. Hier können Sie erzwungene Farben angeben, die in die Palette "<span class="codeph"> adaptive </span>" aufgenommen werden sollen. Wenn die Anzahl der angegebenen Farben kleiner als <span class="codeph"> numColors-</span> ist, werden zusätzliche Farben anhand des Bildinhalts berechnet. </p> <p>Wird nur verwendet, wenn <span class="codeph"> fmt=gif </span> oder <span class="codeph"> fmt=gif-alpha </span>. Andernfalls ignoriert. Die mit <span class="codeph"> <span class="varname"> colorList </span> </span> angegebenen Farben müssen RGB-Werte im Hex6-Format sein (siehe <span class="codeph">-</span>). Andere Farbspezifikatoren sind nicht zulässig. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-b3a979dc9ae3459baa093bf17310988f}

Generieren einer GIF-Miniaturansicht mit der Palette &quot;`web`&quot; ohne Dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Konvertieren Sie das Bild in eine zweifarbige GIF mit Schlüsselfarbtransparenz und erzwingen Sie Farben in Schwarzweiß:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
