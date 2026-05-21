---
description: Filterelement der Adresse. Optional in den Elementen <rule> und <pathrule>.
solution: Experience Manager
title: addressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: 'https://experienceleague.adobe.com/NkzpvFZFbluayVtCa7qBVcSgY2aU5N7R2-rZkQCZHkw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 3%

---

# addressFilter{#addressfilter}

Filterelement der Adresse. Optional in `<rule>`- und `<pathrule>`.

Überschreibt `attribute::ClientAddressFilter` bei Anwendung der Regel.

## Attribute {#section-31e9ad29e9934933ac154bccbc729172}

Keine.

## Daten {#section-c762bdfe425140d689ea5abf25e9a48a}

Liste der IP-Adressen (durch Kommata getrennt) Jede einzelne Adresse kann ein optionales Netzmasken-Suffix enthalten, um die Angabe von IP-Adressbereichen zu ermöglichen. Weitere Informationen finden Sie unter `attribute::ClientAddressFilter` .

## Beschreibung {#section-d561b2485e004ef8a2085997d0f4bca6}

Der Zugriff auf diesen Bildkatalog kann auf eine oder mehrere bestimmte Client-IP-Adressen beschränkt werden, indem diese in einem `<addressfilter>` angegeben werden. Der Fehler „Anfrage abgelehnt“ wird an den Client zurückgegeben, wenn die Client-IP-Adresse nicht übereinstimmt.

Der Zugriff ist nicht eingeschränkt, wenn `<addressfilter>` leer oder nicht angegeben ist.

Wenn die `<expression>` im `<rule>` fehlt oder leer ist, wird die `<addressfilter>` auf alle Anfragen angewendet.

## Verwandte Themen {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
