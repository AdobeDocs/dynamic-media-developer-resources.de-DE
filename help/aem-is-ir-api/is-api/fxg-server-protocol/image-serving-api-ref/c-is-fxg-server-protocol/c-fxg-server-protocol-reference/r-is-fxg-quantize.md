---
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
solution: Experience Manager
title: quantifizieren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Palettentyp {adaptive|web|mac}  </span>  </p> <p>Wählen Sie " <span class="codeph"> web </span>"oder " <span class="codeph"> mac </span>"aus, um eine vordefinierte Palette auszuwählen, oder setzen Sie auf "<span class="codeph"> adaptive </span>", um eine optimale Palette für das Bild zu berechnen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off}- </span> Dithering-Optionen </p> <p>Wählen Sie 'Diffus' für Floyd-Steinberg-Fehlerdiffusion oder 'Aus', um Dithering zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Anzahl der Ausgabefarben (Integer), die in der Palette "<span class="codeph"> adaptive </span>"enthalten sind. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> muss zwischen 2 und 256 liegen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Kommagetrennte Liste von erzwungenen RGB-Farben im Hex6-Format. Ermöglicht die Angabe erzwungener Farben, die in einer Palette "<span class="codeph"> adaptive </span>"enthalten sein sollen. Wenn die Anzahl der angegebenen Farben kleiner ist als <span class="codeph"> numColors </span>, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet. </p> <p>Wird nur verwendet, wenn <span class="codeph"> fmt=gif </span> oder <span class="codeph"> fmt=gif-alpha </span> Andernfalls ignoriert. Die Farben, die mit <span class="codeph"> <span class="varname"> colorList </span> </span> angegeben werden, müssen RGB-Werte im hexadezimalen Format sein (siehe <span class="codeph"> Farbe </span>); keine anderen Farbspezifikatoren sind zulässig. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-b3a979dc9ae3459baa093bf17310988f}

Generieren Sie eine GIF-Miniaturansicht mithilfe der Palette &quot;`web`&quot;und ohne Dithering:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Konvertieren Sie das Bild in eine bitonale GIF-Datei mit Schlüsselfarbtransparenz und erzwingen Sie Farben in Schwarzweiß:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
