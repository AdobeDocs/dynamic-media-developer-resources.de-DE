---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`verblassen`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert die <span class="codeph"> iconEffect</span> , um am oberen Rand des Bildes anzuzeigen, wenn das Bild zurückgesetzt ist und eine verfügbare Aktion für die Interaktion mit dem Bild vorgeschlagen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die maximale Anzahl der <span class="codeph"> iconEffect</span> angezeigt und wieder angezeigt. Ein Wert von <span class="codeph"> -1</span> zeigt an, dass das Symbol immer unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, die der <span class="codeph"> iconEffect</span> bleibt vollständig sichtbar, bevor es automatisch ausgeblendet wird. Das heißt, die Zeit nach dem Abschluss der Einblendanimation, aber bevor die Ausblendung beginnt. Eine Einstellung von <span class="codeph"> 0</span> deaktiviert das automatische Ausblenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
