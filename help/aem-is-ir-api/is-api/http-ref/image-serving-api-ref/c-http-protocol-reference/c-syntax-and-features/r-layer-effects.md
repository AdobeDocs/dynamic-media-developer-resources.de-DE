---
title: Ebeneneffekte
description: Ebenenschatten- und Glüheffekte im Photoshop-Stil werden mithilfe spezieller Unterschichten (Effektebenen) implementiert, die mit jeder Ebene (der übergeordneten Ebene) verbunden werden können, einschließlich Ebene=0 und Ebene=Komp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# Ebeneneffekte{#layer-effects}

Ebenenschatten- und Glüheffekte im Photoshop-Stil werden mithilfe spezieller Unterschichten (Effektebenen) implementiert, die mit jeder Ebene (der übergeordneten Ebene) verbunden werden können, einschließlich Ebene=0 und Ebene=Komp.

Effektebenen unterstützen zwar eine Reihe von standardmäßigen Bild- und Ebenenattributen und -befehlen, sie sind jedoch nicht als Allzweck-Ebenen gedacht und unterstützen keine unabhängigen Bild- oder Textdaten.

Einer übergeordneten Ebene können beliebig viele Ebeneneffekte zugeordnet werden.

## Innere und äußere Effekte {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Innere Effekte* werden über der übergeordneten Ebene gerendert und sind nur in deckenden Bereichen der übergeordneten Ebene sichtbar. *Äußere Effekte* werden hinter der übergeordneten Ebene gerendert (sodass sie nie in deckenden Bereichen der übergeordneten Ebene sichtbar sind) und können an einer beliebigen Stelle auf der Arbeitsfläche für das Zusammensetzen positioniert werden. Ein innerer oder äußerer Effekt wird durch Zuweisen einer positiven oder negativen Effektschichtnummer mit dem Befehl `effect=` ausgewählt. Mit dem Befehl `effect=` wird auch die z-Reihenfolge zwischen mehreren Effektebenen gesteuert, die mit derselben übergeordneten Ebene verbunden sind.

## Beziehung zur übergeordneten Ebene {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Effektebenen werden automatisch so dimensioniert und positioniert, dass sie mit der übergeordneten Ebene übereinstimmen (d. h. die Effektebene übernimmt die `size=`- und `origin=` der übergeordneten Ebene). `pos=` kann verwendet werden, um die Effektebene von der übergeordneten Ebene weg zu verschieben, wie es für Dropdown- und innere Schatteneffekte typischerweise erforderlich ist. Während `pos=` für Standardschichten einen Versatz zwischen den Ursprüngen dieser Ebene und der Ebene 0 angibt, gibt `pos=` für Effektebenen den Versatz zwischen den Ursprüngen der Effektebene und der übergeordneten Ebene an.

## Unterstützte Befehle und Attribute {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Effektebenen akzeptieren die folgenden Befehle und Attribute:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Alle anderen Bild- und Ebenenbefehle, die in den Effektebenen enthalten sind, werden ignoriert.

## Makros für Standardeffekte {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Um die Verwendung von Ebeneneffekten zu vereinfachen, stellt IS zwei Makros mit dem Standardbildkatalog, `$shadow$` und `$glow$`, bereit, die Standardwerte für Effektebenenattribute bereitstellen, die Photoshop-Ebeneneffekten ähnlich sind. In der folgenden Tabelle ist aufgeführt, mit welchen Effektbefehlen und Makros die Standardeffekte implementiert werden sollen. Natürlich können alle in den Makros angegebenen Attribute in der URL geändert werden, oder es können alternative Makros erstellt werden, um benutzerdefinierte Ebeneneffekte zu implementieren.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> erwünschter Effekt</b> </th> 
   <th class="entry"> <b> Befehl</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Schlagschatten </p> </td> 
   <td> <p> <span class="codeph">-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schatten nach innen </p> </td> 
   <td> <p> <span class="codeph"> = 1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schein nach außen </p> </td> 
   <td> <p> <span class="codeph"> Effekt=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schein nach innen </p> </td> 
   <td> <p> <span class="codeph">-Effekt = 1&amp;$Glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-4c449fdf707b43858917fb271fa1fe96}

Fügen Sie einer Ebene einen drei Pixel breiten, roten Rahmen mit 50 % Deckkraft hinzu:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Der Rahmen folgt den Konturen des Alphakanals oder der Maske des Bildes. Durch Festlegen von `effect=1` wird der Rahmen stattdessen an der inneren Kante platziert.

Fügen Sie einem Bild einen bläulichen Schlagschatten hinzu, indem Sie die Standardeffekteinstellungen verwenden (mit Ausnahme der Farbe):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` fügt den unteren rechten Kanten des Bildes einen kleinen Rand hinzu, um zu verhindern, dass der Schlagschatten an den Bildgrenzen abgeschnitten wird.

## Verwandte Themen {#section-1acccccf534549aea23d4c008c17e7c0}

[EFFECT=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Befehlsmakros%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
