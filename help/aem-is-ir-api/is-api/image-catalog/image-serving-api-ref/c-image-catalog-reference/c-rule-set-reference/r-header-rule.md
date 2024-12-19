---
title: Header
description: HTTP-Antwort-Header-Element. Optional in <rule>-Elementen.
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

HTTP-Antwort-Header-Element. Optional in `<rule>`.

## Attribute {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Erforderlich. Gibt den Namen des HTTP-Headers an.

**`Action`= „Satz“ |`"add"`**: Optional. Die Standardeinstellung ist `"set"`, wodurch alle aktuellen Header-Werte ersetzt werden. Geben Sie `"add"` an, damit Sie den Kopfzeilenwert, getrennt durch ein Komma, anhängen können.

## Daten {#section-a387f541396c49d99c29692a38032914}

Header-Wert.

## Beschreibung {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Ermöglicht das Hinzufügen neuer HTTP-Antwort-Header und das Hinzufügen oder Ersetzen von Werten vordefinierter Header. Namen und Werte müssen HTTP-Standards entsprechen. Es wird keine zusätzliche Kodierung angewendet.

Image-Serving-Substitutionsvariablen können im Kopfzeilennamen und im Kopfzeilenwert verwendet werden. Dies ermöglicht die Steuerung beider Zeichenfolgen über die Anfrage.

## Beispiel {#section-cb5b738b9b93407cb2f4d35af3e59c02}

Die folgende Regel wendet eine benutzerdefinierte Kopfzeile an, wenn der Kopfzeilenwert in der Anfrage als Variable angegeben wird:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Diese Regel wird durch die folgende Anfrage ausgelöst, wobei die HTTP-Antwort-Header-`Edge-Control::no-store` festgelegt wird:

`http://server/is/image/cat/id?$Edge-Control=no-store`
