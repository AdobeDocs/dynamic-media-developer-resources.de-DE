---
title: Header
description: HTTP-Antwort-Header-Element. Optional in <rule> -Elemente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# Header{#header}

HTTP-Antwort-Header-Element. Optional in `<rule>` -Elemente.

## Attribute {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Erforderlich. Gibt den Namen des HTTP-Headers an.

**`Action`= &quot;set&quot; |`"add"`**: Optional. Der Standardwert ist `"set"`, der jeden aktuellen Header-Wert ersetzt. Angeben `"add"` so können Sie den Kopfzeilenwert durch Kommas trennen.

## Daten {#section-a387f541396c49d99c29692a38032914}

Kopfzeilenwert.

## Beschreibung {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Ermöglicht das Hinzufügen neuer HTTP-Antwortheader und das Hinzufügen oder Ersetzen von Werten vordefinierter Header. Namen und Werte müssen den HTTP-Standards entsprechen. Es wird keine zusätzliche Kodierung angewendet.

Ersatzvariablen für Image Serving können im Header-Namen und im Header-Wert verwendet werden. Dadurch können beide Zeichenfolgen aus der Anfrage gesteuert werden.

## Beispiel {#section-cb5b738b9b93407cb2f4d35af3e59c02}

Die folgende Regel wendet eine benutzerdefinierte Kopfzeile an, wenn der Kopfzeilenwert in der Anfrage als Variable angegeben ist:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Diese Regel wird durch die folgende Anfrage ausgelöst, bei der der HTTP-Antwortheader festgelegt wird `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
