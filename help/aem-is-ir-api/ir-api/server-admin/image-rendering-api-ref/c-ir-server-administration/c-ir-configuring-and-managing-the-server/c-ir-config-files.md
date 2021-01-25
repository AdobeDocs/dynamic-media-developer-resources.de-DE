---
description: Die Konfigurationseinstellungen für das Image Rendering werden in der Konfigurationsdatei des Plattformservers gespeichert.
seo-description: Die Konfigurationseinstellungen für das Image Rendering werden in der Konfigurationsdatei des Plattformservers gespeichert.
seo-title: Konfigurationsdateien
solution: Experience Manager
title: Konfigurationsdateien
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Konfigurationsdateien{#configuration-files}

Die Konfigurationseinstellungen für das Image Rendering werden in der Konfigurationsdatei des Plattformservers gespeichert.

Die Konfigurationsdatei des Plattformservers befindet sich unter [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Diese Datei ist eine JAVA-Eigenschaftendatei. Es muss darauf geachtet werden, dass die entsprechenden Konventionen eingehalten werden, da andernfalls der Plattformserver möglicherweise nicht in Beginn geraten kann. Bei Windows-Dateipfaden muss ein umgekehrter Schrägstrich (`\\`) oder ein einzelner Schrägstrich (/) anstelle eines einfachen umgekehrten Schrägstrichs (\) verwendet werden, da der umgekehrte Schrägstrich in diesem Dateityp als Escape-Zeichen verwendet wird. Die Datei enthält undokumentierte Eigenschaften, die zur internen Serververwendung bestimmt sind und nicht geändert werden dürfen.

Eine Liste aller Image Rendering-Konfigurationseinstellungen finden Sie im Abschnitt [Konfigurationseinstellungen](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
