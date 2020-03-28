---
description: Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.
seo-description: Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.
seo-title: Warnung zur Priorität des Heap-Speicherplatzes
solution: Experience Manager
title: Warnung zur Priorität des Heap-Speicherplatzes
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Warnung zur Priorität des Heap-Speicherplatzes{#heap-space-priority-alert}

Eine Prioritätswarnung wird gesendet, wenn der freie Java-Heap-Speicherplatz unmittelbar nach einem Java-Garbage Collection-Zyklus unter dem angegebenen Schwellenwert liegt.

Wiederholte Warnungen sollten durch Vergrößerung des Java-Heap-Speichers behoben werden. Nachfolgende Vorkommnisse dieser Bedingung führen erst dann zu einer E-Mail-Benachrichtigung, wenn die mit angegebene Verzögerung abgelaufen `AS::monitorAlertGenerator.heapSpaceResetInterval` ist.
