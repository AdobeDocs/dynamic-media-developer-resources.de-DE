---
description: In diesem Abschnitt wird die grundlegende Syntax des Dynamic Media Image Rendering HTTP-Protokolls beschrieben.
seo-description: In diesem Abschnitt wird die grundlegende Syntax des Dynamic Media Image Rendering HTTP-Protokolls beschrieben.
seo-title: Grundlegende Syntax des Image Rendering-HTTP-Protokolls
solution: Experience Manager
title: Grundlegende Syntax des Image Rendering-HTTP-Protokolls
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 4%

---


# Grundlegende Syntax des Image Rendering HTTP-Protokolls{#image-rendering-http-protocol-basic-syntax}

In diesem Abschnitt wird die grundlegende Syntax des Dynamic Media Image Rendering HTTP-Protokolls beschrieben.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> anfordern</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> Modifikatoren</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Vignette  </span> </p> </td> 
   <td colname="col2"> <p>Vignettenbezeichner (relativer Dateipfad oder Vignettenkatalogeintrag). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Modifikatoren </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp;  <span class="varname"> Modifikator</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>Name eines Befehlmakros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Kommentar  </span> </p> </td> 
   <td colname="col2"> <p>Kommentarzeichenfolge (vom Server ignoriert). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>Name eines Befehls oder Attributs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Name einer benutzerdefinierten Variablen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Wert </span> </p> </td> 
   <td colname="col2"> <p>Befehls- oder Variablenwert. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*,  *`cmdName`*,  *`macro`* und  *`var`* unterscheiden nicht zwischen Groß- und Kleinschreibung. Der Server behält die Groß-/Kleinschreibung aller anderen Zeichenfolgenwerte bei.

**Server-ID**

Der Stammkontext &#39; `/ir/render`&#39; ist für alle HTTP-Anfragen zum Image Rendering erforderlich.

**Kommentare**

Kommentare können überall in Anforderungszeichenfolgen eingebettet werden und durch einen Punkt (.) gekennzeichnet werden unmittelbar nach dem Befehlstrennzeichen (&amp;). Der Kommentar wird durch das nächste Vorkommen eines (nicht kodierten) Befehlstrennzeichens beendet. Diese Funktion kann verwendet werden, um Informationen zur Anforderung hinzuzufügen, die nicht zur Verwendung mit Image Serving bestimmt sind, wie Zeitstempel, Datenbank-IDs usw.

**HTTP-Dekodierung**

Beim Rendern werden zunächst *`object`* und *`modifiers`* aus der eingehenden Anforderung extrahiert. *`object`* wird dann in Pfadelemente aufgeteilt, die einzeln HTTP-dekodiert sind. Die *`modifiers`*-Zeichenfolge wird in *`command`*= *`value`*-Paare getrennt und *`value`* wird dann vor der befehlsspezifischen Verarbeitung HTTP-dekodiert.
