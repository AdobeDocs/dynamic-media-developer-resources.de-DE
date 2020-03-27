---
description: Farbprofil für Ausgabe.
seo-description: Farbprofil für Ausgabe.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

Farbprofil für Ausgabe.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Objekt</span></span> </p></td> 
  <td class="stentry"> <p>ICC-Profil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perzeptiv|relative|sättigung|absolut</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1, um die Blackpoint-Kompensation zu aktivieren, 0, um sie zu deaktivieren. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Dither</span></span> </p></td> 
  <td class="stentry"> <p>1 zum Aktivieren, 0 zum Deaktivieren des Ditherings. </p></td> 
 </tr> 
</table>

*`object`* Gibt das Profil für den Ausgabefarbraum an, in den das Profil konvertiert werden soll, wenn es sich vom bearbeiteten unterscheidet. *`profile`* muss entweder eine gültige `icc::Name` Definition in der ICC-Profil-Map eines Bildkatalogs oder eines Standardkatalogs oder ein relativer Pfad zu einer Profil-Datei sein (normalerweise mit [!DNL .icc] oder [!DNL .icm] Suffix). See [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)for additional information.

>[!NOTE]
>
>*`object`* darf keine &quot;,&quot;-Zeichen enthalten, auch wenn HTTP-kodiert.

*`renderIntent`* ermöglicht das Überschreiben der standardmäßigen Renderpriorität.

*`blackpointComp`* aktiviert die Blackpoint-Kompensation, wenn das Output-Profil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle *`renderIntent`* und *`blackpointComp`* Auswahlmöglichkeiten. Normalerweise werden diese Einstellungen nur berücksichtigt, wenn das ICC-Output-Profil ein Ausgabegerät wie einen Drucker oder einen Monitor kennzeichnet. Einige ICC-Output-Profil unterstützen nicht alle *`renderIntent`* Optionen.

Notiz

*`dither`* ermöglicht Dithering (tatsächlich Fehlerdiffusion), wodurch Farbbanding-Artefakte vermieden oder reduziert werden können.

## Eigenschaften {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Anforderungsattribut. Der Server gibt einen Fehler zurück, wenn ein Bildtyp angegeben ist, mit `fmt=` dem nicht übereinstimmt *`profile`*.

*`renderIntent`* und *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind. CMYK-Ausgabegerät-Profil unterstützen mit höherer Wahrscheinlichkeit unterschiedliche Renderprioritäten.

## Standard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Wenn das Farbmanagement aktiviert ist und nicht angegeben `icc=` ist, stellt der Server das in das Ausgabebild ( `attribute::IccProfile*`) konvertierte Profil bereit, das mit dem angegebenen Bildtyp übereinstimmt `fmt=`.

Wenn nicht angegeben, *`renderIntent`* wird von `attribute::IccRenderIntent`geerbt, *`blackpointComp`* wird von `attribute::IccBlackPointCompensation`übernommen und *`dither`* wird von `attribute::IccDither`.

## Verwandte Themen {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[objectWorkflow,Color Managementσ,ICC Profil ReferenceσiccEmbed](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
