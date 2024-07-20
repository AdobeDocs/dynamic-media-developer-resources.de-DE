---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert die Anzeige des <span class="codeph"> -Bildeffekts</span> über dem Bild, wenn das Bild zurückgesetzt wird. Es ist empfehlenswert, eine verfügbare Aktion auszuführen, um mit dem Bild zu interagieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft das <span class="codeph">-Symbol</span> maximal angezeigt und wieder angezeigt wird. Der Wert <span class="codeph"> -1</span> zeigt an, dass das Symbol immer unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, in denen der <span class="codeph">-Effekt</span> vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach dem Abschluss der Einblendanimation, aber bevor die Ausblendung beginnt. Eine Einstellung von <span class="codeph"> 0</span> deaktiviert das automatische Ausblendeverhalten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
