---
title: Katalog-Attributdateien
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch eine Dateiendung .ini aufweisen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
TQID: 'https://experienceleague.adobe.com/OwtzX3xKh5ByC3eUhz7dmFjGR5HRD9cbE6atUEL0Nic'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 192
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

