---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des zu verwendenden Navigationsrahmens an. Wenn der Wert auf <span class="codeph"> Cursor </span> festgelegt ist, verwendet die Komponente einen Referenz-Cursor fester Größe. Es ist möglich, verschiedene Cursorgrafiken für Desktop-Systeme und Touch-Geräte zu verwenden. Diese Fähigkeit wird mit der Attributauswahl <span class="codeph"> .s7cursor </span> CSS-Klasse und <span class="codeph"> input=mouse|touch </span> gesteuert. Auf Desktop-Systemen wird ein Ankerpunkt in der Mitte des Cursor-Bereichs festgelegt, während sich der Anker auf Touch-Geräten in der unteren Mitte des Cursors befindet. Wenn der Wert auf <span class="codeph"> highlight </span> gesetzt ist, verwendet die Komponente einen Navigationsrahmen mit variabler Größe. Größe und Form des Rahmens hängen vom Zoomfaktor und der Größe der Flyout-Ansicht ab. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Zeit (in Sekunden) fest, in der die Hervorhebung oder der Cursor nach der Aktivierung durch den Benutzer ausgeblendet werden muss. "Einblenden"wird nur auf Touch-Geräten angewendet. Auf Desktop-Systemen wird sie von der Komponente ignoriert. </p> <p>Einblenden gilt für die folgenden Elemente der Benutzeroberfläche: Markierungsrahmen, fester Cursor, Überlagerung (falls der Parameter <span class="codeph"> overlay </span> auf <span class="codeph"> 1 </span> gesetzt ist). Die Animation der Flyout-Ansicht beginnt erst, nachdem das Hervorheben/Verbergen der Animation abgeschlossen ist. Es gibt keine verblassende Animation. Wenn der Benutzer den Flyout deaktiviert, werden die entsprechenden Elemente der Benutzeroberfläche (Cursor, Hervorheben und Überlagerung) sofort ausgeblendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Steuert die Positionierung des Navigationsrahmens. </p> <p>Wenn auf <span class="codeph"> für Bild </span> gesetzt, kann der Navigationsrahmen nur innerhalb des tatsächlichen Bildbereichs in der Hauptansicht positioniert werden. </p> <p>Wenn der Wert auf <span class="codeph"> kostenlos </span> gesetzt ist, kann ein Benutzer den Navigationsrahmen an eine beliebige Stelle im logischen Hauptansichtsbereich verschieben, auch außerhalb des Bildinhalts. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
