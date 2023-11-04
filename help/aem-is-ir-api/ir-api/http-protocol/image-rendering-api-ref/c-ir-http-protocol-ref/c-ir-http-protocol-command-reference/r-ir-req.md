---
title: req
description: Anfragetyp. Gibt den Typ der angeforderten Daten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 4%

---

# req{#req}

Anfragetyp. Gibt den Typ der angeforderten Daten an.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug </span> </p> </td> 
  <td class="stentry"> <p>Führen Sie Befehle im Debug-Modus aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Inhalt </span> </p> </td> 
  <td class="stentry"> <p>Gibt Informationen zu den Objekten in der Vignette zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Führen Sie Befehle aus und geben Sie das gerenderte Bild zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>Gibt Eigenschaften der angegebenen Vignette zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Karte </span> </p> </td> 
  <td class="stentry"> <p>Gibt in die Vignette eingebettete Imagemap-Daten zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Objekt </span> </p> </td> 
  <td class="stentry"> <p>Führen Sie Befehle aus und geben Sie das gerenderte Bild, das der aktuellen Objektauswahl maskiert ist, zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Führen Sie Befehle aus und geben Sie Eigenschaften des Antwortbilds zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata </span> </p> </td> 
  <td class="stentry"> <p>Gibt den Inhalt von aus <span class="codeph"> vignette::UserData </span>. </p> </td> 
 </tr> 
</table>

Sofern in den detaillierten Beschreibungen nichts anderes angegeben ist, gibt der Server Textantworten mit dem MIME-Typ zurück &lt;text plain=&quot;&quot;>.

`debug`

Führt die angegebenen Befehle aus und gibt das gerenderte Bild zurück. Wenn ein Fehler auftritt, werden Fehlerinformationen und Debugging-Informationen anstelle des Fehlerbilds ( `attribute::ErrorImagePath`).

`contents`

Gibt eine XML-Darstellung der Objekthierarchie in der Vignette zurück, einschließlich ausgewählter Objektattribute. Andere Befehle in der Anfrage werden ignoriert.

`img`

Führt die angegebenen Befehle aus und gibt das gerenderte Bild zurück. Das Antwortdatenformat und der Antworttyp werden durch `fmt=`.

`imageprops`

Gibt ausgewählte Eigenschaften der Vignettendatei oder des Katalogeintrags zurück, die bzw. der im URL-Pfad angegeben ist. Siehe [Eigenschaften](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) für eine Beschreibung der Antwortsyntax und des MIME-Typs der Antwort. Andere Befehle in der Anfrage werden ignoriert. Die folgenden Eigenschaften werden zurückgegeben:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Double </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration </span> oder die standardmäßige Live-Zeit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Höhe mit voller Auflösung in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p>Name/Beschreibung des mit dieser Vignette verknüpften Profils. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Boolesch </p> </td> 
   <td colname="col3"> <p>1, wenn das verknüpfte Profil in die Vignette eingebettet ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded FotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>Boolesch </p> </td> 
   <td colname="col3"> <p>1, wenn die Vignette Pfaddaten einbettet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier </span> oder leer, wenn kein Katalogeintrag angegeben ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Pixeltyp des Antwortbilds; kann "CMYK", "RGB"oder "BW"sein (bei Graustufenbildern). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Standardmäßige Druckauflösung in dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p>Änderungsdatum/-uhrzeit (von <span class="codeph"> catalog::TimeStamp </span> oder der Vignettendatei). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Breite mit voller Auflösung in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p>Vignettenname (Name des Wurzel-Vignettenobjekts). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Maximale Objektauflösung in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösung </a> Einheiten (normalerweise Pixel/Zoll). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Durchschnittliche Objektauflösung in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösung </a> Einheiten (normalerweise Pixel/Inc) <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösung </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Minimale Objektauflösung in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösung </a> Einheiten (normalerweise Pixel/Zoll). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Versionsnummer der Vignette-Datei. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Gibt in der Vignette enthaltene Imagemap-Daten zurück. Standardmäßig werden die Zuordnungsdaten für alle äußersten Gruppen zurückgegeben. Die Zuordnungsdaten für alle innersten Gruppen können mit

`req=map&groupLevel=-1`

Die Zuordnungsdaten werden nicht auf `wid=` oder `hei=` oder anderweitig geändert. Der MIME-Typ der Antwort lautet `<text/xml>`.

Die Antwortdaten bestehen aus einer `<map>` -Element, das einen Satz von `<area>` -Elemente ähnlich der HTML `<AREA>` -Tag.

