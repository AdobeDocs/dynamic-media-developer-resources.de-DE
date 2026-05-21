---
title: zoomMode
description: Legt den Typ der Zoom-Interaktion fest.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 2%

---

# zoomMode{#zoommode}

Legt den Typ der Zoom-Interaktion fest.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Continuous|Inline|Auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> kontinuierliche </span> ermöglicht ein klassisches Zoomen, bei dem das Bild schrittweise vergrößert wird, während Sie in der Hauptansicht klicken, doppeltippen oder die Maus ausquetschen. Um zur Anfangsansicht zurückzukehren, verkleinern oder setzen Sie den Zoom-Status zurück. Die Klasse </p> <p> <span class="codeph"> Inline-</span> ermöglicht ein sofortiges Zoomen, bei dem das gezoomte Bild sofort angezeigt wird, wenn Sie den Mauszeiger über die Hauptansicht auf dem Desktop bewegen oder ein Touch-Gerät berühren und halten. Das Bild wird automatisch wieder in den Ausgangszustand versetzt, nachdem Sie die Maus aus der Ansicht bewegt oder den Finger losgelassen haben. Im <span class="codeph">-Inline-</span> werden verschachtelte Bildsets reduziert und als einzelne Miniaturen angezeigt. Die Klasse <span class="codeph"> aktiviert </span> Inline-Modus auf Desktop-Geräten und den kontinuierlichen Modus auf Touch-Geräten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
