---
description: Legt den Typ der Zoom-Interaktion fest.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

Legt den Typ der Zoom-Interaktion fest.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> "Fortlaufend" </span> ermöglicht den klassischen Zoom, bei dem das Bild beim Klicken, Doppeltippen oder Verkleinern in der Hauptansicht nach und nach vergrößert wird. Sie müssen den Zoom-Status explizit verkleinern oder zurücksetzen, um zur Ansicht beim Öffnen zurückzukehren. </p> <p> <span class="codeph"> Inline  </span> ermöglicht sofortigen Zoom, wobei das gezoomte Bild sofort angezeigt wird, wenn Sie den Mauszeiger über die Hauptansicht auf dem Desktop bewegen oder ein Touchgerät berühren und halten. Das Bild wechselt automatisch in den ursprünglichen Zustand zurück, sobald Sie die Maus aus der Ansicht bewegen oder den Finger freigeben. Beachten Sie, dass verschachtelte Bildsets im Inline-Modus </span> im <span class="codeph">-Modus reduziert und als einzelne Miniaturansichten angezeigt werden. <span class="codeph"> automatisch  </span> aktiviert den Inline-Modus auf dem Desktop und den kontinuierlichen Modus auf Touch-Geräten. </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
