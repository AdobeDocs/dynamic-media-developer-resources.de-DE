---
title: Katalog-Attributdateien
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch eine Dateiendung .ini aufweisen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Katalog-Attributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch eine Dateiendung `.ini`. Sie können mit jedem Texteditor problemlos gepflegt werden.

Katalogattributdateien bestehen aus einer Reihe von Textdatensätzen, die durch eine einzelne `<CR>` (ASCII-Code 0xD), eine einzelne `<LF>` (ASCII-Code 0xA) oder ein `<CR><LF>` Paar getrennt sind. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren durch Kommas getrennten Attributwerten:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Name </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributname; kann aus einem oder mehreren Buchstaben, Zahl, - (Bindestrich) und _ (Unterstrich) bestehen; Groß-/Kleinschreibung wird nicht beachtet.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributwert; darf <span class="codeph"> &lt;CR&gt;-</span> oder <span class="codeph"> &lt;LF&gt;-</span> nicht enthalten, es sei denn, sie sind durch einen einfachen umgekehrten Schrägstrich unmittelbar vor dem Zeilenumbruch maskiert. </p> </td> 
 </tr> 
</table>

* Leerraum zwischen Token ist optional.
* Der [!DNL Platform Server] ignoriert Datensätze mit unbekannten Attributnamen.
* Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie `-`-, `_`- und `.` bestehen.
* Wenn derselbe Attributname mehrmals in derselben Attributdatei vorkommt, hat der zuletzt aufgetretene Vorrang.
* Verwenden Sie `#` als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.
