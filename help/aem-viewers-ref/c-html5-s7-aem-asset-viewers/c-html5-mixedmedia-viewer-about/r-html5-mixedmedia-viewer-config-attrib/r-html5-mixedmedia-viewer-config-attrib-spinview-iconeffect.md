---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: 473207d2-7e26-4ea3-940e-5a21f29a2b91
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert das Symbol <span class="codeph"> </span>, das oben im Bild angezeigt wird, wenn das Bild zurückgesetzt ist und eine verfügbare Aktion vorgeschlagen wird, um mit dem Bild zu interagieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft der <span class="codeph">-Effekt</span> maximal angezeigt und wieder angezeigt wird. Der Wert <span class="codeph"> -1</span> zeigt an, dass das Symbol immer unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, in denen der <span class="codeph">-Ikoneffekt</span> vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit, nachdem die Einblendung-Animation abgeschlossen ist, aber bevor die Ausblendung beginnt. Die Einstellung <span class="codeph"> 0</span> deaktiviert das automatische Ausblenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
