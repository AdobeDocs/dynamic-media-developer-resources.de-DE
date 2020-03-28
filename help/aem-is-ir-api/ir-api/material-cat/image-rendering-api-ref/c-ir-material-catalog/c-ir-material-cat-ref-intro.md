---
description: In diesem Dokument wird der Materialkatalog für Scene7-Image Rendering beschrieben.
seo-description: In diesem Dokument wird der Materialkatalog für Scene7-Image Rendering beschrieben.
seo-title: Einführung
solution: Experience Manager
title: Einführung
topic: Scene7 Image Serving - Image Rendering API
uuid: 38da0561-7730-4170-bf29-02de325b3ad9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Einführung{#introduction}

In diesem Dokument wird der Materialkatalog für Scene7-Image Rendering beschrieben.

**Vorgesehene Audience**

Diese Dokumentation richtet sich an erfahrene Programmierer und Website-Entwickler, die Scene7 Image Rendering für eine Website oder eine benutzerdefinierte Anwendung nutzen möchten.

Es wird davon ausgegangen, dass der Leser mit Scene7 Image Authoring und Image Rendering, allgemeinen Standards und Konventionen des HTTP-Protokolls und grundlegenden Terminologie der Bildbearbeitung vertraut ist.

**Dokument-Übereinkommen**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>In Syntaxabschnitten ist nichtkursiver Text literal; dies gilt nicht für Leerzeichen und die Symbole [ ] { }| *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "attribute::" bezieht sich auf ein Bildkatalogattribut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> Katalog: Element </span> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "Katalog::" bezieht sich auf ein Datenfeld des Materialkatalogs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein mit dem Präfix "icc::" bezeichneter Name bezieht sich auf ein Profil in der ICC-Farbfeldzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Makro::Element </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "macro::" bezieht sich auf ein Feld in der Makrodefinitionstabelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleSet::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "ruleSet:" bezieht sich auf ein Element in einem URL-Vorverarbeitungsregelsatz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default:Item </span> </p> </td> 
  <td class="stentry"> <p>Ein mit dem Präfix "default::"vorangestellter Name bezieht sich auf ein Attribut des Standardbildkatalogs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Vignette::Element </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "vignette::"bezieht sich auf ein Feld in der Vignettenzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Optionale Syntaxelemente sind durch eckige Klammern eingeschlossen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Das optionale Syntaxelement kann jederzeit wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> Element 2 </span> </p> </td> 
  <td class="stentry"> <p>Eine vertikale Leiste gibt an, dass entweder das einzelne Syntaxelement links oder das Element rechts verwendet werden kann. Genau ein Element muss ausgewählt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> Gruppe </span> } </p> </td> 
  <td class="stentry"> <p>Zur Gruppierung von Syntaxelementen werden geschweifte Klammern verwendet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> Gruppe </span> } </p> </td> 
  <td class="stentry"> <p>Die Syntaxelemente innerhalb der Gruppe können ein- oder mehrmals wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Leerraum. </p> </td> 
  <td class="stentry"> <p>Leerzeichen (Leerzeichen oder Tabulatoren) sind in HTTP-Anforderungen nicht zulässig. In diesem Dokument wird gelegentlich ein Leerraum zwischen syntaktischen Elementen verwendet, um nur Klarheit zu schaffen. </p> </td> 
 </tr> 
</table>

