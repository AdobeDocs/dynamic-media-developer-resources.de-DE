---
description: Die Konfigurationseinstellungen für das Rendern von Bildern werden in der Konfigurationsdatei  [!DNL Platform Server]  gespeichert.
solution: Experience Manager
title: Konfigurationsdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Konfigurationsdateien{#configuration-files}

Die Konfigurationseinstellungen für das Rendern von Bildern werden in der [!DNL Platform Server] Konfigurationsdatei gespeichert.

Die Konfigurationsdatei des Platform-Servers befindet sich unter [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Diese Datei ist eine JAVA-Eigenschaftendatei. Es muss darauf geachtet werden, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann es sein, dass der [!DNL Platform Server] nicht startet. In Windows-Dateipfaden muss anstelle eines einfachen umgekehrten Schrägstrichs (\) ein doppelter umgekehrter Schrägstrich (`\\`) oder ein einfacher Schrägstrich (/) verwendet werden, da der umgekehrte Schrägstrich in diesem Dateityp als Escape-Zeichen verwendet wird. Die Datei enthält nicht dokumentierte Eigenschaften, die für die interne Verwendung durch den Server bestimmt sind und nicht geändert werden dürfen.

Unter [Konfigurationseinstellungen“ finden Sie ](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) Liste aller Image-Rendering-Konfigurationseinstellungen.
