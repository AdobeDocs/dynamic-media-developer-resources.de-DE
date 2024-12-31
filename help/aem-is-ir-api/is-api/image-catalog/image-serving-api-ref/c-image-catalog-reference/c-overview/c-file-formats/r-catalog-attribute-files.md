---
description: Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch eine Dateiendung .ini aufweisen. Sie können mit jedem Texteditor problemlos gepflegt werden.
solution: Experience Manager
title: Katalog-Attributdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Katalog-Attributdateien{#catalog-attribute-files}

Katalogattributdateien können einen beliebigen Namen haben, müssen jedoch eine Dateiendung .ini aufweisen. Sie können mit jedem Texteditor problemlos gepflegt werden.

Katalogattributdateien bestehen aus einer Reihe von Textdatensätzen, die durch eine einzelne `<CR>` (ASCII-Code-`0xD`), eine einzelne `<LF>` (ASCII-Code-`0xA`) oder ein `<CR><LF>` Paar getrennt sind. Jeder Datensatz besteht aus einem Attributnamen und einem oder mehreren durch Kommas getrennten Attributwerten:

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Werte</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Name</span> </p> </td> 
  <td class="stentry"> <p>Attributname. Kann aus einem oder mehreren Buchstaben, Zahl, - und _ bestehen. Groß-/Kleinschreibung wird nicht berücksichtigt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Val</span> </p></td> 
  <td class="stentry"> <p>Attributwert. Darf keine <span class="codeph"> &lt;CR&gt;</span> oder <span class="codeph"> &lt;LF&gt;</span> Zeichen enthalten, es sei denn, sie werden durch einen einfachen umgekehrten Schrägstrich unmittelbar vor dem Zeilenumbruch maskiert. </p></td> 
 </tr> 
</table>

Leerraum zwischen Token ist optional.

Datensätze mit unbekannten Attributnamen werden vom [!DNL Platform Server] ignoriert.

Attributnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie aus &quot;-&quot;, „_“ und &quot;.“ bestehen.

Wenn derselbe Attributname mehrmals in derselben Attributdatei vorkommt, hat der zuletzt aufgetretene Vorrang.

Verwenden Sie # als erstes Zeichen, um einen Datensatz als Kommentar zu markieren, den der Parser ignoriert.
