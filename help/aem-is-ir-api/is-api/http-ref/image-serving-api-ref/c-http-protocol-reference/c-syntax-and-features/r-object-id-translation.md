---
description: Image Serving bietet einen Mechanismus zum Übersetzen externer Objekt-IDs in gebietsschemaspezifische Objekt-(Katalog-)IDs. Die primäre Anwendung dient der Bereitstellung gebietsschemaspezifischer Inhalte und Inhalte, die von mehreren Gebietsschemata gemeinsam genutzt werden, ohne dass die Client-Anwendung die gebietsschemaspezifischen Objekt-IDs kennen muss.
solution: Experience Manager
title: Übersetzung der Objekt-ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---

# Übersetzung der Objekt-ID{#object-id-translation}

Image Serving bietet einen Mechanismus zum Übersetzen externer Objekt-IDs in gebietsschemaspezifische Objekt-(Katalog-)IDs. Die primäre Anwendung dient der Bereitstellung gebietsschemaspezifischer Inhalte und Inhalte, die von mehreren Gebietsschemata gemeinsam genutzt werden, ohne dass die Client-Anwendung die gebietsschemaspezifischen Objekt-IDs kennen muss.

Das Programm kann nur mit globalen Objekt-IDs geschrieben werden und Image Serving ersetzt automatisch gebietsschemaspezifische Bilder und andere Inhalte, sofern verfügbar.

Der *`locale`* wird in Bildbereitstellungsanfragen mit dem Befehl `locale=` angegeben.

>[!NOTE]
>
>Die Übersetzung der Objekt-ID ist nur für die katalogbasierte Verwendung von Image-Serving anwendbar. Dateinamen können nicht übersetzt werden.

## Umfang {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Alle Verweise auf Einträge in Bild-, SVG- und statischen Inhaltskatalogen werden für Übersetzungsschriftarten berücksichtigt und ICC-Profilverweise werden nicht übersetzt. Zusätzlich zur *`object`* im Pfad von [!DNL /is/image] und [!DNL /is/static requests] unterliegen diese Befehle und Katalogattribute der ID-Übersetzung: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage` und `attribute::Watermark`.

## Die Übersetzungszuordnung der ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` definiert die vom Server verwendeten Regeln, um die ID der lokalisierten Inhalte zu bestimmen, die als Eingaben von der generischen Objekt-ID und dem `locale=`-Wert gegeben ist.

`attribute::LocaleMap` besteht aus einer Liste von *Gebietsschemata* (die mit den mit `locale=` angegebenen Werten übereinstimmen), von denen jedes keine oder mehrere Suffixe für das Ausgabelokal ( `*`locSuffixes`*`) aufweist.

`attribute::LocaleMap` könnte beispielsweise wie folgt aussehen:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

Die Anfrage `/is/image/myCat/myImg?locale=de_de` gibt das Bild zurück, das mit dem Katalogeintrag verknüpft ist `myCat/myImg_D` (unter der Annahme, dass ein solcher Katalogeintrag vorhanden ist).

Weitere Informationen finden Sie in der Beschreibung von `attribute::LocaleMap`.

## Der Übersetzungsprozess {#section-1f64db17e9f644d88e09853670e14a16}

In diesem Beispiel sucht der Server zunächst in der ID-Übersetzungszuordnung nach dem *`locale`* &quot;`de_de`&quot;. Anschließend wird der mit diesem Eintrag verknüpfte *`locSuffixes`* durchlaufen, in diesem Fall &quot;`_D`&quot; und &quot;&quot; (leeres Suffix). Bei jeder Iteration wird das Suffix an die Bild-ID angehängt und die resultierende ID wird auf ihre Existenz im Katalog getestet. Wenn gefunden, wird dieser Katalogeintrag verwendet, andernfalls wird der nächste getestet. In diesem Beispiel werden diese Einträge überprüft: `myCat/myImg_D` und `myCat/myImg`. Wenn keine Übereinstimmung gefunden wird, gibt der Server einen Fehler oder ein Standardbild zurück (falls so konfiguriert).

## Unbekannte Gebietsschemata {#section-b2f3c83f2dc845d69b5908107b775537}

Im obigen Beispiel enthält `attribute::LocaleMap` einen leeren *`locale`*, der die standardmäßige Übersetzungsregel definiert, die für unbekannte `locale=` verwendet wird (d. h. für solche, die nicht explizit in der Übersetzungszuordnung aufgeführt sind). Wenn diese Übersetzungszuordnung auf die Anfrage-`/is/image/myCat/myImg?locale=ja` angewendet würde, würde sie, sofern vorhanden, in `myCat/myImg_E` aufgelöst oder anderweitig `myCat/myImg`.

Wenn eine Übersetzungszuordnung keine standardmäßige Übersetzungsregel angibt, wird für alle Anfragen mit unbekannten `locale=` ein Fehler zurückgegeben.

## Beispiele {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Mehrstufige Suche**

Es ist oft wünschenswert, Gebietsschemata (z. B. Europa, Naher Osten, Nordamerika) zu gruppieren, um regionale Standards zu berücksichtigen. Dies kann mit einer mehrstufigen Suche erreicht werden.

Für dieses Beispiel möchten wir Sammlungen für die Verwendung im Westen und Nahen Osten unterstützen. Beide Sammlungen basieren auf der generischen Bildsammlung und in beiden werden einige Bilder hinzugefügt oder angepasst. Beide Sammlungen werden dann für bestimmte Gebietsschemata weiter verfeinert ( `m1`, `m2` für zwei Varianten des Mittleren Ostens und `w1`, `w2` und `w3` für drei westliche Gebietsschemata), mit der Ausnahme, dass Bilder für `w1` und `w3` freigegeben werden. Unbekannte Gebietsschemata werden nur der generischen Sammlung zugeordnet und haben keinen Zugriff auf gebietsschemaspezifische Bilder.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

Die folgende Tabelle zeigt, welche Katalogeinträge berücksichtigt werden und in welcher Reihenfolge sie für die generische Eingabe-ID `myImg` berücksichtigt werden:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Zu durchsuchende Katalog-IDs</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> W1, W3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> W2-</span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> M1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg-</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg-</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alle anderen </p> </td> 
   <td> <p> <span class="codeph"> myImg-</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Suchen nach bestimmten IDs**

Einige Bildnamenskonventionen unterstützen möglicherweise keine generischen Bild-IDs intern. Die generischen IDs aus der Anfrage müssen immer einer bestimmten ID im Katalog zugeordnet sein. Häufig ist die genaue spezifische ID nicht bekannt.

In diesem Beispiel können Bilder für alle Sprachen das Suffix `_1`, `_2` oder `_3` aufweisen. Bilder, die für französische Gebietsschemata spezifisch sind, können `_22` oder `_23` Suffix aufweisen, und Bilder, die für deutsche Gebietsschemata spezifisch sind, können `_470` oder `_480` Suffix aufweisen.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

Die folgende Tabelle zeigt, welche Katalogeinträge berücksichtigt werden und in welcher Reihenfolge sie für die generische Eingabe-ID `myImg` berücksichtigt werden:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Zu suchende Ausgabe-IDs</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> FR </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alle anderen </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verwandte Themen {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
