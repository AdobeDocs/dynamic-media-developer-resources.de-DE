---
description: In diesem Abschnitt wird die grundlegende Syntax des Dynamic Media Image Rendering-HTTP-Protokolls beschrieben.
solution: Experience Manager
title: Grundlegende Syntax des HTTP-Protokolls "Image Rendering"
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 4%

---

# Grundlegende Syntax des HTTP-Protokolls &quot;Image Rendering&quot;{#image-rendering-http-protocol-basic-syntax}

In diesem Abschnitt wird die grundlegende Syntax des Dynamic Media Image Rendering-HTTP-Protokolls beschrieben.

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
   <td colname="col2"> <p><span class="varname"> server_address</span> [:<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Vignette  </span> </p> </td> 
   <td colname="col2"> <p>Vignettenspezifikator (relativer Dateipfad oder Vignettenkatalogeintrag). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Modifikatoren </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp;  <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>Name eines Befehlsmakros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comment  </span> </p> </td> 
   <td colname="col2"> <p>Kommentar-Zeichenfolge (vom Server ignoriert). </p> </td> 
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

**Server-Kennung**

Der Stammkontext &quot;`/ir/render`&quot;ist für alle HTTP-Anforderungen an das Bild-Rendering erforderlich.

**Kommentare**

Kommentare können überall in Anforderungszeichenfolgen eingebettet werden und werden durch einen Punkt (.) unmittelbar auf das Befehlstrennzeichen (&amp;) folgen. Der Kommentar wird durch das nächste Vorkommen eines (nicht codierten) Befehlstrennzeichens beendet. Diese Funktion kann verwendet werden, um Informationen zur Anforderung hinzuzufügen, die nicht für die Image-Serving-Verwendung vorgesehen ist, wie z. B. Zeitstempel, Datenbank-IDs usw.

**HTTP-Dekodierung**

Beim Rendern von Bildern werden zunächst *`object`* und *`modifiers`* aus der eingehenden Anforderung extrahiert. *`object`* wird dann in Pfadelemente aufgeteilt, die einzeln HTTP-dekodiert sind. Die *`modifiers`*-Zeichenfolge wird in *`command`*= *`value`*-Paare unterteilt und *`value`* wird dann vor der befehlsspezifischen Verarbeitung HTTP-dekodiert.
