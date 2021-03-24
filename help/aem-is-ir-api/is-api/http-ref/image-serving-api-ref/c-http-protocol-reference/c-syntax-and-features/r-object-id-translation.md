---
description: Image Serving bietet einen Mechanismus zum Übersetzen externer Objekt-IDs in Gebietsschema-spezifische Objekt-(Katalog-)IDs. Die Hauptanwendung dient der Bereitstellung von Gebietsschema-spezifischen Inhalten und Inhalten, die von mehreren Gebietsschemas gemeinsam genutzt werden, ohne dass die Client-Anwendung die Gebietsschema-spezifischen Objekt-IDs kennen muss.
solution: Experience Manager
title: Objekt-ID-Übersetzung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 9%

---


# Objekt-ID-Übersetzung{#object-id-translation}

Image Serving bietet einen Mechanismus zum Übersetzen externer Objekt-IDs in Gebietsschema-spezifische Objekt-(Katalog-)IDs. Die Hauptanwendung dient der Bereitstellung von Gebietsschema-spezifischen Inhalten und Inhalten, die von mehreren Gebietsschemas gemeinsam genutzt werden, ohne dass die Client-Anwendung die Gebietsschema-spezifischen Objekt-IDs kennen muss.

Die Anwendung kann nur mit globalen Objekt-IDs geschrieben werden, und Image Serving ersetzt automatisch Gebietsschema-spezifische Bilder und andere Inhalte, sofern verfügbar.

*`locale`* wird in Image Serving-Anforderungen mit dem Befehl `locale=` angegeben.

>[!NOTE]
>
>Die Übersetzung der Objekt-ID gilt nur für katalogbasierte Verwendung von Image Serving. Dateinamen können nicht übersetzt werden.

## Ebene {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Alle Verweise auf Einträge in Bild-, SVG- und statischen Inhaltskatalogen werden für Übersetzungsschriften berücksichtigt, und ICC-Profil-Verweise werden nicht übersetzt. Zusätzlich zu den *`object`* im Pfad von [!DNL /is/image] und [!DNL /is/static requests] unterliegen diese Befehle und Katalogattribute der ID-Übersetzung: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage` und `attribute::Watermark`.

## ID-Übersetzungszuordnung {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` definiert die Regeln, die vom Server zur Bestimmung der ID des lokalisierten Inhalts verwendet werden, wobei die generische Objekt-ID und der  `locale=` Wert als Eingabe angegeben werden.

`attribute::LocaleMap` besteht aus einer Liste von  *Gebietsschemas*  für die Eingabe (die mit den angegebenen Werten übereinstimmen  `locale=`), die jeweils keine oder mehrere Gebietsschema-Suffixe für die Ausgabe enthalten (  `*`locSuffixes`*`).

`attribute::LocaleMap` könnte z. B. wie folgt aussehen:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

Die Anforderung `/is/image/myCat/myImg?locale=de_de` gibt das mit dem Katalogeintrag `myCat/myImg_D` verknüpfte Bild zurück (vorausgesetzt, dass ein solcher Katalogeintrag vorhanden ist).

Weitere Informationen finden Sie in der Beschreibung von `attribute::LocaleMap`.

## Der Übersetzungsprozess {#section-1f64db17e9f644d88e09853670e14a16}

Bei dem obigen Beispiel sucht der Server zuerst nach dem *`locale`* &quot; `de_de`&quot;in der ID-Übersetzungszuordnung. Anschließend wird das *`locSuffixes`*, das mit diesem Eintrag verknüpft ist, in diesem Fall &quot; `_D`&quot;und &quot;&quot;(leeres Suffix) durchlaufen. Für jede Iteration wird das Suffix an die Bild-ID und die resultierende ID angehängt, die auf Vorhandensein im Katalog getestet wurde. Wenn dieser gefunden wird, wird dieser Katalogeintrag verwendet, andernfalls wird der nächste getestet. In diesem Beispiel werden die folgenden Einträge überprüft: `myCat/myImg_D` und `myCat/myImg`. Wenn keine Übereinstimmung gefunden wird, gibt der Server einen Fehler oder ein Standardbild zurück (sofern konfiguriert).

## Unbekannte Gebietsschemata {#section-b2f3c83f2dc845d69b5908107b775537}

Im obigen Beispiel enthält `attribute::LocaleMap` eine leere *`locale`*, die die Standardübersetzungsregel definiert, die für unbekannte `locale=`-Werte verwendet wird (d. h. für Werte, die nicht explizit in der Übersetzungskarte aufgeführt sind). Wenn diese Übersetzungszuordnung auf die Anforderung `/is/image/myCat/myImg?locale=ja` angewendet wurde, würde sie auf `myCat/myImg_E` aufgelöst, falls vorhanden, oder auf andere `myCat/myImg`.

Wenn in einer Übersetzungszuordnung keine Standardübersetzungsregel angegeben ist, wird für alle Anforderungen mit unbekannten Werten `locale=` ein Fehler zurückgegeben.

## Beispiele {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**mehrstufige Suche**

Es ist oft wünschenswert, Gebietsschemata zu gruppieren (z. B. europäische, Nahost- und Nordamerika), um regionale Standards zu erfüllen. Dies kann mit einer mehrstufigen Suche erreicht werden.

In diesem Beispiel möchten wir Sammlungen für die Verwendung im Westen und im Nahen Osten unterstützen. Beide Sammlungen basieren auf der generischen Bildsammlung und in beiden werden einige Bilder hinzugefügt oder angepasst. Beide Sammlungen werden anschließend für bestimmte Gebietsschemata ( `m1`, `m2` für zwei Varianten im mittleren Osten und `w1`, `w2` und `w3` für drei westliche Gebietsschemata) weiter optimiert, mit der Ausnahme, dass Bilder für `w1` und `w3` freigegeben werden. Unbekannte Gebietsschemas sind nur der generischen Sammlung zugeordnet und haben keinen Zugriff auf Gebietsschema-spezifische Bilder.

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
   <td> <p> <span class="codeph"> myImg  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Nach bestimmten IDs suchen**

Einige Konventionen zur Bildbenennung unterstützen möglicherweise keine generischen Bild-IDs intern. Die generischen IDs der Anforderung müssen immer einer bestimmten ID im Katalog zugeordnet werden. Oft ist die genaue spezifische ID möglicherweise nicht bekannt.

In diesem Beispiel können Bilder für alle Sprachen das Suffix `_1`, `_2` oder `_3` haben. Für französische Gebietsschemata spezifische Bilder können das Suffix `_22` oder `_23` haben und für deutsche Gebietsschemas spezifische Bilder können das Suffix `_470` oder `_480` haben.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

Die folgende Tabelle zeigt, welche Katalogeinträge berücksichtigt werden und in welcher Reihenfolge sie für die generische Eingabe-ID `myImg` berücksichtigt werden:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Zu durchsuchende Output-IDs</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de  </span>,  <span class="codeph"> de_at  </span>,  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alle anderen </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verwandte Themen {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ,  [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
