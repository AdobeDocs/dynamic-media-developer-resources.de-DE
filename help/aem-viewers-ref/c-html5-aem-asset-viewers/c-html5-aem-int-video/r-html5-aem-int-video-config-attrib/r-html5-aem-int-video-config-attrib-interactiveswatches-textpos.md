---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: InteractiveSwatches.textpos
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 875d36cc-7372-454e-9a04-32492a2e558e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# InteractiveSwatches.textpos{#interactiveswatches-textpos}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom|top|left|right|none|tooltip</span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wo die Beschriftung relativ zum Musterbild gezeichnet wird. Das heißt, die Beschriftung wird an der angegebenen Position relativ zur Miniaturansicht zentriert. </p> <p>Wenn <span class="codeph"> tooltip</span> angegeben ist, wird der Beschriftungstext als schwebende QuickInfo über dem Miniaturbild angezeigt. </p> <p>Auf <span class="codeph"> none</span> setzen, um die Beschriftung zu deaktivieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`bottom`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
textpos=top
```
