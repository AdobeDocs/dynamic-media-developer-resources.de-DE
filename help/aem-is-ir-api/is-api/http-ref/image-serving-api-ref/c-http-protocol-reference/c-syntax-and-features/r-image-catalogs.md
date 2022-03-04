---
description: Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.
solution: Experience Manager
title: Bildkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# Bildkataloge{#image-catalogs}

Die Funktionen und die Syntax von Bildkatalogen werden in diesem Abschnitt beschrieben.

Bildkataloge bieten die folgenden Funktionen:

* Ermöglicht die dauerhafte Verknüpfung von Bildern mit bestimmten Metadaten- und Modifikatorbefehlen.

   Einträge in Bildkatalogen werden mit einer Tastenkombination referenziert `*`rootId/objId`*`, wobei `*`rootId`*` identifiziert den Bildkatalog und `*`objId`*` identifiziert einen Datensatz im Katalog.
* Stellen Sie Standardwerte für bestimmte Anforderungsattribute bereit, z. B. die JPEG-Qualität oder die Frage, ob ein Wasserzeichen angewendet werden soll.
* Schriftarten, ICC-Profile, Makrodefinitionen und Anforderungsvorlagen verwalten

Selbst wenn keine bestimmten Bildkataloge definiert sind, sind alle Funktionen von Bildkatalogen über den Standardkatalog verfügbar ( [!DNL default.ini]).

Wenn `*`rootId`*` im URL-Pfad der Anforderung übereinstimmt mit `attribute::RootId` eines bestimmten Bildkatalogs wird dieser Katalog zum Hauptkatalog für diese Anforderung. Der Hauptkatalog enthält die Standardattribute und -einstellungen für die gesamte Anforderung. Wenn keine Übereinstimmung gefunden wird, wird stattdessen der Standardkatalog verwendet.

Ein in einem `src=` oder `mask=` -Befehl stellt die folgenden Katalogattribute und Daten für die aktuelle Ebene bereit:

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
   <td> <p> Standard für <span class="codeph"> catalog::Expiration</span> oder Ablauf der aktuellen Ebene, wenn kein Katalogdatensatz beteiligt ist </p> </td> 
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
   <td> <p> Standard für <span class="codeph"> catalog::Resolution</span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog:Anchor</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> anchor=</span> Wert der aktuellen Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> Der kleinste Ablaufwert aller Ebenen wird als Live-Zeitwert des Antwortbilds verwendet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> das Farbprofil des Quellbilds für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Map</span> </p> </td> 
   <td> <p> die Imagemap-Daten für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> Standard für <span class="codeph"> mask=</span> für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> Präfixbefehle für die aktuelle Ebene (jeder Befehl in <span class="codeph"> catalog::Modifier</span> kann durch denselben Befehl in der URL überschrieben werden, wenn er für dieselbe Ebene angegeben ist.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> die Quellbilddatei für die aktuelle Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> Postfix-Befehle für die aktuelle Ebene (ähnlich wie <span class="codeph"> catalog::Modifier</span>, jedoch Befehle in <span class="codeph"> catalog::PostModifier</span> dieselben Befehle außer Kraft setzen, die in der URL oder in <span class="codeph"> catalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> die Objektauflösung der aktuellen Ebene </p> </td> 
  </tr> 
 </tbody> 
</table>

Innerhalb derselben Ebene `src=` und `mask=` muss auf denselben Bildkatalog verweisen (falls vorhanden).

Ein in einem `icc=` -Befehl wird nur verwendet, um einen Eintrag aus der ICC-Profiltabelle des Katalogs nachzuschlagen. Es sind keine anderen Katalogattribute oder -daten beteiligt.

Wenn `*`rootId`*` in einen Katalog aufgelöst und `*`objId`*` wird mit einem `catalog::Id` in diesem Katalog, dann `*`rootId/objId`*` durch den Katalogeintrag ersetzt wird, was in etwa so aussieht:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Verwandte Themen {#section-00e4f6b39cd14244bcce537a3f831259}

[Referenz zum Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
