---
title: SpinView.maxLoadRadius
description: SpinView.maxLoadRadius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
TQID: 'https://experienceleague.adobe.com/h7jV66-f8J9UoMxsROgQrDLSN-ONyXSZ71gj75-Z7v8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# SpinView.maxLoadRadius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Wert</span></span> </p> </td> 
   <td colname="col2"> <p> Stellt die maximale Anzahl von Frames dar, die in jeder Richtung vorgeladen werden sollen, wenn die SpinView inaktiv ist. Bei einem Wert von <span class="codeph"> -1</span> werden alle Frames im Satz vorab geladen. Die vorgeladenen Frames werden immer mit der ursprünglichen Auflösung angezeigt, in der der SpinView ursprünglich geladen wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Steuert die Qualität vorgeladener Frames. Bei Einstellung auf <span class="codeph"> 1 werden </span> Frames in hoher Qualität geladen, die der Größe der Komponente entspricht. Bei <span class="codeph"> 0 wird </span> Vorschaukachel mit niedriger Auflösung geladen. </p> <p>Das Vorabladen in hoher Auflösung verbessert das Erlebnis für Endbenutzer, insbesondere wenn die automatische Drehung aktiviert ist. Gleichzeitig führt dies zu einer langsameren Startzeit und einem höheren Netzwerkverbrauch, daher sollten Sie mit Vorsicht vorgehen. Bei Verwendung einer hochauflösenden Vorspannung befinden sich die vorgeladenen Frames immer in der ursprünglichen Auflösung, in der die Komponente ursprünglich geladen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
