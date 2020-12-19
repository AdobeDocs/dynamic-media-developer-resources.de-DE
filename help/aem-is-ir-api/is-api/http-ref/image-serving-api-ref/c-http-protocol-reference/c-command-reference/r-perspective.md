---
description: Perspektivische Transformation. Wenden Sie eine perspektivische Transformation auf das Ebenenquellenbild an, um den festgelegten Bereich mit dem quadrilateralen zu füllen. Andere Bereiche der Ebene bleiben transparent.
seo-description: Perspektivische Transformation. Wenden Sie eine perspektivische Transformation auf das Ebenenquellenbild an, um den festgelegten Bereich mit dem quadrilateralen zu füllen. Andere Bereiche der Ebene bleiben transparent.
seo-title: Perspektive
solution: Experience Manager
title: Perspektive
topic: Scene7 Image Serving - Image Rendering API
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 2%

---


# perspektive{#perspective}

Perspektivische Transformation. Wenden Sie eine perspektivische Transformation auf das Ebenenquellenbild an, um den festgelegten Bereich mit dem quadrilateralen zu füllen. Andere Bereiche der Ebene bleiben transparent.

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Perspektive quadrilaterale Pixelkoordinaten (8 Real, durch Kommas getrennt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Perspektive quadrilaterale normalisierte Koordinaten (8 Real, getrennt durch Kommas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Resamplingoptionen (siehe unten). </p></td> 
 </tr> 
</table>

*`perspQuad`* besteht aus vier Pixel-Koordinatenwerten im Koordinatenraum der Composite-Ebene (oder Ebene 0), der in der oberen linken Ecke des Composite-Bildes entsteht.

`perspQuadN` besteht aus vier normalisierten Koordinatenwerten, wobei die obere linke Ecke des Composite/Ebene 0-Bilds und  `0.0,0.0` die untere rechte Ecke  `1.0,1.0` übereinstimmen.

Das Eingabebild wird so transformiert, dass die obere linke Ecke des Eingabebilds dem ersten Koordinatenwert von `perspQuad[N]`, die obere rechte Ecke der zweiten Koordinate, die untere rechte Ecke der dritten Koordinate und die untere linke Ecke der vierten Koordinate zugeordnet wird.

>[!NOTE]
>
>`pos=` kann verwendet werden, um die transformierte Ebene im Composite-Bild weiter zu positionieren.

Die perspektivischen quadrilateralen Koordinaten können sich außerhalb des Composite-Bilds befinden.

Verhalten ist nicht definiert, wenn das Quadrilaterale nicht für eine perspektivische Transformation geeignet ist (z. B. wenn zwei oder mehr Scheitelpunkte zusammenfallen, wenn sich drei oder alle Scheitelpunkte auf derselben Linie befinden oder wenn das Quadrilaterale sich selbst schneidet oder konkav ist).

## Qualitätserwägungen {#section-7cc9056afa614300a9b8844d39739fc3}

Während die Standardimplementierung einen vernünftigen Kompromiss zwischen Qualität und Leistung ergibt, kann es manchmal notwendig sein, die Auflösung des Quellbilds zu erhöhen, um die Schärfe zu verbessern oder um es zu reduzieren, um Aliasing-Artefakte zu reduzieren.

Wenn es sich bei der Quelle um ein Bild handelt, verwenden Sie `scale=`, um eine andere Auflösung (relativ zur vollständigen Auflösung des Bilds) auszuwählen. Der angegebene `scale=`-Wert wird auf die nächsthöhere PTIF-Auflösungsebene gerundet. Bei verschachtelten Anforderungsquellen kann die Größe des von der verschachtelten Anforderung erzeugten Bildes angepasst werden, um die gewünschte Schärfe zu erzielen. Bei Textebenen wird die Auflösung des Eingabebilds (des gerenderten Textes) angepasst, indem ein Wert größer size= ausgewählt wird und gleichzeitig die mit `textAttr=` angegebene Auflösung erhöht wird.

*`resOptions`* ermöglicht die Auswahl eines alternativen Resampling-Algorithmus. Die folgenden Werte werden unterstützt (Groß-/Kleinschreibung beachten):

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
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> Super-Sampling mit anpassbarem Jitter (<span class="varname"> n</span> muss ein ganzzahliger Wert zwischen 0 und 200 sein). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-818e57df0a1b4449888543bc6af77751}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Von Effektebenen ignoriert.

`res=` wird immer ignoriert, wenn die Perspektive in derselben Ebene vorhanden ist. `size=` wird ignoriert, wenn für Bildebenen angegeben. `size=` und  `res=` in Ebenen mit  `perspective=` sind für die zukünftige Verwendung reserviert.

## Standard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, für keine perspektivische Transformation.

## Verwandte Themen {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
