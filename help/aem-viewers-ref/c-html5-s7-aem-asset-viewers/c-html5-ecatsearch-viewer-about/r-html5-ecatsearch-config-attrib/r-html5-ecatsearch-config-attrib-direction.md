---
title: Richtung
description: Richtung
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
TQID: 'https://experienceleague.adobe.com/tNKu0P8Sgoxas-opiWd1GWkuWYWDfXE0-j1A-p-j-jM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 2%

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

