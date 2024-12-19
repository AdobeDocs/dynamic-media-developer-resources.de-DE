---
description: Details der Fehlermeldung. Gibt den Detaillierungsgrad für Fehlermeldungen an, die über HTTP als error.message-Wert zurückgegeben werden.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

Details der Fehlermeldung. Gibt den Detaillierungsgrad für Fehlermeldungen an, die über HTTP als error.message-Wert zurückgegeben werden.

Die folgenden Werte sind zulässig:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Nur Titel. Gibt eine kurze allgemeine Beschreibung des Fehlers zurück. Empfohlen für Live-Server, die öffentlich zugänglich sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Kurze Nachricht. Reserviert für zukünftige Verwendung. Gibt derzeit dieselben Informationen wie 0 zurück. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detaillierte Nachricht. Enthält Details auf Benutzerebene zum Fehler. Kann vertrauliche Informationen wie Dateipfade enthalten. Empfohlen für Staging-, Qualitätssicherungs- und Anwendungsentwicklungsserver. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Vollständige Debug-Informationen. Fügt ggf. Java-Stacktraces hinzu. Fehlerbilder enthalten nie Stacktraces und geben stattdessen Informationen der Stufe 2 in <span class="codeph"> $error.message</span> zurück. Diese Informationen können beim Melden von Problemen an den technischen Support von Dynamic Media hilfreich sein. </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-e167895723ca4ad4ba283d3d7b4324de}

Aufzählungswert, muss 0, 1, 2 oder 3 sein.

## Standard {#section-8f27098e509945a18676aca0675c8f41}

Von `default::ErrorDetail` geerbt, wenn nicht angegeben oder leer.

## Verwandte Themen {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
