---
title: zoomMode
description: Legt den Typ der Zoom-Interaktion fest.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# zoomMode{#zoommode}

Legt den Typ der Zoom-Interaktion fest.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fortlaufend|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Fortlaufend </span> ermöglicht den klassischen Zoom, bei dem das Bild beim Klicken, Doppeltippen oder Verkleinern in der Hauptansicht nach und nach vergrößert wird. Um zur ursprünglichen Ansicht zurückzukehren, zoomen Sie aus oder setzen Sie den Zoomstatus zurück. Die Klasse </p> <p> <span class="codeph"> inline </span> ermöglicht sofortigen Zoom, wobei das gezoomte Bild sofort angezeigt wird, wenn Sie den Mauszeiger über die Hauptansicht auf dem Desktop bewegen oder ein Touchgerät berühren und halten. Das Bild wechselt automatisch in den ursprünglichen Zustand zurück, nachdem Sie die Maus aus der Ansicht bewegt oder den Finger losgelassen haben. Im Modus <span class="codeph"> inline </span> werden verschachtelte Bildsets reduziert und als einzelne Miniaturansichten angezeigt. Die Klasse <span class="codeph"> auto </span> aktiviert den Inline-Modus auf dem Desktop und den kontinuierlichen Modus auf Touch-Geräten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
