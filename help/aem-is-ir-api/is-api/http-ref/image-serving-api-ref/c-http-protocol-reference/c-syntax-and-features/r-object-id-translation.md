---
description: Image Serving bietet einen Mechanismus zum Übersetzen externer Objekt-IDs in Gebietsschema-spezifische Objekt-IDs (Katalog). Die primäre Anwendung dient der Bereitstellung von gebietsschemaspezifischen Inhalten und Inhalten, die von mehreren Gebietsschemas gemeinsam genutzt werden, ohne dass die Client-Anwendung die gebietsschemaspezifischen Objekt-IDs kennen muss.
solution: Experience Manager
title: Objekt-ID-Übersetzung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# Objekt-ID-Übersetzung{#object-id-translation}

Image Serving bietet einen Mechanismus zum Übersetzen externer Objekt-IDs in Gebietsschema-spezifische Objekt-IDs (Katalog). Die primäre Anwendung dient der Bereitstellung von gebietsschemaspezifischen Inhalten und Inhalten, die von mehreren Gebietsschemas gemeinsam genutzt werden, ohne dass die Client-Anwendung die gebietsschemaspezifischen Objekt-IDs kennen muss.

Die Anwendung kann nur mit globalen Objekt-IDs geschrieben werden, und Image Serving ersetzt automatisch gebietsschemaspezifische Bilder und andere Inhalte, sofern verfügbar.

Die *`locale`* wird in Image Serving-Anfragen mit der `locale=` Befehl.

>[!NOTE]
>
>Die Übersetzung der Objekt-ID gilt nur für die katalogbasierte Verwendung von Image Serving. Dateinamen können nicht übersetzt werden.

## Anwendungsbereich {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Alle Verweise auf Einträge in Bild-, SVG- und statischen Inhaltskatalogen werden für Übersetzungs-Schriftarten berücksichtigt und ICC-Profilverweise werden nicht übersetzt. Zusätzlich zu den *`object`* im Pfad von [!DNL /is/image] und [!DNL /is/static requests], unterliegen diese Befehle und Katalogattribute der ID-Übersetzung: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, und `attribute::Watermark`.

## ID-Übersetzungszuordnung {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` definiert die Regeln, die vom Server zur Bestimmung der ID des lokalisierten Inhalts verwendet werden, wobei die generische Objekt-ID und die `locale=` -Wert.

`attribute::LocaleMap` besteht aus einer Liste von Eingaben *locales* (entspricht den Werten, die mit `locale=`), jeweils mit keinem oder mehr Gebietsschema-Suffixen ( `*`locSuffixes`*`).

Beispiel: `attribute::LocaleMap` könnte wie folgt aussehen:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

Die Anfrage `/is/image/myCat/myImg?locale=de_de` würde das mit dem Katalogeintrag verknüpfte Bild zurückgeben. `myCat/myImg_D` (vorausgesetzt, dass ein solcher Katalogeintrag vorhanden ist).

Siehe Beschreibung von `attribute::LocaleMap` für Details.

## Der Übersetzungsprozess {#section-1f64db17e9f644d88e09853670e14a16}

Im obigen Beispiel sucht der Server zunächst nach dem *`locale`* &quot; `de_de`&quot;in der ID-Übersetzungszuordnung. Anschließend iteriert es die *`locSuffixes`* mit diesem Eintrag verknüpft ist, in diesem Fall &quot; `_D`&quot; und &quot;&quot; (leeres Suffix). Für jede Iteration wird das Suffix an die Bild-ID und die resultierende ID angehängt, die auf Existenz im Katalog getestet wurde. Wenn dieser Katalogeintrag gefunden wird, wird er verwendet, andernfalls wird der nächste getestet. In diesem Beispiel werden diese Einträge überprüft: `myCat/myImg_D`, und `myCat/myImg`. Wenn keine Übereinstimmung gefunden wird, gibt der Server einen Fehler oder ein Standardbild zurück (sofern konfiguriert).

## Unbekannte Gebietsschemata {#section-b2f3c83f2dc845d69b5908107b775537}

Im obigen Beispiel `attribute::LocaleMap` enthält ein leeres *`locale`* , die die standardmäßige Übersetzungsregel für unbekannt definiert definiert `locale=` -Werte (d. h. nicht explizit in der Übersetzungskarte aufgeführte Werte). Wenn diese Übersetzungszuordnung auf die Anfrage angewendet wurde `/is/image/myCat/myImg?locale=ja`, wird `myCat/myImg_E`, falls vorhanden, oder anderweitig `myCat/myImg`.

Wenn in einer Übersetzungszuordnung keine standardmäßige Übersetzungsregel angegeben ist, wird für alle Anforderungen mit unbekanntem Fehler zurückgegeben. `locale=` -Werte.

## Beispiele {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Mehrstufige Suche**

Es ist oft wünschenswert, Gebietsschemata (z. B. europäisch, mittelöstlich, nordamerikanisch) zu gruppieren, um regionale Standards zu erreichen. Dies kann mit einer mehrstufigen Suche erreicht werden.

In diesem Beispiel möchten wir Sammlungen für die Verwendung im Westen und im Nahen Osten unterstützen. Beide Sammlungen basieren auf der generischen Bildsammlung und in beiden werden einige Bilder hinzugefügt oder angepasst. Beide Sammlungen werden dann für bestimmte Gebietsschemata weiter optimiert ( `m1`, `m2` bei zwei mittleren Ost-Varianten und `w1`, `w2`, und `w3` für drei westliche Gebietsschemata), mit dem Unterschied, dass Bilder für `w1` und `w3`. Unbekannte Gebietsschemas sind nur der generischen Sammlung zugeordnet und haben keinen Zugriff auf Gebietsschema-spezifische Bilder.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

Die folgende Tabelle zeigt, welche Katalogeinträge berücksichtigt werden und in welcher Reihenfolge sie für die generische Eingabe-ID berücksichtigt werden `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Zu suchende Katalog-IDs</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alle anderen </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Suche nach bestimmten IDs**

Einige Bildbenennungskonventionen unterstützen möglicherweise interne generische Bild-IDs nicht. Die generischen IDs aus der Anfrage müssen immer einer bestimmten ID im Katalog zugeordnet werden. Oft ist die genaue spezifische ID nicht bekannt.

Für dieses Beispiel können Bilder für alle Sprachen `_1`, `_2`oder `_3` Suffix. Für französische Gebietsschemata spezifische Bilder können `_22` oder `_23` -Suffix und für deutsche Gebietsschemata spezifische Bilder haben möglicherweise `_470` oder `_480` Suffix.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

Die folgende Tabelle zeigt, welche Katalogeinträge berücksichtigt werden und in welcher Reihenfolge sie für die generische Eingabe-ID berücksichtigt werden `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Zu suchende Ausgabe-IDs</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alle anderen </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verwandte Themen {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
