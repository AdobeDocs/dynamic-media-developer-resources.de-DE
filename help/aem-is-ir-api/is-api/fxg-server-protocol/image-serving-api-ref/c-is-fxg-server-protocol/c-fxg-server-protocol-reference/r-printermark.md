---
description: Anzeigen von Druckmarken. Gibt an, wie die Druckmarken angezeigt werden.
seo-description: Anzeigen von Druckmarken. Gibt an, wie die Druckmarken angezeigt werden.
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Scene7 Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printerMark{#printermark}

Anzeigen von Druckmarken. Gibt an, wie die Druckmarken angezeigt werden.

` printerMark= *`Trim`*, *`marksbleed`*, *`marksregistration`*, *`marksccolor`*, *`barspage information styleline`*, *``*, *``*, *`weightLayer embed`*`

Die verschiedenen Markierungen können deaktiviert oder aktiviert werden. Der Stil der Druckmarken kann auch gesteuert werden.

Die folgenden Werte sind gültig:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Standard </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Standard ist Standard </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>line Gewichtung= </p></td> 
  <td class="stentry"> <p>Jeder Wert im Bereich 0.125 - 2.0, beide Werte inklusive. </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „0.25“. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Der Standardwert ist „1“. </p></td> 
 </tr> 
</table>

## Beispiel {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
