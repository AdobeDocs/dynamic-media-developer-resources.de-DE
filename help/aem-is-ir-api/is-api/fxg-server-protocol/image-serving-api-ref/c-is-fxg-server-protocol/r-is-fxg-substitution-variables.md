---
description: Ersatzvariable wird verwendet, um Werte von der Anforderungs-URL an auf dem Server gespeicherte FXG-Vorlagen zu übertragen.
solution: Experience Manager
title: Ersatzvariablen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# Ersatzvariablen{#substitution-variables}

Ersatzvariable wird verwendet, um Werte von der Anforderungs-URL an auf dem Server gespeicherte FXG-Vorlagen zu übertragen.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variablenname. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable gesetzt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

* Variablendefinitionen und -verweise können im Abfrageabschnitt der Anforderungs-URL auftreten.
* Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle; der vorangestellte &#39;$&#39; identifiziert den Befehl als Variablendefinition.
* Beim Variablennamen `*`var`*` wird zwischen Groß- und Kleinschreibung unterschieden und es kann sich um eine beliebige Kombination aus Buchstaben, Zahlen, &#39;-&#39; und &#39;_&#39; handeln.
* Für eine sichere HTTP-Übertragung muss der wichtige Wert als URL-kodiert mit einem Durchgang angegeben werden.
