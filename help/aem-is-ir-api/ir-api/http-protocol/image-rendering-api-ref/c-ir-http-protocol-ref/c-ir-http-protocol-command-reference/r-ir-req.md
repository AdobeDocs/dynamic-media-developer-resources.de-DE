---
title: Erf
description: Anfragetyp. Gibt den Typ der angeforderten Daten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 3%

---

# Erf{#req}

Anfragetyp. Gibt den Typ der angeforderten Daten an.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">-</span> </p> </td> 
  <td class="stentry"> <p>Führen Sie Befehle im Debugging-Modus aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">-</span> </p> </td> 
  <td class="stentry"> <p>Gibt Informationen zu den Objekten in der Vignette zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Führt Befehle aus und gibt das gerenderte Bild zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ImageProps-</span> </p> </td> 
  <td class="stentry"> <p>Gibt die Eigenschaften der angegebenen Vignette zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Gibt die in die Vignette eingebetteten Imagemap-Daten zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">-</span> </p> </td> 
  <td class="stentry"> <p>Führt Befehle aus und gibt das gerenderte Bild, das maskiert ist, an die aktuelle Objektauswahl zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Props </span> </p> </td> 
  <td class="stentry"> <p>Führt Befehle aus und gibt Eigenschaften des Antwortbildes zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> UserData-</span> </p> </td> 
  <td class="stentry"> <p>Gibt den Inhalt <span class="codeph"> Vignette::UserData-</span> zurück. </p> </td> 
 </tr> 
</table>

Sofern in den detaillierten Beschreibungen nicht anders angegeben, gibt der Server Textantworten mit dem MIME-Typ &lt;text/plain> zurück.

`debug`

Führt die angegebenen Befehle aus und gibt das gerenderte Bild zurück. Wenn ein Fehler auftritt, werden Fehler- und Debuginformationen anstelle des Fehlerbilds ( `attribute::ErrorImagePath`) zurückgegeben.

`contents`

Gibt eine XML-Darstellung der Objekthierarchie in der Vignette zurück, einschließlich ausgewählter Objektattribute. Andere Befehle in der Anfrage werden ignoriert.

`img`

Führt die angegebenen Befehle aus und gibt das gerenderte Bild zurück. Das Format der Antwortdaten und der Antworttyp werden durch `fmt=` bestimmt.

`imageprops`

