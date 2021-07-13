---
description: Ein Image-Server-Proxy kann verwendet werden, um die Größe von Bildern für japanische Telefone zu ändern.
solution: Experience Manager
title: Image-Server-Proxy
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Image-Server-Proxy{#image-server-proxy}

Ein Image-Server-Proxy kann verwendet werden, um die Größe von Bildern für japanische Telefone zu ändern.

## URL-Format {#section-2e8c40b0547c4f99874cdf502b338940}

Das URL-Format für den IS-Proxy ähnelt sehr normalen IS-Anforderungen. Alle an den Proxy übergebenen IS-Modifikatoren werden an den Image-Server übergeben. Informationen zu den IS-Modifikatoren finden Sie in der [HTTP-Protokollreferenz](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Proxy-spezifische Modifikatorliste {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Gibt den Prozentsatz der nutzbaren Breite des Geräts an, der als Bildbreite verwendet werden soll. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Gibt den Prozentsatz der nutzbaren Höhe des Geräts an, der als Bildhöhe verwendet werden soll. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Gibt den Prozentsatz der Eigenschaft "Speicherlimit für eingebettete Medien"des Geräts an, auf den die Antwortgröße beschränkt werden soll. Dies gilt nur für jpg-Antworten. Die Bildqualität wird verringert, bis die Antwortgröße innerhalb des festgelegten Prozentsatzes liegt. </p></td> 
 </tr> 
</table>

## Speicherlimit für eingebettete Bilder {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Wenn das Gerät eine Beschränkung der Größe von Bildern hat, die auf einer Web-Seite eingebettet werden können, ist die Bildgröße auf diese Größe beschränkt, solange das Antwortformat jpg ist. Der Proxy begrenzt die Antworten auf 500 MB, wenn das Gerät keine Beschränkung hat.

## Backend-Verarbeitung {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Der Proxy lädt die Device Atlas-Datendatei einmal täglich herunter, überprüft und lädt sie. Die Überprüfung ruft verschiedene Eigenschaften für verschiedene Geräte ab und vergleicht sie mit den erwarteten Werten, bevor die neuen Daten akzeptiert werden.
