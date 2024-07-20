---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duration`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Folie|Umschalten|auto</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des Effekts an, der bei der Bildänderung angewendet wird. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> aktiviert eine Transition, bei der der alte Frame aus der Ansicht verschwindet und der neue Frame in die Ansicht verschoben wird. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Turn</span> aktiviert einen Seitenumbrucheffekt, wenn ein Benutzer eine der vier breiteten Ecken ziehen und ein interaktives Seitenumblättern durchführen kann. </p> <p>Wenn <span class="codeph"> Turn</span> verwendet wird, wird das Erscheinungsbild der Komponente mit dem Modifikator <span class="codeph"> pageturnstyle</span> gesteuert und die CSS-Klasse <span class="codeph"> .s7pagedivider</span> wird ignoriert. </p> <p>Hinweis:  <p>Die Animation <span class="codeph"> Turn</span> wird auf Motorola Xoom nicht unterstützt. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> legt den Umschalt-Frame-Übergang auf Desktop-Systemen und den Folienübergang auf Touch-Geräten fest. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer eines Übergangseffekts vom Typ <span class="codeph"> Folie</span> oder <span class="codeph"> Umdrehen</span> in Sekunden an. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optional.

## Standard {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Beispiel {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
