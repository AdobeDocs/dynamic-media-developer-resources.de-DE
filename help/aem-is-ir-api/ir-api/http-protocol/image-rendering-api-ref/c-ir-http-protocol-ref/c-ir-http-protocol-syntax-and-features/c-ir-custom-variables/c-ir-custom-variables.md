---
title: Benutzerdefinierte Variablen
description: Der Abfrageabschnitt der Anforderungen und Vignettenänderungs-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Benutzerdefinierte Variablen{#custom-variables}

Der Abfrageabschnitt der Anforderungen und die Vignetten::Modifier-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Variablenname. Kann aus einer beliebigen Kombination aus alphanumerischen, numerischen und sicheren Zeichen bestehen, mit Ausnahme von `$`.

`[!DNL value]` - Wert, auf den die Variable festgelegt werden soll (Zeichenfolge).

Variablen werden ähnlich wie andere Serverbefehle unter Verwendung der oben genannten Syntax definiert. Variablen müssen definiert werden, bevor sie referenziert werden können. Variablen, die in `vignette::Modifier` definiert sind, können in der URL-Anforderung referenziert werden und umgekehrt.

>[!NOTE]
>
>`[!DNL value]` muss URL-kodiert mit Einzeldurchlauf sein, um eine sichere HTTP-Übertragung zu ermöglichen. Doppelte Kodierung ist erforderlich, wenn `[!DNL value]` über HTTP erneut übertragen wird. Dies ist der Fall, wenn `[!DNL value]` durch eine verschachtelte ausländische Anforderung ersetzt wird.

Variablen werden referenziert, indem der Variablenname (eingeschlossen durch einen vorangestellten und nachfolgenden `$`) an einer beliebigen Stelle in Befehlswerte eingebettet wird. Beispielsweise zwischen dem `=`, das auf den Befehlsnamen folgt, und dem nachfolgenden `&` oder dem Ende der Anfrage. Der Server ersetzt jedes Vorkommen von `$ [!DNL name]$` durch `[!DNL string]`. Bei Instanzen von `$ [!DNL name]$` in Befehlsnamen (vor dem Gleichheitszeichen eines Befehls) und im Pfadabschnitt der Anfrage erfolgt kein Ersatz.

Benutzerdefinierte Variablen sind möglicherweise nicht verschachtelt. Alle Vorkommnisse von `$ [!DNL name]$` innerhalb von `[!DNL string]` werden nicht ersetzt. Beispielsweise wird das Anforderungsfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` in `text=my$var2$tree` aufgelöst.

`$` ist kein reserviertes Zeichen; es kann andernfalls in der Anfrage auftreten. Beispiel: `src=my$texture$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Materialkatalogeintrag oder eine Texturdatei mit dem Namen `[!DNL my$texture$file.tif]` vorhanden ist), während `wid=$number$` nicht ist, da `wid=` ein numerisches Argument erfordert.
