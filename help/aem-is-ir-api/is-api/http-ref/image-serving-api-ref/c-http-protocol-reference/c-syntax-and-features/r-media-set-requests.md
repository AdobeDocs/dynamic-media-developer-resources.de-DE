---
description: Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (XML oder JSON), die alle Ressourcen und Metadaten darstellt, die mit dem ImageSet-Katalog für einen bestimmten Datensatz verknüpft sind.
solution: Experience Manager
title: Medienset-Anfragen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Medienset-Anfragen{#media-set-requests}

Image Serving bietet einen Mechanismus zum Abrufen einer hierarchischen Textantwort (XML oder JSON), die alle Ressourcen und Metadaten darstellt, die mit catalog:ImageSet für einen bestimmten Datensatz verknüpft sind.

Die Betrachter können diesen Mechanismus verwenden, um Antworten zu generieren und so über die Präsentation von einfachen Bildern, Videos, Videosets, Mustersets, Rotationssets, Seitensets (E-Katalogen) und Mediensets zu informieren.

## Anfragesyntax {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

Die festgelegte Antwort für eine `catalog::ImageSet` kann mithilfe des Modifikators &quot;`req=set`&quot; abgerufen werden und im nächsten Pfad auf die ID des Katalogdatensatzes verweisen. Alternativ können Sie das Bildset direkt in der URL angeben, indem Sie den Modifikator `imageset=` verwenden. Wenn der Modifikator `imageset=` zum Angeben des Bildsets verwendet wird, sollte der gesamte Wert in geschweifte Klammern eingeschlossen werden, um den Wert des Bildsets mit Escape-Zeichen zu versehen und sicherzustellen, dass eingeschlossene Modifikatoren nicht als Teil der URL-Abfragezeichenfolge interpretiert werden.

## Typen von Antworten {#section-93eb0a1f70344da2a888e56372ad3896}

Der Set-Mechanismus unterstützt die folgenden Arten von Antworten:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Einfache Bilder </p></td> 
  <td class="stentry"> <p>Ein Bilddatensatz, ohne dass <span class="codeph"> Katalog::ImageSet</span> definiert ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Einfache Videos </p></td> 
  <td class="stentry"> <p>Eine Videoaufzeichnung im statischen Inhaltskatalog. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Mustersets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einem Verweis auf einen Bilddatensatz und einem optionalen separaten Verweis auf einen Bilddatensatz besteht, der als Muster verwendet wird. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Hierarchische Mustersets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einem grundlegenden Musterelement oder einem Verweis auf einen Mustersatzdatensatz besteht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Rotationssets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einer einfachen Liste von Bild-IDs besteht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Zweidimensionale Rotationssets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einem einfachen Bild oder einem Verweis auf ein grundlegendes Rotationsset besteht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Seitensätze </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einer Liste von bis zu drei Seitenbildern besteht </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Mediensets </p></td> 
  <td class="stentry"> <p>Eine Gruppe von Elementen, die aus einfachen Bildern, Videosets, Mustersets, hierarchischen Mustersets, Rotationssets, zweidimensionalen Rotationssets, Seitensets und Video-Assets besteht. Jedes Medienset-Element kann auch ein optionales Farb-/Bildmuster enthalten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Videosets </p></td> 
  <td class="stentry"> <p>Ein Satz von Elementen, der aus einer Liste einfacher Videos besteht. </p></td> 
 </tr> 
</table>

## Erkennung des äußeren Satzes {#section-3dd6e453528d46898e559d31458a59ba}

Wenn eine `req=set`-Anfrage empfangen wird, wird der Typ der zu generierenden Antwort durch den Wert von `catalog::AssetType` bestimmt. Wenn `catalog::AssetType` nicht definiert ist, wird der Antworttyp durch die folgenden Regeln bestimmt:

* Wenn der Datensatz im Bildkatalog gefunden wird UND `catalog::ImageSet` definiert ist

   * Angenommen, E-Katalog-Set, wenn mindestens ein Eintrag im Feld „Bildset“ einen Doppelpunkt enthält
   * Angenommen, ein Medienset ist vorhanden, wenn mindestens ein Eintrag im Feld „Bildset-Datensatz“ zwei Semikolons enthält.
   * Angenommen, ein Bildset wird verwendet, wenn mindestens ein Eintrag im Feld „Bildset-Datensatz“ ein Semikolon enthält.
   * Angenommen, ein Rotationsset wird verwendet, wenn kein Eintrag einen Doppelpunkt oder Semikolon enthält, aber mindestens ein Eintrag ein referenziertes Set oder Inline-Set enthält (dies ist ein 2D-Rotationsset).
   * Angenommen, ein unbekannter Satz liegt vor, wenn kein Eintrag einen Doppelpunkt, ein Semikolon, einen referenzierten Satz oder einen Inline-Satz enthält (d. h. eine durch Kommas getrennte Liste von Bildern).

* Wenn der Datensatz sowohl in Bild- als auch in statischen Inhaltskatalogen gefunden wird

   * Angenommen, Video, wenn die Dateierweiterung im folgenden Satz vorhanden ist: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten Bild annehmen

* Wenn der Datensatz im statischen Inhaltskatalog, aber NICHT im Bildkatalog gefunden wird

   * Angenommen, Video, wenn die Dateierweiterung im folgenden Satz vorhanden ist: mp3, mp4, flv, f4v, swf, xml
   * Ansonsten „statisch“ annehmen

* Wenn ein Datensatz im Bildkatalog, aber NICHT im statischen Inhaltskatalog gefunden wird

   * Bild annehmen

* Wenn der Datensatz NICHT im Bildkatalog und NICHT im statischen Inhaltskatalog gefunden wird

   * Angenommen, die Dateierweiterung basiert auf Video, wenn sie wie folgt festgelegt ist: mp3, mp4, flv, f4v, swf, xml
   * Angenommen, das dateibasierte Bild ist anders

In allen Fällen entspricht die resultierende XML-Antwort dem angegebenen XML-Dokument, wobei der Stammknoten dem erkannten Typ entspricht.

## Erkennung des inneren Satztyps {#section-8f46490e467247e69ce284704def06f3}

Wenn das äußere Set als Typ „Medienset“ erkannt wird, enthält die Antwort einen Satz von Medienset-Elementen, die jedem Medienset-Eintrag in `catalog::ImageSet` entsprechen. Wenn der optionale Typparameter für einen bestimmten Mediensatzeintrag angegeben ist, wird er gemäß der folgenden Tabelle einem Ausgabetyp zugeordnet:

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

Wenn der optionale Typparameter für einen bestimmten Mediensatzeintrag nicht angegeben ist oder einem nicht unterstützten Typ entspricht, wird der Elementtyp des Mediensatzes automatisch anhand derselben Regeln erkannt, die auf der Ebene des äußeren Satzes angewendet wurden.

## XML-Spezifikation {#section-c1bd60948ef545759a16885bb6fcc607}

Die zurückgegebene XML-Antwort entspricht der folgenden Spezifikation:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Der Modifikator `labelkey=` wird zusammen mit dem Feld `catalog::UserData` verwendet, um Beschriftungen für Bilder und Farbfelder zu generieren. Das `catalog:UserData` Feld wird als Satz von Schlüssel/Wert-Paaren geparst und der labelKey indiziert in diesem Satz, um den Wert für den angegebenen Schlüssel abzurufen. Dieser Wert wird dann im *`l`*-Attribut für die *`s`* und *`i`* zurückgegeben.

## Erzwungene Einschränkungen {#section-b9f042873bee45a5ae11b69fd42f2bca}

Um die Größe der Antwort zu begrenzen und Probleme mit Selbstverweisen zu vermeiden, wird die maximale Verschachtelungstiefe durch die Server-Eigenschaft `PS::fvctx.nestingLimit` gesteuert. Wenn diese Grenze überschritten wird, wird ein Fehler zurückgegeben.

Um die Größe der XML-Antworten für große E-Katalog-Sets zu begrenzen, werden private Metadaten für Broschüren-Set-Elemente gemäß der Server-Eigenschaft `PS::fvctx.brochureLimit` unterdrückt. Alle mit der Broschüre verknüpften privaten Metadaten werden exportiert, bis das Limit für die Broschüre erreicht ist. Nachdem das Limit überschritten wurde, werden private Zuordnungen und Benutzerdaten unterdrückt und ein entsprechendes Flag gesetzt, um anzugeben, welcher Datentyp unterdrückt wurde.

Verschachtelte Mediensets werden nicht unterstützt. Ein verschachteltes Medienset wird als Medienset definiert, das ein Medienset-Element des Typs Medienset enthält. Wenn dieser Zustand erkannt wird, wird ein Fehler zurückgegeben.

## Beispiele {#section-588c9d33aa05482c86cd2b1936887228}

XML-Beispielantworten für `req=set` Anfrage finden Sie auf der Seite „Eigenschaften“ unter der Kopfzeile &quot;HTML-Beispiele“.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Verwandte Themen {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Image-Katalogreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
