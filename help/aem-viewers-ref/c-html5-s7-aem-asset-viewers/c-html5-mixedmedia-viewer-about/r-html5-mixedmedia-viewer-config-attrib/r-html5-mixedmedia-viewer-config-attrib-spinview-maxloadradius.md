---
title: SpinView.maxloadradius
description: Stellt die maximale Anzahl von Frames dar, die bei inaktiver SpinView in jede Richtung vorgeladen werden sollen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Stellt die maximale Anzahl von Frames dar, die bei inaktiver SpinView in jede Richtung vorgeladen werden sollen.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Der Wert <span class="codeph"> -1</span> lädt alle Frames im Satz vorab. Die vorgeladenen Frames werden immer mit der ursprünglichen Auflösung angezeigt, die die SpinView ursprünglich geladen hatte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Steuert die Qualität der vorgeladenen Frames. </p> <p>Wenn der Wert auf <span class="codeph"> 1</span> festgelegt ist, werden die Frames in hoher Qualität geladen und entsprechen der Größe der Komponente. </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, wird nur die Kachel für die Vorschau mit niedriger Auflösung geladen.</p> <p>Das Vorausfüllen in hoher Auflösung verbessert das Benutzererlebnis, insbesondere bei aktivierter automatischer Rotation. Gleichzeitig führt dies zu einer langsameren Startzeit und einem höheren Netzwerkverbrauch, daher sollte es mit Vorsicht verwendet werden. Bei Verwendung einer hochauflösenden Vorlast befinden sich die vorgeladenen Frames immer in der ursprünglichen Auflösung, in der die Komponente ursprünglich geladen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
