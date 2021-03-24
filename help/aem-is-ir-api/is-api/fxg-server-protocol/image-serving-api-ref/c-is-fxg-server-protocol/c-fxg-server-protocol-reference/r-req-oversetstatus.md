---
description: Anforderungstyp Gibt den Anforderungstyp an.
solution: Experience Manager
title: req
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# req{#req}

Anforderungstyp Gibt den Anforderungstyp an.

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
   <td colname="col2"> <p> Gibt Fehler beim Rendern der FXG-Datei mit den bereitgestellten URL-Modifikatoren zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Inhalt</span> </p> </td> 
   <td colname="col2"> <p> Gibt die XML-Liste aller Elemente mit dem Attributwert <span class="codeph"> s7:element</span> und einer Liste aller Seiten im fxg-Dokument zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Gibt die XML-Liste zurück, deren <span class="codeph"> &lt;RichText/&gt;</span> -Elemente überschrieben werden. </p> <p>Gibt eine XML-Liste von <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-Elementen zurück, die zur Verarbeitung auf Clientseite überschrieben werden. Es werden nur <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-Elemente zurückgegeben, die Übersatz sind. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidis ein erforderliches  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> Attribut bei Verwendung von  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Beliebige Übersatzelemente <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> ohne <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> werden nicht aufgelistet. Jedes <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-Element in der Liste hat das <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> und den Begrenzungsrahmen des Übersatztextrahmens. Das Attribut <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> gibt den Textindex im Textabschnitt an, bis zu dem Text in den Rahmen passen konnte. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonly gilt nur für  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> Elemente im angeforderten FXG. Es werden keine <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-Elemente aus eingebetteten FXGs Liste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vorhanden</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId, eindeutige Anforderungskennung </p> <p>Gibt eine einzelne Eigenschaft mit dem Namen catalogRecord.exists zurück. Der Eigenschaftswert wird auf "1"gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf "0". "req=exists"-Anforderungen für den Kontext "/is/content"weisen auf das Vorhandensein oder Fehlen eines bestimmten Datensatzes im statischen Inhaltskatalog hin. </p> </td> 
  </tr> 
 </tbody> 
</table>

