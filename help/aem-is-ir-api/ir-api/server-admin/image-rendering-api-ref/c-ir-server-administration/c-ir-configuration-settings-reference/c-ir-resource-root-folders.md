---
title: Ressourcen-Stammordner (ir.resourceRootPaths)
description: Eine Liste von Pfaden, durch Semikolons getrennt, dient als Stamm für alle Datendateien mit relativen Dateipfaden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
TQID: 'https://experienceleague.adobe.com/5mKCVHonfG4riWoIenUyFHtMnSg3cmL-Lm-YTGN34fA'
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
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 0%

---

# Ressourcen-Stammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Eine Liste von Pfaden, durch Semikolons getrennt, dient als Stamm für alle Datendateien mit relativen Dateipfaden.

Es kann sich entweder um absolute Pfade oder um Pfade relativ zu *[!DNL install_folder]* handeln. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wird. Der Standardwert lautet [!DNL ./resources] für einen standardmäßigen Stammpfad von [!DNL install_folder/resources].

