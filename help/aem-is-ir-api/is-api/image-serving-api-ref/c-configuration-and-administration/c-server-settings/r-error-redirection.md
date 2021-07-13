---
description: Verwenden Sie diese Servereinstellungen, um Fehler umzuleiten.
solution: Experience Manager
title: Fehlerumleitung
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Fehlerumleitung{#error-redirection}

Verwenden Sie diese Servereinstellungen, um Fehler umzuleiten.

>[!NOTE]
>
>Pipeline-Zeichen (|) im Netzpfad werden für die Umleitung von Fehlern nicht unterstützt.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

Die Stamm-URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) für die sekundäre Image-Serving-Bereitstellung, an die Anforderungen, die lokal fehlschlagen, umgeleitet werden sollen. Die Umleitung von Fehlern ist deaktiviert (Standard), wenn diese Einstellung leer oder nicht definiert ist.

## PS::errorRedirect.connectTimeout - Redirect Connection Timeout {#section-3971be8f720d4b32a2cc7860b4085971}

Maximale Zeit (in ms) wartet der Server, bis eine Verbindung mit dem sekundären Server hergestellt ist, bevor ein Fehler an den Client zurückgegeben wird.

## PS::errorRedirect.socketTimeout - Redirect Response Timeout {#section-69d8579f748d4044bca99dfb64dd523c}

Maximale Zeit (in ms) wartet der Server, bis der sekundäre Server Daten zurückgibt, bevor er die Weiterleitungsanfrage abbricht und einen Fehler an den Client zurückgibt.
