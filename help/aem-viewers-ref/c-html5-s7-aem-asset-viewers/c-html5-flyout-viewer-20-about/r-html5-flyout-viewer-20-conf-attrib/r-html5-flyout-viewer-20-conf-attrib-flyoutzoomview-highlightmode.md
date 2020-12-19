---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor  </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des zu verwendenden Navigationsrahmens an. Bei Einstellung auf <span class="codeph"> Cursor </span> verwendet die Komponente einen Referenz-Cursor fester Größe. Es ist möglich, verschiedene Cursorgrafiken für Desktop-Systeme und Touch-Geräte zu haben, diese werden mit <span class="codeph"> .s7cursor </span> CSS-Klasse und <span class="codeph"> input=mouse|touch </span> Attributauswahl gesteuert. Auf Desktop-Systemen wird ein Ankerpunkt in der Mitte des Cursorbereichs gesetzt, während sich der Anker auf den Touchgeräten in der unteren Mitte des Cursors befindet. Bei Einstellung auf <span class="codeph"> Hervorhebung </span> verwendet die Komponente einen Navigationsrahmen variabler Größe. Die Größe und Form des Rahmens hängen vom Zoomfaktor und der Größe der Flyout-Ansicht ab. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Zeit (in Sekunden) fest, die es dauert, bis die Markierung oder der Cursor eingeblendet wird, nachdem sie vom Benutzer aktiviert wurde. "Einblenden"wird nur auf Touch-Geräte angewendet. auf Desktop-Systemen wird sie von der Komponente ignoriert. </p> <p>Einblenden gilt für die folgenden UI-Elemente: Markierungsrahmen, fester Cursor, Überlagerung (in dem Fall <span class="codeph"> Überlagerung </span> auf <span class="codeph"> 1 </span> eingestellt ist). Die Flyout-Ansicht-Animation beginnt erst, nachdem die Hervorhebung/der Cursor in der Animation ausgeblendet wurde. Es gibt keine Animation zum Ausblenden. Wenn der Benutzer das Flyout deaktiviert, werden die entsprechenden Elemente der Benutzeroberfläche (Cursor, Hervorhebung und Überlagerung) sofort ausgeblendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Steuert die Positionierung des Navigationsrahmens. </p> <p>Wenn auf <span class="codeph"> auf ein Bild </span> gesetzt, kann der Navigationsrahmen nur innerhalb des eigentlichen Bildbereichs innerhalb der Haupt-Ansicht positioniert werden. </p> <p>Bei Festlegung auf <span class="codeph"> free </span> kann ein Benutzer den Navigationsrahmen an eine beliebige Stelle im Bereich der logischen Hauptversion verschieben, auch außerhalb des Bildinhalts. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
