---
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.
seo-description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.
seo-title: Katalogattributdateien
solution: Experience Manager
title: Katalogattributdateien
topic: Scene7 Image Serving - Image Rendering API
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Textdatensätzen, die durch ein einzelnes `<CR>` (ASCII-Code `0xD`), ein einzelnes `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>`-Paar getrennt sind. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren durch Komma getrennten Attributwerten:

` *``*= *`Namenswerte`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Werte</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Attributname. Kann aus einem oder mehreren Buchstaben, Zahlen, - und _ bestehen. Groß-/Kleinschreibung nicht beachten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Attributwert. Muss keine <span class="codeph">- oder </span>- oder <span class="codeph">-</span>-Zeichen enthalten, es sei denn, ein einzelner umgekehrter Schrägstrich unmittelbar vor dem Zeilenumbruchzeichen ist mit einem Escape-Zeichen versehen. </p></td> 
 </tr> 
</table>

Leerzeichen zwischen Token sind optional.

Datensätze mit unbekannten Attributnamen werden vom Plattformserver ignoriert.

Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;, &quot;_&quot;und &quot;.&quot;bestehen.

Wenn derselbe Attributname in derselben Attributdatei mehrmals vorkommt, ist der letzte aufgetretene Attributname vorhanden.

Verwenden Sie # als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, der vom Parser ignoriert wird.
