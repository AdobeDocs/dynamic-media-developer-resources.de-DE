---
description: Details der Fehlermeldung. Gibt den Detaillierungsgrad für Fehlermeldungen an, die über HTTP als error.message-Wert zurückgegeben werden.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
TQID: 'https://experienceleague.adobe.com/CZ2k-H1kZI3t3ZAtgm7qj8eo97u4NPmumdErNU--uvU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 168
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
  <td class="stentry"> <p>Vollständige Debug-Informationen. Fügt ggf. Java-Stacktraces hinzu. Fehlerbilder enthalten nie Stacktraces und geben stattdessen Informationen der Stufe 2 in <span class="codeph"> $error.message</span> zurück. Diese Informationen können beim Melden von Problemen an den technischen Support von Dynamic Media nützlich sein. </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-e167895723ca4ad4ba283d3d7b4324de}

Aufzählungswert, muss 0, 1, 2 oder 3 sein.

## Standard {#section-8f27098e509945a18676aca0675c8f41}

Von `default::ErrorDetail` geerbt, wenn nicht angegeben oder leer.

## Verwandte Themen {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
