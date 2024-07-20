---
title: icc
description: Profil der Ausgabefarben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# icc{#icc}

Profil der Ausgabefarben.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profile</span></span> </p></td> 
  <td class="stentry"> <p>ICC-Farbprofil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>perceptual | relative | Sättigung | absolute </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 zur Aktivierung, 0 zur Deaktivierung der Blackpoint-Kompensation. </p></td> 
 </tr> 
</table>

*`profile`* Gibt das Profil des Ausgabefarbraums an, in den das gerenderte Bild konvertiert werden soll, wenn es sich vom Arbeitsprofil unterscheidet. *`profile`* Muss entweder eine gültige `icc::Name` sein, die in der ICC-Profilzuordnung eines Bildkatalogs oder Standardkatalogs definiert ist, oder ein relativer Pfad zu einer Profildatei (normalerweise mit dem Suffix [!DNL `.icc`] oder [!DNL `.icm`]).

>[!NOTE]
>
>*`profile`* Darf auch keine &quot;,&quot;-Zeichen enthalten, selbst wenn HTTP-kodiert.

*`renderIntent`* Ermöglicht das Überschreiben des standardmäßigen Rendering-Intents.

*`blackpointComp`* Aktiviert die Blackpoint-Kompensation, wenn das Ausgabeprofil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle Optionen *`renderIntent`* und *`blackpointComp`*. In der Regel werden diese Einstellungen nur berücksichtigt, wenn das ICC-Ausgabeprofil ein Ausgabegerät wie einen Drucker oder einen Monitor charakterisiert. Einige ICC-Ausgabeprofile unterstützen auch nicht alle *`renderIntent`*-Optionen.

## Eigenschaften {#section-b4042623a8ea40248c11b2153e5906b1}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Wenn der Bildtyp mit `fmt=` nicht mit *`profile`* übereinstimmt, wird ein Fehler zurückgegeben.

Sowohl *`renderIntent`* als auch *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind.

Die Wahrscheinlichkeit, dass CMYK-Ausgabegeräteprofile verschiedene Rendering-Intents unterstützen, ist höher.

## Standard {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Wenn das Farbmanagement aktiviert ist und `icc=` nicht angegeben ist, stellt der Server das in das Ausgabeprofil ( `attribute::IccProfile*`) konvertierte Bild bereit, das dem mit `fmt=` angegebenen Bildtyp entspricht.

Wenn nichts angegeben ist, wird *`renderIntent`* von `attribute::IccRenderIntent` vererbt und *`blackpointComp`* von `attribute::IccBlackPointCompensation` vererbt.

## Verwandte Themen {#section-37ef83149fd74345956a98f633cc0294}

[Farbmanagement](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
