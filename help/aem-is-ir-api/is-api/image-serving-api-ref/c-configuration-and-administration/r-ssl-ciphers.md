---
description: Das Connector-Tag in server.xml unterstützt ein ciphers-Attribut, um die für eine SSL-Verbindung auswählbaren Chiffren zu begrenzen.
solution: Experience Manager
title: Definieren von SSL-Verschlüsselungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# Definieren von SSL-Verschlüsselungen{#defining-ssl-ciphers}

Das Connector-Tag in server.xml unterstützt ein ciphers-Attribut, um die für eine SSL-Verbindung auswählbaren Chiffren zu begrenzen.

Standardmäßig sind alle Chiffren verfügbar. Die Liste ist kommagetrennt und kann einen der folgenden Werte enthalten:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Wenn einer der Werte falsch ist, aktiviert Tomcat jede einzelne Chiffre. Daher ist es wichtig, nach der Konfiguration mit einem externen Tool zu überprüfen, um zu sehen, welche Chiffren tatsächlich aktiviert sind.

Beispielsweise werden mit der folgenden Konfiguration nur die Chiffre-Suites &quot;128 Bit&quot;und höher aktiviert:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
