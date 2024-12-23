---
title: Schränke
description: Schrankmaterialien spezifizieren eine Schrankstil-Datei (.vnc-Dateierweiterung), eine spezielle Datendatei, die fotografische Darstellungen von Schränken zusammen mit parametrischen Layout-Definitionen und andere Informationen enthält, die für die Darstellung von Schrankfronten erforderlich sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Schränke{#cabinets}

Schrankmaterialien spezifizieren eine Schrankstil-Datei (.vnc-Dateierweiterung), eine spezielle Datendatei, die fotografische Darstellungen von Schränken zusammen mit parametrischen Layout-Definitionen und andere Informationen enthält, die für die Darstellung von Schrankfronten erforderlich sind.

[!DNL vnc] Dateien können entweder eine wiederholbare Holzmaserung enthalten, oder die Textur kann extern über ein zweites Argument zur `src=` bereitgestellt werden. Bestimmte [!DNL vnc] ermöglichen das Einfärben oder Texturieren ausgewählter Bereiche von Schrankfronten (typischerweise für Laminat-Schrankstile verwendet).

Schrankmaterialien können nur auf Schrankobjekte angewendet werden.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Kabinettstil-Datei; erforderlich. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Optionale Texturbilddatei (zweiter Wert für <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Optionale Texturauflösung. </p> </td> 
   <td colname="col3"> <p> <span class="codeph">::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>Färbt Schrank und/oder Textur. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Scharfzeichnen. </p> </td> 
   <td colname="col3"> <p>0 (keine Scharfzeichnung) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> Flags= </span> </a> </p> </td> 
   <td colname="col2"> <p>Spezielle Render-Flags. </p> </td> 
   <td colname="col3"> <p>0 (keine Flags) </p> </td> 
  </tr> 
 </tbody> 
</table>
