---
title: icc
description: Farbprofil für Ausgabe.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 3%

---

# icc{#icc}

Farbprofil für Ausgabe.

`icc= *`Objekt`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Objekt</span> </span> </p></td> 
  <td class="stentry"> <p>ICC-Farbprofil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptual|relative|sättigung|absolute</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 zur Aktivierung, 0 zur Deaktivierung der Blackpoint-Kompensation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dither</span></span> </p></td> 
  <td class="stentry"> <p>1 zum Aktivieren, 0 zum Deaktivieren des Ditherings. </p></td> 
 </tr> 
</table>

Der Wert *`object`* gibt das Profil des Ausgabefarbraums an, in den das Bild konvertiert werden soll, wenn es sich vom Arbeitsprofil unterscheidet. Der Wert *`profile`* muss entweder ein gültiges `icc::Name` definiert in der ICC-Profilzuordnung eines Bildkatalogs oder Standardkatalogs oder eines relativen Pfads zu einer Profildatei (normalerweise mit [!DNL .icc] oder [!DNL .icm] Suffix). Siehe [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) für weitere Informationen.

>[!NOTE]
>
>Der Wert *`object`* darf keine &quot;,&quot;-Zeichen enthalten, auch wenn HTTP-kodiert.

Der Wert *`renderIntent`* ermöglicht das Überschreiben des standardmäßigen Rendering-Intents.

Der Wert *`blackpointComp`* ermöglicht eine Blackpoint-Kompensation, wenn das Ausgabeprofil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle *`renderIntent`* und *`blackpointComp`* auswählen. In der Regel werden diese Einstellungen nur berücksichtigt, wenn das ICC-Ausgabeprofil ein Ausgabegerät wie einen Drucker oder einen Monitor charakterisiert. Einige ICC-Ausgabeprofile unterstützen nicht alle *`renderIntent`* auswählen.

Notiz

Der Modifikator *`dither`* ermöglicht Dithering (tatsächlich Fehlerdiffusion), wodurch Farbstreifen-Artefakte vermieden oder reduziert werden können.

## Eigenschaften {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Anforderungsattribut. Der Server gibt einen Fehler zurück, wenn ein Bildtyp mit `fmt=` , die nicht übereinstimmt *`profile`*.

Die Modifikatoren *`renderIntent`* und *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind. Die Wahrscheinlichkeit, dass CMYK-Ausgabegeräteprofile verschiedene Rendering-Intents unterstützen, ist höher.

## Standard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Wenn das Farbmanagement aktiviert ist und `icc=` nicht angegeben ist, stellt der Server das in das Ausgabeprofil konvertierte Bild ( `attribute::IccProfile*`), der dem angegebenen Bildtyp entspricht, mit `fmt=`.

Falls nicht angegeben, *`renderIntent`* wird von `attribute::IccRenderIntent`, *`blackpointComp`* wird von `attribute::IccBlackPointCompensation`, und *`dither`* wird von `attribute::IccDither`.

## Verwandte Themen {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [Objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Farbmanagement](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [ICC-Profilzuordnungsreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
