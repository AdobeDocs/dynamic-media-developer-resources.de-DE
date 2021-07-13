---
description: Die grundlegende Syntax des HTTP-Protokolls lautet wie folgt.
solution: Experience Manager
title: Grundlegende Syntax des Image Serving-HTTP-Protokolls
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# Grundlegende Syntax des Image Serving-HTTP-Protokolls{#image-serving-http-protocol-basic-syntax}

Die grundlegende Syntax des HTTP-Protokolls lautet wie folgt:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Anfrage</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modifiers</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Objekt</span> </span> </p></td> 
  <td class="stentry"> <p>Quellobjektspezifikator (Bildpfad oder Eintrag im Bildkatalog). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifiers</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Name eines Befehlsmakros.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comment</span> </span> </p></td> 
  <td class="stentry"> <p>Kommentar-Zeichenfolge (vom Server ignoriert).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Einer der unterstützten Befehl- oder Attributnamen.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Name einer benutzerdefinierten Variablen.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Befehls- oder Variablenwert. </p></td> 
 </tr> 
</table>

*`server_address`*,  *`cmdName`*,  *`macro`* und  *`var`* unterscheiden nicht zwischen Groß- und Kleinschreibung. Der Server behält die Groß-/Kleinschreibung aller anderen Zeichenfolgenwerte bei.

*`value`* ist befehlsspezifisch und kann aus einem oder mehreren durch Kommas getrennten Werten bestehen. Weitere Informationen finden Sie in der Beschreibung der einzelnen Befehle .

## Server-Kennung {#section-926ae55ddba14b8d952147a5fd701e14}

Der Stammkontext [!DNL /is/image] ist für alle HTTP-Anfragen an Image Serving erforderlich.

## HTTP-Dekodierung {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving extrahiert zunächst *`object`* und *`modifiers`* aus der eingehenden Anfrage. *`object`* wird dann in Pfadelemente aufgeteilt, die einzeln HTTP-dekodiert sind. Die *`modifiers`*-Zeichenfolge wird in *`command`*= *`value`*-Paare unterteilt und *`value`* wird dann vor der befehlsspezifischen Verarbeitung HTTP-dekodiert.

>[!NOTE]
>
>Sofern in der Dokumentation nicht anders angegeben, müssen alle unsicheren Zeichen gemäß dem HTTP-Standard kodiert werden. Weitere Informationen finden Sie in der HTTP-Spezifikation .

## Kommentare {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Kommentare können überall in Anforderungszeichenfolgen eingebettet werden und werden durch einen Punkt (.) identifiziert unmittelbar auf das Befehlstrennzeichen (&amp;) folgen. Der Kommentar wird durch das nächste Vorkommen eines (nicht kodierten) Befehlstrennzeichens beendet. Mit dieser Funktion können Informationen zur Anforderung hinzugefügt werden, die nicht für die Image-Serving-Verwendung vorgesehen ist, z. B. Zeitstempel und Datenbank-IDs.

## Verwandte Themen {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Datentypen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa),  [HTTP/1.1-Spezifikation](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
