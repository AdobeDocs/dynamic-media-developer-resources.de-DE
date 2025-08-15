---
title: Einführung
description: In diesem Dokument wird das HTTP-Protokoll für das Dynamic Media Image Rendering beschrieben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Einführung{#introduction}

In diesem Dokument wird das HTTP-Protokoll für das Dynamic Media Image Rendering beschrieben.

Es werden nur die öffentlich zugänglichen Aspekte des Protokolls beschrieben. Der Server unterstützt möglicherweise zusätzliche Befehle, die für die Verwendung durch die Dynamic Media-Client-Software reserviert sind.

**Vorgesehene Zielgruppe**

Dieses Dokument richtet sich an erfahrene Programmierer und Website-Entwickler, die Dynamic Media Image Rendering für eine Website oder ein benutzerdefiniertes Programm verwenden möchten.

Es wird davon ausgegangen, dass der Leser mit der Dynamic Media-Bildbearbeitung und dem Bild-Rendering, den allgemeinen HTTP-Protokollstandards und -Konventionen und der grundlegenden Bildterminologie vertraut ist.

**Dokumentkonventionen**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>In Syntaxabschnitten ist nicht kursiver Text literal; er gilt nicht für Leerzeichen und die Symbole [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'Literal' </p> </td> 
  <td class="stentry"> <p>In beschreibenden Abschnitten ist nicht kursiver Text in einfachen Anführungszeichen Literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Parameter </span> </p> </td> 
  <td class="stentry"> <p>Kursiv gibt eine Variable oder einen Parameter an, der durch einen tatsächlichen Wert ersetzt werden soll. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">::Item-</span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „attribute::“ bezieht sich auf ein Bildkatalogattribut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">::Item-</span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „catalog::“ bezieht sich auf ein Materialkatalogdatenfeld. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „icc::“ bezieht sich auf ein Feld in der ICC-Farbprofilzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Makro::Element </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „Makro::“ bezieht sich auf ein Feld in der Makrodefinitionstabelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „ruleset::“ bezieht sich auf ein Element in einem Regelsatz zur Vorverarbeitung von URLs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „default::“ bezieht sich auf ein Attribut des Standardbildkatalogs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph">::</span> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix „vignette::“ bezieht sich auf ein Feld in der Vignettenkarte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optionale </span> ] </p> </td> 
  <td class="stentry"> <p>Optionale Syntaxelemente werden durch eckige Klammern eingeschlossen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optionale </span> ] </p> </td> 
  <td class="stentry"> <p>Das optionale Syntaxelement kann nicht oder nicht mehrmals wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>Ein vertikaler Balken zeigt an, dass entweder das einzelne Syntaxelement links oder das Element rechts verwendet werden kann. Es muss genau ein Element ausgewählt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>Geschweifte Klammern werden verwendet, um Syntaxelemente zu gruppieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>Die Syntaxelemente innerhalb der Gruppe können ein- oder mehrmals wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Leerraum </p> </td> 
  <td class="stentry"> <p>Leerzeichen (Leerzeichen oder Tabulatoren) sind in HTTP-Anfragen nicht zulässig. In diesem Dokument werden zwischen syntaktischen Elementen gelegentlich Leerzeichen verwendet, um die Übersichtlichkeit zu erhöhen. </p> </td> 
 </tr> 
</table>

**Allgemeine Begriffe**

** *`MSS`* ** Materialspezifikationssegment : Ein Satz von Materialattributen zwischen zwei Auswahlbefehlen in der Anforderung.

** *`vignette`* ** Ein Bild, das in der Dynamic Media-Bildbearbeitung für die Verwendung mit dem Bild-Rendering vorbereitet wurde.