Jeder `<area>` -Element enthält den Standard `type=` und `coord=` -Attributen und einer `name=` -Attribut, das den Vignettengruppennamen oder Namenspfad angibt. Mehrere `<area>` -Elemente mit demselben Namen sind vorhanden, wenn die Masken der entsprechenden Objektgruppe unterschiedliche Bereiche aufweisen.

Zusätzlich zu den Standardattributen können Vignetten zusätzliche Attribute definieren, sofern dies der Fall ist. Solche benutzerdefinierten Attribute werden als Objektgruppenattribute definiert. Die Namen benutzerdefinierter Attribute müssen mit `map` in der `<area>` -Elemente. Beispiel: Wenn die Gruppenattribute `map.href=http://www.scene7.com`, der entsprechenden `<area>` Element enthält `href="http://www.scene7.com"`.

Ein XML-Dokument mit einem leeren `<map>` -Element zurückgegeben, wenn die Vignette keine Zuordnungsdaten enthält.

`object`

Führt die angegebenen Befehle aus und gibt das gerenderte Bild zurück, das durch die Restobjektauswahl maskiert wurde (die Gruppe oder das Objekt, die bzw. das mit der letzten ausgewählt wurde) `sel=` oder `obj=` -Befehl in der -Anfrage). Wird normalerweise mit einem Bildformat verwendet, das Alpha unterstützt (siehe [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Wenn ein Bildformat verwendet wird, das Alpha nicht unterstützt, sind die Bereiche außerhalb der Maske schwarz.

`props`

Führt die angegebenen Befehle aus und gibt Vignetteneigenschaften sowie Gruppen- oder Objekteigenschaften zurück, anstatt das gerenderte Bild. Siehe [Eigenschaften](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) für eine Beschreibung der Antwortsyntax und des MIME-Antworttyps. Die Standardauswahl gilt, sofern `obj=` oder `sel=` wird ebenfalls angegeben (siehe [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

Die Antwort kann die folgenden Eigenschaften enthalten:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Eigenschaft </p> </th> 
   <th class="entry"> <p> Typ </p> </th> 
   <th class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Hintergrundfarbe des Antwortbilds. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Integer </p> </td> 
   <td> <p> Antwortbildhöhe in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Boolesch </p> </td> 
   <td> <p>True , wenn das ICC-Profil in das Antwortbild eingebettet ist (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Verknüpfungsname des mit dem Antwortbild verknüpften Profils (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Boolesch </p> </td> 
   <td> <p> True , wenn das Antwortbild Alpha enthält. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Boolesch </p> </td> 
   <td> <p> True , wenn das Antwortbild Pfaddaten enthält (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Typ des Antwortbilds, kann "CMYK", "RGB"oder "BW"sein (für Graustufenbilder) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Druckauflösung (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Ganzzahl, boolesch </p> </td> 
   <td> <p> JPEG-Qualität und Chroma-Markierung (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> MIME-Typ für das Antwortbild (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Antwortbildbreite in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Attributzeichenfolge für die aktuelle Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Anzahl der Objekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Einzugswert der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Vollständiger Namenspfad der aktuellen Objektauswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.überlappend </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Anzahl der überlappenden Objekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p>Anzahl der renderbaren Objekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Anzahl der texturierbaren Objekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Aktueller Ein-/Ausblendestatus der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> z-order-Wert des ersten überlappenden Objekts in der aktuellen Auswahl. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Gibt den Inhalt von aus `vignette::UserData`. Der Server ersetzt alle Vorkommen von `'??'` in `vignette::UserData` mit Zeilenenden ( `<cr><lf>`). Die Antwort wird als Textdaten formatiert, wobei der MIME-Antworttyp auf &lt;text plain=&quot;&quot;>.

Wenn das im URL-Pfad angegebene Objekt nicht in einen gültigen Vignettenzuordnungs-Eintrag aufgelöst wird oder wenn die Variable `vignette::UserData` leer ist, enthält die Antwort nur einen Zeilenende-Zeichen ( `CR/LF`).

Alle anderen Befehle in der Anforderungszeichenfolge werden ignoriert.

## Eigenschaften {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Anforderungsbefehl. Kann an einer beliebigen Stelle in der Anforderungszeichenfolge auftreten.

## Standard {#section-00c593cbf1af4364b6b78812e6b93c64}

Wenn die URL keinen Bildpfad oder keine Modifikatoren enthält, dann:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Andernfalls `req=img`

## Verwandte Themen {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Eigenschaften](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
