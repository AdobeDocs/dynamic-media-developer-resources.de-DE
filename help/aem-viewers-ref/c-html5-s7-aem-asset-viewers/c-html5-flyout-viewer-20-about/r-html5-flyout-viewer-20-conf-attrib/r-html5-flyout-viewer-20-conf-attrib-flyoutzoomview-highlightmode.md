---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
TQID: 'https://experienceleague.adobe.com/x43ipzx6iKOODZ10S8o8yJA9pg0Gl8mldfS5fEiVQJ4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">|Cursor-</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des zu verwendenden Navigationsrahmens an. Bei Festlegung auf <span class="codeph"> Cursor-</span> verwendet die Komponente einen Referenzcursor fester Größe. Für Desktop-Systeme und Touch-Geräte können unterschiedliche Cursor-Grafiken verwendet werden. Diese Funktion wird mit <span class="codeph"> CSS-Klasse .s7cursor </span> der <span class="codeph"> input=mouse|touch-</span> gesteuert. Auf Desktop-Systemen wird ein Ankerpunkt in der Mitte des Cursor-Bereichs festgelegt, während auf Touch-Geräten der Ankerpunkt in der unteren Mitte des Cursors liegt. Bei Festlegung auf <span class="codeph"> </span> Hervorhebungsebene verwendet die Komponente einen Navigationsrahmen variabler Größe. Die Größe und Form des Rahmens hängt vom Zoomfaktor und der Größe der Flyout-Ansicht ab. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Zeit (in Sekunden) fest, die die Hervorhebung oder der Cursor nach der Benutzeraktivierung einblenden muss. Das Einblenden wird nur auf Touch-Geräten angewendet, auf Desktop-Systemen wird es von der Komponente ignoriert. </p> <p>Einblenden gilt für die folgenden Benutzeroberflächenelemente: Hervorhebungsrahmen, fester Cursor, Überlagerung (falls <span class="codeph"> Überlagerung </span> Parameter auf <span class="codeph"> 1 </span> gesetzt ist). Die Flyout-Ansichtsanimation beginnt erst nach Abschluss der Hervorhebung/Cursorüberblendung in der Animation. Es gibt keine Ausblendanimation. Wenn Benutzende das Flyout deaktivieren, werden die entsprechenden Elemente der Benutzeroberfläche (Cursor, Hervorhebung und Überlagerung) sofort ausgeblendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onImage|Kostenlose </span> </p> </td> 
   <td colname="col2"> <p> Steuert die Positionierung des Navigationsrahmens. </p> <p>Wenn auf <span class="codeph"> onImage-</span> festgelegt, kann der Navigationsrahmen nur innerhalb des eigentlichen Bildbereichs innerhalb der Hauptansicht positioniert werden. </p> <p>Wenn auf <span class="codeph"> festgelegt, kann </span> Benutzer den Navigationsrahmen an eine beliebige Stelle im logischen Hauptansichtsbereich verschieben, auch außerhalb des Bildinhalts. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
