---
description: 'null'
seo-description: 'null'
seo-title: Richtung
solution: Experience Manager
title: Richtung
topic: Dynamic media
uuid: 185824c5-d6f2-4e1b-99ac-726a295ec5f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Richtung{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie die Ansichten in der Hauptansicht und in den Miniaturansichten angezeigt werden. Er gibt auch an, wie der Benutzer mit der Benutzeroberfläche des Viewers interagiert, um zwischen den Katalograhmen zu wechseln. </p> <p>Wenn <span class="codeph"> links verwendet </span> wird, wird eine rechte Ausrichtung für die Anfangsseite und eine linke Ausrichtung für die letzte Seite festgelegt. Es ordnet einzelne Seiten-Unterbilder für die Renderreihenfolge von links nach rechts. Außerdem wird die Hauptversion so eingestellt, dass eine Diashow-Animation von rechts nach links verwendet wird, um den Katalog zu erweitern (falls <span class="codeph"> "PageView.frametransition"auf "folien" </span> eingestellt ist). Schließlich werden Miniaturansichten für eine Füllreihenfolge von links nach rechts festgelegt. </p> <p>Bei Verwendung der <span class="codeph"> rechten Seite </span> wird eine linke Ausrichtung für die Anfangsseite und eine rechte Ausrichtung für die letzte Seite festgelegt. Es werden einzelne Seiten-Unterbilder für die Renderreihenfolge von rechts nach links zusammengeführt. Außerdem wird die Hauptversion so eingestellt, dass eine Diashow-Animation von links nach rechts verwendet wird, um den Katalog zu erweitern (falls <span class="codeph"> "PageView.frametransition"auf "folien"festgelegt </span> ist). Schließlich wird die Reihenfolge der Miniaturansichten umgekehrt, sodass die Ansicht für Miniaturansichten von rechts nach links und von oben nach unten gefüllt wird. </p> <p>Wenn <span class="codeph"> auto festgelegt </span> ist, wendet der Viewer den <span class="codeph"> richtigen </span> Modus an, wenn locale auf <span class="codeph"> ja eingestellt ist. </span>Andernfalls wird der <span class="codeph"> linke </span> Modus verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optional.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Beispiel {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
