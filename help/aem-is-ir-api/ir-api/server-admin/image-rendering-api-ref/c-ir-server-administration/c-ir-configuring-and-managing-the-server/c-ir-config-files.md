---
description: Die Konfigurationseinstellungen für das Rendern von Bildern werden im [!DNL Platform Server] Konfigurationsdatei.
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

Die Konfigurationseinstellungen für das Rendern von Bildern werden im [!DNL Platform Server] Konfigurationsdatei.

Die Konfigurationsdatei für den Plattformserver befindet sich unter [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Diese Datei ist eine JAVA-Eigenschaftendatei. Es ist darauf zu achten, dass die entsprechenden Konventionen eingehalten werden. Andernfalls muss die [!DNL Platform Server] kann nicht starten. Ein doppelter umgekehrter Schrägstrich (`\\`) oder ein einzelner Schrägstrich (/) anstelle eines einfachen umgekehrten Schrägstrichs (\) in Windows-Dateipfaden verwendet werden, da der umgekehrte Schrägstrich in diesem Dateityp als Escape-Zeichen verwendet wird. Die Datei enthält nicht dokumentierte Eigenschaften, die zur internen Verwendung auf dem Server bestimmt sind und nicht geändert werden dürfen.

Siehe Abschnitt [Referenz zu Konfigurationseinstellungen](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) für eine Liste aller Einstellungen der Image Rendering-Konfiguration.
