---
description: Verwenden Sie die folgenden Befehle zum Kodieren von Zeichen.
solution: Experience Manager
title: Zeichenkodierung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---


# Zeichenkodierung{#character-encoding}

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
   <td> <p><span class="varname"> Es </span> muss ein zweistelliger Hexadezimalwert sein. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Einzelnes Unicode-Zeichen. </p> </td> 
   <td> <p><span class="varname"> Eine </span> vorzeichenbehaftete 2-Byte-Ganzzahl und somit ein Unicode-Wert größer als 32767 muss als negative Zahl ausgedrückt werden. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode-Zeichengröße. </p> </td> 
   <td> <p>Anzahl der Bytes, die dem angegebenen Unicode-Zeichen entsprechen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>Es folgen Zeichen aus dem unteren ANSI-Bereich. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>Es folgen Zeichen aus dem Hochformat ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>Es folgen Dubletten-Byte-Zeichen. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

