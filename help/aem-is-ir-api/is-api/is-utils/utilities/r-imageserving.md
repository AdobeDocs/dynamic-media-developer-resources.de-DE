---
description: Image-Serving-Steuerungs-Skript. Dieses Skript wird verwendet, um Image Serving Server Supervisor zu starten, zu stoppen oder neu zu starten, wodurch wiederum alle anderen Image Serving-Komponenten gestartet, beendet oder neu gestartet werden.
solution: Experience Manager
title: Bildbereitstellung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# Bildbereitstellung{#imageserving}

Image-Serving-Steuerungs-Skript. Dieses Skript wird verwendet, um Image Serving Server Supervisor zu starten, zu stoppen oder neu zu starten, wodurch wiederum alle anderen Image Serving-Komponenten gestartet, beendet oder neu gestartet werden.

## Nutzung {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`Befehl`*`

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Starten Sie den Server-Supervisor und alle anderen Image-Serving-Komponenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Beenden Sie alle Bildbereitstellungskomponenten, einschließlich des Server-Supervisors. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Neustart </span> </p> </td> 
   <td colname="col2"> <p>Starten Sie alle Image-Serving-Komponenten neu, einschließlich Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Neustart { ps | ist | svg } </span> </p> </td> 
   <td colname="col2"> <p> Startet Tomcat/[!DNL Platform Server], den Bildserver oder SVG neu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [ ps | ist | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Gibt Informationen zur Betriebszeit und zur aktuellen Speichernutzung für den Bildserver, Tomcat/[!DNL Platform Server] und SVG-Server oder den Status nur für den angegebenen Server zurück. Stattdessen wird eine Informationsmeldung zurückgegeben, wenn der Server Supervisor nicht ausgeführt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>
