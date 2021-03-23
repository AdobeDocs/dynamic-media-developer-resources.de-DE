---
description: Verwenden Sie diese Servereinstellungen, um Fehler umzuleiten.
seo-description: Verwenden Sie diese Servereinstellungen, um Fehler umzuleiten.
seo-title: Fehler-Umleitung
solution: Experience Manager
title: Fehler-Umleitung
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Fehler-Umleitung{#error-redirection}

Verwenden Sie diese Servereinstellungen, um Fehler umzuleiten.

>[!NOTE]
>
>Pipe-Zeichen (|) im Netzpfad werden für die Fehlerumleitung nicht unterstützt.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

Die Stamm-URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) für die sekundäre Image Serving-Bereitstellung, an die Anforderungen, die lokal fehlschlagen, umgeleitet werden sollten. Die Fehlerumleitung ist deaktiviert (Standard), wenn diese Einstellung leer oder nicht definiert ist.

## PS::errorRedirect.connectTimeout - Redirect Connection Timeout {#section-3971be8f720d4b32a2cc7860b4085971}

Maximale Zeit (in msec) wartet der Server, bis eine Verbindung mit dem sekundären Server hergestellt wird, bevor ein Fehler an den Client zurückgegeben wird.

## PS::errorRedirect.socketTimeout - Redirect Response Timeout {#section-69d8579f748d4044bca99dfb64dd523c}

Maximale Zeit (in msec) wartet der Server, bis der sekundäre Server Daten zurückgibt, bevor die Weiterleitungsanfrage abgebrochen und ein Fehler an den Client zurückgegeben wird.
