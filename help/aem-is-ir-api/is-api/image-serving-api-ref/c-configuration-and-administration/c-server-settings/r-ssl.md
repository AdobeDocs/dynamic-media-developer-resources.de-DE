---
description: Verwenden Sie diese Server-Einstellungen für SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# SSL{#ssl}

Verwenden Sie diese Server-Einstellungen für SSL.

## TC::SSLport - Listening-Port {#section-c80eb582bf684b3fa7313a77cc606769}

Gibt den Überwachungs-Port für die [!DNL Platform Server] für SSL-Verbindungen an. Die Standardgrenze ist 8443.

## TC::keystoreFile - Keystore-Dateipfad {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geben Sie den Pfad/Namen der SSL-Keystore-Datei an. Kann ein absoluter Pfad oder ein Pfad relativ zu [!DNL *[!DNL install_folder]*/conf] sein. Die Standardeinstellung ist *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore-Kennwort {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Das Kennwort für die KeyStore-Datei. Der Standardwert ist `scene7`.

## TC::keystoreType - Keystore-Typ {#section-8f263e1ba67740728cd39181960d7c7d}

Typ des Keystores auswählen. &#39; `Java'` (Standard) und &#39; `PKCS12`&#39; werden unterstützt.
