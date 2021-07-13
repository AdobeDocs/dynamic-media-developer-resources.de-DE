---
description: Die Seitenanzeige zeigt den aktuellen Seitenindex und die Seitenzahl insgesamt an. Sie wird in der Hauptsteuerleiste auf Desktop-Systemen und Tablets angezeigt, auf Mobiltelefonen wird sie zur sekundären Steuerleiste hinzugefügt. Die Seitenanzeige kann von CSS skaliert, gehärtet und positioniert werden.
solution: Experience Manager
title: Seitenanzeige
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 3%

---

# Seitenanzeige{#page-indicator}

Die Seitenanzeige zeigt den aktuellen Seitenindex und die Seitenzahl insgesamt an. Sie wird in der Hauptsteuerleiste auf Desktop-Systemen und Tablets angezeigt, auf Mobiltelefonen wird sie zur sekundären Steuerleiste hinzugefügt. Die Seitenanzeige kann von CSS skaliert, gehärtet und positioniert werden.

Der Indikator für die Darstellungsseite wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7pageindicator`

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
   <td colname="col2"> <p>Position vom oberen Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Abstandflächen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Abstandflächen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Abstandflächen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Abstandflächen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Seitenanzeige. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Seitenanzeige. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Schriftfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer Seitenanzeige mit einer Größe von 56 x 28 Pixel, einer horizontalen Zentrierung und Positionierung von 4 Pixel vom unteren Rand der Hauptsteuerleiste und der Verwendung einer Helvetica-Schriftart mit 14 Pixel.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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
