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
ht-degree: 1%

---

# Einführung{#introduction}

In diesem Dokument wird das HTTP-Protokoll für das Dynamic Media Image Rendering beschrieben.

Nur die öffentlich zugänglichen Aspekte des Protokolls werden beschrieben. Der Server unterstützt möglicherweise zusätzliche Befehle, die für die Verwendung durch die Dynamic Media-Clientsoftware reserviert sind.

**Vorgesehene Zielgruppe**

Dieses Dokument richtet sich an erfahrene Programmierer und Website-Entwickler, die das Dynamic Media Image Rendering für eine Website oder eine benutzerdefinierte Anwendung verwenden möchten.

Es wird davon ausgegangen, dass der Leser mit Dynamic Media Image Authoring und Image Rendering, allgemeinen HTTP-Protokollstandards und -Konventionen und grundlegender Imaging-Terminologie vertraut ist.

**Dokumentkonventionen**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>In Syntaxabschnitten ist nichtkursiv Text literal; es gilt nicht für Leerzeichen und die Symbole [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>In beschreibenden Abschnitten ist nichtkursiver Text in einfachen Anführungszeichen literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Parameter </span> </p> </td> 
  <td class="stentry"> <p>Eine kursive Formatierung bezeichnet eine Variable oder einen Parameter, die durch einen tatsächlichen Wert ersetzt werden soll. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "attribute::"bezieht sich auf ein Bildkatalogattribut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog:Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "catalog::"bezieht sich auf ein Datenfeld des Materialkatalogs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc:Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "icc::"bezieht sich auf ein Feld in der ICC-Farbprofilzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro:Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "macro::" bezieht sich auf ein Feld in der Makrodefinitionstabelle. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset:Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "ruleset:" bezieht sich auf ein Element in einem Regelsatz für die URL-Vorverarbeitung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Standard::Item </span> </p> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "default::"bezieht sich auf ein Attribut des Standard-Bildkatalogs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> Vignette::Item </span> </td> 
  <td class="stentry"> <p>Ein Name mit dem Präfix "vignette::"bezieht sich auf ein Feld in der Vignettenzuordnung. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Optionale Syntaxelemente sind durch eckige Klammern eingeschlossen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Das optionale Syntaxelement kann nicht oder mehrmals wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>Ein vertikaler Balken zeigt an, dass entweder das einzelne Syntaxelement links oder das Element rechts verwendet werden kann. Genau ein Element muss ausgewählt sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> Gruppe </span> } </p> </td> 
  <td class="stentry"> <p>geschweifte Klammern dienen der Gruppierung von Syntaxelementen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> Gruppe </span> } </p> </td> 
  <td class="stentry"> <p>Die Syntaxelemente innerhalb der Gruppe können ein- oder mehrmals wiederholt werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Leerraum </p> </td> 
  <td class="stentry"> <p>Leerzeichen (Leerzeichen oder Tabulatoren) sind in HTTP-Anforderungen nicht zulässig. In diesem Dokument wird gelegentlich nur aus Gründen der Klarheit Leerraum zwischen syntaktischen Elementen verwendet. </p> </td> 
 </tr> 
</table>

**Allgemeine Begriffe**

** *`MSS`* ** Materialspezifizierungs-Segment: eine Reihe von materiellen Attributen zwischen zwei Auswahlbefehlen in der Anfrage.

** *`vignette`* ** Ein Bild, das in der Dynamic Media-Bildbearbeitung zur Verwendung mit dem Bild-Rendering vorbereitet wurde.
