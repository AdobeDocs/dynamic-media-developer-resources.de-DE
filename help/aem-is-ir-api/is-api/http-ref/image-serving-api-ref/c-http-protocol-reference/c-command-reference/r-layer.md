---
title: Layer
description: Wählen Sie Ebene aus. Wählt eine Ebene aus und startet ein neues Ebenendefinitionssegment in der Befehlssequenz.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Layer{#layer}

Wählen Sie Ebene aus. Wählt eine Ebene aus und startet ein neues Ebenendefinitionssegment in der Befehlssequenz.

`layer= *`n`*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Anzahl der auszuwählenden Ebenen (0 oder mehr int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Wählen Sie das Composite-Bild aus. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Ebenenname. </p></td> 
 </tr> 
</table>

Alle Befehle im Ebenensegment werden auf die angegebene Ebene angewendet. Ein Ebenensegment wird bis zum nächsten beendet `layer=` oder `effect=` -Befehl oder das Ende der Anfrage.

Angeben `layer=comp` , um das zusammengesetzte Bild (oder bei einigen Befehlen die Ansicht) auszuwählen.

Die Ebenennummer gibt effektiv die z-Reihenfolge für die Ebene an. Höhere Ebenen werden auf unternummerierten Ebenen platziert.

Ebenennummern müssen nicht aufeinander folgen. Ebene 0 ist erforderlich.

Ein Name kann einer Ebene mit der `layer= *`n`*, *`name`*` Befehlsvariante. Nachdem eine benannte Ebene definiert wurde, kann sie mit ` layer= *`name`*`, ohne die Ebenennummer kennen zu müssen. Dieselbe Ebene können mehrere Namen zugewiesen werden, wobei mehrere `layer= *`n`*, *`name`*` Befehle.

>[!NOTE]
>
>Ebene 0 bestimmt die Gesamtgröße der Arbeitsfläche. Alle Teile von Schichten, die außerhalb der Grenzen der Ebene 0 fallen, werden bei der Erstellung des Composite abgeschnitten.

## Eigenschaften {#section-499963ee52c14f2898f0d0f90c1d01be}

Ebenenbefehl. Ersatzvariablenverweise werden in `layer=`.

`comp` ist nicht zulässig als *`name`* Zeichenfolge. Ein Fehler wird zurückgegeben, wenn dasselbe *`name`* wird mehr als einer Ebene zugewiesen oder wenn eine Ebene durch *`name`* die zuvor nicht definiert wurde.

## Standard {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Viele Befehle und Attribute gelten für Ebene 0, wenn `layer=comp`.

## Sonderfälle {#section-e087cb2e3562473e8d391abfa3b9489f}

* Wenn der gleiche Name mehreren Ebenen zugeordnet ist (z. B.: `layer=1,image&layer=2,image`), tritt ein Fehler auf.
* Wenn derselbe Name mehrmals einer Ebene zugeordnet wird (z. B.: `layer=1,image&layer=1,image`), wird der Umfang wie gewohnt ohne Fehler festgelegt.
* Es werden mehrere Namen für dieselbe Ebene unterstützt.

  Mit beiden Namen können Sie auf die Ebene verweisen (z. B.: `layer=1,image&layer=1,picture`).
* Wenn ein referenzierter Name nie einer Ebenennummer zugeordnet wird (z. B.: `layer=1,image&layer=picture`), tritt ein Fehler auf.
* Ersatzvariablen werden in Ebenen-Modifikatoren nicht unterstützt (z. B.: `layer=$image$`).

  Dies gilt für alle Permutationen, nicht nur für Ebenennamen, sondern auch für allgemeine Ebenenmodifikatoren.

* Alle Zusammenführungs- und Überschreibungsregeln sollten genau so funktionieren, wie wenn dieselbe Ebene in mehreren Quellen referenziert wird (Katalogdatensätze vor oder nach dem Modifikator, Makros usw.).

## Beispiel {#section-cc40de6a0a754178aa752601539c815b}

Siehe Beispiele unter [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
