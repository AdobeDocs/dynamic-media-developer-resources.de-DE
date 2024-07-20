---
title: quantifizieren
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> Palettentyp </p> <p>Wählen Sie "<span class="codeph"> web </span>"oder "<span class="codeph"> mac </span>", um eine vordefinierte Palette auszuwählen, oder setzen Sie auf "<span class="codeph"> adaptive </span>", um eine optimale Palette für das Bild zu berechnen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> Dithering Options </p> <p>Wählen Sie 'Diffus' für Floyd-Steinberg-Fehlerdiffusion oder 'Aus', um Dithering zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Anzahl der in der Palette "<span class="codeph"> adaptive </span>" enthaltenen Ausgabefarben (Integer). </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> muss zwischen 2 und 256 liegen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Kommagetrennte Liste von erzwungenen RGB-Farben im Hex6-Format. Ermöglicht die Angabe erzwungener Farben, die in einer Palette "<span class="codeph"> adaptiv </span>" enthalten sein sollen. Wenn die angegebene Anzahl von Farben kleiner als <span class="codeph"> numColors </span> ist, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet. </p> <p>Wird nur verwendet, wenn <span class="codeph"> fmt=gif </span> oder <span class="codeph"> fmt=gif-alpha </span>. Andernfalls ignoriert. Die mit <span class="codeph"> <span class="varname"> colorList </span> </span> angegebenen RGB-Werte müssen im Hexadezimalformat vorliegen (siehe <span class="codeph"> color </span>). Es sind keine anderen Farbspezifikatoren zulässig. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-b3a979dc9ae3459baa093bf17310988f}

Generieren Sie eine GIF-Miniaturansicht mithilfe der Palette &quot;`web`&quot; und ohne Dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Konvertieren Sie das Bild in eine bi-tonale GIF mit Schlüsselfarbtransparenz und erzwingen Sie Farben in Schwarzweiß:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
