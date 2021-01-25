---
description: Verwenden Sie diese Servereinstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.
seo-description: Verwenden Sie diese Servereinstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.
seo-title: Überwachungs- und Warnsystem
solution: Experience Manager
title: Überwachungs- und Warnsystem
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 944c7d53-09ec-443e-ac8c-85684d8fda0f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Überwachungs- und Warnsystem{#monitoring-and-alerting-system}

Verwenden Sie diese Servereinstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.

## AS::monitorAlertGenerator.enableGlobalAlerting - Warnsystem Aktivieren {#section-612f8ea61794426ab205e22e5f665fa9}

Aktivieren Sie die E-Mail-Benachrichtigung, indem Sie auf &quot;true&quot;setzen und die Einstellungen für die E-Mail-Benachrichtigung konfigurieren. Durch die Einstellung auf `false` werden alle E-Mail-Warnungen deaktiviert - dies kann nützlich sein, wenn ein Server für die Wartung offline geschaltet wird. Boolesch.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

Die IP-Adresse des SMTP-E-Mail-Servers.

## AS::mailSender.port- SMTP Port {#section-4b25efca8fd84d5c92dafacd0555e99d}

Der Listening-Anschluss für den SMTP-E-Mail-Server.

## AS::monitorAlertGenerator.messageTo - Message Empfänger {#section-0017bbaa15434117a70900c3f1163960}

Eine oder mehrere E-Mail-Adressen, an die Warnungen gesendet werden sollen. Verwenden Sie Semikolons als Trennzeichen.

## AS::monitorAlertGenerator.messageFrom - Message Sender {#section-db320cba4ac2438ca1cfe6abce4aed87}

Die E-Mail-Adresse, die im E-Mail-Feld **[!UICONTROL Von]** verwendet werden soll.

## AS::monitorAlertGenerator.alertInterval - Überwachungsintervall {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Das Überwachungssystem sammelt während des Warnungsintervalls Alarmbedingungen und sendet am Ende jedes Intervalls eine Warnmeldung per E-Mail, die alle akkumulierten Warnungen enthält. Millisekunden, ganzzahliger Wert, 60000 oder höher. Normalerweise auf 5 oder 10 Minuten eingestellt.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Heap Space Alert Interval {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Mindestzeit nach einer Heap Space-Warnung, bevor eine andere ausgegeben wird. Intervallzeit in msec. Ganzzahlwert, 0 oder größer.

## AS::monitorAlertGenerator.minTrafficForAlerts - Minimum Traffic to Enable Alerting {#section-8b4db2d6f96642309ca35c49eb3ab230}

Anforderungen pro Sekunde Wenn der Traffic unter diesen Schwellenwert fällt, werden keine Antwortzeit- und Fehlerwarnungen ausgegeben. Auf 0 setzen, um Antwortzeit- und Fehlerwarnungen unabhängig vom Traffic-Volumen zu senden. Realer Wert 0 oder größer.
