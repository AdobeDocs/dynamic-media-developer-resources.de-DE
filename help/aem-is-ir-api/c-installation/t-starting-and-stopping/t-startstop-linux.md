---
title: Starten oder Anhalten unter Linux®
description: Es gibt zwei Möglichkeiten, die Bildbereitstellung unter Linux® zu starten oder zu stoppen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
TQID: 'https://experienceleague.adobe.com/i3Ai03O29-qmhMpCRNl7MZkqXjRDnQT1M2sVX-Z3eho'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 0%

---

# Starten oder Anhalten unter Linux® {#starting-or-stopping-on-linux}

Es gibt zwei Möglichkeiten, die Bildbereitstellung unter Linux® zu starten oder zu stoppen.

* Das Skript zum Überprüfen des Status von Image Serving oder zum Starten und Beenden von Image Serving befindet sich im Ordner [!DNL ImageServing/bin] :

  `ImageServing.sh {start|stop|restart|status}`
* Die folgende Alternative sollte Systemadministratoren bekannt sein:

  `/sbin/service ImageServing {start|stop|status}`

