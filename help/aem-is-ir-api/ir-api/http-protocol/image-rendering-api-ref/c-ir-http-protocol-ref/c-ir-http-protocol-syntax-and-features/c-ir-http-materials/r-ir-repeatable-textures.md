---
title: Wiederholbare Texturen
description: Zu den wiederholbaren Texturen gehören Innen- und Außenmaterialien wie Stoffe (sowohl Kleidung als auch Polsterwaren), Wandverkleidungen, Tapeten, Gegenmaterial, Korntexturen aus Holz, Dächer- und Seitenmaterial sowie alle anderen allgemeinen Texturen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---

# Wiederholbare Texturen{#repeatable-textures}

Zu den wiederholbaren Texturen gehören Innen- und Außenmaterialien wie Stoffe (sowohl Kleidung als auch Polsterwaren), Wandverkleidungen, Tapeten, Gegenmaterial, Korntexturen aus Holz, Dächer- und Seitenmaterial sowie alle anderen allgemeinen Texturen.

Wiederholbare Texturen können auf flache, fließende, skizzierende, ebene, wand- und schachtelförmige Objekte angewendet werden. Bei Anwendung auf ein nicht texturierbares Objekt wird das Objekt mit `color=` (oder `bgc=`, wenn `color=` nicht angegeben ist) gestrichen.

Ein Material gilt als Textur, wenn es ein `src=` -Attribut enthält, das ein Bild spezifiziert, und wenn es in einem anderen MSS als Dekorrahmen oder Wandrahmen auftritt.

Beim Rendern wird die Textur an das Objekt ausgerichtet, indem der Punkt `anchor=` des Texturmaterials mit dem Texturursprungpunkt des Objekts (wie in der Vignette verfasst) abgeglichen wird.

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col2"> <p>Wiederholbares Texturbild; erforderlich </p> </td> 
   <td colname="col3"> <p>Keine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturauflösung </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturausrichtungspunkt </p> </td> 
   <td colname="col3"> <p>Oben links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>Wiederholungsmodus </p> </td> 
   <td colname="col3"> <p>0 (gerade Wiederholung). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> spitze= </span> </a> </p> </td> 
   <td colname="col2"> <p>Scharfzeichnen </p> </td> 
   <td colname="col3"> <p>0 (keine Scharfzeichnung). </p> </td> 
  </tr> 
 </tbody> 
</table>

Zusätzlich zu diesen grundlegenden Attributen unterstützen wiederholbare Texturen die folgenden Zweckattribute für erweiterte Anwendungen:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span> </a> </p> </td> 
   <td colname="col2"> <p>Grobfarbe und Dicke; nützlich für keramische/steinförmige Materialien </p> </td> 
   <td colname="col3"> <p>Groß bereits im Bild vorhanden </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Ausrichtungsmodus (zwischen Objekten); für Polsterung von Anwendungen verwendet </p> </td> 
   <td colname="col3"> <p>zentrierte </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturdrehwinkel; nicht von Wandobjekten unterstützt </p> </td> 
   <td colname="col3"> <p>0 (keine Drehung) </p> </td> 
  </tr> 
 </tbody> 
</table>
