---
description: Legt Metadatenwerte für ein bestimmtes mit setAssetMetadata verwendetes Asset fest. Beschreibt die Änderungen, die Sie an Metadaten vornehmen möchten.
solution: Experience Manager
title: MetadataUpdate
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# [!DNL MetadataUpdate]{#metadataupdate}

Legt Metadatenwerte für ein bestimmtes mit setAssetMetadata verwendetes Asset fest. Beschreibt die Änderungen, die Sie an Metadaten vornehmen möchten.

>[!NOTE]
>
>Wenn das Einzelwertfeld übergeben wird, wird der Tag-Wert des Assets auf den angegebenen Tag-Wert zurückgesetzt.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle der Metadatenfelder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Wert</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Wert der Metadatenaktualisierung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Boolescher Metadatenwert (nur für Felder mit boolescher Eingabe). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Langer Metadatenwert (nur für int-typisierte Felder). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Doppelter Metadatenwert (nur für schwebende Felder). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datums-Metadatenwert (nur für Felder vom Typ „Datum„). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> <p>Fügt zur vorhandenen Tag-Werteliste für das Asset hinzu. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">In Tag-Feldern mit einem Wert wird nur der letzte Wert gespeichert. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Ein festes Wörterbuch-Tag-Feld gibt einen Fehler zurück, wenn der Wert nicht im Wörterbuch enthalten ist. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3">Ersetzt die vorhandene Tag-Werteliste für das Asset. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">In Tag-Feldern mit einem Wert wird nur der letzte Wert gespeichert. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Ein festes Wörterbuch-Tag-Feld gibt einen Fehler zurück, wenn der Wert nicht im Wörterbuch enthalten ist. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:StringArray</span> </td> 
   <td colname="col3"> Löscht die angegebenen Werte aus der Tag-Wert-Liste des Assets, falls vorhanden. </td> 
  </tr> 
 </tbody> 
</table>
