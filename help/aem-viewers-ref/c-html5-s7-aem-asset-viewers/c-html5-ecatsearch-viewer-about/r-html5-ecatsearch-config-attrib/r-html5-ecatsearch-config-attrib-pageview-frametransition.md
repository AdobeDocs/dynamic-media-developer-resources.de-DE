---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`Dauer`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schieben|Umschalten|Auto</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der bei einer Bildänderung angewendet wird. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> Die </span> Deaktivierung einer Transition, bei der der alte Rahmen aus der Ansicht verschoben und der neue Rahmen in die Ansicht verschoben wird. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Ein </span> Turnkey ermöglicht einen Seitenumblätterungseffekt, wenn ein Benutzer eine der vier Druckbogenecken ziehen und einen interaktiven Seitenumbruch durchführen kann. </p> <p>Wenn <span class="codeph"> Turn</span> verwendet wird, wird das Erscheinungsbild der Komponente mit dem Modifikator <span class="codeph"> pageturnstyle</span> gesteuert und die CSS-Klasse <span class="codeph"> .s7pagedivider</span> wird ignoriert. </p> <p>Hinweis:  <p><span class="codeph"> Die </span> Turnanimation wird auf Motorola Xoom nicht unterstützt. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> Legt die Transition des Drehrahmens auf Desktop-Systemen und die Transition der Folie auf Touch-Geräten </span> automatisch fest. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer in Sekunden eines <span class="codeph">-Dias</span> oder <span class="codeph"> Umblätterungseffekts</span> der Transition an. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optional.

## Standard {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Beispiel {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
