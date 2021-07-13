---
description: Alle Konfigurationsdateien befinden sich im Ordner install_folder/conf und können mit den meisten Texteditoren bearbeitet werden. Möglicherweise muss der Server neu gestartet werden, damit die Änderungen wirksam werden.
solution: Experience Manager
title: Serverkonfigurationsdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Serverkonfigurationsdateien{#server-configuration-files}

Alle Konfigurationsdateien befinden sich im Ordner install_folder/conf und können mit den meisten Texteditoren bearbeitet werden. Möglicherweise muss der Server neu gestartet werden, damit die Änderungen wirksam werden.

>[!NOTE]
>
>Die meisten Serverkonfigurationsdateien enthalten zusätzliche Eigenschaften und Werte, die in diesem Dokument nicht beschrieben werden. Diese Eigenschaften sind für die interne Verwendung des Servers bestimmt und dürfen nur geändert werden, wenn dies vom technischen Support von Dynamic Media ausdrücklich angewiesen ist.

In diesem Dokument werden die Einstellungen für die folgenden Konfigurationsdateien erläutert:

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Konfigurationsdatei</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>Server-Supervisor-Konfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat-Konfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>Plattformserverkonfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Konfiguration des Katalogdienstes . </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>Konfiguration der Serverüberwachung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Image-Server-Konfiguration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Konfigurationsdateien werden weiter unten in diesem Dokument erläutert.
