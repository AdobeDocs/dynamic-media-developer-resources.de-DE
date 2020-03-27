---
description: Normalisierte Größe. Dient zum Festlegen von Bildgrößen oder Rechteckgrößen, die relativ zur Größe der Ebene 0 oder eines anderen Bilds normalisiert werden.
seo-description: Normalisierte Größe. Dient zum Festlegen von Bildgrößen oder Rechteckgrößen, die relativ zur Größe der Ebene 0 oder eines anderen Bilds normalisiert werden.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sizeN{#sizen}

Normalisierte Größe. Dient zum Festlegen von Bildgrößen oder Rechteckgrößen, die relativ zur Größe der Ebene 0 oder eines anderen Bilds normalisiert werden.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>normalisierte Breite und Höhe relativ zu einem anderen Bild (real, real, größer als 0) </p></td> 
 </tr> 
</table>

Sowohl *nx* als auch *nx* müssen größer als 0 sein. 0,0 kann angeben, dass eine bestimmte Standardgröße verwendet werden soll. 1,1 gibt eine Größe an, die dem Referenzbild entspricht.
