---
title: Zeichenkodierung
description: Verwenden Sie die folgenden Befehle zum Kodieren von Zeichen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '87'
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
   <td> <p><span class="varname"> HH</span> muss ein 2-stelliger Hexadezimalwert sein. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Einzelnes Unicode-Zeichen. </p> </td> 
   <td> <p><span class="varname"> N</span> ist eine vorzeichenbehaftete 2-Byte-Ganzzahl und daher muss ein Unicode-Wert größer als 32767 als negative Zahl ausgedrückt werden. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode-Zeichengröße. </p> </td> 
   <td> <p>Anzahl der Bytes, die einem bestimmten Unicode-Zeichen entsprechen. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Zeichen aus dem unteren ANSI-Bereich. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Zeichen aus dem hochgelegenen ANSI-Bereich. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Es folgen Double-Byte-Zeichen. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
