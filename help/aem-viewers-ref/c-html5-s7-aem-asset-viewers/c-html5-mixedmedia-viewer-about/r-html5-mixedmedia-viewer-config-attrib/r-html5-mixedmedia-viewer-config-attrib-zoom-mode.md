---
description: Legt den Typ der Zoominteraktion fest.
seo-description: Legt den Typ der Zoominteraktion fest.
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
topic: Dynamic media
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# zoomMode{#zoommode}

Legt den Typ der Zoominteraktion fest.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> uous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> "Fortlaufend" </span> ermöglicht klassischen Zoom, bei dem das Bild beim Klicken, Tippen auf die Dublette oder Herausziehen in der Ansicht allmählich vergrößert wird. Sie müssen den Zoomstatus explizit verkleinern oder zurücksetzen, um zur ursprünglichen Ansicht zurückzukehren. </p> <p> <span class="codeph"> Inline-Modus </span> ermöglicht sofortiges Zoomen, wobei das gezoomte Bild sofort angezeigt wird, wenn Sie den Mauszeiger über die Haupt-Ansicht auf dem Desktop bewegen oder ein Touch-Gerät berühren und halten; wird automatisch der Anfangsstatus zurückgesetzt, sobald Sie die Maus von der Ansicht bewegen oder den Finger loslassen. Beachten Sie, dass verschachtelte Bildsätze im <span class="codeph"> Inline- </span> Modus reduziert und als einzelne Miniaturansichten angezeigt werden. <span class="codeph"> auto </span> aktiviert den Inline-Modus auf dem Desktop und den kontinuierlichen Modus auf Touch-Geräten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
