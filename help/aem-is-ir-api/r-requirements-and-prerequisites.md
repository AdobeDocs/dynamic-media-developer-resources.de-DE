---
description: Bevor Sie Dynamic Media Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.
solution: Experience Manager
title: Systemanforderungen und Voraussetzungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Systemanforderungen und Voraussetzungen{#system-requirements-and-prerequisites}

Bevor Sie Dynamic Media Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.

## Serverhardware {#section-f3c14a7bc1b745118602659628df779f}

Ihr Server sollte die folgenden Hardwareanforderungen erfüllen.

>[!NOTE]
>
>Systeme mit Prozessoren mit AMD64 und Intel® EM64T werden normalerweise als NUMA-Plattformen (Non-Uniform Memory Architecture) konfiguriert. Dies bedeutet, dass der Kernel mehrere Speicherknoten beim Booten erstellt, anstatt einen einzelnen Speicherknoten zu erstellen. Das Konstrukt mit mehreren Knoten kann zu einer Speichererschöpfung auf einem oder mehreren Knoten führen, bevor andere Knoten erschöpft sind. Wenn die Speichererschöpfung eintritt, kann der Kernel Prozesse beenden (z. B. den Image-Server oder Platform-Server), obwohl verfügbarer Speicher vorhanden ist. Daher empfiehlt Adobe Systems, NUMA zu deaktivieren, wenn Sie ein solches System ausführen. Verwenden Sie die Startoption `numa=off`, um zu vermeiden, dass der Kernel diese Prozesse stoppt.

**Windows**

* Intel Xeon® oder AMD® Opteron-CPU mit mindestens 4 Kernen.
* Mindestens 16 GB RAM.
* Tauschen Sie Speicherplatz aus, der mindestens dem Zweifachen des physischen Arbeitsspeichers (RAM) entspricht.
* 2 GB verfügbarer Festplattenspeicher für die Installation und den grundlegenden Betrieb, zusätzlicher Speicherplatz für Quellbilder, Protokolle, Daten-Caches und Manifestdateien.
* Fast-Ethernet-Netzwerkschnittstellenkarte.

**Linux**

* Intel Xeon® oder AMD® Opteron-CPU mit mindestens 4 Kernen.
* Mindestens 16 GB RAM.
* Swapping deaktiviert (empfohlen).
* 2 GB verfügbarer Festplattenspeicher für die Installation und den grundlegenden Betrieb, zusätzlicher Speicherplatz für Quellbilder, Protokolle, Daten-Caches und Manifestdateien.
* Fast-Ethernet-Netzwerkschnittstellenkarte.

**Hinweis (Linux):** Image Serving funktioniert nicht mit aktiviertem SELinux. Diese Option ist standardmäßig aktiviert. Um SELinux zu deaktivieren, bearbeiten Sie die Datei [!DNL /etc/selinux/config] und ändern Sie den SELinux-Wert von:

`SELINUX=enforcing`

in / zu

`SELINUX=disabled`

**Hinweis (Linux):**  Stellen Sie sicher, dass der Hostname des Servers in eine IP-Adresse aufgelöst werden kann. Wenn dies nicht möglich ist, fügen Sie [!DNL /etc/hosts] den vollständig qualifizierten Hostnamen und die IP-Adresse wie im folgenden Beispiel hinzu.

`<ip address> <fully qualified hostname>`

## Server-Software {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving erfordert die folgende Serversoftware.

**Windows**

* Microsoft® Windows 2008 Server.
* 64-Bit-Betriebssystem.

**Linux**

* Red Hat® Enterprise 5 oder CentOS 5.5 und höher mit aktuellen Fix-Patches.
* 64-Bit-Betriebssystem.

**Hinweis:** Um Image Serving unter Windows zu verwenden, müssen Sie Microsoft Visual Studio 2010 Redistributable installieren.
