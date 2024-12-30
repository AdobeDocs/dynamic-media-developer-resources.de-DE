---
title: ICC
description: Ausgabefarbprofil.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# ICC{#icc}

Ausgabefarbprofil.

ICC= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Profil</span></span> </p></td> 
  <td class="stentry"> <p>ICC-Farbprofil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>wahrnehmungsorientiert | Verwandter | Sättigung | absolut </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 zu aktivieren, 0 zum Deaktivieren der Schwarzpunktkompensation. </p></td> 
 </tr> 
</table>

*`profile`* Gibt das Profil des Ausgabefarbraums an, in den das gerenderte Bild konvertiert werden soll, wenn es sich vom Arbeitsprofil unterscheidet. *`profile`* Muss entweder ein gültiger `icc::Name` sein, der in der ICC-Profilzuordnung eines Bildkatalogs oder Standardkatalogs definiert ist, oder ein relativer Pfad zu einer Profildatei (normalerweise mit [!DNL `.icc`] oder [!DNL `.icm`] Suffix).

>[!NOTE]
>
>*`profile`* darf keine &quot;,“-Zeichen enthalten, auch wenn HTTP-kodiert ist.

*`renderIntent`* Ermöglicht das Überschreiben des standardmäßigen Rendering-Intents.

*`blackpointComp`* Aktiviert die Schwarzpunktkompensation, wenn das Ausgabeprofil diese Funktion unterstützt.

>[!NOTE]
>
>Nicht alle Farbkonvertierungen unterstützen alle *`renderIntent`*- und *`blackpointComp`*. In der Regel werden diese Einstellungen nur berücksichtigt, wenn das ICC-Ausgabeprofil ein Ausgabegerät, z. B. einen Drucker oder einen Monitor, charakterisiert. Außerdem unterstützen einige ICC-Ausgabeprofile nicht alle *`renderIntent`*.

## Eigenschaften {#section-b4042623a8ea40248c11b2153e5906b1}

Kann überall in der Anfrage auftreten. Ein Fehler wird zurückgegeben, wenn der Bildtyp mit angegeben wird `fmt=` nicht mit *`profile`* übereinstimmt.

Sowohl *`renderIntent`* als auch *`blackpointComp`* werden ignoriert, wenn sie nicht mit dem angegebenen ICC-Profil kompatibel sind.

CMYK-Ausgabegeräteprofile unterstützen mit höherer Wahrscheinlichkeit unterschiedliche Rendering-Intents.

## Standard {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Wenn das Farbmanagement aktiviert ist und `icc=` nicht angegeben ist, stellt der Server das Bild bereit, das in das Ausgabeprofil (`attribute::IccProfile*`) konvertiert wurde, das dem mit `fmt=` angegebenen Bildtyp entspricht.

Wenn nichts angegeben ist, wird *`renderIntent`* von `attribute::IccRenderIntent` und *`blackpointComp`* von `attribute::IccBlackPointCompensation` geerbt.

## Verwandte Themen {#section-37ef83149fd74345956a98f633cc0294}

[Farbmanagement](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
