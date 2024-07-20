---
title: req
description: Anfragetyp. Gibt den Anforderungstyp an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# req{#req}

Anfragetyp. Gibt den Anforderungstyp an.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wert </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> validate</span> </p> </td> 
   <td colname="col2"> <p> Gibt Fehler beim Rendern des FXG mit den bereitgestellten URL-Modifikatoren zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contents</span> </p> </td> 
   <td colname="col2"> <p> Gibt eine XML-Liste aller Elemente mit dem Attributwert <span class="codeph"> s7:element</span> und eine Liste aller Seiten im FXG-Dokument zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Gibt eine XML-Liste zurück, deren Elemente <span class="codeph"> &lt;RichText/&gt;</span> überschrieben sind. </p> <p>Gibt eine XML-Liste von <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elementen zurück, die für die Verarbeitung auf Client-Seite überschrieben sind. Es werden nur <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente zurückgegeben, die überschrieben sind. Das Attribut <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> ist ein erforderliches Attribut <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> bei Verwendung von <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Alle übergesetzten <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente ohne <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> werden nicht aufgeführt. Jedes Element <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> in der Liste hat den Wert <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, den Wert <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> und den Begrenzungsrahmen des übergesetzten Textrahmens. Das Attribut <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> gibt den Textindex in der Geschichte an, bis zu dem Text in den Frame passt. Der <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> gilt nur für <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente im angeforderten FXG. Es werden keine <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente aus eingebetteten FXGs aufgelistet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>eindeutige Anforderungskennung von reqId </p> <p>Es wird eine einzelne Eigenschaft mit dem Namen catalogRecord.exists zurückgegeben. Der Eigenschaftswert wird auf "1"gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf "0". req=exists -Anfragen für den /is/content-Kontext geben an, ob ein angegebener Datensatz im statischen Inhaltskatalog vorhanden ist oder nicht. </p> </td> 
  </tr> 
 </tbody> 
</table>
