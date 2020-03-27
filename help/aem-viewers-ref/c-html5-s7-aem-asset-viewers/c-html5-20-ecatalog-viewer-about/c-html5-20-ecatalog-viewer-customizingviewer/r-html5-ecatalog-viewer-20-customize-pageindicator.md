---
description: Der Seitenindikator zeigt den aktuellen Seitenindex und die Gesamtzahl der Seiten an. Es wird in der Hauptsteuerungsleiste auf Desktop-Systemen und Tablets angezeigt, auf Mobiltelefonen wird es der sekundären Steuerungsleiste hinzugefügt. Der Seitenindikator kann mithilfe von CSS skaliert, gestapelt und positioniert werden.
seo-description: Der Seitenindikator zeigt den aktuellen Seitenindex und die Gesamtzahl der Seiten an. Es wird in der Hauptsteuerungsleiste auf Desktop-Systemen und Tablets angezeigt, auf Mobiltelefonen wird es der sekundären Steuerungsleiste hinzugefügt. Der Seitenindikator kann mithilfe von CSS skaliert, gestapelt und positioniert werden.
seo-title: Seitenindikator
solution: Experience Manager
title: Seitenindikator
topic: Dynamic media
uuid: 5e33c149-fdc7-419a-b5ff-b9be3f342d9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Seitenindikator{#page-indicator}

Der Seitenindikator zeigt den aktuellen Seitenindex und die Gesamtzahl der Seiten an. Es wird in der Hauptsteuerungsleiste auf Desktop-Systemen und Tablets angezeigt, auf Mobiltelefonen wird es der sekundären Steuerungsleiste hinzugefügt. Der Seitenindikator kann mithilfe von CSS skaliert, gestapelt und positioniert werden.

Das Erscheinungsbild des Seitenindikators wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand der Hauptsteuerungsleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerungsleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position von der rechten Kante der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand der Hauptsteuerungsleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerungsleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Seitenanzeige. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Seitenindikators. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Schriftfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Seitenindikators, der 56 x 28 Pixel groß ist, horizontal zentriert und 4 Pixel vom unteren Rand der Hauptsteuerungsleiste positioniert ist, und zum Verwenden einer Helvetica-Schrift mit 14 Pixel.

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```

