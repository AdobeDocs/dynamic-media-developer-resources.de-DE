---
description: Anzeigen von Druckermarkierungen. Gibt an, wie die Druckermarkierungen angezeigt werden.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 18%

---

# printerMark{#printermark}

Anzeigen von Druckermarkierungen. Gibt an, wie die Druckermarkierungen angezeigt werden.

` printerMark= *`Schnittmarken`*, *`Anschnittmarkierungen`*, *`Registrierungsmarkierungen`*, *`Farbbalken`*, *`Seiteninformationen`*, *`Stil`*, *`Zeilenstärke`*, *`Einbettung der Ebene`*`}

Die verschiedenen Markierungen können deaktiviert oder aktiviert werden. Der Stil der Druckermarkierungen kann ebenfalls gesteuert werden.

Die folgenden Werte sind gültig:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Anschnittmarkierungen= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Registrierungszeichen= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Farbbalken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Standard </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Der Standardwert ist Standard . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Zeilengewicht = </p></td> 
  <td class="stentry"> <p>Jeder Wert im Bereich 0,125-2,0, beide Werte enthalten. </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 1. </p></td> 
 </tr> 
</table>

## Beispiel {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
