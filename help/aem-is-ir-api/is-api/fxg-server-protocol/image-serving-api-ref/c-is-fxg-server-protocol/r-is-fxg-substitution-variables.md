---
description: Substitutionsvariablen werden verwendet, um Werte von der Anfrage-URL an die auf dem Server gespeicherten FXG-Vorlagen zu übertragen.
solution: Experience Manager
title: Substitutionsvariablen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 0%

---

# Substitutionsvariablen{#substitution-variables}

Substitutionsvariablen werden verwendet, um Werte von der Anfrage-URL an die auf dem Server gespeicherten FXG-Vorlagen zu übertragen.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variablenname. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable gesetzt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

* Variablendefinitionen und -verweise können im Abfrageteil der Anfrage-URL auftreten.
* Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle. Das führende &quot;$&quot; identifiziert den Befehl als eine Variablendefinition.
* Beim Variablennamen `*`var`*` wird zwischen Groß- und Kleinschreibung unterschieden. Er kann aus einer beliebigen Kombination von Buchstaben, Zahlen, &#39;-&#39; und &#39;_&#39; bestehen.
* Wichtiger Wert muss für eine sichere HTTP-Übertragung URL-kodiert in einem Durchgang sein.
