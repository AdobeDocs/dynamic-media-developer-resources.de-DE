---
description: Fehlermeldungsdetails. Gibt die Detailtiefe für Fehlermeldungen an, die über HTTP als error.message -Wert zurückgegeben werden.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# ErrorDetail{#errordetail}

Fehlermeldungsdetails. Gibt die Detailtiefe für Fehlermeldungen an, die über HTTP als error.message -Wert zurückgegeben werden.

## Titel {#section-c10d75d72ee24d16a67cc8d927f1deba}

Die folgenden Werte sind zulässig:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Nur Titel. Gibt eine kurze allgemeine Beschreibung des Fehlers zurück. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Kurze Nachricht. Für zukünftige Verwendung reserviert. Gibt derzeit dieselben Informationen wie 0 zurück. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detaillierte Nachricht. Bietet Details auf Benutzerebene zum Fehler. Kann vertrauliche Informationen enthalten, z. B. Dateipfade. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Vollständige Debugging-Informationen. Fügt ggf. Java Stack Traces hinzu. Fehlerbilder enthalten keine Stacktraces und geben stattdessen Informationen der Stufe 2 in <span class="codeph"> $error.message</span> zurück. </p></td> 
 </tr> 
</table>

* Level 0 wird für Live-Server empfohlen, auf die öffentlich zugegriffen werden kann.
* Level 2 wird für Staging-, Qualitätssicherung- und Anwendungsentwicklungsserver empfohlen.
* Informationen der Stufe 3 können bei der Meldung von Problemen beim technischen Support von Dynamic Media nützlich sein.

## Eigenschaften {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Aufzählungswert: 0, 1, 2 oder 3.

## Standard {#section-5e78d550050840cc9a1de811c581b94f}

Wird von `default::ErrorDetail` übernommen, wenn nicht angegeben oder leer.

## Verwandte Themen {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
