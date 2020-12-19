---
description: Profil der Ausgabefarbe.
seo-description: Profil der Ausgabefarbe.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 1%

---


# icc{#icc}

Profil der Ausgabefarbe.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profil</span></span> </p></td> 
  <td class="stentry"> <p>ICC-Profil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>wahrnehmungsfähig | relative | Sättigung | absolut </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1, um die Blackpoint-Kompensation zu aktivieren, 0, um sie zu deaktivieren. </p></td> 
 </tr> 
</table>

*`profile`* Gibt das Profil für den Ausgabefarbraum an, in den das gerenderte Profil konvertiert werden soll, wenn es sich vom bearbeiteten unterscheidet. *`profile`* muss entweder eine gültige  `icc::Name` Definition in der ICC-Profil-Map eines Bildkatalogs oder eines Standardkatalogs oder ein relativer Pfad zu einer Profil-Datei sein (normalerweise mit  [!DNL .icc]oder  [!DNL .icm] Suffix).

>[!NOTE]
>
>*`profile`* darf keine &quot;,&quot;-Zeichen enthalten, auch wenn HTTP-kodiert.

*`renderIntent`* ermöglicht das Überschreiben der standardmäßigen Renderpriorität.

*`blackpointComp`* aktiviert die Blackpoint-Kompensation, wenn das Output-Profil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle Auswahlmöglichkeiten *`renderIntent`* und *`blackpointComp`*. Normalerweise werden diese Einstellungen nur berücksichtigt, wenn das ICC-Output-Profil ein Ausgabegerät wie einen Drucker oder einen Monitor kennzeichnet. Einige ICC-Output-Profil unterstützen auch nicht alle *`renderIntent`*-Auswahlmöglichkeiten.

## Eigenschaften {#section-b4042623a8ea40248c11b2153e5906b1}

Kann an einer beliebigen Stelle innerhalb der Anforderung auftreten. Es wird ein Fehler zurückgegeben, wenn der Bildtyp mit `fmt=` nicht mit *`profile`* übereinstimmt.

*`renderIntent`* und  *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind.

CMYK-Ausgabegerät-Profil unterstützen mit höherer Wahrscheinlichkeit unterschiedliche Renderprioritäten.

## Standard {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Wenn das Farbmanagement aktiviert ist und `icc=` nicht angegeben ist, stellt der Server das in das Ausgabebild ( `attribute::IccProfile*`) konvertierte Profil ( &lt;a1/>) bereit, das dem mit `fmt=` angegebenen Bildtyp entspricht.

Wenn nicht angegeben, wird *`renderIntent`* von `attribute::IccRenderIntent` geerbt und *`blackpointComp`* von `attribute::IccBlackPointCompensation` übernommen.

## Verwandte Themen {#section-37ef83149fd74345956a98f633cc0294}

[Farbmanagement](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d),  [Attribut::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [Attribut::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [Attribut::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
