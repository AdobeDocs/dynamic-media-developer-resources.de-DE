---
description: Verwenden Sie die folgenden Befehle zum Kodieren von Zeichen.
seo-description: Verwenden Sie die folgenden Befehle zum Kodieren von Zeichen.
seo-title: Zeichenkodierung
solution: Experience Manager
title: Zeichenkodierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Character encoding{#character-encoding}

Verwenden Sie die folgenden Befehle zum Kodieren von Zeichen.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Befehl </th> 
   <th class="entry"> Beschreibung </th> 
   <th class="entry"> Anmerkungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Einzelnes 8-Bit-Zeichen. </p> </td> 
   <td> <p><span class="varname"> Er</span> muss ein zweistelliger Hexadezimalwert sein. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Einzelnes Unicode-Zeichen. </p> </td> 
   <td> <p><span class="varname"> N</span> ist eine vorzeichenbehaftete 2-Byte-Ganzzahl und daher muss ein Unicode-Wert größer als 32767 als negative Zahl ausgedrückt werden. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode-Zeichengröße. </p> </td> 
   <td> <p>Anzahl der Bytes, die dem angegebenen Unicode-Zeichen entsprechen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Es folgen Zeichen aus dem unteren ANSI-Bereich. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Es folgen Zeichen aus dem Hochformat ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Es folgen Dubletten-Byte-Zeichen. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

