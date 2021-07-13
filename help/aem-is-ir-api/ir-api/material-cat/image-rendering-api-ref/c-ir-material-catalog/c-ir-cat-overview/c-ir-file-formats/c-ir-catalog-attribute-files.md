---
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
title: Katalogattributdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können mit jedem Texteditor problemlos gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Textdatensätzen, getrennt durch ein einzelnes `<CR>` (ASCII-Code 0xD), ein einzelnes `<LF>` (ASCII-Code 0xA) oder ein `<CR><LF>`-Paar. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren kommagetrennten Attributwerten:

`*``*= *``*&#42;[, *`namevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributname; kann aus einem oder mehreren Buchstaben, einer Zahl, einem '-' und einem '_' bestehen; nicht zwischen Groß- und Kleinschreibung unterscheiden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributwert; darf keine <span class="codeph"> &lt;CR&gt; </span>- oder <span class="codeph"> &lt;LF&gt; </span>-Zeichen enthalten, es sei denn, diese Zeichen sind durch einen einzigen umgekehrten Schrägstrich unmittelbar vor dem Zeilenumbruchzeichen geschützt. </p> </td> 
 </tr> 
</table>

* Leerzeichen zwischen Token sind optional.
* Datensätze mit unbekannten Attributnamen werden vom Platform-Server ignoriert.
* Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;, &quot;_&quot;und &quot;.&quot;bestehen.
* Wenn derselbe Attributname mehrmals in derselben Attributdatei vorkommt, hat der zuletzt aufgetretene Name Vorrang.
* Verwenden Sie &quot;#&quot;als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.
