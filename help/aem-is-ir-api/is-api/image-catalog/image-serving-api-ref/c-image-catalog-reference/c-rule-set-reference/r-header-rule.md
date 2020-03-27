---
description: HTTP-Antwort-Header-Element. Optional in <rule>-Elementen.
seo-description: HTTP-Antwort-Header-Element. Optional in <rule>-Elementen.
seo-title: Header
solution: Experience Manager
title: Header
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Header{#header}

HTTP-Antwort-Header-Element. Optional in `<rule>` Elementen.

## Attribute {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**: Erforderlich. Gibt den Namen des HTTP-Headers an.

**`Action`= &quot;set&quot;|`"add"`**: Optional. Der Standardwert ist`"set"`der, der alle aktuellen Kopfzeilenwerte ersetzt. Geben Sie`"add"`an, den Kopfzeilenwert durch ein Komma getrennt anzuhängen.

## Daten {#section-a387f541396c49d99c29692a38032914}

Kopfzeilenwert.

## Beschreibung {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Ermöglicht das Hinzufügen neuer HTTP-Antwort-Kopfzeilen sowie das Hinzufügen oder Ersetzen von Werten vordefinierter Kopfzeilen. Namen und Werte müssen den HTTP-Standards entsprechen. Es wird keine zusätzliche Kodierung angewendet.

Image Serving-Ersatzvariablen können im Kopfzeilennamen und im Kopfzeilenwert verwendet werden. Dadurch können beide Zeichenfolgen von der Anforderung gesteuert werden.

## Beispiel {#section-cb5b738b9b93407cb2f4d35af3e59c02}

Die folgende Regel wendet einen benutzerdefinierten Header an, wenn der Header-Wert in der Anforderung als Variable angegeben wird:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Diese Regel wird durch die folgende Anforderung ausgelöst, bei der der HTTP-Antwort-Header festgelegt wird `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
