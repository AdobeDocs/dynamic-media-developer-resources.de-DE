---
description: Image Serving-Steuerelementskript. Dieses Skript wird zum Beginn, Beenden oder Neustart des Image Serving Server Supervisor verwendet, der wiederum alle anderen Image Serving-Komponenten Beginn, anhält oder neu startet.
seo-description: Image Serving-Steuerelementskript. Dieses Skript wird zum Beginn, Beenden oder Neustart des Image Serving Server Supervisor verwendet, der wiederum alle anderen Image Serving-Komponenten Beginn, anhält oder neu startet.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# ImageServing{#imageserving}

Image Serving-Steuerelementskript. Dieses Skript wird zum Beginn, Beenden oder Neustart des Image Serving Server Supervisor verwendet, der wiederum alle anderen Image Serving-Komponenten Beginn, anhält oder neu startet.

## Nutzung {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## Befehle {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Befehl </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> starten </span> </p> </td> 
   <td colname="col2"> <p> Beginn des Server Supervisor und aller anderen Image Serving-Komponenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Beenden Sie alle Image Serving-Komponenten, einschließlich Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Neu starten </span> </p> </td> 
   <td colname="col2"> <p>Starten Sie alle Image Serving-Komponenten einschließlich Server Supervisor neu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Neustart { | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Startet Tomcat/Platform Server, den Image-Server oder SVG neu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Gibt Informationen zur Betriebszeit und aktuellen Speicherbelegung für Image-Server, Tomcat/Platform-Server und SVGserver oder zum Status nur für den angegebenen Server zurück; Stattdessen wird eine Informationsmeldung zurückgegeben, wenn der Server Supervisor nicht ausgeführt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

