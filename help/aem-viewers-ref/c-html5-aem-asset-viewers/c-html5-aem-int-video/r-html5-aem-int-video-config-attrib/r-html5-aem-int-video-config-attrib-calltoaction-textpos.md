---
title: CallToAction.textpos
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# CallToAction.textpos{#calltoaction-textpos}

Konfigurationsattribut für interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom|top|left|right|none|tooltip</span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wo der Titel relativ zum Miniaturbild gezeichnet wird. Das heißt, die Bezeichnung wird an der angegebenen Stelle relativ zur Miniaturansicht zentriert. </p> <p>Wenn <span class="codeph"> tooltip</span> angegeben wird, wird der Beschriftungstext als schwebende QuickInfo über das Miniaturbild angezeigt. </p> <p>Auf <span class="codeph"> none</span> setzen, um die Beschriftung zu deaktivieren. </p> </td> 
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
