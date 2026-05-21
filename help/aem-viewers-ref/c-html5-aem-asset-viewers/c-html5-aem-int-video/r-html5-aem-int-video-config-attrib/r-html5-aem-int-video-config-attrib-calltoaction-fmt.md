---
title: CallToAction.fmt
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
TQID: 'https://experienceleague.adobe.com/mLNh164dQipHeG5d-YZqeasnxuF0rb4FakXYhqqgk-0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 4%

---

# CallToAction.fmt{#calltoaction-fmt}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das die Komponente zum Laden von Bildern vom Bildserver verwendet. </p> <p>Wenn das angegebene Format mit "<span class="codeph"> -alpha</span>" endet, rendert die Komponente die Bilder als transparenten Inhalt. Für alle anderen Bildformate behandelt die Komponente die Bilder als undurchsichtig. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
