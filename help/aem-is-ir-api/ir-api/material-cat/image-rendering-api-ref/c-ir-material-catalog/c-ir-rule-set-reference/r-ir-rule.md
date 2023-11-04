---
description: Anforderungsregelelement. Eine oder mehrere sind optional im <ruleset> -Element.
solution: Experience Manager
title: Regel
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 4%

---

# Regel{#rule}

Anforderungsregelelement. Eine oder mehrere sind optional im `<ruleset>` -Element.

## Attribute {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Optional. Der Standardwert ist &quot;break&quot;.

` Name=" *`text`*"` Optional. Wird verwendet, um die `<rule>` -Element in Debug-Protokollen und Fehlermeldungen.

Darüber hinaus `<rule>` -Elemente können eines der folgenden Attribute in jeder beliebigen Kombination definieren. Wenn angegeben und die Regel erfolgreich abgeglichen wurde, überschreiben sie die entsprechenden Katalogattribute für diese Anfrage.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; attribute </p> </th> 
   <th colname="col2" class="entry"> <p>Entsprechendes Bildkatalog-Attribut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribute::DefaultPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Ablauf </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attribute::Expiration </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attribute::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attribute::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Weitere Informationen finden Sie in der Beschreibung des entsprechenden Bildkatalogattributs.

Das Attribut Gültigkeit überschreibt nur den Standardwert des Attributs. Es wird ignoriert, wenn ein bestimmtes Attribut `catalog::Expiration` -Wert auf die Anfrage angewendet.

## Daten {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>Optional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>Optional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Optional. </p> </td> 
 </tr> 
</table>

## Anmerkungen {#section-a27b91f9a03047c0bb7edc0967fb4216}

Wenn `<expression>` und `<substitution>` festgelegt sind und keine erfassten Unterzeichenfolgen verwendet werden, wird die erste übereinstimmende Unterzeichenfolge durch `<substitution>`.

Wenn `<expression>` nicht angegeben ist, entspricht jeder Pfad und `<substitution>` wird am Ende des Pfads angehängt.

Wenn `<substitution>` nicht angegeben ist, wird die übereinstimmende Teilzeichenfolge entfernt.

Die `<addressfilter>` wird nur angewendet, wenn eine Übereinstimmung auftritt, und bevor Abfrageregeln angewendet werden.
