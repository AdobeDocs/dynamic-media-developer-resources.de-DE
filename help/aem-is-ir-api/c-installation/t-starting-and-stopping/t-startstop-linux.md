---
description: Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.
seo-description: Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.
seo-title: Starten oder Beenden unter Linux
solution: Experience Manager
title: Starten oder Beenden unter Linux
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# Starten oder Beenden unter Linux{#starting-or-stopping-on-linux}

Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.

* Das Skript zum Beginn, Beenden und Überprüfen des Status des Image-Servers befindet sich im Ordner [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Die folgende Alternative sollte Systemadministratoren kennen:

   `/sbin/service ImageServing {start|stop|status}`
