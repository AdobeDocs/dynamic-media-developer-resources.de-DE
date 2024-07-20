---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Stellt die maximale Anzahl von Frames dar, die bei inaktiver SpinView in jede Richtung vorgeladen werden sollen. Der Wert <span class="codeph"> -1</span> lädt alle Frames im Satz vorab. Die vorgeladenen Frames werden immer mit der ursprünglichen Auflösung angezeigt, die die SpinView ursprünglich geladen hatte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Steuert die Qualität der vorgeladenen Frames. Wenn der Wert auf <span class="codeph"> 1</span> Frames festgelegt ist, werden diese in hoher Qualität geladen und entsprechen der Größe der Komponente. Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, wird nur die Kachel für die Vorschau mit niedriger Auflösung geladen. </p> <p>Das Vorausfüllen in hoher Auflösung verbessert das Benutzererlebnis, insbesondere wenn die automatische Rotation aktiviert ist. Gleichzeitig führt dies zu einer langsameren Startzeit und einem höheren Netzwerkverbrauch. Seien Sie daher vorsichtig. Wenn eine hochauflösende Vorlast verwendet wird, befinden sich die vorgeladenen Frames immer in der ursprünglichen Auflösung, in der die Komponente ursprünglich geladen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
