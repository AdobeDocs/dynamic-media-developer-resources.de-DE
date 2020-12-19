---
description: Substitutionsvariable wird verwendet, um Werte von der Anforderungs-URL auf auf dem Server gespeicherte FXG-Vorlagen zu übertragen.
seo-description: Substitutionsvariable wird verwendet, um Werte von der Anforderungs-URL auf auf dem Server gespeicherte FXG-Vorlagen zu übertragen.
seo-title: Ersatzvariablen
solution: Experience Manager
title: Ersatzvariablen
topic: Scene7 Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
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
* Beim Variablennamen ` *`var`*` wird die Groß-/Kleinschreibung beachtet und kann aus einer beliebigen Kombination von Buchstaben, Zahlen, &#39;-&#39; und &#39;_&#39; bestehen.
* Wichtiger Wert muss für eine sichere HTTP-Übertragung mit einer einzigen Pass-URL kodiert sein.

