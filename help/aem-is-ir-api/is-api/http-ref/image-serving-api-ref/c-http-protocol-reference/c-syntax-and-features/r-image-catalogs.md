---
description: Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.
solution: Experience Manager
title: Bildkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Bildkataloge{#image-catalogs}

Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.

Bildkataloge bieten die folgenden Funktionen:

* Ermöglicht die persistente Zuordnung von Bildern zu bestimmten Metadaten und Modifikatorbefehlen.

  Einträge in Bildkatalogen werden mit der Verknüpfungsnotation `*`rootId/objId`*` referenziert, wobei `*`rootId`*` den Bildkatalog und `*`objId`*` einen Datensatz im Katalog bezeichnet.
* Geben Sie Standardwerte für bestimmte Anforderungsattribute an, z. B. die JPEG-Qualität oder ob ein Wasserzeichen angewendet werden soll.
* Schriftarten, ICC-Profile, Makrodefinitionen und Anfragevorlagen verwalten

Selbst wenn keine spezifischen Bildkataloge definiert sind, sind alle Funktionen von Bildkatalogen über den Standardkatalog verfügbar ( [!DNL default.ini]).

Wenn `*`rootId`*` im URL-Pfad der Anfrage mit `attribute::RootId` eines bestimmten Bildkatalogs übereinstimmt, wird dieser Katalog zum Hauptkatalog für diese Anfrage. Der Hauptkatalog stellt die Standardattribute und Einstellungen für die gesamte Anfrage bereit. Wenn keine Übereinstimmung gefunden wird, wird stattdessen der Standardkatalog verwendet.

Ein in einem `src=`- oder `mask=`-Befehl identifizierter Katalog stellt der aktuellen Ebene die folgenden Katalogattribute und Daten bereit:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>/Daten</b> </th> 
   <th class="entry"> <b> Anmerkungen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">::DefaultExt</span> </p> </td> 
   <td> <p> Die Standarderweiterung für alle Bilddateipfade in der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Expiration</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> Katalog::Expiration</span> oder Expiration der aktuellen Ebene, wenn kein Katalogdatensatz beteiligt ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::icc*</span> </p> </td> 
   <td> <p> Das funktionierende ICC-Farbprofil, die Render-Absicht und die Blackpoint-Kompensations-Markierung für die Anfrage und/oder die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::RootPath</span> </p> </td> 
   <td> <p> Wird für alle Quelldateipfade der aktuellen Ebene verwendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Resolution</span> </p> </td> 
   <td> <p> Standard nur für <span class="codeph"> Katalog::Auflösung</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Anchor</span> </p> </td> 
   <td> <p> Standard für den <span class="codeph"> Anker=</span> Wert der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Expiration</span> </p> </td> 
   <td> <p> Der kleinste Gültigkeitswert aller Ebenen wird als Time-to-Live-Wert des Antwortbildes verwendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::IccProfile</span> </p> </td> 
   <td> <p> Das Farbprofil des Quellbildes für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Map</span> </p> </td> 
   <td> <p> Die Imagemap-Daten für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::MaskPath</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> Maske=</span> für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Modifier</span> </p> </td> 
   <td> <p> -Präfixbefehle für die aktuelle Ebene (jeder Befehl in <span class="codeph"> Catalog::Modifier</span> kann mit demselben Befehl in der URL überschrieben werden, wenn er für dieselbe Ebene angegeben ist) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Path</span> </p> </td> 
   <td> <p> Die Quellbilddatei für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::PostModifier</span> </p> </td> 
   <td> <p> Postfix-Befehle für die aktuelle Ebene (ähnlich wie <span class="codeph"> catalog::Modifier</span>, aber Befehle in <span class="codeph"> catalog::PostModifier</span> überschreiben dieselben Befehle, die in der URL oder <span class="codeph"> catalog::Modifier</span> angegeben sind </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Resolution</span> </p> </td> 
   <td> <p> Die Objektauflösung der aktuellen Ebene </p> </td> 
  </tr> 
 </tbody> 
</table>

Innerhalb derselben Ebene müssen `src=` und `mask=` auf denselben Bildkatalog verweisen (falls vorhanden).

Ein in einem `icc=`-Befehl identifizierter Katalog wird nur zum Nachschlagen eines Eintrags aus der ICC-Profiltabelle des Katalogs verwendet. Es sind keine anderen Katalogattribute oder Daten beteiligt.

Wenn `*`rootId`*` in einen Katalog aufgelöst wird und `*`objId`*` mit einem `catalog::Id` in diesem Katalog abgeglichen wird, wird `*`rootId/objId`*` effektiv durch den Katalogeintrag ersetzt, der etwa wie folgt aussieht:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Verwandte Themen {#section-00e4f6b39cd14244bcce537a3f831259}

[Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
