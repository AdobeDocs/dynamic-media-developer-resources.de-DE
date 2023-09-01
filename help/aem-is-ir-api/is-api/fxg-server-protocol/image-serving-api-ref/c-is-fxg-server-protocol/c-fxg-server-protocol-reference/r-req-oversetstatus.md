---
title: req
description: Anfragetyp. Gibt den Anforderungstyp an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

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
   <td colname="col1"> <p> <span class="codeph"> validieren</span> </p> </td> 
   <td colname="col2"> <p> Gibt Fehler beim Rendern des FXG mit den bereitgestellten URL-Modifikatoren zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Inhalt</span> </p> </td> 
   <td colname="col2"> <p> Gibt die XML-Liste aller Elemente mit einer <span class="codeph"> s7:element</span> -Attributwert und eine Liste aller Seiten im FXG-Dokument. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Gibt eine XML-Liste von zurück, die <span class="codeph"> &lt;richtext /&gt;</span> -Elemente überschreiben. </p> <p>Gibt eine XML-Liste von <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -Elemente, die für die Verarbeitung auf Client-Seite überschrieben werden. Nur <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -Elemente zurückgegeben werden, die überschrieben wurden. Die <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> ist erforderlich <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> Attribut bei Verwendung von <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Jede Überlagerung <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -Elemente ohne <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> nicht aufgeführt ist. Jeder <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -Element in der Liste <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>und der Begrenzungsrahmen des übergesetzten Textrahmens. Die <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> -Attribut gibt den Textindex in der Story an, bis zu dem Text in den Rahmen passen konnte. Die <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span> gilt nur für <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -Elemente in der angeforderten FXG. Es werden keine <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -Elemente aus eingebetteten FXGs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vorhanden</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>eindeutige Anforderungskennung von reqId </p> <p>Es wird eine einzelne Eigenschaft mit dem Namen catalogRecord.exists zurückgegeben. Der Eigenschaftswert wird auf "1"gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf "0". req=exists -Anfragen für den /is/content-Kontext geben an, ob ein angegebener Datensatz im statischen Inhaltskatalog vorhanden ist oder nicht. </p> </td> 
  </tr> 
 </tbody> 
</table>
