---
title: Schicht
description: Ebene auswählen. Wählt eine Ebene aus und startet ein neues Ebenendefinitionssegment in der Befehlssequenz.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Schicht{#layer}

Ebene auswählen. Wählt eine Ebene aus und startet ein neues Ebenendefinitionssegment in der Befehlssequenz.

`layer= *`n`*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> N</span></span> </p></td> 
  <td class="stentry"> <p>Anzahl der auszuwählenden Ebenen (0 oder höher int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Abschl</span> </p></td> 
  <td class="stentry"> <p>Wählen Sie das zusammengesetzte Bild aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Name</span></span> </p></td> 
  <td class="stentry"> <p>Ebenenname. </p></td> 
 </tr> 
</table>

Alle Befehle innerhalb des Ebenensegments werden auf die angegebene Ebene angewendet. Ein Ebenensegment wird durch den nächsten `layer=`- oder `effect=`-Befehl oder das Ende der Anfrage beendet.

Geben Sie `layer=comp` an, um das zusammengesetzte Bild (oder bei einigen Befehlen die Ansicht) auszuwählen.

Die Ebenennummer gibt effektiv die z-Reihenfolge für die Ebene an. Ebenen mit höheren Nummern werden auf Ebenen mit niedrigeren Nummern platziert.

Ebenennummern müssen nicht aufeinander folgend sein. Ebene 0 ist erforderlich.

Einer Ebene kann ein Name mit der Befehlsvariante `layer= *`n`*, *`name`*` zugewiesen werden. Sobald eine benannte Ebene definiert ist, kann sie mit &quot;` layer= *`&quot; `*` werden, ohne die Ebenennummer kennen zu müssen. Der gleichen Ebene können mehrere Namen zugewiesen werden, indem mehrere `layer= *`n`*, *`name`*`-Befehle verwendet werden.

>[!NOTE]
>
>Ebene 0 bestimmt die Gesamtgröße der Arbeitsfläche für die Komposition. Alle Teile von Schichten, die außerhalb der Grenzen der Schicht 0 liegen, werden beim Aufbau des Verbundes abgeschnitten.

## Eigenschaften {#section-499963ee52c14f2898f0d0f90c1d01be}

Ebenenbefehl. Verweise auf Substitutionsvariablen werden in `layer=` nicht unterstützt.

`comp` ist als *`name`* nicht zulässig. Ein Fehler wird zurückgegeben, wenn dieselbe *`name`* mehr als einer Ebene zugewiesen ist oder wenn eine Ebene von *`name`* referenziert wird, die zuvor nicht definiert wurde.

## Standard {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Viele Befehle und Attribute gelten für Ebene 0, falls `layer=comp`.

## Sonderfälle {#section-e087cb2e3562473e8d391abfa3b9489f}

* Wenn derselbe Name mehreren Ebenen zugeordnet wird (z. B.: `layer=1,image&layer=2,image`), tritt ein Fehler auf.
* Wenn derselbe Name einer einzelnen Ebene mehrmals zugeordnet wird (z. B.: `layer=1,image&layer=1,image`), wird der Umfang wie gewohnt und ohne Fehler festgelegt.
* Es werden mehrere Namen für dieselbe Ebene unterstützt.

  Beide Namen können für Verweise auf die Ebene verwendet werden (z. B.: `layer=1,image&layer=1,picture`).
* Wenn ein referenzierter Name nie einer Ebenennummer zugeordnet wird (z. B.: `layer=1,image&layer=picture`), tritt ein Fehler auf.
* Substitutionsvariablen werden in Ebenenmodifikatoren nicht unterstützt (z. B.: `layer=$image$`).

  Dies gilt für alle Permutationen, nicht nur für Ebenennamen, sondern für Ebenenmodifikatoren im Allgemeinen.

* Alle Zusammenführungs- und Überschreibungsregeln sollten genau so funktionieren wie wenn dieselbe Ebene in mehreren Quellen referenziert wird (Anfrage, Datensätze im Pre- oder Post-Modifikator-Katalog, Makros usw.).

## Beispiel {#section-cc40de6a0a754178aa752601539c815b}

Siehe Beispiele in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
