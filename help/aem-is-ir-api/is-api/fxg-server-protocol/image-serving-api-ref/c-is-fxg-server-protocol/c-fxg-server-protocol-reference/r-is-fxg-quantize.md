---
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
seo-description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
seo-title: quantifizieren
solution: Experience Manager
title: quantifizieren
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Palettentyp {adaptive|web|mac} </span> </p> <p>Wählen Sie " <span class="codeph"> Web </span>"oder " <span class="codeph"> mac </span>", um eine vordefinierte Palette auszuwählen, oder legen Sie " <span class="codeph"> adaptiv </span>"fest, um eine optimale Palette für das Bild zu berechnen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Dither </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> -Dithering-Optionen </p> <p>Wählen Sie 'diffuse' für Floyd-Steinberg Fehlerdiffusion oder 'off', um Dithering zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
  <td class="stentry"> <p>Anzahl der Ausgabefarben (Ganzzahl) in der Palette " <span class="codeph"> adaptiv </span>". </p> <p> <span class="codeph"> Die <span class="varname"> numColors </span> </span> müssen zwischen 2 und 256 liegen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
  <td class="stentry"> <p>Kommagetrennte Liste von erzwungenen RGB-Farben im Hex6-Format. Ermöglicht Ihnen das Festlegen erzwungener Farben, die in einer Palette " <span class="codeph"> adaptiv" </span>enthalten sein sollen. Wenn die Anzahl der angegebenen Farben kleiner als <span class="codeph"> numColors ist, werden weitere Farben basierend auf dem Bildinhalt berechnet </span>. </p> <p>Wird nur verwendet, wenn <span class="codeph"> fmt=gif </span> oder <span class="codeph"> fmt=gif-alpha </span>. Andernfalls ignoriert. Die mit <span class="codeph"> colorList angegebenen Farben <span class="varname"> müssen RGB-Werte im hex6-Format sein (siehe </span> color </span> <span class="codeph"> </span>). keine anderen Farbspezifikatoren zulässig sind. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-b3a979dc9ae3459baa093bf17310988f}

Erstellen Sie eine GIF-Miniaturansicht mit der Palette `web`&quot;ohne Dithering&quot;:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Konvertieren Sie das Bild in ein bitonales GIF mit Key-Farbtransparenz und erzwingen Sie Farben in Schwarzweiß:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
