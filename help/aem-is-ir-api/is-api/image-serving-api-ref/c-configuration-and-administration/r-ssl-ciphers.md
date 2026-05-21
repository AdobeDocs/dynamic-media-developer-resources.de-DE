---
description: Das Connector-Tag in server.xml unterstützt ein Chiffrier-Attribut, um die Chiffren zu beschränken, die für eine SSL-Verbindung ausgewählt werden können.
solution: Experience Manager
title: Definieren von SSL-Chiffren
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
TQID: 'https://experienceleague.adobe.com/ZFBdAmbRRWCrrgGiXxdwCqMT9FYDNzoMc4IMQCwGCtw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 0%

---

# Definieren von SSL-Chiffren{#defining-ssl-ciphers}

Das Connector-Tag in server.xml unterstützt ein Chiffrier-Attribut, um die Chiffren zu beschränken, die für eine SSL-Verbindung ausgewählt werden können.

Standardmäßig sind alle Chiffren verfügbar. Die Liste ist durch Kommata getrennt und kann einen der folgenden Werte enthalten:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

Wenn einer der Werte falsch ist, aktiviert Tomcat jede einzelne Chiffre. Daher ist es wichtig, nach der Konfiguration mit einem externen Tool zu überprüfen, welche Chiffren tatsächlich aktiviert sind.

Beispielsweise aktiviert die folgende Konfiguration nur die Chiffrier-Suites „128-Bit“ und höher:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`
