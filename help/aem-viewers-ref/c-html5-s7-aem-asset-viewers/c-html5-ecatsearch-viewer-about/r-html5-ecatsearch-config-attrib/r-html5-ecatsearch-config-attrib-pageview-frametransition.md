---
description: PageView.frameTransition
solution: Experience Manager
title: PageView.frameTransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
TQID: 'https://experienceleague.adobe.com/X3qkuLchMxlcb-CpwM4-KLGNphsJe-DJMD3fsYz7KyY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 3%

---

# PageView.frameTransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duration`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Folie|Drehen|Auto</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des Effekts an, der bei der Rahmenänderung angewendet wird. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> Folie</span> Aktiviert eine Transition, bei der der alte Rahmen aus der Ansicht verschoben wird und der neue Rahmen in die Ansicht verschoben wird. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> aktiviert </span> einen Effekt für die Seitenumkehrung, wenn ein Benutzer eine der vier ausgeblendeten Ecken ziehen und eine interaktive Seitenumkehrung durchführen kann. </p> <p>Wenn <span class="codeph"> Zug </span> wird, wird das Erscheinungsbild der Komponente mit dem <span class="codeph"> pageturnstyle</span>-Modifikator gesteuert und die <span class="codeph"> CSS-Klasse .s7pagedivider</span> wird ignoriert. </p> <p>Hinweis:  <p><span class="codeph"> wird </span> Animation auf Motorola Xoom nicht unterstützt. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> Auto</span> Legt die Drehrahmenübergänge auf Desktop-Systemen und die Folienübergänge auf Touch-Geräten fest. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer in Sekunden eines <span class="codeph"> Folie</span> oder <span class="codeph"> Drehungs</span>Übergangseffekts an. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optional.

## Standard {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Beispiel {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
