---
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute an, um die Komprimierungsstufe zu steuern. Dies ändert wiederum die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 15%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute an, um die Komprimierungsstufe zu steuern. Dies ändert wiederum die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Qualität  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Kodierungsqualität (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Chroma  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Chromatizitäts-Downsampling (0=normal, 1=disable); optional ist, ist der Standardwert 0. </p> </td> 
 </tr> 
</table>

Wird nur verwendet, wenn `fmt=jpg`. Andernfalls ignoriert

Höhere Qualitätswerte erhöhen Dateigröße und Qualität, geringere Werte verringern die Dateigröße und die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das Flag `chroma`, um das RGB-Chromatizitäts-Downsampling zu deaktivieren, das von typischen JPEG-Kodierern verwendet wird. Dies kann die wahrgenommene Schärfe der Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung der Farbe und nicht durch die Helligkeit definiert wird. Das Festlegen dieses Flag kann zu einer leichten Vergrößerung der Datei führen. Experimentieren Sie mit dieser Einstellung, wenn Text etwas verschwommen scheint.

`chroma` wird ignoriert, wenn der Ausgabepipeltyp CMYK oder grau ist.

## Beispiel {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
