---
description: 'Scene7 Image Serving umfasst die folgenden Komponenten '
solution: Experience Manager
title: Image Serving-Komponenten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---

# Image Serving-Komponenten{#image-serving-components}

Scene7 Image Serving umfasst die folgenden Komponenten:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponente </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Server Supervisor </p> </td> 
   <td colname="col2"> <p>Eigenständige ausführbare Datei, die für das Starten, Beenden und Sicherstellen der Gesundheit der anderen Komponenten verantwortlich ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Stellt die Umgebung für die meisten Java-basierten Komponenten bereit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Monitoring-/Warnungsdienst </p> </td> 
   <td colname="col2"> <p>J2EE-Anwendung. Ermöglicht Serverüberwachung und E-Mail-Warnungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Platform Server </p> </td> 
   <td colname="col2"> <p>J2EE-Anwendung. Verwaltet Client-Verbindungen, Protokollierung und Kommunikation mit anderen Komponenten. HTTP-Zugriff unter <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caching-Dienst </p> </td> 
   <td colname="col2"> <p>J2EE-Anwendung. Verwaltet die Daten-Caches des Platform-Servers. HTTP-Zugriff unter /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image-Server </p> </td> 
   <td colname="col2"> <p>Führt alle I/O-Vorgänge zur Bildverarbeitung und zur Bilddatei aus. Sowohl 32-Bit- als auch 64-Bit-ausführbare Prozessoren sind für Linux verfügbar (nur 32-Bit für Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Render Component </p> </td> 
   <td colname="col2"> <p>Eine oder mehrere Instanzen des Text-Rendering-Dienstes können aktiv sein, wenn <span class="codeph"> textPs=</span> -Vorgänge ausgeführt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG-Rendering-Komponente </p> </td> 
   <td colname="col2"> <p>Eigenständige Java-Anwendung (nicht von Tomcat gehostet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media Image Rendering (auch: Rendering-Server) </p> </td> 
   <td colname="col2"> <p>Erfordert eine separate Lizenz zum Aktivieren. HTTP-Zugriff unter <span class="filepath"> /ir/render</span>. Alle Funktionen zum Rendern von Bildern sind in den Platform-Server und den Image-Server integriert, ohne dass separate ausführbare Komponenten vorhanden sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere Konfigurationseinstellungen werden vom Standardkatalog ( [!DNL default.ini]) oder bestimmten Bildkatalogen bereitgestellt (weitere Informationen finden Sie unter [Bildkataloge](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)).
