---
title: Server-Konfigurationsdateien
description: Alle Konfigurationsdateien befinden sich im Installationsordner/conf und können mit den meisten Texteditoren bearbeitet werden. Starten Sie den Server neu, damit die Änderungen wirksam werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Server-Konfigurationsdateien{#server-configuration-files}

Alle Konfigurationsdateien befinden sich im `install_folder/conf` und können mit den meisten Texteditoren bearbeitet werden. Starten Sie den Server neu, damit die Änderungen wirksam werden.

>[!NOTE]
>
>Die meisten Server-Konfigurationsdateien enthalten zusätzliche Eigenschaften und Werte, die in diesem Dokument nicht beschrieben werden. Solche Eigenschaften sind für die interne Verwendung durch den Server bestimmt und dürfen nur geändert werden, wenn dies vom technischen Support von Dynamic Media angewiesen wird.

In diesem Dokument werden Einstellungen für die folgenden Konfigurationsdateien erläutert:

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Konfigurationsdatei</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.</span> </p> </td> 
   <td> <p>Server-Supervisor-Konfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat-Konfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] Konfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Konfiguration des Katalog-Service. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf </span> </p> </td> 
   <td> <p>Konfiguration der Serverüberwachung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Image-Server-Konfiguration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Konfigurationsdateien werden später in diesem Dokument detaillierter erläutert.
