---
description: Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (xml oder json), die alle Ressourcen und Metadaten darstellt, die mit dem Katalog ImageSet für einen bestimmten Datensatz verknüpft sind.
solution: Experience Manager
title: Medienset-Anforderungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Medienset-Anforderungen{#media-set-requests}

Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (xml oder json), die alle Ressourcen und Metadaten darstellt, die mit catalog::ImageSet für einen bestimmten Datensatz verknüpft sind.

Mit diesem Mechanismus können Viewer Antworten generieren, um die Präsentation einfacher Bilder, Videos, Videosets, Mustersets, Rotationssets, Seitensätze (E-Kataloge) und Mediensets zu informieren.

## Anforderungssyntax {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

Die festgelegte Antwort für `catalog::ImageSet` kann mithilfe des Modifikators `req=set` abgerufen werden und die Katalogdatensatz-ID im Netzpfad referenzieren. Alternativ kann das Bildset direkt in der URL mithilfe des Modifikators `imageset=` angegeben werden. Wenn der Modifikator `imageset=` zum Angeben des Bildsatzes verwendet wird, sollte der gesamte Wert in geschweifte Klammern gesetzt werden, um den Bildsatzwert zu maskieren und sicherzustellen, dass eingeschlossene Modifikatoren nicht als Teil der URL-Abfragezeichenfolge interpretiert werden.

## Typen von festgelegten Antworten {#section-93eb0a1f70344da2a888e56372ad3896}

Der festgelegte Mechanismus unterstützt die folgenden Arten von Antworten:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>einfache Bilder </p></td> 
  <td class="stentry"> <p>Ein Bilddatensatz ohne <span class="codeph"> -Katalog::ImageSet</span> definiert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>einfache Videos </p></td> 
  <td class="stentry"> <p>Ein Videodatensatz im statischen Inhaltskatalog. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Mustersets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, bestehend aus einem Verweis auf einen Bilddatensatz und einem optionalen separaten Verweis auf einen Bilddatensatz, der als Muster verwendet wird. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>hierarchische Mustersets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, bestehend aus einem grundlegenden Musterelement oder einem Verweis auf einen Musterset-Datensatz. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Rotationssets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einer einfachen Liste von Bild-IDs besteht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>zweidimensionale Rotationssets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einem einfachen Bild oder einem Verweis auf ein einfaches Rotationsset besteht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seitensätze </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, bestehend aus einer Liste mit bis zu drei Seitenbildern </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Mediensets </p></td> 
  <td class="stentry"> <p>Eine Gruppe von Elementen, die aus einfachen Bildern, Videosets, Mustersets, hierarchischen Mustersets, Rotationssets, zweidimensionalen Rotationssets, Seitensätzen und Video-Assets bestehen. Jedes Medienset-Element kann auch ein optionales Muster enthalten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Videosets </p></td> 
  <td class="stentry"> <p>Ein Satz von Artikeln, bestehend aus einer Liste einfacher Videos. </p></td> 
 </tr> 
</table>

## Typerkennung für äußere Einsätze {#section-3dd6e453528d46898e559d31458a59ba}

Wenn eine `req=set` -Anfrage empfangen wird, wird der Typ der zu generierenden Antwort durch den Wert von `catalog::AssetType` bestimmt. Wenn `catalog::AssetType` nicht definiert ist, wird der Antworttyp durch die folgenden Regeln bestimmt:

* Wenn der Datensatz im Bildkatalog gefunden wird UND `catalog::ImageSet` definiert ist

   * Nehmen wir einen E-Katalog-Satz an, wenn mindestens ein Eintrag im Datensatzbildset-Feld einen Doppelpunkt enthält
   * Nehmen Sie als Medienset an, wenn mindestens ein Eintrag im Datensatzbildset-Feld zwei Semikolons enthält.
   * Nehmen wir an, dass ein Bildset mindestens einen Eintrag im Bildset-Datensatzfeld ein Semikolon enthält.
   * Angenommen, ein Rotationsset ist vorhanden, wenn kein Eintrag Doppelpunkt oder Semikolon enthält, aber mindestens ein Eintrag einen Referenzsatz oder einen Inline-Satz enthält (dies ist ein 2D-Rotationsset).
   * Nehmen Sie als unbekannter Satz an, wenn kein Eintrag Doppelpunkt, keinen Semikolon oder einen Referenzsatz oder einen Inline-Satz enthält (d. h. eine durch Kommas getrennte Liste von Bildern).

* Wenn Datensatz sowohl in Bild- als auch in statischen Inhaltskatalogen gefunden wird

   * Nehmen Sie als Video an, wenn die Dateierweiterung in folgendem Satz liegt: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten Bild annehmen

* Wenn Datensatz im statischen Inhaltskatalog, NICHT jedoch im Bildkatalog gefunden wird

   * Nehmen Sie als Video an, wenn die Dateierweiterung in folgendem Satz liegt: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten statische Annahme

* Wenn Eintrag im Bildkatalog, aber NICHT im statischen Inhaltskatalog gefunden wird

   * Angenommen, Bild

* Wenn der Datensatz NICHT im Bildkatalog gefunden wird und NICHT im statischen Inhaltskatalog zu finden ist

   * Nehmen Sie ein dateibasiertes Video an, wenn die Dateierweiterung in folgendem Satz liegt: mp3, mp4, flv, f4v, swf, xml
   * Angenommen, dateibasiertes Bild ist anders

In allen Fällen entspricht die resultierende XML-Antwort dem angegebenen XML-Dokument mit dem festgelegten Stammknoten, der dem erkannten Typ entspricht.

## Erkennung des inneren Sets {#section-8f46490e467247e69ce284704def06f3}

Wenn der äußere Satz als Mediensatz vom Typ erkannt wird, enthält die Antwort einen Satz von Medienset-Elementen, die jedem Medienset-Eintrag in `catalog::ImageSet` entsprechen. Wenn der optionale Typparameter für einen bestimmten Mediensatzeintrag angegeben ist, wird er gemäß der folgenden Tabelle einem Ausgabetyp zugeordnet:

| Eingabetyp | Ausgabetyp |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Wenn der optionale Typparameter für einen bestimmten Mediensatzeintrag nicht angegeben ist oder einem nicht unterstützten Typ entspricht, wird der Mediensatz-Elementtyp automatisch anhand der gleichen Regeln erkannt, die auf der äußeren Satzebene angewendet wurden.

## XML-Spezifikation {#section-c1bd60948ef545759a16885bb6fcc607}

Die zurückgegebene XML-Antwort entspricht der folgenden Spezifikation:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Der Modifikator `labelkey=` wird zusammen mit dem Feld `catalog::UserData`verwendet, um Beschriftungen für Bilder und Muster zu generieren. Das Feld `catalog:UserData` wird als Satz von Schlüssel/Wert-Paaren analysiert und die Beschriftungsschlüssel indiziert in diesen Satz, um den Wert für den angegebenen Schlüssel abzurufen. Dieser Wert wird dann im *`l`*-Attribut für *`s`* und *`i`* zurückgegeben.

## Erzwungene Einschränkungen {#section-b9f042873bee45a5ae11b69fd42f2bca}

Um die Größe der Antwort zu begrenzen und selbstreferenzierende Probleme zu vermeiden, wird die maximale Verschachtelungstiefe durch die Servereigenschaft `PS::fvctx.nestingLimit` gesteuert. Wenn diese Grenze überschritten wird, wird ein Fehler zurückgegeben.

Um die Größe der XML-Antworten für große E-Katalog-Sets zu begrenzen, werden private Metadaten für Prospektset-Elemente entsprechend der Servereigenschaft `PS::fvctx.brochureLimit` unterdrückt. Alle privaten Metadaten, die mit der Broschüre verknüpft sind, werden exportiert, bis das Limit für die Broschüre erreicht ist. Sobald der Grenzwert überschritten wird, werden private Maps und Benutzerdaten unterdrückt und eine entsprechende Markierung gesetzt, die angibt, welcher Datentyp unterdrückt wurde.

Verschachtelte Mediensets werden nicht unterstützt. Ein verschachteltes Medienset ist definiert als ein Medienset, das ein Medienset-Element vom Typ Medienset enthält. Wenn diese Bedingung erkannt wird, wird ein Fehler zurückgegeben.

## Beispiele {#section-588c9d33aa05482c86cd2b1936887228}

Beispiel-XML-Antworten für `req=set`-Anforderungen finden Sie auf der Seite Eigenschaften unter der Kopfzeile HTML-Beispiele .

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Verwandte Themen {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md),  [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
