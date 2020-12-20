---
description: Ebenenschatten- und Schein-Effekte im Photoshop-Stil werden mithilfe spezieller Unterebenen (Effektebenen) implementiert, die an jede Ebene (die übergeordnete Ebene), einschließlich layer=0 und layer=comp, angehängt werden können.
seo-description: Ebenenschatten- und Schein-Effekte im Photoshop-Stil werden mithilfe spezieller Unterebenen (Effektebenen) implementiert, die an jede Ebene (die übergeordnete Ebene), einschließlich layer=0 und layer=comp, angehängt werden können.
seo-title: Ebeneneffekte
solution: Experience Manager
title: Ebeneneffekte
topic: Scene7 Image Serving - Image Rendering API
uuid: 076e98de-cbbb-457b-984a-367a935b4356
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 2%

---


# Ebeneneffekte{#layer-effects}

Ebenenschatten- und Schein-Effekte im Photoshop-Stil werden mithilfe spezieller Unterebenen (Effektebenen) implementiert, die an jede Ebene (die übergeordnete Ebene), einschließlich layer=0 und layer=comp, angehängt werden können.

Obwohl Effektebenen eine Reihe von standardmäßigen Bild- und Ebenenattributen und Befehlen unterstützen, sind sie nicht als allgemeine Zielebenen gedacht und unterstützen keine unabhängigen Bild- oder Textdaten.

An eine einzelne übergeordnete Ebene können beliebig viele Ebeneneffekte angehängt werden.

## Innere und äußere Effekte {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Innere* Effekte werden über der übergeordneten Ebene gerendert und sind nur in undurchsichtigen Bereichen der übergeordneten Ebene sichtbar. *Äußere* Effekte werden hinter der übergeordneten Ebene gerendert (sodass sie nicht in undurchsichtigen Bereichen der übergeordneten Ebene sichtbar sind) und können an einer beliebigen Stelle in der Arbeitsfläche des Zusammenstellens positioniert werden. Ein innerer oder äußerer Effekt wird durch Zuweisen einer Positiv- oder Negativ-Effekt-Ebenenzahl mit dem Befehl `effect=` ausgewählt. Der Befehl `effect=` steuert auch die z-Reihenfolge zwischen mehreren Effektebenen, die an derselben übergeordneten Ebene befestigt sind.

## Verhältnis zur übergeordneten Ebene {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Die Effektebenen werden automatisch angepasst und so positioniert, dass sie mit der übergeordneten Ebene zusammenfallen (d. h. die Effektebene übernimmt die Werte `size=` und `origin=` der übergeordneten Ebene). `pos=` kann verwendet werden, um die Effektebene von der übergeordneten Ebene weg zu verschieben, wie es normalerweise für Schlagschatten- und Innenschatteneffekte erforderlich ist. Bei Standardebenen gibt `pos=` einen Offset zwischen den Herkünfte dieser Ebene und Ebene 0 an, bei Effektebenen `pos=` den Offset zwischen den Herkünfte der Effektebene und der übergeordneten Ebene.

## Unterstützte Befehle und Attribute {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Für Effektebenen gelten die folgenden Befehle und Attribute:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Alle anderen Bild- und Ebenenbefehle, die in Effektebenen enthalten sind, werden ignoriert.

## Standardeffektmakros {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Um die Verwendung von Ebeneneffekten zu erleichtern, stellt IS zwei Makros mit dem Standardbildkatalog zur Verfügung: `$shadow$` und `$glow$`, die Standardwerte für Effekt-Ebenenattribute bereitstellen, die den Photoshop-Ebeneneffekten ähnlich sind. Die folgenden Listen, die den Effekt-Befehl und das Makro enthalten, sollten zur Implementierung der Standardebene-Effekte verwendet werden. Natürlich können alle in den Makros angegebenen Attribute in der URL geändert werden oder alternative Makros zur Implementierung benutzerdefinierter Ebeneneffekte erstellt werden.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Gewünschter Effekt</b> </th> 
   <th class="entry"> <b> Befehl</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Schlagschatten </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schatten nach innen </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schein nach außen </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schein nach innen </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-4c449fdf707b43858917fb271fa1fe96}

hinzufügen einer Ebene mit einer Deckkraft von 50 % einen roten Rand von drei Pixeln:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Der Rahmen folgt den Konturen des Alpha-Kanals oder der Maske des Bilds. Durch das Festlegen von `effect=1` wird der Rand stattdessen an der Innenseite platziert.

hinzufügen Sie einem Bild einen blauen Schlagschatten unter Verwendung der Standardeinstellungen für den Effekt (mit Ausnahme der Farbe):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` fügt am unteren rechten Rand des Bilds einen kleinen Rand hinzu, wodurch verhindert wird, dass der Schlagschatten an die Bildgrenzen geklickt wird.

## Verwandte Themen {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135),  [Befehlsmakros%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
