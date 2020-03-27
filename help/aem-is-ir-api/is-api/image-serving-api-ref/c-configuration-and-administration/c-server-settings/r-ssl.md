---
description: Verwenden Sie diese Servereinstellungen für SSL.
seo-description: Verwenden Sie diese Servereinstellungen für SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SSL{#ssl}

Verwenden Sie diese Servereinstellungen für SSL.

## TC::SslPort - Überwachungsanschluss {#section-c80eb582bf684b3fa7313a77cc606769}

Gibt den Listening-Anschluss für den Plattformserver für SSL-Verbindungen an. Der Standardwert ist „8443“.

## TC::keystoreFile - Keystore-Dateipfad {#section-0cdf9b3cfcf249818b22221d01bafebe}

Geben Sie den Pfad/Namen der SSL-Keystore-Datei an. Kann ein absoluter Pfad oder ein Pfad relativ zu [!DNL *[!DNL install_folder]*/conf] sein. Die Standardeinstellung ist *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore-Kennwort {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Das Kennwort für die Keystore-Datei. Die Standardgrenze ist `scene7`.

## TC::keystoreType - Keystore-Typ {#section-8f263e1ba67740728cd39181960d7c7d}

Wählen Sie den Keystore-Typ aus. &#39; `Java'` (Standard) und &#39; `PKCS12`&#39; werden unterstützt.
