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

* Ermöglicht die dauerhafte Verknüpfung von Bildern mit bestimmten Metadaten- und Modifikatorbefehlen.

  Einträge in Bildkatalogen werden mit der Kurzschreibweise `*`rootId/objId`*` referenziert, wobei `*`rootId`*` den Bildkatalog und `*`objId`*` einen Datensatz im Katalog angibt.
* Stellen Sie Standardwerte für bestimmte Anforderungsattribute bereit, z. B. die JPEG-Qualität oder die Frage, ob ein Wasserzeichen angewendet werden soll.
* Schriftarten, ICC-Profile, Makrodefinitionen und Anforderungsvorlagen verwalten

Selbst wenn keine bestimmten Bildkataloge definiert sind, sind alle Funktionen von Bildkatalogen über den Standardkatalog ( [!DNL default.ini]) verfügbar.

Wenn `*`rootId`*` im URL-Pfad der Anforderung mit `attribute::RootId` eines bestimmten Bildkatalogs übereinstimmt, wird dieser Katalog zum Hauptkatalog für diese Anforderung. Der Hauptkatalog enthält die Standardattribute und -einstellungen für die gesamte Anforderung. Wenn keine Übereinstimmung gefunden wird, wird stattdessen der Standardkatalog verwendet.

Ein in einem Befehl `src=` oder `mask=` identifizierter Katalog stellt die folgenden Katalogattribute und Daten für die aktuelle Ebene bereit:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Daten</b> </th> 
   <th class="entry"> <b> Hinweise</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> die Standarderweiterung für alle Bilddateipfade in der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Standardeinstellung für <span class="codeph"> -Katalog::Ablauf</span> oder Ablauf der aktuellen Ebene, wenn kein Katalogdatensatz beteiligt ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ICC*</span> </p> </td> 
   <td> <p> das funktionierende ICC-Farbprofil, die Rendering-Absicht und die Blackpoint-Kompensationskennzeichnung für die Anforderung und/oder die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> wird für alle Quelldateipfade der aktuellen Ebene verwendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> Standard nur für <span class="codeph"> -Katalog::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> Standardwert für den Wert <span class="codeph"> anchor=</span> der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> Der kleinste Ablaufwert aller Ebenen wird als Live-Zeitwert des Antwortbilds verwendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> das Quellbildfarbprofil für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> die Imagemap-Daten für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> mask=</span> für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> Präfixbefehle für die aktuelle Ebene (jeder Befehl im <span class="codeph">-Katalog::Modifier</span> kann durch denselben Befehl in der URL überschrieben werden, sofern er für dieselbe Ebene festgelegt ist) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> die Quellbilddatei für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> Postfix-Befehle für die aktuelle Ebene (ähnlich dem <span class="codeph"> -Katalog::Modifier</span>, aber Befehle im <span class="codeph"> -Katalog::PostModifier</span> überschreiben dieselben Befehle, die in der URL oder im <span class="codeph"> -Katalog angegeben sind::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> die Objektauflösung der aktuellen Ebene </p> </td> 
  </tr> 
 </tbody> 
</table>

Innerhalb derselben Ebene müssen `src=` und `mask=` auf denselben Bildkatalog verweisen (falls vorhanden).

Ein in einem `icc=` -Befehl identifizierter Katalog wird nur zum Nachschlagen eines Eintrags aus der ICC-Profiltabelle des Katalogs verwendet. Es sind keine anderen Katalogattribute oder -daten beteiligt.

Wenn `*`rootId`*` in einen Katalog aufgelöst wird und `*`objId`*` mit einem `catalog::Id` in diesem Katalog übereinstimmt, wird `*`rootId/objId`*` effektiv durch den Katalogeintrag in etwa folgender Form ersetzt:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Verwandte Themen {#section-00e4f6b39cd14244bcce537a3f831259}

[Referenz zum Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
