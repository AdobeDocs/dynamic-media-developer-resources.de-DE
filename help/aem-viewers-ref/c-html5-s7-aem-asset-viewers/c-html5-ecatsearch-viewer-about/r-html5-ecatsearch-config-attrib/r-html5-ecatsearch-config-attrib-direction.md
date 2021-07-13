---
description: Richtung
solution: Experience Manager
title: Richtung
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 3%

---

# Richtung{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie Seiten in der Hauptansicht und in Miniaturansichten angezeigt werden. Außerdem wird angegeben, wie der Benutzer mit der Viewer-Benutzeroberfläche interagiert, um zwischen Katalograhmen zu wechseln. </p> <p>Wenn <span class="codeph"> left </span> verwendet wird, wird eine rechte Ausrichtung für die Anfangsseite und eine linke Ausrichtung für die letzte Seite festgelegt. Es werden einzelne Seitenunterbilder für die Rendering-Reihenfolge von links nach rechts zugeordnet. Außerdem wird die Hauptansicht so eingestellt, dass die von rechts nach links gehaltene Dia-Animation verwendet wird, um den Katalog voranzutreiben (falls <span class="codeph"> PageView.frametransition </span> auf Folie eingestellt ist). Schließlich werden Miniaturansichten für eine von links nach rechts angeordnete Füllung festgelegt. </p> <p>Wenn <span class="codeph"> rechts </span> verwendet wird, wird eine linke Ausrichtung für die Anfangsseite und eine rechte Ausrichtung für die letzte Seite festgelegt. Es werden einzelne Seitenunterbilder für die Rendering-Reihenfolge von rechts nach links zugeordnet. Es wird auch die Hauptansicht festgelegt, die die von links nach rechts gerichtete Diashow verwendet, um den Katalog voranzubringen (falls <span class="codeph"> PageView.frametransition </span> auf Folie eingestellt ist). Schließlich wird die Reihenfolge der Miniaturansichten umgekehrt, sodass die Miniaturansicht von rechts nach links und von oben nach unten gefüllt wird. </p> <p>Wenn <span class="codeph"> auto </span> festgelegt ist, wendet der Viewer den Modus <span class="codeph"> right </span> an, wenn das Gebietsschema auf <span class="codeph"> ja gesetzt ist. </span>Andernfalls wird <span class="codeph"> linker </span>-Modus verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optional.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Beispiel {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
