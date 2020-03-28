---
description: Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (xml oder json), die alle Ressourcen und Metadaten darstellt, die mit dem Katalog ImageSet für einen bestimmten Datensatz verknüpft sind.
seo-description: Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (xml oder json), die alle Ressourcen und Metadaten darstellt, die mit dem Katalog ImageSet für einen bestimmten Datensatz verknüpft sind.
seo-title: Medienset-Anforderungen
solution: Experience Manager
title: Medienset-Anforderungen
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Medienset-Anforderungen{#media-set-requests}

Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (xml oder json), die alle Ressourcen und Metadaten darstellt, die mit catalog::ImageSet für einen bestimmten Datensatz verknüpft sind.

Die Viewer können auf diese Weise Antworten generieren, um die Präsentation einfacher Bilder, Videos, Videosets, Mustersets, Rotationssets, Seitensätze (E-Kataloge) und Mediensets zu informieren.

## Anforderungssyntax {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

Die eingestellte Antwort für einen Datensatz `catalog::ImageSet` kann mit dem `req=set` Modifikator abgerufen werden und die Katalogdatensatz-ID im Netzpfad referenziert werden. Alternativ kann der Bildsatz direkt in der URL mit dem `imageset=` Modifikator angegeben werden. Wenn der `imageset=` Modifikator zum Angeben des Bildsatzes verwendet wird, sollte der gesamte Wert in geschweifte Klammern gesetzt werden, um den Bildsatzwert zu vermeiden und sicherzustellen, dass eingeschlossene Modifikatoren nicht als Bestandteil der URL-Abfrage-Zeichenfolge interpretiert werden.

## Arten von eingestellten Antworten {#section-93eb0a1f70344da2a888e56372ad3896}

Der festgelegte Mechanismus unterstützt die folgenden Arten von Antworten:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>einfache Bilder </p></td> 
  <td class="stentry"> <p>Ein Bilddatensatz ohne <span class="codeph"> Katalog::ImageSet</span> definiert. </p></td> 
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
  <td class="stentry"> <p>Hierarchische Mustersets </p></td> 
  <td class="stentry"> <p>Eine Gruppe von Elementen, die aus einem grundlegenden Musterelement oder einem Verweis auf einen Musterset-Datensatz besteht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Rotationssets </p></td> 
  <td class="stentry"> <p>Eine Gruppe von Elementen, die aus einer einfachen Liste von Bild-IDs bestehen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>zweidimensionale Rotationssets </p></td> 
  <td class="stentry"> <p>Eine Gruppe von Elementen, die aus einem einfachen Bild oder einem Verweis auf ein einfaches Rotationsset bestehen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seitensätze </p></td> 
  <td class="stentry"> <p>Eine Gruppe von Elementen bestehend aus einer Liste von bis zu drei Seitenbildern </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Mediensets </p></td> 
  <td class="stentry"> <p>Eine Reihe von Elementen, die aus einfachen Bildern, Videosets, Mustersets, hierarchischen Mustersets, Rotationssets, zweidimensionalen Rotationssets, Seitensätzen und Video-Assets bestehen. Jedes Medienset-Element kann auch ein optionales Farbfeld enthalten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Videosets </p></td> 
  <td class="stentry"> <p>Eine Reihe von Elementen, die aus einer Liste von einfachen Videos bestehen. </p></td> 
 </tr> 
</table>

## Typerkennung nach außen {#section-3dd6e453528d46898e559d31458a59ba}

Wenn eine `req=set` Anforderung empfangen wird, wird der Typ der zu generierenden Antwort vom Wert `catalog::AssetType`von bestimmt. Wenn `catalog::AssetType` der Antworttyp nicht definiert ist, wird er durch die folgenden Regeln bestimmt:

* Wenn Datensatz im Bildkatalog gefunden wird UND definiert `catalog::ImageSet` ist

   * Angenommen, ein E-Katalog-Satz enthält mindestens einen Eintrag im Bildsatz-Datensatzfeld einen Doppelpunkt
   * Nehmen Sie an, dass ein Medienset mindestens einen Eintrag im Bildsatz-Feld zwei Semikolons enthält.
   * Angenommen, ein Bildsatz enthält mindestens einen Eintrag im Bildsatz-Feld ein Semikolon.
   * Angenommen, ein Rotationsset enthält keinen Doppelpunkt oder Semikolon, aber mindestens ein Eintrag enthält einen Referenzsatz oder einen Inline-Satz (dies ist ein 2D-Rotationsset).
   * Nehmen Sie einen unbekannten Satz an, wenn kein Eintrag Doppelpunkt, kein Semikolon oder einen Referenzsatz oder einen Inline-Satz enthält (d. h. eine kommagetrennte Liste von Bildern).

* Wenn sowohl in Bild- als auch in statischen Inhaltskatalogen Datensätze gefunden werden

   * Gehen Sie von Video aus, wenn die Dateierweiterung in folgendem Satz liegt: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten Bild annehmen

* Wenn Datensatz im statischen Inhaltskatalog, aber NICHT im Bildkatalog gefunden wird

   * Gehen Sie von Video aus, wenn die Dateierweiterung in folgendem Satz liegt: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten statisch annehmen

* Wenn Eintrag im Bildkatalog, aber NICHT im statischen Inhaltskatalog gefunden

   * Abbildung annehmen

* Wenn der Datensatz NICHT im Bildkatalog und NICHT im statischen Inhaltskatalog gefunden wird

   * Nehmen Sie ein dateibasiertes Video an, wenn die Dateierweiterung in folgendem Satz liegt: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten dateibasiertes Bild

In allen Fällen entspricht die resultierende XML-Antwort dem angegebenen XML-Dokument, wobei die Set-Stamm-Node dem erkannten Typ entspricht.

## Typerkennung für Innen-Set {#section-8f46490e467247e69ce284704def06f3}

Wenn der äußere Satz als Typ-Mediensatz erkannt wird, enthält die Antwort eine Reihe von Medienset-Elementen, die den einzelnen Mediensatzeinträgen in `catalog::ImageSet`entsprechen. Wenn der optionale Typparameter für einen bestimmten Mediensatzeintrag angegeben ist, wird er einem Ausgabetyp gemäß der folgenden Tabelle zugeordnet:

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

Wenn der optionale Typparameter für einen bestimmten Mediensatzeintrag nicht angegeben ist oder einem nicht unterstützten Typ entspricht, wird der Mediensatzelementtyp automatisch anhand derselben Regeln erkannt, die auf der äußeren Einstellungsebene angewendet wurden.

## XML-Spezifikation {#section-c1bd60948ef545759a16885bb6fcc607}

Die zurückgegebene XML-Antwort entspricht der folgenden Spezifikation:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Der `labelkey=` Modifikator wird zusammen mit dem `catalog::UserData`Feld verwendet, um Beschriftungen für Bilder und Muster zu generieren. Das `catalog:UserData` Feld wird als Satz Schlüssel/Wert-Paare analysiert und die Schlüssel-Indizes in diesem Satz, um den Wert für den angegebenen Schlüssel abzurufen. Dieser Wert wird dann im *`l`* -Attribut für den *`s`* und zurückgegeben *`i`*.

## Erzwungene Beschränkungen {#section-b9f042873bee45a5ae11b69fd42f2bca}

Um die Größe der Antwort zu begrenzen und Probleme mit Selbstverweisen zu vermeiden, wird die maximale Verschachtelungstiefe von der Servereigenschaft gesteuert `PS::fvctx.nestingLimit`. Wenn diese Grenze überschritten wird, wird ein Fehler zurückgegeben.

Um die Größe der XML-Antworten für große E-Katalog-Sets zu beschränken, werden private Metadaten für Prospektset-Elemente entsprechend der Servereigenschaft unterdrückt `PS::fvctx.brochureLimit`. Alle mit der Broschüre verknüpften privaten Metadaten werden exportiert, bis die Prospektbeschränkung erreicht ist. Sobald der Grenzwert überschritten wurde, werden private Maps und Benutzerdaten unterdrückt und ein entsprechendes Flag wird gesetzt, um anzugeben, welcher Datentyp unterdrückt wurde.

Verschachtelte Mediensets werden nicht unterstützt. Ein verschachtelter Mediensatz ist definiert als ein Mediensatz, der ein Mediensatzelement vom Typ Mediensatz enthält. Wenn diese Bedingung erkannt wird, wird ein Fehler zurückgegeben.

## Beispiele {#section-588c9d33aa05482c86cd2b1936887228}

Beispiel-XML-Antworten für eine `req=set` Anforderung finden Sie auf der Seite Eigenschaften unter der Kopfzeile HTML-Beispiele.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Verwandte Themen {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Bildkatalog-Referenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

