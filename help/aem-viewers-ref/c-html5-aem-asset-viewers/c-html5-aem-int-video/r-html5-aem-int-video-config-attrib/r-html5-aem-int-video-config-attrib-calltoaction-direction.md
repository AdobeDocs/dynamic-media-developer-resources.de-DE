---
title: CallToAction.direction
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
TQID: 'https://experienceleague.adobe.com/YehjMoK88ylklqHA9ZpjPgW8xoMwhLQqR-2e73ayWRM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie Miniaturen in der Ansicht gefüllt werden. </p> <p>Auf <span class="codeph"> linke </span> festlegen, um die Füllreihenfolge von links nach rechts festzulegen. </p> <p>Wenn auf <span class="codeph"> rechte </span> festgelegt, wird die Reihenfolge umgekehrt, sodass die Ansicht von rechts nach links und von oben nach unten gefüllt wird. </p> <p>Wenn auf <span class="codeph"> automatische </span> festgelegt, wird die Komponente im Rechtsmodus angewendet, wenn das Gebietsschema auf <span class="codeph"> „ja“-</span> festgelegt ist. Andernfalls wird <span class="codeph"> linke </span> verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
