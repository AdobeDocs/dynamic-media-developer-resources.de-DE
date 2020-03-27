---
description: 'Die grundlegende Syntax des HTTP-Protokolls lautet wie folgt:'
seo-description: 'Die grundlegende Syntax des HTTP-Protokolls lautet wie folgt:'
seo-title: Grundlegende Syntax des Image Serving-HTTP-Protokolls
solution: Experience Manager
title: Grundlegende Syntax des Image Serving-HTTP-Protokolls
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Grundlegende Syntax des Image Serving-HTTP-Protokolls{#image-serving-http-protocol-basic-syntax}

Die grundlegende Syntax des HTTP-Protokolls lautet wie folgt:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Anforderung</span></span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> Modifikatoren</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Server </span></span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Objekt</span></span> </p></td> 
  <td class="stentry"> <p>Quell-Objektspezifikator (Bildpfad oder Bildkatalogeintrag). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Modifikatoren</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Modifikator</span>*[&amp;<span class="varname"> Modifikator</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> -Modifikator</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> , Befehl</span></span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> Wert</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Makro</span></span> </p> </td> 
  <td class="stentry"> <p>Name eines Befehlmakros. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Kommentar</span></span> </p></td> 
  <td class="stentry"> <p>Kommentarzeichenfolge (vom Server ignoriert). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span></span> </p></td> 
  <td class="stentry"> <p>Einer der unterstützten Befehl- oder Attributnamen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span></span> </p> </td> 
  <td class="stentry"> <p>Name einer benutzerdefinierten Variablen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Wert</span></span> </p></td> 
  <td class="stentry"> <p>Befehls- oder Variablenwert. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* und *`var`* die Groß-/Kleinschreibung wird nicht beachtet. Der Server behält die Groß-/Kleinschreibung aller anderen Zeichenfolgenwerte bei.

*`value`* ist befehlsspezifisch und kann aus einem oder mehreren durch Kommas getrennten Werten bestehen. Einzelheiten dazu finden Sie in der Beschreibung der einzelnen Befehle.

## Server-ID {#section-926ae55ddba14b8d952147a5fd701e14}

Der [!DNL /is/image] Stammkontext ist für alle HTTP-Anforderungen an Image Serving erforderlich.

## HTTP-Dekodierung {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving extrahiert zuerst *`object`* und *`modifiers`* aus der eingehenden Anforderung. *`object`* wird dann in Pfadelemente aufgeteilt, die einzeln HTTP-dekodiert sind. Die *`modifiers`* Zeichenfolge wird in *`command`*= *`value`* *`value`* -Paare aufgeteilt und anschließend vor der Befehlsverarbeitung HTTP-dekodiert.

>[!NOTE]
>
>Sofern in der Dokumentation nicht anders angegeben, müssen alle unsicheren Zeichen gemäß dem HTTP-Standard kodiert werden. Weitere Informationen finden Sie in der HTTP-Spezifikation.

## Kommentare {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Kommentare können überall in Anforderungszeichenfolgen eingebettet werden und durch einen Punkt (.) gekennzeichnet werden. unmittelbar nach dem Befehl separator(&amp;). Der Kommentar wird durch das nächste Vorkommen eines (nicht kodierten) Befehlstrennzeichens beendet. Diese Funktion kann verwendet werden, um Informationen zur Anforderung hinzuzufügen, die nicht zur Verwendung mit Image Serving bestimmt sind, wie Zeitstempel, Datenbank-IDs usw.

## Verwandte Themen {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Datentypen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1-Spezifikation](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
