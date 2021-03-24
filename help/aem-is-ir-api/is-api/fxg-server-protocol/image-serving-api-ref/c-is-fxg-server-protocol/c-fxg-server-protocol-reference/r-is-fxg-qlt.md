---
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an. Dies wiederum ändert die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 15%

---


# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an. Dies wiederum ändert die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Qualität  </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualität der JPEG-Kodierung (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Chroma  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Farb-Downsampling (0 = normal, 1 = deaktiviert); optional ist, ist der Standardwert 0. </p> </td> 
 </tr> 
</table>

Wird nur verwendet, wenn `fmt=jpg`. Andernfalls ignoriert

Höhere Qualitätswerte erhöhen Dateigröße und Qualität, geringere Werte verringern die Dateigröße und die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das `chroma`-Flag, um die RGB-Farbwertanpassung zu deaktivieren, die von typischen JPEG-Kodierern verwendet wird. Dies kann die wahrgenommene Schärfe der Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons und nicht der Helligkeit definiert wird. Das Festlegen dieses Flag kann zu einer leichten Vergrößerung der Datei führen. Experimentieren Sie mit dieser Einstellung, wenn der Text etwas verschwommen aussieht.

`chroma` wird ignoriert, wenn der Ausgabepixeltyp CMYK oder Grau ist.

## Beispiel {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
