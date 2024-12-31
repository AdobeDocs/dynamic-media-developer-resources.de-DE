---
title: Perspektive
description: Perspektivische Transformation. Wenden Sie eine perspektivische Transformation auf das Ebenenquellbild an, sodass es den mit dem Viereck angegebenen Bereich ausfüllt. Andere Bereiche der Schicht bleiben transparent.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Perspektive{#perspective}

Perspektivische Transformation. Wenden Sie eine perspektivische Transformation auf das Ebenenquellbild an, sodass es den mit dem Viereck angegebenen Bereich ausfüllt. Andere Bereiche der Schicht bleiben transparent.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Perspektivische vierseitige Pixel-Koordinaten (8 Real, durch Kommas getrennt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Perspektivische quadrilaterale normalisierte Koordinaten (8 Real, durch Kommas getrennt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Resampling-Optionen (siehe unten). </p></td> 
 </tr> 
</table>

Der Modifikator *`perspQuad`* besteht aus vier Pixelkoordinatenwerten im zusammengesetzten (oder Ebene 0) Koordinatenraum, der an der oberen linken Ecke des zusammengesetzten Bildes entsteht.

Der Modifikator `perspQuadN` besteht aus vier normalisierten Koordinatenwerten, wobei `0.0,0.0` der linken oberen Ecke des Bildes „Verbund/Ebene 0“ und der rechten unteren Ecke `1.0,1.0`.

Das Eingabebild wird transformiert, sodass die obere linke Ecke des Eingabebildes dem ersten Koordinatenwert von `perspQuad[N]`, die obere rechte Ecke der zweiten Koordinate, die untere rechte Ecke der dritten Koordinate und die untere linke Ecke der vierten Koordinate zugeordnet wird.

>[!NOTE]
>
>Mit dem Modifikator `pos=` kann die transformierte Schicht im Verbundbild weiter positioniert werden.

Die perspektivischen Viereck-Koordinaten können sich außerhalb des Verbundbildes befinden.

Das Verhalten ist undefiniert, wenn das Viereck nicht für eine Perspektivtransformation geeignet ist. Wenn beispielsweise zwei oder mehr Scheitelpunkte zusammenfallen, sich drei oder alle Scheitelpunkte auf derselben Linie befinden oder das Viereck sich selbst schneidet oder konkav ist.

## Überlegungen zur Qualität {#section-7cc9056afa614300a9b8844d39739fc3}

Während die Standardimplementierung einen vernünftigen Kompromiss zwischen Qualität und Leistung darstellt, kann es erforderlich sein, die Auflösung des Quellbilds zu erhöhen, um die Schärfe zu verbessern oder sie zu reduzieren, um Alias-Artefakte zu reduzieren.

Wenn die Quelle ein Bild ist, wählen Sie mithilfe von `scale=` eine andere Auflösung aus (relativ zur vollständigen Auflösung des Bildes). Der angegebene `scale=` wird auf die nächsthöhere PTIF-Auflösungsebene gerundet. Wenn eine verschachtelte Anfragequelle vorhanden ist, kann die Größe des durch die verschachtelte Anfrage erzeugten Bildes angepasst werden, um die gewünschte Schärfe zu erreichen. Bei Textebenen wird die Auflösung des Eingabebilds (der gerenderte Text) angepasst, indem ein größerer Wert für size= ausgewählt wird, wobei die mit `textAttr=` angegebene Auflösung erhöht wird.

Mit dem Modifikator-*`resOptions`* können Sie einen alternativen Resampling-Algorithmus auswählen. Die folgenden Werte werden unterstützt (unter Berücksichtigung von Groß- und Kleinschreibung):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Wert</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Nächster Nachbar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bilinear. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Standard-Super-Sampling (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super-Sampling mit einstellbarem Jitter (<span class="varname"> n</span> muss ein ganzzahliger Wert zwischen 0 und 200 sein). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-818e57df0a1b4449888543bc6af77751}

Ebenenbefehl. Gilt für die aktuelle Ebene oder, falls `layer=comp`, für Ebene 0. Von Effektebenen ignoriert.

Der Modifikator `res=` wird immer ignoriert, wenn die Perspektive in derselben Ebene vorhanden ist. Der `size=` wird ignoriert, wenn er für Bildebenen angegeben wird. Die Modifikatoren `size=` und `res=` in Ebenen mit `perspective=` sind für die zukünftige Verwendung reserviert.

## Standard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, für keine Perspektivtransformation.

## Verwandte Themen {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
