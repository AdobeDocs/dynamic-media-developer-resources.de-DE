---
description: Das Connector-Tag in server.xml unterstützt ein ciphers-Attribut, um die für eine SSL-Verbindung auswählbaren Chiffren zu beschränken.
seo-description: Das Connector-Tag in server.xml unterstützt ein ciphers-Attribut, um die für eine SSL-Verbindung auswählbaren Chiffren zu beschränken.
seo-title: Definieren von SSL-Chiffern
solution: Experience Manager
title: Definieren von SSL-Chiffern
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Definieren von SSL-Chiffern{#defining-ssl-ciphers}

Das Connector-Tag in server.xml unterstützt ein ciphers-Attribut, um die für eine SSL-Verbindung auswählbaren Chiffren zu beschränken.

Standardmäßig sind alle Chiffren verfügbar. Die Liste ist durch Kommas getrennt und kann einen der folgenden Werte enthalten:

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

Wenn einer der Werte falsch ist, aktiviert Tomcat jeden einzelnen Chipher. Daher ist es wichtig, nach der Konfiguration mit einem externen Tool zu prüfen, welche Chiffren tatsächlich aktiviert sind.

Beispielsweise werden mit der folgenden Konfiguration nur die &quot;128-Bit&quot;-Chipher-Suites und höher aktiviert:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
