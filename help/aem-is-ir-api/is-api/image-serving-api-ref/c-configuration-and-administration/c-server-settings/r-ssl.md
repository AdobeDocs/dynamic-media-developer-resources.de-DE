---
description: Verwenden Sie diese Servereinstellungen für SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# SSL{#ssl}

Verwenden Sie diese Servereinstellungen für SSL.

## TC::SslPort - Listening Port {#section-c80eb582bf684b3fa7313a77cc606769}

Gibt den Listening-Anschluss für den Platform Server für SSL-Verbindungen an. Der Standardwert ist „8443“.

## TC::keystoreFile - Keystore-Dateipfad {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geben Sie den Pfad/Namen der SSL-Keystore-Datei an. Kann ein absoluter Pfad oder ein Pfad relativ zu [!DNL *[!DNL install_folder]*/conf] sein. Der Standardwert ist *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore Password {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Das Kennwort für die Keystore-Datei. Die Standardgrenze ist `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Wählen Sie den Keystore-Typ aus. &#39; `Java'` (Standard) und &#39; `PKCS12`&#39; werden unterstützt.
