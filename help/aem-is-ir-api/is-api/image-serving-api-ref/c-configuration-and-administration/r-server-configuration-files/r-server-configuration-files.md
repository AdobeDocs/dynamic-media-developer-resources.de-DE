---
title: Server-Konfigurationsdateien
description: Alle Konfigurationsdateien befinden sich im Installationsordner/conf und können mit den meisten Texteditoren bearbeitet werden. Starten Sie den Server neu, damit die Änderungen wirksam werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
TQID: 'https://experienceleague.adobe.com/Gp1W--QzWptazkc1ygnmw59lO8zrNmgmabYMOz8jUG4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 0%

---

# Server-Konfigurationsdateien{#server-configuration-files}

Alle Konfigurationsdateien befinden sich im `install_folder/conf` und können mit den meisten Texteditoren bearbeitet werden. Starten Sie den Server neu, damit die Änderungen wirksam werden.

>[!NOTE]
>
>Die meisten Server-Konfigurationsdateien enthalten zusätzliche Eigenschaften und Werte, die in diesem Dokument nicht beschrieben werden. Solche Eigenschaften sind für die interne Verwendung durch den Server bestimmt und dürfen nur geändert werden, wenn der technische Support von Dynamic Media dies anweist.

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
