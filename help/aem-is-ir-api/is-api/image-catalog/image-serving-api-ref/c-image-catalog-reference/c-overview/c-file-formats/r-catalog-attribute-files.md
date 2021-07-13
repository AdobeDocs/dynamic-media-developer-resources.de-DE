---
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
title: Katalogattributdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können mit jedem Texteditor problemlos gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Textdatensätzen, getrennt durch ein einzelnes `<CR>` (ASCII-Code `0xD`), ein einzelnes `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>`-Paar. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren kommagetrennten Attributwerten:

`*``*= *`namvalues`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Werte</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> [, <span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Attributname. Kann aus einem oder mehreren Buchstaben, einer Zahl, - und _ bestehen. Nicht zwischen Groß- und Kleinschreibung unterscheiden. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Attributwert. Darf keine <span class="codeph"> &lt;CR&gt;</span>- oder <span class="codeph"> &lt;LF&gt;</span>-Zeichen enthalten, es sei denn, diese Zeichen werden durch einen einzigen umgekehrten Schrägstrich kurz vor dem Zeilenumbruchzeichen maskiert. </p></td> 
 </tr> 
</table>

Leerzeichen zwischen Token sind optional.

Datensätze mit unbekannten Attributnamen werden vom Platform-Server ignoriert.

Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;, &quot;_&quot;und &quot;.&quot;bestehen.

Wenn derselbe Attributname mehrmals in derselben Attributdatei vorkommt, hat der zuletzt aufgetretene Name Vorrang.

Verwenden Sie # als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, was der Parser ignoriert.
