---
title: ICC
description: Ausgabefarbprofil.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# ICC{#icc}

Ausgabefarbprofil.

`icc= *`object`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Objekt</span> </span> </p></td> 
  <td class="stentry"> <p>ICC-Farbprofil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> Perzeptiv|Relativ|Sättigung|Absolut</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 zu aktivieren, 0 zum Deaktivieren der Schwarzpunktkompensation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> zaudern</span></span> </p></td> 
  <td class="stentry"> <p>1 zum Aktivieren, 0 zum Deaktivieren der Dithering-Funktion </p></td> 
 </tr> 
</table>

Der Wert *`object`* gibt das Profil des Ausgabefarbraums an, in den das Bild konvertiert werden soll, wenn es sich von dem des Arbeitsprofils unterscheidet. Der Wert *`profile`* muss entweder ein gültiger `icc::Name` sein, der in der ICC-Profilzuordnung eines Bildkatalogs oder Standardkatalogs definiert ist, oder ein relativer Pfad zu einer Profildatei (normalerweise mit [!DNL .icc] oder [!DNL .icm] Suffix). Weitere Informationen finden Sie unter [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) .

>[!NOTE]
>
>Der Wert *`object`* darf keine &quot;,“-Zeichen enthalten, auch wenn er HTTP-kodiert ist.

Der Wert *`renderIntent`* das Überschreiben des standardmäßigen Rendering-Intents.

Der Wert *`blackpointComp`* aktiviert die Schwarzpunktkompensation, wenn das Ausgabeprofil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle *`renderIntent`*- und *`blackpointComp`*. In der Regel werden diese Einstellungen nur berücksichtigt, wenn das ICC-Ausgabeprofil ein Ausgabegerät, z. B. einen Drucker oder einen Monitor, charakterisiert. Außerdem unterstützen einige ICC-Ausgabeprofile nicht alle *`renderIntent`*.

Notiz

Der Modifikator *`dither`* ermöglicht Dithering (tatsächliche Fehlerdiffusion), wodurch Farbbandfehler vermieden oder reduziert werden können.

## Eigenschaften {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Anforderungsattribut. Der Server gibt einen Fehler zurück, wenn ein Bildtyp mit `fmt=` angegeben wird, der nicht mit *`profile`* übereinstimmt.

Die Modifikatoren *`renderIntent`* und *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind. CMYK-Ausgabegeräteprofile unterstützen mit höherer Wahrscheinlichkeit unterschiedliche Rendering-Intents.

## Standard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Wenn das Farbmanagement aktiviert ist und `icc=` nicht angegeben ist, stellt der Server das Bild bereit, das in das Ausgabeprofil (`attribute::IccProfile*`) konvertiert wurde, das dem mit `fmt=` angegebenen Bildtyp entspricht.

Wenn nichts angegeben ist, wird *`renderIntent`* von `attribute::IccRenderIntent`, *`blackpointComp`* von `attribute::IccBlackPointCompensation` und *`dither`* von `attribute::IccDither` geerbt.

## Verwandte Themen {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
