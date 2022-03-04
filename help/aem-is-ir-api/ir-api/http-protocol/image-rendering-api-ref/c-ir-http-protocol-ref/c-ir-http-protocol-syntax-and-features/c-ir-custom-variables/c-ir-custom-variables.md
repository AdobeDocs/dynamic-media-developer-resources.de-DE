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

Der Abfrageabschnitt der Anforderungen und die Vignettenzeichenfolgen::Modifier kann benutzerdefinierte Variablen enthalten.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Variablenname. Kann aus einer beliebigen Kombination aus alphanumerischen, stelligen und sicheren Zeichen bestehen, außer `$`.

`[!DNL value]` - Wert, auf den die Variable festgelegt werden soll (Zeichenfolge).

Variablen werden ähnlich wie andere Serverbefehle unter Verwendung der oben genannten Syntax definiert. Variablen müssen definiert werden, bevor sie referenziert werden können. Variablen, die in `vignette::Modifier` kann in der URL-Anfrage referenziert werden und umgekehrt.

>[!NOTE]
>
>`[!DNL value]` muss URL-kodiert mit einem Durchgang sein, um eine sichere HTTP-Übertragung zu ermöglichen. Doppelte Kodierung erforderlich, wenn `[!DNL value]` wird über HTTP erneut übertragen. Dies ist der Fall, wenn `[!DNL value]` wird in eine verschachtelte ausländische Anforderung ersetzt.

Variablen werden referenziert, indem der Variablenname eingebettet wird (eingeschlossen durch einen vorangestellten und einen nachfolgenden `$`) an eine beliebige Stelle in den Befehlswerten. Beispielsweise zwischen dem `=`  nach dem Befehlsnamen und dem nachfolgenden `&` oder das Ende der Anfrage. Der Server ersetzt jedes dieser Vorkommen von `$ [!DNL name]$` mit `[!DNL string]`. Bei Vorkommen von `$ [!DNL name]$` in Befehlsnamen (vor dem Gleichheitszeichen eines Befehls) und im Pfadabschnitt der Anfrage.

Benutzerdefinierte Variablen sind möglicherweise nicht verschachtelt. Alle Vorkommnisse von `$ [!DNL name]$` Innerhalb `[!DNL string]` nicht ersetzt werden. Beispielsweise das Anforderungsfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` löst `text=my$var2$tree`.

`$` ist kein reserviertes Zeichen; kann es andernfalls in der Anfrage auftreten. Beispiel: `src=my$texture$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Materialkatalog-Eintrag oder eine Texturdatei mit dem Namen `[!DNL my$texture$file.tif]` ist vorhanden), während `wid=$number$` nicht, weil `wid=` erfordert ein numerisches Argument.
