---
description: Substitutionsvariable wird verwendet, um Werte von der Anforderungs-URL auf auf dem Server gespeicherte FXG-Vorlagen zu übertragen.
solution: Experience Manager
title: Ersatzvariablen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Substitutionsvariablen{#substitution-variables}

Substitutionsvariable wird verwendet, um Werte von der Anforderungs-URL auf auf dem Server gespeicherte FXG-Vorlagen zu übertragen.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Variablenname. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable festgelegt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

* Variablendefinitionen und -verweise können im Abschnitt &quot;Abfrage&quot;der Anforderungs-URL auftreten.
* Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle. der führende &#39;$&#39; identifiziert den Befehl als Variablendefinition.
* Beim Variablennamen `*`var`*` wird die Groß-/Kleinschreibung beachtet und kann aus einer beliebigen Kombination von Buchstaben, Zahlen, &#39;-&#39; und &#39;_&#39; bestehen.
* Wichtiger Wert muss für eine sichere HTTP-Übertragung mit einer einzigen Pass-URL kodiert sein.

