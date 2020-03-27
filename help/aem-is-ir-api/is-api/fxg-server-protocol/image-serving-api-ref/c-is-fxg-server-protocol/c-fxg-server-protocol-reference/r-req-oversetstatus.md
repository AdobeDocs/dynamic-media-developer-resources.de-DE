---
description: Anforderungstyp Gibt den Anforderungstyp an.
seo-description: Anforderungstyp Gibt den Anforderungstyp an.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col2"> <p> Gibt die XML-Liste aller Elemente mit dem <span class="codeph"> s7:element</span> -Attributwert und einer Liste aller Seiten im fxg-Dokument zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Gibt die XML-Liste zurück, von der <span class="codeph"> &lt;RichText/&gt;</span> -Elemente übersetzt sind. </p> <p>Gibt eine XML-Liste von <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elementen zurück, die zur Verarbeitung auf Clientseite überschrieben werden. Es werden nur <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente zurückgegeben, die Übersatz sind. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> ist ein erforderliches <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> Attribut bei Verwendung von <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Übersatzelemente <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> ohne <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> werden nicht aufgeführt. Jedes <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Element in der Liste hat den <span class="+ topic/ph pr-d/codeph codeph"> Wert s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>und den Begrenzungsrahmen des Übersatztextrahmens. Das <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> -Attribut gibt den Textindex in der Geschichte an, bis zu dem Text in den Rahmen passen konnte. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> gilt nur für <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente in der angeforderten FXG-Datei. Es werden keine <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> -Elemente aus eingebetteten FXGs Liste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vorhanden</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId, eindeutige Anforderungskennung </p> <p>Gibt eine einzelne Eigenschaft mit dem Namen catalogRecord.exists zurück. Der Eigenschaftswert wird auf "1"gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf "0". "req=exists"-Anforderungen für den Kontext "/is/content"weisen auf das Vorhandensein oder Fehlen eines bestimmten Datensatzes im statischen Inhaltskatalog hin. </p> </td> 
  </tr> 
 </tbody> 
</table>

