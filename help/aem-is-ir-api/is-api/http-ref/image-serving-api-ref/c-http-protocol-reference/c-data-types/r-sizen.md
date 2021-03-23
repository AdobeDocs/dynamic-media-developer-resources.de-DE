---
description: Normalisierte Größe. Dient zum Festlegen von Bildgrößen oder Rechteckgrößen, die relativ zur Größe der Ebene 0 oder eines anderen Bilds normalisiert werden.
seo-description: Normalisierte Größe. Dient zum Festlegen von Bildgrößen oder Rechteckgrößen, die relativ zur Größe der Ebene 0 oder eines anderen Bilds normalisiert werden.
seo-title: sizeN
solution: Experience Manager
title: sizeN
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# sizeN{#sizen}

Normalisierte Größe. Dient zum Festlegen von Bildgrößen oder Rechteckgrößen, die relativ zur Größe der Ebene 0 oder eines anderen Bilds normalisiert werden.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>normalisierte Breite und Höhe relativ zu einem anderen Bild (real, real, größer als 0) </p></td> 
 </tr> 
</table>

Sowohl *nx* als auch *ny* müssen größer als 0 sein. 0,0 kann angeben, dass eine bestimmte Standardgröße verwendet werden soll. 1,1 gibt eine Größe an, die dem Referenzbild entspricht.
