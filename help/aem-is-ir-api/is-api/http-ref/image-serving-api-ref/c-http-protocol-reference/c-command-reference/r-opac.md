---
description: Passen Sie die Bilddeckkraft an. Ermöglicht die Verringerung der Vordergrunddeckkraft eines Bildes, Textes, einer Volltonfarbe oder einer Effektebene.
seo-description: Passen Sie die Bilddeckkraft an. Ermöglicht die Verringerung der Vordergrunddeckkraft eines Bildes, Textes, einer Volltonfarbe oder einer Effektebene.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# opac{#opac}

Passen Sie die Bilddeckkraft an. Ermöglicht die Verringerung der Vordergrunddeckkraft eines Bildes, Textes, einer Volltonfarbe oder einer Effektebene.

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Deckkraft</span> </p> </td> 
  <td class="stentry"> <p>Primäre Deckkraft (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Fülldeckkraft (0...100 int). </p></td> 
 </tr> 
</table>

Die Vordergrunddeckkraft einer Bildebene wird durch die Ebenenmaske oder den Alpha-Kanal des Bilds bestimmt oder, wenn keine der beiden vorhanden ist, 100 %. Die Vordergrunddeckkraft einer Textebene beträgt 100 %, die einer Vollfarbebene wird durch `color=`eingestellt.

`opac=` ändert die Deckkraft von Bereichen, die mit `color=` oder `bgColor=`, mit Ausnahme der Vordergrundbereiche von Volltonfarbe und Effektebenen (mit `color=`) gefüllt sind, nie.

Wenn dies in einer Bild-, Text- oder Farbebene angegeben ist, *`opacity`* wird die gesamte Ebene, einschließlich aller zugehörigen Effektebenen, angewendet, während dies nur für den Inhalt der primären Ebene *`fillOpacity`* gilt. Wird in einer Effektebene angegeben, *`opacity`* wird auf die Effektebene angewendet, während sie ignoriert *`fillOpacity`* wird.

Die effektive Deckkraft für den Inhalt der Hauptschicht ist ( *`opacity`* * *`fillOpacity`* / 100). Die effektive Deckkraft für Effektebenen ist (Haupteffekt *`opacity`* * *`opacity`* / 100).

## Eigenschaften {#section-ac3f136ff1584a2eab87500b7164f7fa}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das Composite-Bild, falls `layer=comp`dies der Fall ist.

## Standard {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, damit sich die Deckkraft der Ebene nicht ändert.

## Beispiel {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

Die Texttrübung in diesem Beispiel beträgt 90*70/100=63% und die Effekteschichtdeckkraft 90*50/100=45%.

## Verwandte Themen {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