Gibt ausgewählte Eigenschaften der Vignettendatei oder des Katalogeintrags zurück, die im URL-Pfad angegeben sind. Unter [Eigenschaften](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) finden Sie eine Beschreibung der Antwortsyntax und des MIME-Typs der Antwort. Andere Befehle in der Anfrage werden ignoriert. Die folgenden Eigenschaften werden zurückgegeben:

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
   <td colname="col3"> <p> <span class="codeph">::Expiration </span> oder die Standardlebensdauer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Höhe in voller Auflösung in Pixeln. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile-</span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p>Name/Beschreibung des mit dieser Vignette verknüpften Profils. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile-</span> </p> </td> 
   <td colname="col2"> <p>Boolesch </p> </td> 
   <td colname="col3"> <p>1 , wenn das zugehörige Profil in die Vignette eingebettet ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded FotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>Boolesch </p> </td> 
   <td colname="col3"> <p>1 Wenn die Vignette Pfaddaten einbettet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier-</span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p> <span class="codeph">::Modifier </span> oder leer, wenn es sich nicht um einen Katalogeintrag handelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td colname="col2"> <p>Aufzählung </p> </td> 
   <td colname="col3"> <p>Pixeltyp des Antwortbildes. Kann „CMYK“, "RGB" oder „BW“ (für Graustufenbilder) sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes-</span> </p> </td> 
   <td colname="col2"> <p>Reell </p> </td> 
   <td colname="col3"> <p>Standardmäßige Druckauflösung in dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp-</span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p>Änderungsdatum/-uhrzeit (aus <span class="codeph"> Katalog::TimeStamp </span> oder der Vignettendatei). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Breite in voller Auflösung in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>Zeichenfolge </p> </td> 
   <td colname="col3"> <p>Name der Vignette (Namenszeichenfolge des Stamm-Vignettenobjekts) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Reell </p> </td> 
   <td colname="col3"> <p>Maximale Objektauflösung in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösungs-</a> (normalerweise Pixel/Zoll). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Reell </p> </td> 
   <td colname="col3"> <p>Durchschnittliche Objektauflösung in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösungs-</a> (typischerweise Pixel/<a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösung </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Reell </p> </td> 
   <td colname="col3"> <p>Minimale Objektauflösung in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> Materialauflösungs-</a> (normalerweise Pixel/Zoll). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Versionsnummer der Vignettendatei. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Gibt die in der Vignette enthaltenen Imagemap-Daten zurück. Standardmäßig werden die Zuordnungsdaten für alle äußersten Gruppen zurückgegeben. Die Kartendaten für alle innersten Gruppen können abgerufen werden mit

`req=map&groupLevel=-1`

Die Zuordnungsdaten werden nicht auf `wid=` oder `hei=` skaliert oder anderweitig geändert. Der Antwort-MIME-Typ ist `<text/xml>`.

Die Antwortdaten bestehen aus einem `<map>`, das eine Reihe von `<area>` enthält, ähnlich dem HTML-`<AREA>`-Tag.

Jedes `<area>`-Element enthält die standardmäßigen `type=`- und `coord=`-Attribute sowie ein `name=`-Attribut, das den Namen der Vignettengruppe oder den Namenspfad angibt. Mehrere `<area>` mit demselben Namen sind vorhanden, wenn die Masken der entsprechenden Objektgruppe unterbrochene Bereiche aufweisen.

Zusätzlich zu den Standardattributen können Vignetten bei Bedarf zusätzliche Attribute definieren. Solche benutzerdefinierten Attribute werden als Objektgruppenattribute definiert. Die Namen von benutzerdefinierten Attributen müssen mit `map` beginnen, damit sie in die `<area>` Elemente aufgenommen werden können. Wenn die Gruppenattribute beispielsweise `map.href=http://www.scene7.com` enthalten, enthält das entsprechende `<area>`-Element `href="http://www.scene7.com"`.

Ein XML-Dokument mit einem leeren `<map>` wird zurückgegeben, wenn die Vignette keine Zuordnungsdaten enthält.

`object`

Führt die angegebenen Befehle aus und gibt das gerenderte Bild zurück, das durch die Auswahl des Restobjekts maskiert ist (die Gruppe oder das Objekt, die bzw. das mit dem letzten `sel=`- oder `obj=`-Befehl in der Anfrage ausgewählt wurde). Wird normalerweise mit einem Bildformat verwendet, das Alpha unterstützt (siehe [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Wenn ein Bildformat verwendet wird, das Alpha nicht unterstützt, sind die Bereiche außerhalb der Maske schwarz.

`props`

Führt die angegebenen Befehle aus und gibt Vignetteneigenschaften und Gruppen- oder Objekteigenschaften anstelle des gerenderten Bildes zurück. Unter [Eigenschaften](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) finden Sie eine Beschreibung der Antwortsyntax und des MIME-Typs der Antwort. Die Standardauswahl gilt, sofern nicht auch `obj=` oder `sel=` angegeben ist (siehe [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

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
   <td> <p> Hintergrundfarbe des Antwortbildes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Integer </p> </td> 
   <td> <p> Höhe des Antwortbildes in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed-</span> </p> </td> 
   <td> <p> Boolesch </p> </td> 
   <td> <p>True, wenn das ICC-Profil in das Antwortbild eingebettet ist (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile-</span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Verknüpfungsname des Profils, das dem Antwortbild zugeordnet ist (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Boolesch </p> </td> 
   <td> <p> True, wenn das Antwortbild Alpha enthält. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed-</span> </p> </td> 
   <td> <p> Boolesch </p> </td> 
   <td> <p> True, wenn das Antwortbild Pfaddaten enthält (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Typ des Antwortbildes, kann 'CMYK', 'RGB' oder 'BW' (für Graustufenbilder) sein </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes-</span> </p> </td> 
   <td> <p> Reell </p> </td> 
   <td> <p> Druckauflösung (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Ganze Zahl, boolesch </p> </td> 
   <td> <p> JPEG-Qualität und Chroma-Flag (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> MIME-Typ des Antwortbildes (siehe <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Breite des Antwortbildes in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.attributes </span> </p> </td> 
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
   <td> <p> Wert der aktuellen Auswahl einrücken. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> Zeichenfolge </p> </td> 
   <td> <p> Vollständiger Namenspfad der aktuellen Objektauswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlap </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Anzahl der Überschneidungsobjekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p>Anzahl der renderfähigen Objekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Anzahl der texturierbaren Objekte in der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.visible </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Aktueller Einblenden-/Ausblenden-Status der aktuellen Auswahl. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder-</span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Z-Reihenfolgenwert des ersten Überschneidungsobjekts in der aktuellen Auswahl. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Gibt den Inhalt von `vignette::UserData` zurück. Der Server ersetzt alle Vorkommen von `'??'` in `vignette::UserData` durch Zeilenabschlüsse ( `<cr><lf>`). Die Antwort ist als Textdaten formatiert, wobei der MIME-Typ der Antwort auf &lt;text/plain> festgelegt ist.

Wenn das im URL-Pfad angegebene Objekt nicht in einen gültigen Vignettenzuordnungseintrag aufgelöst wird oder der `vignette::UserData` leer ist, enthält die Antwort nur einen Zeilenabschluss ( `CR/LF`).

Alle anderen Befehle in der Anfragezeichenfolge werden ignoriert.

## Eigenschaften {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Befehl anfordern. Kann an beliebiger Stelle in der Anfragezeichenfolge auftreten.

## Standard {#section-00c593cbf1af4364b6b78812e6b93c64}

Wenn die URL keinen Bildpfad oder keine Modifikatoren enthält, gehen Sie wie folgt vor:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Andernfalls `req=img`

## Verwandte Themen {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
