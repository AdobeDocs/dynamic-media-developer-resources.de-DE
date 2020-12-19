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
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 5%

---


# icc{#icc}

Farbprofil für Ausgabe.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dither</span></span> </p></td> 
  <td class="stentry"> <p>1 zum Aktivieren, 0 zum Deaktivieren des Ditherings. </p></td> 
 </tr> 
</table>

*`object`* Gibt das Profil für den Ausgabefarbraum an, in den das Profil konvertiert werden soll, wenn es sich vom bearbeiteten unterscheidet. *`profile`* muss entweder eine gültige  `icc::Name` Definition in der ICC-Profil-Map eines Bildkatalogs oder eines Standardkatalogs oder ein relativer Pfad zu einer Profil-Datei sein (normalerweise mit  [!DNL .icc] oder  [!DNL .icm] Suffix). Weitere Informationen finden Sie unter [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

>[!NOTE]
>
>*`object`* darf keine &quot;,&quot;-Zeichen enthalten, auch wenn HTTP-kodiert.

*`renderIntent`* ermöglicht das Überschreiben der standardmäßigen Renderpriorität.

*`blackpointComp`* aktiviert die Blackpoint-Kompensation, wenn das Output-Profil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle Auswahlmöglichkeiten *`renderIntent`* und *`blackpointComp`*. Normalerweise werden diese Einstellungen nur berücksichtigt, wenn das ICC-Output-Profil ein Ausgabegerät wie einen Drucker oder einen Monitor kennzeichnet. Einige ICC-Output-Profil unterstützen auch nicht alle *`renderIntent`*-Auswahlmöglichkeiten.

Notiz

*`dither`* ermöglicht Dithering (tatsächlich Fehlerdiffusion), wodurch Farbbanding-Artefakte vermieden oder reduziert werden können.

## Eigenschaften {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Anforderungsattribut. Der Server gibt einen Fehler zurück, wenn ein Bildtyp mit `fmt=` angegeben wurde, der nicht mit *`profile`* übereinstimmt.

*`renderIntent`* und  *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind. CMYK-Ausgabegerät-Profil unterstützen mit höherer Wahrscheinlichkeit unterschiedliche Renderprioritäten.

## Standard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Wenn das Farbmanagement aktiviert ist und `icc=` nicht angegeben ist, stellt der Server das in das Ausgabebild ( `attribute::IccProfile*`) konvertierte Profil ( &lt;a1/>) bereit, das dem mit `fmt=` angegebenen Bildtyp entspricht.

Wenn nicht angegeben, wird *`renderIntent`* von `attribute::IccRenderIntent` geerbt, *`blackpointComp`* von `attribute::IccBlackPointCompensation` und *`dither`* wird von `attribute::IccDither` geerbt.

## Verwandte Themen {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)  [objectWorkflow,Color Managementσ,ICC Profil ReferenceσiccEmbed](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
