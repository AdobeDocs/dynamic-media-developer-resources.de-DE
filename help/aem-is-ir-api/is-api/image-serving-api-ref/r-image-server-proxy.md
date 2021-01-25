---
description: Ein Image-Server-Proxy kann verwendet werden, um die Größe von Bildern für japanische Telefone zu ändern.
seo-description: Ein Image-Server-Proxy kann verwendet werden, um die Größe von Bildern für japanische Telefone zu ändern.
seo-title: Image-Server-Proxy
solution: Experience Manager
title: Image-Server-Proxy
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Image-Server-Proxy{#image-server-proxy}

Ein Image-Server-Proxy kann verwendet werden, um die Größe von Bildern für japanische Telefone zu ändern.

## URL-Format {#section-2e8c40b0547c4f99874cdf502b338940}

Das URL-Format für den IS-Proxy ist mit den normalen IS-Anforderungen sehr ähnlich. Alle an den Proxy weitergeleiteten IS-Modifikatoren werden an den Image-Server weitergeleitet. Informationen zu den IS-Modifikatoren finden Sie in der [HTTP-Protokollreferenz](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Proxy-spezifische Modifikator-Liste {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Gibt den Prozentsatz der nutzbaren Breite des Geräts an, der als Bildbreite verwendet werden soll. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Gibt den Prozentsatz der nutzbaren Höhe des Geräts als Bildhöhe an. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Gibt den Prozentsatz der Eigenschaft "Speichergrenze für eingebettete Medien"des Geräts an, auf den die Antwortgröße beschränkt werden soll. Dies gilt nur für JPG-Antworten. Die Bildqualität wird verringert, bis die Antwortgröße innerhalb des angegebenen Prozentsatzes liegt. </p></td> 
 </tr> 
</table>

## Maximale Speicherkapazität für eingebettete Bilder {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Wenn das Gerät eine Beschränkung der Größe von Bildern hat, die auf einer Webseite eingebettet werden können, ist die Bildgröße auf diese Größe beschränkt, solange das Antwortformat jpg ist. Der Proxy begrenzt die Antworten auf 500 MB, wenn das Gerät keine Beschränkung hat.

## Backend processing {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Der Proxy lädt die Geräteatlas-Datendatei einmal täglich herunter, prüft sie und lädt sie. Bei der Überprüfung werden verschiedene Eigenschaften für verschiedene Geräte herausgezogen und mit den erwarteten Werten verglichen, bevor die neuen Daten akzeptiert werden.
