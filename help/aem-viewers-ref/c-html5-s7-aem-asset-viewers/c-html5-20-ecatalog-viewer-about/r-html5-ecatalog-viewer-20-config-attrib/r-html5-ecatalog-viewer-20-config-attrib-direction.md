---
description: Richtung
solution: Experience Manager
title: Richtung
uuid: 185824c5-d6f2-4e1b-99ac-726a295ec5f4
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# Richtung{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie die Ansichten in der Hauptansicht und in den Miniaturansichten angezeigt werden. Er gibt auch an, wie der Benutzer mit der Benutzeroberfläche des Viewers interagiert, um zwischen den Katalograhmen zu wechseln. </p> <p>Wenn <span class="codeph"> links </span> verwendet wird, wird eine rechte Ausrichtung für die Anfangsseite und eine linke Ausrichtung für die letzte Seite festgelegt. Es ordnet einzelne Seiten-Unterbilder für die Renderreihenfolge von links nach rechts. Außerdem wird die Hauptversion so eingestellt, dass die Diashow-Animation von rechts nach links verwendet wird, um den Katalog zu erweitern (falls <span class="codeph"> PageView.frametransition </span> auf "folien"festgelegt ist). Schließlich werden Miniaturansichten für eine Füllreihenfolge von links nach rechts festgelegt. </p> <p>Bei Verwendung von <span class="codeph"> rechts </span> wird eine linke Ausrichtung für die Anfangsseite und eine rechte Ausrichtung für die letzte Seite festgelegt. Es werden einzelne Seiten-Unterbilder für die Renderreihenfolge von rechts nach links zusammengeführt. Außerdem wird die Hauptversion so eingestellt, dass die Diashow-Animation von links nach rechts verwendet wird, um den Katalog zu erweitern (falls <span class="codeph"> PageView.frametransition </span> auf "folien"eingestellt ist). Schließlich wird die Reihenfolge der Miniaturansichten umgekehrt, sodass die Ansicht für Miniaturansichten von rechts nach links und von oben nach unten gefüllt wird. </p> <p>Wenn <span class="codeph"> auto </span> festgelegt ist, wendet der Viewer den Modus <span class="codeph"> right </span> an, wenn das Gebietsschema auf <span class="codeph"> ja eingestellt ist. </span>Andernfalls wird <span class="codeph"> left </span>-Modus verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optional.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Beispiel {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
