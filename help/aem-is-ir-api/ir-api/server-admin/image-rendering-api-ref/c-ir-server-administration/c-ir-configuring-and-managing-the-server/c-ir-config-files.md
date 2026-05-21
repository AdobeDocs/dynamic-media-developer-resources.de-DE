---
description: Die Konfigurationseinstellungen für das Rendern von Bildern werden in der Konfigurationsdatei  [!DNL Platform Server]  gespeichert.
solution: Experience Manager
title: Konfigurationsdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
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
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Konfigurationsdateien{#configuration-files}

Die Konfigurationseinstellungen für das Rendern von Bildern werden in der [!DNL Platform Server] Konfigurationsdatei gespeichert.

Die Konfigurationsdatei des Platform-Servers befindet sich unter [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Diese Datei ist eine JAVA-Eigenschaftendatei. Es muss darauf geachtet werden, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann es sein, dass der [!DNL Platform Server] nicht startet. In Windows-Dateipfaden muss anstelle eines einfachen umgekehrten Schrägstrichs (\) ein doppelter umgekehrter Schrägstrich (`\\`) oder ein einfacher Schrägstrich (/) verwendet werden, da der umgekehrte Schrägstrich in diesem Dateityp als Escape-Zeichen verwendet wird. Die Datei enthält nicht dokumentierte Eigenschaften, die für die interne Verwendung durch den Server bestimmt sind und nicht geändert werden dürfen.

Unter [Konfigurationseinstellungen“ finden Sie &#x200B;](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) Liste aller Image-Rendering-Konfigurationseinstellungen.
