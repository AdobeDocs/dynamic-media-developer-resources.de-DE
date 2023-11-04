---
title: Ebeneneffekte
description: Ebenenschatten und Glüheffekte im Photoshop-Stil werden mithilfe spezieller Unterschichten (Effektschichten) implementiert, die an jede Ebene (die übergeordnete Ebene) angehängt werden können, einschließlich layer=0 und layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 2%

---

# Ebeneneffekte{#layer-effects}

Ebenenschatten und Glüheffekte im Photoshop-Stil werden mithilfe spezieller Unterschichten (Effektschichten) implementiert, die an jede Ebene (die übergeordnete Ebene) angehängt werden können, einschließlich layer=0 und layer=comp.

Obwohl Effektebenen eine Reihe von standardmäßigen Bild- und Ebenenattributen und -befehlen unterstützen, sind sie nicht für allgemeine Zielschichten vorgesehen und unterstützen keine unabhängigen Bild- oder Textdaten.

Eine beliebige Anzahl von Ebeneneffekten kann an eine einzelne übergeordnete Ebene angehängt werden.

## Innen- und Außenwirkung {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Innere Effekte* werden über der übergeordneten Ebene gerendert und sind nur in undurchsichtigen Bereichen der übergeordneten Ebene sichtbar. *Nebenwirkungen* werden hinter der übergeordneten Ebene gerendert (sodass sie in undurchsichtigen Bereichen der übergeordneten Ebene nicht sichtbar sind) und können an einer beliebigen Stelle auf der Arbeitsfläche der Komposition positioniert werden. Ein innerer oder äußere Effekt wird durch Zuweisung einer Positiv- oder Negativ-Effektschichtnummer mit der `effect=` Befehl. Die `effect=` -Befehl steuert auch die z-Reihenfolge zwischen mehreren Effektebenen, die an dieselbe übergeordnete Ebene angehängt sind.

## Beziehung zur übergeordneten Ebene {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Die Effektebenen werden automatisch skaliert und so positioniert, dass sie mit der übergeordneten Ebene zusammenfallen (d. h. die Effektebene erbt die `size=` und `origin=` -Werte der übergeordneten Ebene). `pos=` kann verwendet werden, um die Effektebene von der übergeordneten Ebene weg zu verschieben, wie dies für Ablegen- und Innenhungseffekte normalerweise erforderlich ist. Für Standardschichten `pos=` gibt für Effektebenen einen Offset zwischen den Ursprüngen dieser Ebene und Ebene 0 an `pos=` gibt den Versatz zwischen den Ursprüngen der Effektebene und der übergeordneten Ebene an.

## Unterstützte Befehle und Attribute {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Die Effektebenen akzeptieren die folgenden Befehle und Attribute:

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

Um die Verwendung von Ebeneneffekten zu erleichtern, stellt IS zwei Makros mit dem standardmäßigen Bildkatalog bereit: `$shadow$` und `$glow$`, die Standardwerte für Effekt-Layer-Attribute bereitstellen, die Photoshop-Ebeneneffekten ähnlich sind. In der folgenden Tabelle ist aufgeführt, welcher Effektbefehl und welches Makro zur Implementierung der standardmäßigen Ebeneneffekte verwendet werden sollen. Natürlich kann jedes der in den Makros angegebenen Attribute in der URL geändert werden, oder es können alternative Makros erstellt werden, um benutzerdefinierte Ebeneneffekte zu implementieren.

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
   <td> <p> <span class="codeph"> Effect=-1&amp;$Shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schatten nach innen </p> </td> 
   <td> <p> <span class="codeph"> Effect=1&amp;$Shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schein nach außen </p> </td> 
   <td> <p> <span class="codeph"> Effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Schein nach innen </p> </td> 
   <td> <p> <span class="codeph"> Effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-4c449fdf707b43858917fb271fa1fe96}

Fügen Sie einer Ebene einen drei Pixel breiten roten Rahmen mit einer Deckkraft von 50 % hinzu:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Der Rahmen folgt den Konturen des Alphakanals oder der Maske des Bildes. Einstellung `effect=1` den Rahmen stattdessen an der Innenseite platzieren.

Fügen Sie einem Bild einen blauen Schlagschatten hinzu, indem Sie die Standardeinstellungen für den Effekt verwenden (mit Ausnahme der Farbe):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` fügt einen kleinen Rand zu den unteren rechten Kanten des Bildes hinzu, wodurch verhindert wird, dass der Schlagschatten an die Bildgrenzen geklickt wird.

## Verwandte Themen {#section-1acccccf534549aea23d4c008c17e7c0}

[Effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Befehlsmakros%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
