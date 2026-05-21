---
title: qlt
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

` qlt= *`Qualität`*[, *`Chroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Qualität </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualität der JPEG-Kodierung (1…100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Chroma </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Chromatizitäts-Downsampling (0=normal, 1=disable); optional, der Standardwert ist 0. </p> </td> 
 </tr> 
</table>

Wird nur verwendet, wenn `fmt=jpg`. Andernfalls ignoriert

Höhere Qualitätswerte erhöhen Dateigröße und Qualität, geringere Werte verringern die Dateigröße und die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das Flag `chroma` , um die RGB-Chromatizitäts-Downsampling zu deaktivieren, die bei typischen JPEG-Codierern verwendet wird. Dies kann die wahrgenommene Schärfe von Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons anstatt der Helligkeit definiert ist. Das Setzen dieses Flags kann zu einer leichten Erhöhung der Dateigröße führen. Experimentieren Sie mit dieser Einstellung, wenn der Text leicht unscharf erscheint.

Die `chroma` wird ignoriert, wenn der Ausgabe-Pixeltyp CMYK oder Grau ist.

## Beispiel {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
