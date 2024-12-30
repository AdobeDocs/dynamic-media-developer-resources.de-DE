---
title: Erf
description: Anfragetyp. Gibt den Anfragetyp an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Erf{#req}

Anfragetyp. Gibt den Anfragetyp an.

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
   <td colname="col2"> <p> Gibt alle Fehler beim Rendern des Tags mit den bereitgestellten URL-Modifikatoren zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Inhalte</span> </p> </td> 
   <td colname="col2"> <p> Gibt eine XML-Liste aller Elemente mit einem <span class="codeph"> s7:element</span> -Attributwert und einer Liste aller Seiten im FXG-Dokument zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetStatus</span> </p> </td> 
   <td colname="col2"> <p>Gibt eine XML-Liste zurück, in der <span class="codeph"> &lt;RichText/&gt;</span> Elemente überschrieben sind. </p> <p>Gibt eine XML-Liste mit <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> zurück, die für die Client-seitige Verarbeitung überlagert sind. Nur <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Elemente, die überschrieben sind, werden zurückgegeben. Die <span class="+ topic/ph pr-d/codeph codeph"> s7:elementId</span> ist ein erforderliches <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> bei Verwendung <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Alle <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Elemente ohne <span class="+ topic/ph pr-d/codeph codeph"> s7:elementId</span> werden nicht aufgeführt. Jedes <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Element in der Liste hat die <span class="+ topic/ph pr-d/codeph codeph"> s7:elementId</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> und den Begrenzungsrahmen des Übersatztextrahmens. Das <span class="+ topic/ph pr-d/codeph codeph"> Attribut s7:endCharIndex</span> gibt den Textindex in der Story an, bis zu dem der Text in den Rahmen passen konnte. Die <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> gilt nur für <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Elemente im angeforderten FXG. Es werden keine <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Elemente aus eingebetteten FXGs aufgelistet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vorhanden</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>Eindeutige Anforderungskennung reqId </p> <p>Es wird eine einzelne Eigenschaft mit dem Namen catalogRecord.exists zurückgegeben. Der Eigenschaftswert wird auf „1“ gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist. Andernfalls wird er auf „0“ gesetzt. req=exists Anfragen für den /is/content-Kontext zeigen an, dass ein bestimmter Datensatz im statischen Inhaltskatalog vorhanden oder nicht vorhanden ist. </p> </td> 
  </tr> 
 </tbody> 
</table>
