---
title: Perspektive
description: Perspektive Transformation. Wenden Sie eine Perspektivumwandlung auf das Ebenenquellenbild an, um den Bereich zu füllen, der mit dem Quadrilateralen angegeben ist. Andere Bereiche der Ebene bleiben transparent.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# Perspektive{#perspective}

Perspektive Transformation. Wenden Sie eine Perspektivumwandlung auf das Ebenenquellenbild an, um den Bereich zu füllen, der mit dem Quadrilateralen angegeben ist. Andere Bereiche der Ebene bleiben transparent.

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

*`perspQuad`* besteht aus vier Pixelkoordinatenwerten im Koordinatenraum der Composite-Ebene (oder Ebene 0), der in der linken oberen Ecke des Composite-Bildes liegt.

`perspQuadN` besteht aus vier normalisierten Koordinatenwerten, wobei `0.0,0.0` entspricht der oberen linken Ecke des Composite/Layer 0-Bildes und `1.0,1.0` in der unteren rechten Ecke.

Das Eingabebild wird so umgewandelt, dass die obere linke Ecke des Eingabebilds dem ersten Koordinatenwert von `perspQuad[N]`, die obere rechte Ecke zur zweiten Koordinate, die untere rechte Ecke zur dritten Koordinate und die untere linke Ecke zur vierten Koordinate.

>[!NOTE]
>
>`pos=` kann verwendet werden, um die transformierte Ebene im Composite-Bild weiter zu positionieren.

Die quadrilateralen Koordinaten der Perspektive können sich außerhalb des zusammengesetzten Bildes befinden.

Das Verhalten ist nicht definiert, wenn das Quadrilateral nicht für eine perspektivische Transformation geeignet ist (z. B. wenn zwei oder mehr Scheitelpunkte zusammenfallen, wenn sich drei oder alle Scheitelpunkte auf derselben Linie befinden oder wenn das quadrilaterale Objekt sich selbst überschneidet oder konkav ist).

## Qualitätsaspekte {#section-7cc9056afa614300a9b8844d39739fc3}

Während die Standardimplementierung einen angemessenen Kompromiss zwischen Qualität und Leistung herstellt, kann es manchmal notwendig sein, die Auflösung des Quellbilds zu erhöhen, um die Schärfe zu verbessern oder um es zu reduzieren, um Aliasing-Artefakte zu reduzieren.

Wenn die Quelle ein Bild ist, verwenden Sie `scale=` , um eine andere Auflösung zu wählen (relativ zur vollständigen Auflösung des Bildes). Die angegebene `scale=` wird auf die nächsthöhere PTIF-Auflösungsebene gerundet. Bei verschachtelten Anforderungsquellen kann die Größe des von der verschachtelten Anforderung erzeugten Bildes angepasst werden, um die gewünschte Schärfe zu erzielen. Bei Textebenen wird die Auflösung des Eingabebilds (des gerenderten Texts) angepasst, indem ein größerer size= -Wert ausgewählt wird und gleichzeitig die mit `textAttr=`.

*`resOptions`* ermöglicht die Auswahl eines alternativen Resampling-Algorithmus. Die folgenden Werte werden unterstützt (Groß-/Kleinschreibung muss beachtet werden):

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
   <td> <p> Super-Sampling mit verstellbarem Jitter (<span class="varname"> n</span> muss ein ganzzahliger Wert zwischen 0 und 200 sein.) </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-818e57df0a1b4449888543bc6af77751}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Wird von Effektebenen ignoriert.

`res=` wird immer ignoriert, wenn die Perspektive in derselben Ebene vorhanden ist. `size=` wird ignoriert, wenn für Bildebenen angegeben. `size=` und `res=` in Ebenen mit `perspective=` sind für die zukünftige Verwendung reserviert.

## Standard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, für keine perspektivische Umwandlung.

## Verwandte Themen {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
