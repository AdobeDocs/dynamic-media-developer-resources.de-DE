---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`Dauer`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|Turn|auto</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des Effekts an, der bei der Bildänderung angewendet wird. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> Folie</span> Aktiviert eine Transition, bei der der alte Rahmen aus der Ansicht wegrutscht und der neue Rahmen in die Ansicht verschoben wird. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> drehen</span> aktiviert einen Seitenumbrucheffekt, wenn ein Benutzer eine der vier breiteten Ecken ziehen und ein interaktives Seitenumblättern durchführen kann. </p> <p>Wann <span class="codeph"> drehen</span> verwendet wird, wird das Erscheinungsbild der Komponente mit dem <span class="codeph"> pageturnstyle</span> -Modifikator und die <span class="codeph"> .s7pagedivider</span> CSS-Klasse wird ignoriert. </p> <p>Hinweis:  <p><span class="codeph"> drehen</span> Animation wird nicht auf Motorola Xoom unterstützt. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> stellt den Umschalt-Frame-Übergang auf Desktop-Systemen und den Folienübergang auf Touch-Geräten ein. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer in Sekunden für einen <span class="codeph"> Folie</span> oder <span class="codeph"> drehen</span> Übergangseffekt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optional.

## Standard {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Beispiel {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
