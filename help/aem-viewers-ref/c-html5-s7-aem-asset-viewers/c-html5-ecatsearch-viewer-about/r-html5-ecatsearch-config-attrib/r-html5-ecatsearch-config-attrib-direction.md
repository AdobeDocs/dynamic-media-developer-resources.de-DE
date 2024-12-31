---
title: Richtung
description: Richtung
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# Richtung{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie Seiten in der Hauptansicht und in den Miniaturen angezeigt werden. Sie gibt auch die Art und Weise an, wie Benutzende mit der Viewer-Benutzeroberfläche interagieren, um zwischen Katalogfeldern zu wechseln. </p> <p>Wenn <span class="codeph"> linke </span> verwendet wird, wird für die erste Seite die Ausrichtung nach rechts und für die letzte Seite die Ausrichtung nach links festgelegt. Dabei werden einzelne Seitenunterbilder für die Renderreihenfolge von links nach rechts zugeordnet. Außerdem wird die Hauptansicht so festgelegt, dass durch eine von rechts nach links gerichtete Folienanimation der Katalog vorangebracht wird (falls <span class="codeph"> PageView.frameTransition-</span> auf Folie eingestellt ist). Schließlich werden Miniaturen für eine Links-nach-rechts-Füllreihenfolge festgelegt. </p> <p>Wenn <span class="codeph"> rechte </span> verwendet wird, legt er für die erste Seite eine linke Ausrichtung und für die letzte Seite eine rechte Ausrichtung fest. Dabei werden einzelne Seitenunterbilder für die Rechts-nach-links-Renderreihenfolge zusammengefügt. Außerdem wird die Hauptansicht so festgelegt, dass durch von links nach rechts gerichtete Folienanimation der Katalog vorangebracht wird (falls <span class="codeph"> PageView.frameTransition-</span> auf Folie eingestellt ist). Schließlich wird die Reihenfolge der Miniaturen umgekehrt, sodass die Miniaturansicht von rechts nach links, von oben nach unten gefüllt wird. </p> <p>Wenn <span class="codeph"> automatische </span> festgelegt ist, wendet der Viewer <span class="codeph"> Modus </span> rechts an, wenn das Gebietsschema auf <span class="codeph"> ja eingestellt ist. </span>Andernfalls wird <span class="codeph"> Modus </span> links verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optional.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Beispiel {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
