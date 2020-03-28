---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyoutsition
solution: Experience Manager
title: FlyoutZoomView.flyoutsition
topic: Dynamic media
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyoutsition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|folio|fade </span></span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des Effekts an, der angewendet wird, wenn die Flyout-Ansicht ein- oder ausgeblendet wird. Bei <span class="codeph"> keiner </span>Option wird das Flyout-Bild sofort angezeigt, sobald es aktiviert und fertig ist; die <span class="codeph"> Folie </span> bewirkt, dass die Animation von links nach rechts abgespielt wird; Beim <span class="codeph"> </span> Überblenden wird eine Alpha-Transition auf das Flyout-Bild angewendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Showtime </span></span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der Animation dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation der Anzeige auslöst, und dem Beginn der Animation selbst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span></span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der Animation zum Ausblenden dauert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span></span> </p> </td> 
   <td colname="col2"> <p> Die Verzögerung in Sekunden zwischen der Benutzeraktion, die die Animation zum Ausblenden auslöst, und dem Beginn der Animation zum Ausblenden selbst. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
