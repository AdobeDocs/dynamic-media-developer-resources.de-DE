---
title: Grundlegende Syntax des HTTP-Protokolls zum Rendern von Bildern
description: In diesem Abschnitt wird die grundlegende Syntax des Dynamic Media Image Rendering-HTTP-Protokolls beschrieben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Grundlegende Syntax des HTTP-Protokolls zum Rendern von Bildern{#image-rendering-http-protocol-basic-syntax}

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
   <td colname="col1"> <p><span class="varname"> Anfrage</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> Modifikatoren</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Server-</span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> SERVER_ADDRESS</span> [ :<span class="varname"> Port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Vignette </span> </p> </td> 
   <td colname="col2"> <p>Vignettenspezifikator (relativer Dateipfad oder Vignettenkatalogeintrag). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Modifikatoren </span> </p> </td> 
   <td colname="col2"> <p><span class="varname">-Modifikator</span> *[ und <span class="varname">-Modifikator</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">-</span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> Befehl</span> | { $ <span class="varname"> Makro</span> $ } | { .<span class="varname"> Kommentar</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">-</span> </p> </td> 
   <td colname="col2"> <p>&lbrace; <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> Wert</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> </span> </p> </td> 
   <td colname="col2"> <p>Name eines Befehlsmakros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> </span> </p> </td> 
   <td colname="col2"> <p>Kommentarzeichenfolge (vom Server ignoriert). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName-</span> </p> </td> 
   <td colname="col2"> <p>Name eines Befehls oder Attributs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Name einer benutzerdefinierten Variablen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Wert </span> </p> </td> 
   <td colname="col2"> <p>Wert des Befehls oder der Variablen. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* und *`var`* wird nicht zwischen Groß- und Kleinschreibung unterschieden. Der Server behält die Groß-/Kleinschreibung aller anderen Zeichenfolgenwerte bei.

**Server-Kennung**

Der Stammkontext `/ir/render` ist für alle HTTP-Anfragen an das Bild-Rendering erforderlich.

**Kommentare**

Kommentare können an beliebiger Stelle in Anfragezeichenfolgen eingebettet werden und werden durch einen Punkt (.) unmittelbar nach dem Befehlstrennzeichen (&amp;) gekennzeichnet. Der Kommentar wird beim nächsten Auftreten eines (nicht kodierten) Befehlstrennzeichens beendet. Mit dieser Funktion können Sie der Anfrage Informationen hinzufügen, die nicht für die Verwendung in der Bildbereitstellung vorgesehen sind, z. B. Zeitstempel und Datenbank-IDs.

**HTTP-Dekodierung**

Das Bild-Rendering extrahiert zunächst *`object`* und *`modifiers`* aus der eingehenden Anfrage. Die *`object`* wird dann in Pfadelemente aufgeteilt, die einzeln HTTP-decodiert werden. Die *`modifiers`* Zeichenfolge wird in *`command`*= *`value`* Paare aufgeteilt und *`value`* vor der befehlsspezifischen Verarbeitung HTTP-decodiert.
