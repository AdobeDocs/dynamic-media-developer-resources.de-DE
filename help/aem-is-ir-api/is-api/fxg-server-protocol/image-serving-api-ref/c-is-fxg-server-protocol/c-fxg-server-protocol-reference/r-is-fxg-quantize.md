---
title: quantifizieren
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> Palettentyp </p> <p>Auswählen " <span class="codeph"> Web </span>' or ' <span class="codeph"> mac </span>", um eine vordefinierte Palette auszuwählen, oder auf " <span class="codeph"> adaptive </span>", um eine optimale Palette für das Bild zu berechnen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> Dithering-Optionen </p> <p>Wählen Sie 'Diffus' für Floyd-Steinberg-Fehlerdiffusion oder 'Aus', um Dithering zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Anzahl der Ausgabefarben (Integer), die im <span class="codeph"> adaptive </span>' Palette </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> muss zwischen 2 und 256 liegen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Kommagetrennte Liste von erzwungenen RGB-Farben im Hex6-Format. Ermöglicht die Angabe erzwungener Farben, die in einem <span class="codeph"> adaptive </span>' Palette Wenn die angegebene Anzahl von Farben kleiner ist als <span class="codeph"> numColors </span>, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet. </p> <p>Wird nur verwendet, wenn <span class="codeph"> fmt=gif </span> oder <span class="codeph"> fmt=gif-alpha </span>. Andernfalls ignoriert. Die mit <span class="codeph"> <span class="varname"> colorList </span> </span> muss RGB-Werte im Hex6-Format sein (siehe <span class="codeph"> color </span>); keine anderen Farbspezifikatoren sind zulässig. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-b3a979dc9ae3459baa093bf17310988f}

Generieren einer GIF-Miniaturansicht mithilfe des `web`&#39; Palette und kein Dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Konvertieren Sie das Bild in eine bi-tonale GIF mit Schlüsselfarbtransparenz und erzwingen Sie Farben in Schwarzweiß:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
