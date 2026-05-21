---
description: Normalisierte Größe. Wird verwendet, um Bildgrößen oder Rechteckgrößen anzugeben, die relativ zur Größe von Ebene 0 oder einem anderen Bild normalisiert sind.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
TQID: 'https://experienceleague.adobe.com/QXDv6qIlXZVW050N-6GmKH6PrIiwuN-zzZFuRApBYK4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 0%

---

# sizeN{#sizen}

Normalisierte Größe. Wird verwendet, um Bildgrößen oder Rechteckgrößen anzugeben, die relativ zur Größe von Ebene 0 oder einem anderen Bild normalisiert sind.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> NX</span> </span>, <span class="codeph"><span class="varname"> NY</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> NX</span> </span>, <span class="codeph"><span class="varname"> NY</span></span> </p></td> 
  <td class="stentry"> <p>Normalisierte Breite und Höhe relativ zu einem anderen Bild (real, real, größer als 0) </p></td> 
 </tr> 
</table>

Sowohl *nx* als auch *ny* müssen größer als 0 sein. 0,0 kann bedeuten, dass eine bestimmte Standardgröße verwendet werden soll. 1,1 legt eine Größe fest, die der Größe des Referenzbilds entspricht.
