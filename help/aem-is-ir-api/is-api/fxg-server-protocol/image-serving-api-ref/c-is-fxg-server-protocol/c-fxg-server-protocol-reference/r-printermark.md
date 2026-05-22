---
description: Druckermarkierungen anzeigen. Gibt an, wie die Druckermarkierungen angezeigt werden.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
TQID: 'https://experienceleague.adobe.com/tit-a3stXGj0fZoMgi15lPIk-MtZSvUDOqlcayfNlwk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 24%

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
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Anzapfungsmarkierungen= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Passmarken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Farbbalken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seiteninformationen= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Standard </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Standard ist Standard </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Zeilengewicht </p></td> 
  <td class="stentry"> <p>Beliebiger Wert im Bereich von 0,125 bis 2,0, beide Werte inklusive. </p></td> 
  <td class="stentry"> <p>Der Standardwert ist 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ebene einbetten= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist 1. </p></td> 
 </tr> 
</table>

## Beispiel {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
