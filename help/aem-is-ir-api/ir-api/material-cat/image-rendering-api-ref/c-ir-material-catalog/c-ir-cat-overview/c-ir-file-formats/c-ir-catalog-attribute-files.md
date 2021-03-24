---
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.
solution: Experience Manager
title: Katalogattributdateien
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können problemlos mit jedem Texteditor gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Textdatensätzen, die durch ein einzelnes `<CR>` (ASCII-Code 0xD), ein einzelnes `<LF>` (ASCII-Code 0xA) oder ein `<CR><LF>`-Paar getrennt sind. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren durch Komma getrennten Attributwerten:

`*``*= *``*&#42;[, *`namevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributname; kann aus einem oder mehreren Buchstaben, Zahlen, '-' und '_' bestehen; Groß-/Kleinschreibung nicht beachten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributwert; darf keine <span class="codeph">- oder </span>- oder <span class="codeph">- </span>-Zeichen enthalten, es sei denn, ein einzelner umgekehrter Schrägstrich unmittelbar vor dem Zeilenumbruchzeichen ist mit einem Escape-Zeichen versehen. </p> </td> 
 </tr> 
</table>

* Leerzeichen zwischen Token sind optional.
* Datensätze mit unbekannten Attributnamen werden vom Plattformserver ignoriert.
* Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;, &quot;_&quot;und &quot;.&quot;bestehen.
* Wenn derselbe Attributname in derselben Attributdatei mehrmals vorkommt, ist der letzte aufgetretene Attributname vorhanden.
* Verwenden Sie &quot;#&quot;als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.

