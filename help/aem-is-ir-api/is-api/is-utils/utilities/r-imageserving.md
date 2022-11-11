---
description: Image Serving Control-Skript. Mit diesem Skript wird der Image Serving Server Supervisor gestartet, beendet oder neu gestartet, der alle anderen Image Serving-Komponenten startet, stoppt oder neu startet.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# ImageServing{#imageserving}

Image Serving Control-Skript. Mit diesem Skript wird der Image Serving Server Supervisor gestartet, beendet oder neu gestartet, der alle anderen Image Serving-Komponenten startet, stoppt oder neu startet.

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
   <td colname="col2"> <p> Starten Sie den Server Supervisor und alle anderen Image Serving-Komponenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> Beenden Sie alle Image Serving-Komponenten, einschließlich des Server Supervisors. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Neu starten </span> </p> </td> 
   <td colname="col2"> <p>Starten Sie alle Image Serving-Komponenten einschließlich des Server Supervisors neu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Neustart { ps | is | svg } </span> </p> </td> 
   <td colname="col2"> <p> Startet Tomcat/ neu.[!DNL Platform Server], dem Image-Server oder SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Gibt Informationen zur Betriebszeit und aktuellen Speicherbelegung für Image-Server, Tomcat/ zurück[!DNL Platform Server], und SVGserver oder Status nur für den angegebenen Server; Stattdessen wird eine Informationsmeldung zurückgegeben, wenn der Server-Supervisor nicht ausgeführt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>
