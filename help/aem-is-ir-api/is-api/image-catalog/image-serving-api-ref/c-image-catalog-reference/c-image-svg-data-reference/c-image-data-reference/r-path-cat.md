---
description: Pfad der Bilddatei.
solution: Experience Manager
title: Pfad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
TQID: 'https://experienceleague.adobe.com/dpQY2E7P1LzEhYg05p6C5MQRvx9jgdMB-GrBReIIqig'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 2%

---

# Pfad{#path}

Pfad der Bilddatei.

Relativer oder absoluter Pfad und Name der Quellbilddatei, die mit diesem Katalogeintrag verknüpft ist. Der Server verwendet die unter Verwalten von Source-Daten beschriebenen Regeln für die Pfadauflösung, um die Datendatei zu finden.

## Eigenschaften {#path-properties}

Text-String Erforderlich für Bilddatensätze, darf für Vorlagendatensätze leer sein. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Dateipfad des Image-Servers handeln. attribute::DefaultExt wird angehängt, wenn kein Dateisuffix vorhanden ist.

## Unterstützte Bilddateiformate {#path-supported-image-file-formats}

Eine vollständige Liste der unterstützten Dateiformate finden Sie in der Beschreibung des Image Converter-Dienstprogramms (IC).

Anwendungen, für die Bilddaten in mehreren Auflösungen erforderlich sind, erzielen die besten Ergebnisse, wenn das PTIFF-Format (Dynamic Media Pyramid TIFF) mit mehreren Auflösungen verwendet wird. Das IC-Dienstprogramm wird verwendet, um PTIFF-Bilder aus jedem unterstützten Bildformat zu erstellen.

## Standard {#path-default}

Keine.

## Verwandte Themen {#path-seealso}

[IC-Dienstprogramm](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
