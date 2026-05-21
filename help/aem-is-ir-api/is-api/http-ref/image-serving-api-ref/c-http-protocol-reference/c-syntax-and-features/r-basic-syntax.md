---
description: Die grundlegende Syntax des HTTP-Protokolls sieht wie folgt aus.
solution: Experience Manager
title: Grundlegende Syntax des Image Serving-HTTP-Protokolls
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
TQID: 'https://experienceleague.adobe.com/fB60CyCuBYstiJJesDefrK1DW7w-2t0PJqqt-iLgZOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 1%

---

# Grundlegende Syntax des Image Serving-HTTP-Protokolls{#image-serving-http-protocol-basic-syntax}

Die grundlegende Syntax des HTTP-Protokolls sieht wie folgt aus:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Anfrage</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> Modifiers</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Objekt</span> </span> </p></td> 
  <td class="stentry"> <p>Source-Objektbezeichner (Bildpfad oder Bildkatalogeintrag). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Modifikatoren</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Modifikator</span>*[&amp;<span class="varname"> Modifikator</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Modifikator</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">Befehl|{$<span class="varname"> Makro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Befehl</span> </span> </p> </td> 
  <td class="stentry"> <p><code>{</code><span class="varname"> cmdName</span>|<code>{$</code><span class="varname"> var</span><code>}}[=</code><span class="varname">-Wert</span><code>]</code> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Makro</span> </span> </p> </td> 
  <td class="stentry"> <p>Name eines Befehlsmakros.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Kommentar</span> </span> </p></td> 
  <td class="stentry"> <p>Kommentarzeichenfolge (vom Server ignoriert).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Einer der unterstützten Befehls- oder Attributnamen.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Name einer benutzerdefinierten Variablen.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Wert</span> </span> </p></td> 
  <td class="stentry"> <p>Wert des Befehls oder der Variablen. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* und *`var`* wird nicht zwischen Groß- und Kleinschreibung unterschieden. Der Server behält die Groß-/Kleinschreibung aller anderen Zeichenfolgenwerte bei.

*`value`* ist befehlsspezifisch und kann aus einem oder mehreren Werten bestehen, die durch Kommas getrennt sind. Weitere Informationen finden Sie in der Beschreibung der einzelnen Befehle.

## Server-Kennung {#section-926ae55ddba14b8d952147a5fd701e14}

Der [!DNL /is/image]-Stammkontext ist für alle HTTP-Anfragen an Image Serving erforderlich.

## HTTP-Dekodierung {#section-20922baccd804d2d986b44ce9a183a7d}

Die Bildbereitstellung extrahiert zunächst *`object`* und *`modifiers`* aus der eingehenden Anfrage. *`object`* wird dann in Pfadelemente aufgeteilt, die einzeln HTTP-decodiert werden. Die *`modifiers`* Zeichenfolge wird in *`command`*= *`value`* Paare aufgeteilt und *`value`* vor der befehlsspezifischen Verarbeitung HTTP-decodiert.

>[!NOTE]
>
>Sofern in der Dokumentation nicht anders angegeben, müssen alle unsicheren Zeichen gemäß dem HTTP-Standard codiert werden. Weitere Informationen finden Sie in der HTTP-Spezifikation .

## Kommentare {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Kommentare können überall in Anfragezeichenfolgen eingebettet werden und werden durch einen Punkt (.) gekennzeichnet. unmittelbar nach dem Befehl separator(&amp;). Der Kommentar wird beim nächsten Auftreten eines (nicht kodierten) Befehlstrennzeichens beendet. Mit dieser Funktion können Sie der Anfrage Informationen hinzufügen, die nicht für die Bildbereitstellung vorgesehen sind, z. B. Zeitstempel und Datenbank-IDs.

## Verwandte Themen {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Datentypen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1 Spezifikation](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
