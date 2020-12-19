---
description: Die Fensterverkleidungsmaterialien umfassen sowohl weiche Fensterverkleidungen (Tränen, Täler, Café-Vorhänge) als auch harte Fensterverkleidungen (Schattierungen und Jalousien).
seo-description: Die Fensterverkleidungsmaterialien umfassen sowohl weiche Fensterverkleidungen (Tränen, Täler, Café-Vorhänge) als auch harte Fensterverkleidungen (Schattierungen und Jalousien).
seo-title: Fensterbeläge
solution: Experience Manager
title: Fensterbeläge
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---


# Fensterbeläge{#window-coverings}

Die Fensterverkleidungsmaterialien umfassen sowohl weiche Fensterverkleidungen (Tränen, Täler, Café-Vorhänge) als auch harte Fensterverkleidungen (Schattierungen und Jalousien).

Fensterabdeckende Materialien geben eine *Fensterbedeckungsstil-Datei* ( [!DNL .vnw] Dateierweiterung) an, eine spezielle Datendatei ähnlich einer Vignette, die Maske-, Beleuchtungs-, Layout- und Texturdaten enthält, die die Fensterbedeckung definieren.

[!DNL vnw] Dateien enthalten nicht die Farbe und Textur (Stoff) für die Fensterbedeckung. Diese Informationen werden separat angegeben, ähnlich wie bei wiederholbaren Texturen.

Fensterbedeckende Materialien können nur auf Fensterbedeckungsrahmen-Objekte angewendet werden, bei denen es sich um überlappende Objekte handelt.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
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
   <td colname="col2"> <p>Stildatei für die Fensterabdeckung; erforderlich. </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturbilddatei (zweiter Wert für <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturauflösung. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Wiederholungsmodus. </p> </td> 
   <td colname="col3"> <p>0 (gerade Wiederholung) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Feste Farbe (oder färbt Textur). </p> </td> 
   <td colname="col3"> <p>128 (neutrales Grau) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Scharfzeichnen. </p> </td> 
   <td colname="col3"> <p>0 (kein Scharfzeichnen) </p> </td> 
  </tr> 
 </tbody> 
</table>

