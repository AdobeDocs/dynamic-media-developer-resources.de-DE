---
title: Starten oder Anhalten unter Linux®
description: Es gibt zwei Möglichkeiten, die Bildbereitstellung unter Linux® zu starten oder zu stoppen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Starten oder Anhalten unter Linux® {#starting-or-stopping-on-linux}

Es gibt zwei Möglichkeiten, die Bildbereitstellung unter Linux® zu starten oder zu stoppen.

* Das Skript zum Überprüfen des Status von Image Serving oder zum Starten und Beenden von Image Serving befindet sich im Ordner [!DNL ImageServing/bin] :

  `ImageServing.sh {start|stop|restart|status}`
* Die folgende Alternative sollte Systemadministratoren bekannt sein:

  `/sbin/service ImageServing {start|stop|status}`
