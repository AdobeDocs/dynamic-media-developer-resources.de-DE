---
description: Verwenden Sie diese Server-Einstellungen, um Warnschwellen zu konfigurieren.
solution: Experience Manager
title: Warnschwellen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Warnschwellen{#alert-thresholds}

Verwenden Sie diese Server-Einstellungen, um Warnschwellen zu konfigurieren.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Ein Warnhinweis zur Reaktionszeit wird ausgegeben, wenn die durchschnittliche Verarbeitungszeit für eine Anfrage während des Sampling-Intervalls den hier festgelegten Schwellenwert überschreitet. In ms angegeben; Ganzzahl 0 oder größer. Typische Werte liegen je nach Komplexität der Vorgänge zwischen 100 und 1000 ms.

>[!NOTE]
>
>Anfragen, die zu einem 4xx- oder 5xx-Antwortstatus führen, werden für diesen Warnhinweis nicht berücksichtigt.

## AS::monitorAlertGenerator.maxErrorRate - Schwellenwert für die FehlerantwortrateAS::monitorAlertGenerator.maxErrorRate - Fehlerantwortrate {#section-76ba77fd3102419395e0f86719a1f3ec}

Ein Fehler-Warnhinweis wird ausgegeben, wenn das Verhältnis der HTTP-Fehlerantworten zu den gesamten Antworten während des Sampling-Intervalls den angegebenen Schwellenwert überschreitet.

Tatsächlicher Wert zwischen 0,0 und 1,0. Normalerweise festgelegt auf zwischen 0,005 und 0,1. Auf 1 setzen, um Fehler-Warnhinweise zu deaktivieren.

## AS::monitorAlertGenerator.minRequestRate - Niedriger Traffic-Schwellenwert {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Ein minimaler Traffic-Warnhinweis wird gesendet, wenn die durchschnittliche Anzahl von Anfragen pro Sekunde, die während des aktuellen Sampling-Intervalls empfangen wurden, unter diesen Schwellenwert fällt. Deaktivieren Sie den Warnhinweis, indem Sie diesen Wert auf 0 setzen. In Anforderungen pro Sekunde ausgedrückt. Realer Wert 0 oder höher.

## AS::monitorAlertGenerator.minFreeHeapSpace - Schwellenwert für freien Heap-Speicherplatz {#section-ce6705045f6842769030ccb1894594cc}

Gibt den minimalen freien Java-Heap-Speicherplatz an. Ein Prioritätswarnhinweis wird sofort nach einem Java-Speicherbereinigungszyklus gesendet, wenn der freie Heap-Speicherplatz unter diesem Schwellenwert liegt. Für den sicheren Betrieb des [!DNL Platform Server] werden 50 MB empfohlen. Wenn Sie den freien Heap-Speicherplatz über diesem Wert belassen, wird die Häufigkeit von Speicherbereinigungszyklen reduziert, was die Gesamtleistung des Servers verbessern kann. Ganzzahliger Wert in Byte, 0 oder höher.

## AS::monitorAlertGenerator.maxOverlap - Maximale Anzahl gleichzeitiger Anfragen {#section-ddc6925bff944758ab19bcc9cf3f2589}

Ein Überschneidungs-Warnhinweis wird ausgelöst, wenn die durchschnittliche Anzahl von Anfragen, die während des Durchschnittsintervalls gleichzeitig verarbeitet werden, diesen Schwellenwert überschreitet. Eine hohe Überschneidung kann auf eine mögliche Serverüberlastung hinweisen.

Ganzzahliger Wert 1 oder höher. Der typische Bereich liegt zwischen 20 und 50, je nach Cache-Trefferrate und Anfragekomplexität.

## AS::monitorAlertGenerator.lockedThreshold - Schwellenwert für gesperrte Anfragen {#section-012a1c9937d445708380339279c62d80}

Gibt die Anzahl der Sekunden an, die eine Anfrage ausstehen muss, bevor sie als gesperrt oder hängen gilt. Ein Warnhinweis für eine gesperrte Anfrage wird ausgegeben, wenn am Ende eines Durchschnittsintervalls mindestens eine Anfrage länger als der angegebene Zeitraum ausstand. Positiver ganzzahliger Wert in ms.

Um komplexen Render-Anfragen und Anfragen Rechnung zu tragen, bei denen Daten von fremden HTTP-Servern abgerufen werden, wird empfohlen, diesen Wert auf mindestens 30 Sekunden festzulegen (es sei denn, eine solche Bedingung wird von diesem Warnhinweis erkannt).
