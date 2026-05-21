---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
TQID: 'https://experienceleague.adobe.com/DAvANJggSrj6-wEEL8qYAMlOeuavo7usySKl1g-npVg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> keine|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das im ersten Frame angezeigt werden soll, bevor die Wiedergabe des Videos beginnt, wird gegen <span class="codeph"> ServerUrl aufgelöst</span>. Wenn in der URL angegeben, kodieren Sie Folgendes HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> als <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> wie <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Wenn der Wert <span class="codeph"><span class="varname"> image_id</span></span> weggelassen wird, versucht die Komponente, stattdessen das standardmäßige Posterbild für dieses Asset zu verwenden. </p> <p>Wenn das Video als Pfad angegeben ist, wird die standardmäßige Katalog-ID der Poster-Bilder aus dem Videopfad als <span class="codeph"> Paar catalog_id/image_id</span> abgeleitet, wobei <span class="codeph"> catalog_id</span> dem ersten Token im Pfad entspricht. Und <span class="codeph"> image_id</span> ist der Name des Videos, aus dem die Erweiterung entfernt wurde. Wenn das Bild mit dieser ID nicht vorhanden ist, wird das Standbild nicht angezeigt. </p> <p>Um die Anzeige des standardmäßigen Posterbildes zu verhindern, geben Sie <span class="codeph"> Wert none</span> als Wert für das Posterbild an. Wenn nur die <span class="codeph"><span class="varname"> isCommands</span></span> angegeben sind, werden die Befehle auf das standardmäßige Posterbild angewendet, bevor das Bild angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Keine.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
