---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.textpos
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# CallToAction.textpos{#calltoaction-textpos}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom|top|left|right|none|tooltip</span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wo die Beschriftung relativ zum Miniaturbild gezeichnet wird. Das heißt, die Beschriftung wird an der angegebenen Position relativ zur Miniaturansicht zentriert. </p> <p>Wenn <span class="codeph"> tooltip</span> angegeben ist, wird der Beschriftungstext als schwebende QuickInfo über dem Miniaturbild angezeigt. </p> <p>Auf <span class="codeph"> none</span> setzen, um die Beschriftung zu deaktivieren. </p> </td> 
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
