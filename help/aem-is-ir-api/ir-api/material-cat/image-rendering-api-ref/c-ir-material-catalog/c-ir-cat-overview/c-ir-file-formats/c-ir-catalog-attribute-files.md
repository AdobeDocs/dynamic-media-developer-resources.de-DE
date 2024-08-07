---
title: Katalogattributdateien
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch über ein .ini-Dateisuffix verfügen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Katalogattributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch das Suffix &quot;`.ini`&quot; aufweisen. Sie können mit jedem Texteditor problemlos gepflegt werden.

Katalogattributdateien bestehen aus einem Satz von Textdatensätzen, getrennt durch ein einzelnes &quot;`<CR>`&quot;(ASCII-Code 0xD), ein einzelnes &quot;`<LF>`&quot;(ASCII-Code 0xA) oder ein &quot;`<CR><LF>`&quot;-Paar. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren kommagetrennten Attributwerten:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributname; kann aus einem oder mehreren Buchstaben, Zahl, - (Bindestrich) und _ (Unterstrich) bestehen; nicht zwischen Groß- und Kleinschreibung unterscheiden.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Der Attributwert darf nicht die Zeichen <span class="codeph"> &lt;CR&gt; </span> oder <span class="codeph"> &lt;LF&gt; </span> enthalten, es sei denn, er wird durch einen einzelnen umgekehrten Schrägstrich direkt vor dem Zeilenumbruchzeichen maskiert. </p> </td> 
 </tr> 
</table>

* Leerzeichen zwischen Token sind optional.
* Der [!DNL Platform Server] ignoriert Datensätze mit unbekannten Attributnamen.
* Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, Zahlen und Zeichen `-`, `_` und `.` bestehen.
* Wenn derselbe Attributname mehrmals in derselben Attributdatei vorkommt, hat der zuletzt aufgetretene Name Vorrang.
* Verwenden Sie `#` als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.
