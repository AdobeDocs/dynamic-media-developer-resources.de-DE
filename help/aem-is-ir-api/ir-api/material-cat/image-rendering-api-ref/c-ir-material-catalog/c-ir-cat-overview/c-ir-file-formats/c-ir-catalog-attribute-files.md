---
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.
seo-description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.
seo-title: Katalogattributdateien
solution: Experience Manager
title: Katalogattributdateien
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Datensätzen, die durch einen einzelnen `<CR>` (ASCII-Code 0xD), einen einzelnen `<LF>` (ASCII-Code 0xA) oder ein `<CR><LF>` Paar getrennt sind. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren durch Komma getrennten Attributwerten:

` *``*= *``*&#42;[, *`namevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Name </span></span> </p> </td> 
  <td class="stentry"> <p>Attributname; kann aus einem oder mehreren Buchstaben, Zahlen, '-' und '_' bestehen; Groß-/Kleinschreibung nicht beachten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span></span> </p> </td> 
  <td class="stentry"> <p>Attributwert; darf keine <span class="codeph"> &lt;CR&gt;- </span>oder <span class="codeph"> &lt;LF&gt;- </span> Zeichen enthalten, es sei denn, ein umgekehrter Schrägstrich unmittelbar vor dem Zeilenumbruchzeichen ist mit einem Escape-Zeichen versehen. </p> </td> 
 </tr> 
</table>

* Leerzeichen zwischen Token sind optional.
* Datensätze mit unbekannten Attributnamen werden vom Plattformserver ignoriert.
* Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;, &quot;_&quot;und &quot;.&quot;bestehen.
* Wenn derselbe Attributname in derselben Attributdatei mehrmals vorkommt, ist der letzte aufgetretene Attributname vorhanden.
* Verwenden Sie &quot;#&quot;als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.

