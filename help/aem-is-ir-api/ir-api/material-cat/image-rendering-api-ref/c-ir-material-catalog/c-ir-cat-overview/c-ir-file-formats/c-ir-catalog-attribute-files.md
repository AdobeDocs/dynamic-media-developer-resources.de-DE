---
title: Katalogattributdateien
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über eine `.ini` Dateisuffix. Sie können mit jedem Texteditor problemlos gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Textdatensätzen, getrennt durch eine `<CR>` (ASCII-Code 0xD), ein `<LF>` (ASCII-Code 0xA) oder einem `<CR><LF>` ein. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren kommagetrennten Attributwerten:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributname; kann aus einem oder mehreren Buchstaben, einer Zahl, einem '-' und einem '_' bestehen; nicht zwischen Groß- und Kleinschreibung unterscheiden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributwert; darf nicht enthalten <span class="codeph"> &lt;cr&gt; </span>oder <span class="codeph"> &lt;lf&gt; </span> -Zeichen, es sei denn, sie werden durch einen einzigen umgekehrten Schrägstrich kurz vor dem Zeilenumbruchzeichen maskiert. </p> </td> 
 </tr> 
</table>

* Leerzeichen zwischen Token sind optional.
* Datensätze mit unbekannten Attributnamen werden vom Platform-Server ignoriert.
* Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen und &quot;-&quot;, &quot;_&quot;und &quot;.&quot;bestehen.
* Wenn derselbe Attributname mehrmals in derselben Attributdatei vorkommt, hat der zuletzt aufgetretene Name Vorrang.
* Verwenden Sie &quot;#&quot;als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.
