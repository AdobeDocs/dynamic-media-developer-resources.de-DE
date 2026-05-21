---
title: OPAC
description: Anpassen der Bilddeckkraft. Ermöglicht das Verringern der Vordergrunddeckkraft eines Bildes, Textes, einer Volltonfarbe oder einer Effektebene.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
TQID: 'https://experienceleague.adobe.com/--AimuhKd3XDT-daEAA73WfUPmCZmaCXSrXmLVO8Y6I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
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
