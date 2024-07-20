---
title: Perspektive
description: Perspektive Transformation. Wenden Sie eine Perspektivumwandlung auf das Ebenenquellenbild an, damit es den Bereich füllt, der mit dem Quadrilateralbild angegeben wurde. Andere Bereiche der Ebene bleiben transparent.
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

Perspektive Transformation. Wenden Sie eine Perspektivumwandlung auf das Ebenenquellenbild an, damit es den Bereich füllt, der mit dem Quadrilateralbild angegeben wurde. Andere Bereiche der Ebene bleiben transparent.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Perspektive quadrilaterale Pixelkoordinaten (8 Real, durch Kommas getrennt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Perspektive quadrilaterale normalisierte Koordinaten (8 Real, durch Kommas getrennt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Resampling-Optionen (siehe unten). </p></td> 
 </tr> 
</table>

Der Modifikator *`perspQuad`* besteht aus vier Pixelkoordinatenwerten im Koordinatenraum &quot;Composite&quot;(oder &quot;Layer 0&quot;), der aus der oberen linken Ecke des Composite-Bildes stammt.

Der Modifikator `perspQuadN` besteht aus vier normalisierten Koordinatenwerten, wobei `0.0,0.0` der oberen linken Ecke des Composite/Layer 0-Bildes und `1.0,1.0` der unteren rechten Ecke entspricht.

Das Eingabebild wird so transformiert, dass die obere linke Ecke des Eingabebilds dem ersten Koordinatenwert von `perspQuad[N]`, die obere rechte Ecke der zweiten Koordinate, die untere rechte Ecke der dritten Koordinate und die untere linke Ecke zur vierten Koordinate zugeordnet werden.

>[!NOTE]
>
>Der Modifikator `pos=` kann verwendet werden, um die transformierte Ebene im Composite-Bild weiter zu positionieren.

Die quadrilateralen Koordinaten der Perspektive können sich außerhalb des zusammengesetzten Bildes befinden.

Das Verhalten ist nicht definiert, wenn das Quadrilaterale für eine Perspektivumwandlung nicht geeignet ist. Wenn beispielsweise zwei oder mehr Scheitelpunkte zusammenfallen, wenn sich drei oder alle Scheitelpunkte auf derselben Linie befinden oder wenn sich die quadrilaterale Linie selbst schneidet oder sich verbergt.

## Qualitätsaspekte {#section-7cc9056afa614300a9b8844d39739fc3}

Die Standardimplementierung führt zwar zu einem angemessenen Kompromiss zwischen Qualität und Leistung, es kann jedoch erforderlich sein, die Auflösung des Quellbilds zu erhöhen, um die Schärfe zu verbessern oder um die Skalierung von Artefakten zu reduzieren.

Wenn es sich bei der Quelle um ein Bild handelt, wählen Sie mit &quot;`scale=`&quot;eine andere Auflösung (relativ zur vollständigen Auflösung des Bildes). Der angegebene `scale=` -Wert wird auf die nächste höhere PTIF-Auflösungsebene gerundet. Wenn eine verschachtelte Anforderungsquelle vorhanden ist, kann die Größe des von der verschachtelten Anforderung erzeugten Bildes angepasst werden, um die gewünschte Schärfe zu erzielen. Bei Textebenen wird die Auflösung des Eingabebilds (des gerenderten Texts) angepasst, indem ein größerer size= -Wert ausgewählt wird, wobei die mit `textAttr=` angegebene Auflösung erhöht wird.

Mit dem Modifikator *`resOptions`* können Sie einen alternativen Resampling-Algorithmus auswählen. Die folgenden Werte werden unterstützt (Groß-/Kleinschreibung muss beachtet werden):

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
   <td> <p> Standard-Supersampling (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super-Sampling mit verstellbarem Jitter (<span class="varname"> n</span> muss ein ganzzahliger Wert von 0 bis 200 sein). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-818e57df0a1b4449888543bc6af77751}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Wird von Effektebenen ignoriert.

Der Modifikator `res=` wird immer ignoriert, wenn die Perspektive in derselben Ebene vorhanden ist. Der Modifikator `size=` wird ignoriert, wenn er für Bildebenen angegeben wird. Die Modifikatoren `size=` und `res=` in Ebenen mit `perspective=` sind für die zukünftige Verwendung reserviert.

## Standard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, für keine perspektivische Umwandlung.

## Verwandte Themen {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
