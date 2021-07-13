---
description: Stellt die maximale Anzahl von Frames dar, die bei inaktiver SpinView in jede Richtung vorgeladen werden sollen.
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Stellt die maximale Anzahl von Frames dar, die bei inaktiver SpinView in jede Richtung vorgeladen werden sollen.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valueHeighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Wert</span></span> </p> </td> 
   <td colname="col2"> <p> Der Wert <span class="codeph"> -1</span> lädt alle Frames im Satz vorab. Die vorgeladenen Frames werden immer mit der ursprünglichen Auflösung angezeigt, die die SpinView ursprünglich geladen hatte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Steuert die Qualität der vorgeladenen Frames. </p> <p>Wenn auf <span class="codeph"> 1</span> gesetzt, werden die Frames in hoher Qualität geladen und entsprechen der Größe der Komponente. </p> <p>Wenn auf <span class="codeph"> 0</span> gesetzt, wird nur die Kachel mit niedriger Auflösung für die Vorschau geladen. </p> <p>Das Vorausfüllen in hoher Auflösung verbessert das Benutzererlebnis, insbesondere bei aktivierter automatischer Rotation. Gleichzeitig führt dies zu einer langsameren Startzeit und einem höheren Netzwerkverbrauch, daher sollte es mit Vorsicht verwendet werden. Bei Verwendung einer hochauflösenden Vorlast befinden sich die vorgeladenen Frames immer in der ursprünglichen Auflösung, in der die Komponente ursprünglich geladen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
