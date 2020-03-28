---
description: Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.
seo-description: Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.
seo-title: Bildkataloge
solution: Experience Manager
title: Bildkataloge
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bildkataloge{#image-catalogs}

Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.

Bildkataloge Angebot der folgenden Funktionen:

* Beständige Verknüpfung von Bildern mit bestimmten Metadaten und Modifikatorbefehlen zulassen.

   Auf Einträge in Bildkatalogen wird mit der Kurzbefehlsnotation ` *`rootId/objId`*`verwiesen, wobei ` *`rootId`*` den Bildkatalog identifiziert und ` *`objId`*` einen Datensatz im Katalog identifiziert.
* Geben Sie Standardwerte für bestimmte Anforderungsattribute an, z. B. für die JPEG-Qualität oder für die Anwendung eines Wasserzeichens.
* Verwalten von Schriftarten, ICC-Profilen, Makrodefinitionen und Anforderungsvorlagen

Auch wenn keine bestimmten Bildkataloge definiert sind, stehen alle Funktionen von Bildkatalogen über den Standardkatalog ( [!DNL default.ini]) zur Verfügung.

Wenn die ` *`rootId`*` im URL-Pfad der Anforderung mit `attribute::RootId` einem bestimmten Bildkatalog übereinstimmt, wird dieser Katalog zum Hauptkatalog für diese Anforderung. Der Hauptkatalog enthält die Standardattribute und -einstellungen für die gesamte Anforderung. Wenn keine Übereinstimmung gefunden wird, wird stattdessen der Standardkatalog verwendet.

Ein Katalog, der in einem `src=` oder `mask=` -Befehl identifiziert wird, stellt die folgenden Katalogattribute und Daten für die aktuelle Ebene bereit:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Daten</b> </th> 
   <th class="entry"> <b> Anmerkungen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> die Standarderweiterung für alle Bilddateipfade in der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> Katalog::Ablauf</span> oder Ablauf der aktuellen Ebene, wenn kein Katalogdatensatz involviert ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute: Icc*</span> </p> </td> 
   <td> <p> das funktionierende ICC-Profil, die Renderpriorität und die Blackpoint-Kompensation für die Anforderung und/oder die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> für alle Quelldateipfade der aktuellen Ebene verwendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> Katalog: nur Auflösung</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog: Anker</span> </p> </td> 
   <td> <p> Standard für den <span class="codeph"> Anker=</span> -Wert der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Ablauf</span> </p> </td> 
   <td> <p> der kleinste Ablaufwert aller Ebenen als Wert für die Zeit bis zum Limit des Antwortbilds verwendet wird </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::IccProfile</span> </p> </td> 
   <td> <p> das Profil für die Farbe des Quellbilds für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Map</span> </p> </td> 
   <td> <p> die Imagemap-Daten für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::MaskPath</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> mask=</span> für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Modifier</span> </p> </td> 
   <td> <p> Präfix-Befehle für die aktuelle Ebene (jeder Befehl im <span class="codeph"> Katalog::Modifier</span> kann durch denselben Befehl in der URL überschrieben werden, sofern er für dieselbe Ebene festgelegt wurde) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Pfad</span> </p> </td> 
   <td> <p> die Quellbilddatei für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::PostModifier</span> </p> </td> 
   <td> <p> postfix-Befehle für die aktuelle Ebene (ähnlich wie <span class="codeph"> Katalog::Modifier</span>, aber Befehle im <span class="codeph"> Katalog::PostModifier</span> setzen dieselben Befehle außer Kraft, die in der URL oder im <span class="codeph"> Katalog::Modifier</span>angegeben sind) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog:Auflösung</span> </p> </td> 
   <td> <p> die Objektauflösung der aktuellen Ebene </p> </td> 
  </tr> 
 </tbody> 
</table>

Innerhalb derselben Ebene `src=` `mask=` und muss auf denselben Bildkatalog verweisen (falls vorhanden).

Ein in einem `icc=` Befehl identifizierter Katalog wird nur zum Nachschlagen eines Eintrags aus der ICC-Profil-Tabelle des Katalogs verwendet. Es sind keine anderen Katalogattribute oder Daten betroffen.

Wenn ` *`rootId`*` zu einem Katalog aufgelöst wird und ` *`objId`*` mit einem `catalog::Id` in diesem Katalog übereinstimmt, wird ` *`rootId/objId`*` effektiv durch den Katalogeintrag ersetzt, der in etwa so aussieht:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Verwandte Themen {#section-00e4f6b39cd14244bcce537a3f831259}

[Bildkatalog-Referenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anker=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
