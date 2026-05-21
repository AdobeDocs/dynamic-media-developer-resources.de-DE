---
description: Auf statische Inhaltsquellendatendateien kann nur über die [!DNL Platform Server] zugegriffen werden.
solution: Experience Manager
title: Statische Quelldaten für Inhalte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Statische Quelldaten für Inhalte{#static-content-source-data}

Auf statische Inhaltsquellendatendateien kann nur über die [!DNL Platform Server] zugegriffen werden.

Der Pfad für statische Inhaltsdatendateien wird wie folgt aufgelöst:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt wird.

Alle ` *[!DNL rootPath]*` können leere, relative oder absolute Pfadsegmente sein.

` *[!DNL catalogPath]*` ist entweder ein absoluter oder relativer Dateipfad/-name. *[!DNL requestPath]* muss ein relativer Dateipfad/Dateiname sein.

In können mehrere `PS::staticContent.rootPaths` definiert [!DNL PlatformServer.conf]. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der [!DNL Platform Server] versucht alternative Pfade in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.
