---
title: OPAC
description: Anpassen der Bilddeckkraft. Ermöglicht das Verringern der Vordergrunddeckkraft eines Bildes, Textes, einer Volltonfarbe oder einer Effektebene.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# OPAC{#opac}

Anpassen der Bilddeckkraft. Ermöglicht das Verringern der Vordergrunddeckkraft eines Bildes, Textes, einer Volltonfarbe oder einer Effektebene.

`opac= *`opacity`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Deckkraft</span> </p> </td> 
  <td class="stentry"> <p>Primäre Deckkraft (0…100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Fülldichte (0…100 int). </p></td> 
 </tr> 
</table>

Die Vordergrundopazität für eine Bildebene wird durch die Ebenenmaske oder den Alphakanal des Bildes bestimmt, oder, falls keine der beiden vorhanden sind, beträgt sie 100%. Die Vordergrunddeckkraft einer Textebene beträgt 100 %, und die einer einfarbigen Ebene wird durch `color=` festgelegt.

`opac=` ändert niemals die Deckkraft von Bereichen, die mit `color=` oder `bgColor=` gefüllt sind, mit Ausnahme der Vordergrundbereiche mit Volltonfarbe und Effektebenen (festgelegt mit `color=`).

Wenn in einer Bild-, Text- oder Vollfarbschicht angegeben, wendet *`opacity`* die gesamte Ebene einschließlich aller zugehörigen Effektebenen an, während *`fillOpacity`* nur für die Primärschichtinhalte gilt. Wenn in einer Effektebene angegeben, wird *`opacity`* auf die Effektebene angewendet, während *`fillOpacity`* ignoriert wird.

Die effektive Deckkraft für den Inhalt der Hauptebene ist ( *`opacity`* &#42; *`fillOpacity`* / 100). Die effektive Deckkraft für Effektebenen ist (Haupt *`opacity`* &#42; Effekt *`opacity`* / 100).

## Eigenschaften {#section-ac3f136ff1584a2eab87500b7164f7fa}

Ebenenattribut. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`.

## Standard {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, für keine Änderung der Deckkraft der Ebene.

## Beispiel {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

Die Textdeckkraft in diesem Beispiel beträgt 90&#42;70/100 = 63 %, und die Effektschichtdeckkraft beträgt 90&#42;50/100 = 45 %.

## Verwandte Themen {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
