---
description: Details zur Fehlermeldung. Gibt die Detailebene für Fehlermeldungen an, die über HTTP als error.message-Wert zurückgegeben werden.
solution: Experience Manager
title: ErrorDetail
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 5%

---


# ErrorDetail{#errordetail}

Details zur Fehlermeldung. Gibt die Detailebene für Fehlermeldungen an, die über HTTP als error.message-Wert zurückgegeben werden.

Die folgenden Werte sind zulässig:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Nur Titel. Gibt eine kurze allgemeine Beschreibung des Fehlers zurück. Empfohlen für Live-Server, auf die öffentlich zugegriffen werden kann. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Kurze Nachricht. Für zukünftige Verwendung reserviert. Gibt derzeit die gleichen Informationen wie 0 zurück. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detaillierte Meldung. Stellt Details zum Fehler auf Benutzerebene bereit. Kann vertrauliche Informationen wie Dateipfade enthalten. Empfohlen für Staging-, Qualitätssicherungs- und Anwendungsentwicklungsserver. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Vollständige Debugging-Informationen. Fügt ggf. Java-Stapelspuren hinzu. Fehlerbilder enthalten keine Stapelspuren und geben stattdessen Informationen der Stufe 2 in <span class="codeph"> $error.message</span> zurück. Diese Informationen können nützlich sein, wenn der Berichte Probleme mit dem technischen Support von Dynamic Media hat. </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-e167895723ca4ad4ba283d3d7b4324de}

Enumerierter Wert muss 0, 1, 2 oder 3 sein.

## Standard {#section-8f27098e509945a18676aca0675c8f41}

Von `default::ErrorDetail` übernommen, wenn nicht angegeben oder leer.

## Verwandte Themen {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
