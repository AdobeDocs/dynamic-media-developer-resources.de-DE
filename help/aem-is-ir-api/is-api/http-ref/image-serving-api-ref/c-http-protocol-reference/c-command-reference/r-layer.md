---
description: Wählen Sie Ebene. Wählt eine Ebene aus und Beginn ein neues Ebenendefinitionssegment in der Befehlssequenz.
seo-description: Wählen Sie Ebene. Wählt eine Ebene aus und Beginn ein neues Ebenendefinitionssegment in der Befehlssequenz.
seo-title: layer
solution: Experience Manager
title: layer
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# layer{#layer}

Wählen Sie Ebene. Wählt eine Ebene aus und Beginn ein neues Ebenendefinitionssegment in der Befehlssequenz.

`layer= *``*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Anzahl der auszuwählenden Ebene (0 oder höher). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Wählen Sie das Composite-Bild aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Name der Ebene. </p></td> 
 </tr> 
</table>

Alle Befehle im Ebenensegment werden auf die angegebene Ebene angewendet. Ein Ebenensegment wird durch den nächsten Befehl `layer=` oder `effect=` oder das Ende der Anforderung beendet.

Geben Sie `layer=comp` an, um das Composite-Bild (oder bei einigen Befehlen die Ansicht) auszuwählen.

Die Nummer der Ebene gibt die z-Reihenfolge der Ebene an. Ebenen mit einer höheren Nummerierung werden über Ebenen mit einer niedrigeren Nummerierung platziert.

Die Nummern der Ebenen müssen nicht aufeinander folgen. Ebene 0 ist erforderlich.

Ein Name kann einer Ebene mit der Befehlsvariante `layer= *`n`*, *`name`*` zugewiesen werden. Sobald eine benannte Ebene definiert ist, kann auf sie mit ` layer= *`name`*` verwiesen werden, ohne dass die Nummer der Ebene angegeben werden muss. Mit mehreren Befehlen `layer= *`n`*, *`name`*` können derselben Ebene mehrere Namen zugewiesen werden.

>[!NOTE]
>
>Ebene 0 bestimmt die Gesamtgröße der Arbeitsfläche. Alle Teile von Ebenen, die außerhalb der Ebene 0 liegen, werden beim Aufbau des Composite abgeschnitten.

## Eigenschaften {#section-499963ee52c14f2898f0d0f90c1d01be}

Ebene, Befehl. Substitutionsvariablenverweise werden in `layer=` nicht unterstützt.

`comp` ist nicht als  *`name`* Zeichenfolge zulässig. Ein Fehler wird zurückgegeben, wenn dieselbe *`name`* mehreren Ebenen zugewiesen ist oder wenn eine Ebene durch *`name`* referenziert wird, die zuvor nicht definiert wurde.

## Standard {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Viele Befehle und Attribute gelten für Ebene 0, wenn `layer=comp`.

## Sonderfälle {#section-e087cb2e3562473e8d391abfa3b9489f}

* Wenn der gleiche Name mehreren Ebenen zugeordnet ist (z. B.: `layer=1,image&layer=2,image`), tritt ein Fehler auf.
* Wenn derselbe Name mehrmals einer einzelnen Ebene zugeordnet wird (z. B.: `layer=1,image&layer=1,image`), wird der Gültigkeitsbereich wie gewohnt ohne Fehler festgelegt.
* Es werden mehrere Namen für dieselbe Ebene unterstützt.

   Sie können entweder einen Namen verwenden, um auf die Ebene zu verweisen (z. B.: `layer=1,image&layer=1,picture`).
* Wenn ein referenzierter Name nie einer Ebenennummer zugeordnet wird (z. B.: `layer=1,image&layer=picture`), tritt ein Fehler auf.
* Substitutionsvariablen werden in Ebenenmodifikatoren nicht unterstützt (z. B.: `layer=$image$`).

   Dies gilt für alle Permutationen, nicht nur für Ebenennamen, sondern auch für Ebenenmodifikatoren im Allgemeinen.

* Alle Regeln zum Zusammenführen und Überschreiben sollten genau so funktionieren, wie wenn dieselbe Ebene in mehreren Quellen referenziert wird (Katalogeinträge vor oder nach dem Modifizieren, Makros usw.).

## Beispiel {#section-cc40de6a0a754178aa752601539c815b}

Siehe Beispiele unter [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
