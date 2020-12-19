---
description: Die Cabinets-Materialien geben eine Möbeldatei (.vnc Dateierweiterung) an, eine spezielle Datendatei, die fotografische Darstellungen der Schränke sowie parametrische Layoutdefinitionen und weitere Informationen enthält, die für das Rendering der Schachtelfronten erforderlich sind.
seo-description: Die Cabinets-Materialien geben eine Möbeldatei (.vnc Dateierweiterung) an, eine spezielle Datendatei, die fotografische Darstellungen der Schränke sowie parametrische Layoutdefinitionen und weitere Informationen enthält, die für das Rendering der Schachtelfronten erforderlich sind.
seo-title: Möbel
solution: Experience Manager
title: Möbel
topic: Scene7 Image Serving - Image Rendering API
uuid: d515c613-07c5-49ef-ad6e-568a1f6c1335
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 5%

---


# Möbel{#cabinets}

Die Cabinets-Materialien geben eine Möbeldatei (.vnc Dateierweiterung) an, eine spezielle Datendatei, die fotografische Darstellungen der Schränke sowie parametrische Layoutdefinitionen und weitere Informationen enthält, die für das Rendering der Schachtelfronten erforderlich sind.

[!DNL vnc] Dateien können entweder eine wiederholbare Holzkornstruktur enthalten, oder die Textur kann extern über ein zweites Argument an  `src=`bereitgestellt werden. Bestimmte [!DNL vnc]-Dateien ermöglichen das Färben oder Texturieren ausgewählter Bereiche von Schaltflächenfronten (üblicherweise für Laminatschränke verwendet).

Möbel können nur auf Möbel des Schranks aufgetragen werden.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Möbeldatei; erforderlich. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Optionale Textur-Bilddatei (zweiter Wert für <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Optionale Texturauflösung. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Färbt Schrank und/oder Textur. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Scharfzeichnen. </p> </td> 
   <td colname="col3"> <p>0 (kein Scharfzeichnen) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Spezielle Render-Flags. </p> </td> 
   <td colname="col3"> <p>0 (keine Flags) </p> </td> 
  </tr> 
 </tbody> 
</table>

