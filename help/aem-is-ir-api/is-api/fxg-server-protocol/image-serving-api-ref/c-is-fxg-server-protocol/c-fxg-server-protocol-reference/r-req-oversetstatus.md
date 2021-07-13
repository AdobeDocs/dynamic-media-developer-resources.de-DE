---
description: Anfragetyp. Gibt den Anforderungstyp an.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '246'
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
   <td colname="col2"> <p> Gibt eine XML-Liste aller Elemente mit dem Attributwert <span class="codeph"> s7:element</span> und einer Liste aller Seiten im FXG-Dokument zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Gibt die XML-Liste zurück, deren <span class="codeph"> &lt;RichText/&gt;</span> -Elemente überschrieben werden. </p> <p>Gibt eine XML-Liste mit <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Elementen zurück, die für die Verarbeitung auf Client-Seite überschrieben sind. Nur <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> überschriebene Elemente werden zurückgegeben. <span class="+ topic/ph pr-d/codeph codeph"> s7: </span> elementidis ist ein erforderliches  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> Attribut bei Verwendung von  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Alle Übersatzelemente <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> ohne <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> werden nicht aufgeführt. Jedes <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Element in der Liste hat den <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> und den Begrenzungsrahmen des übergesetzten Textrahmens. Das Attribut <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> gibt den Textindex in der Story an, bis zu dem der Text in den Frame passt. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonly gilt nur für  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> Elemente in der angeforderten FXG. Es werden keine <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente aus eingebetteten FXGs aufgelistet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vorhanden</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>eindeutige Anforderungskennung von reqId </p> <p>Gibt eine einzelne Eigenschaft mit dem Namen catalogRecord.exists zurück. Der Eigenschaftswert wird auf "1"gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf "0". req=exists -Anforderungen für den /is/content-Kontext zeigen an, ob ein angegebener Datensatz im statischen Inhaltskatalog vorhanden ist oder nicht. </p> </td> 
  </tr> 
 </tbody> 
</table>
