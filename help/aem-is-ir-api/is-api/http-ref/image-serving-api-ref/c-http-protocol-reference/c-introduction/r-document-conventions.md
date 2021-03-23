---
description: Dieses Dokument verwendet die folgenden Konventionen.
seo-description: Dieses Dokument verwendet die folgenden Konventionen.
seo-title: Dokument-Übereinkommen
solution: Experience Manager
title: Dokument-Übereinkommen
uuid: c929774b-8560-4f8a-98fd-1b75d4419c4d
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# Dokument-Konventionen{#document-conventions}

Dieses Dokument verwendet die folgenden Konventionen.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>In Syntaxabschnitten ist nichtkursiver Text literal; dies gilt nicht für Leerzeichen und die Symbole [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>In beschreibenden Abschnitten ist nichtkursiver Text in einfachen Anführungszeichen wörtlich. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Parameter </span> </p> </td> 
  <td class="stentry"> <p>Kursivdruck gibt eine Variable oder einen Parameter an, die durch einen tatsächlichen Wert ersetzt werden soll. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command=  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit einem nachgestellten '=' bezieht sich auf einen Image Serving HTTP Protocol-Befehl. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph">-Attribut: </span> bezieht sich auf ein Bildkatalogattribut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Katalog: Element  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph"> Katalog: </span> bezieht sich auf ein Bildkatalogdatenfeld. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph"> icc: </span> bezieht sich auf ein Profil in der ICC-Farbfeldzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph"> font: </span> bezieht sich auf ein Feld in der Schriftzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Makro: Posten  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph">-Makro: </span> bezieht sich auf ein Feld in der Makrodefinitionstabelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleSet::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph">: </span> bezieht sich auf ein Element in einem URL-Vorverarbeitungsregelsatz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default:Item  </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix <span class="codeph"> default: </span> bezieht sich auf ein Attribut des Standardbildkatalogs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [  <span class="varname"> optional  </span>]  </span> </p> </td> 
  <td class="stentry"> <p>Optionale Syntaxelemente sind durch eckige Klammern eingeschlossen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[  <span class="varname"> optional  </span>]  </span> </p> </td> 
  <td class="stentry"> <p>Das <span class="varname"> optionale </span>-Syntaxelement kann jederzeit wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1  </span>|  <span class="varname"> Element 2  </span> </span> </p> </td> 
  <td class="stentry"> <p>Eine vertikale Leiste gibt an, dass entweder das einzelne Syntaxelement links oder das Element rechts verwendet werden kann. Genau ein Element muss ausgewählt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> {  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>Zur Gruppierung von Syntaxelementen werden geschweifte Klammern verwendet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>Die Syntaxelemente innerhalb der Gruppe können ein- oder mehrmals wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Leerraum </p> </td> 
  <td class="stentry"> <p>Leerzeichen (Leerzeichen oder Tabulatoren) sind in HTTP-Anforderungen nicht zulässig. In diesem Dokument wird gelegentlich ein Leerraum zwischen syntaktischen Elementen verwendet, um nur Klarheit zu schaffen. </p> </td> 
 </tr> 
</table>

