---
description: Druckermarkierungen anzeigen. Gibt an, wie die Druckermarkierungen angezeigt werden.
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

Druckermarkierungen anzeigen. Gibt an, wie die Druckermarkierungen angezeigt werden.

` printerMark= *`Schnittmarken`*, *`Anschnittzeichen`*, *`Registrierungsmarken`*, *`Farbbalken`*, *`Seiteninformationen`*, *`style`*, *`line weight`*, *`layer embed`*`

Die verschiedenen Markierungen können ein- oder ausgeschaltet werden. Der Stil der Druckermarken kann ebenfalls gesteuert werden.

Im Folgenden finden Sie die gültigen Werte:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Trimmmarken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Anzapfungsmarkierungen= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Passmarken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Farbbalken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seiteninformationen= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Standard </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Standard ist Standard </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Zeilengewicht </p></td> 
  <td class="stentry"> <p>Beliebiger Wert im Bereich von 0,125 bis 2,0, beide Werte inklusive. </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ebene einbetten= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Die Standardgrenze ist 1. </p></td> 
 </tr> 
</table>

## Beispiel {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
