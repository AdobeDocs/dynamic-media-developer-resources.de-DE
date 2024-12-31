---
title: Image-Serving-Komponenten
description: Dynamic Media Image Serving besteht aus den folgenden Komponenten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# Image-Serving-Komponenten{#image-serving-components}

Dynamic Media Image Serving umfasst die folgenden Komponenten:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponente </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Server-Verantwortlicher </p> </td> 
   <td colname="col2"> <p>Eine eigenständige ausführbare Datei, die für das Starten, Beenden und die Sicherstellung des Zustands der anderen Komponenten verantwortlich ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Es stellt die Umgebung für die meisten Java-basierten Komponenten bereit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Überwachungs-/Warndienst </p> </td> 
   <td colname="col2"> <p>J2EE-Anwendung. Ermöglicht Serverüberwachung und E-Mail-Warnungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE-Anwendung. Verwaltet Client-Verbindungen, Protokollierung und Kommunikation mit anderen Komponenten. HTTP-Zugriff unter <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caching-Service </p> </td> 
   <td colname="col2"> <p>J2EE-Anwendung. Verwaltet die Daten-Caches des [!DNL Platform Server]. HTTP-Zugriff unter /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image-Server </p> </td> 
   <td colname="col2"> <p>Alle I/O-Vorgänge für Bildverarbeitung und Bilddatei werden ausgeführt. Sowohl 32-Bit- als auch 64-Bit-ausführbare Dateien sind für Linux® verfügbar (32-Bit nur für Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rendering-Komponente für Datumstext </p> </td> 
   <td colname="col2"> <p>Eine oder mehrere Instanzen des Text-Rendering-Services können aktiv sein, wenn <span class="codeph"> Vorgänge des Typs textPs=</span> ausgeführt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG-Render-Komponente </p> </td> 
   <td colname="col2"> <p>Eigenständige Java™-Anwendung (nicht von Tomcat gehostet) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media Image Rendering (auch: Render-Server) </p> </td> 
   <td colname="col2"> <p>Zur Aktivierung ist eine separate Lizenz erforderlich. HTTP-Zugriff unter <span class="filepath"> /ir/render</span>. Alle Image-Rendering-Funktionen sind in die [!DNL Platform Server] und den Image-Server integriert, ohne separate ausführbare Komponenten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere Konfigurationseinstellungen sind über den Standardkatalog ([!DNL default.ini]) oder bestimmte Bildkataloge verfügbar (weitere Informationen finden [ unter ](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)).
