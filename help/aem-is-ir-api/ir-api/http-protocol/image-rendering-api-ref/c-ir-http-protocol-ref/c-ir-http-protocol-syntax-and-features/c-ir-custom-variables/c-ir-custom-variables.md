---
description: Der Abfrageabschnitt der Anforderungen und Vignettenänderungs-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
solution: Experience Manager
title: Benutzerdefinierte Variablen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Benutzerdefinierte Variablen{#custom-variables}

Der Abfrageabschnitt der Anforderungen und die Vignettenzeichenfolgen::Modifier kann benutzerdefinierte Variablen enthalten.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variablenname. Kann aus einer beliebigen Kombination aus alphanumerischen, numerischen und sicheren Zeichen bestehen, mit Ausnahme von &quot;$&quot;.

** *[!DNL value]* ** Wert, auf den die Variable gesetzt werden soll (Zeichenfolge).

Variablen werden ähnlich wie andere Serverbefehle unter Verwendung der oben genannten Syntax definiert. Variablen müssen definiert werden, bevor sie referenziert werden können. Variablen, die in `vignette::Modifier` definiert sind, können in der URL-Anforderung referenziert werden und umgekehrt.

>[!NOTE]
>
>*[!DNL value]* muss URL-kodiert mit einem Durchgang sein, um eine sichere HTTP-Übertragung zu ermöglichen. Eine Doppelkodierung ist erforderlich, wenn *[!DNL value]* über HTTP erneut übertragen wird. Dies ist der Fall, wenn *[!DNL value]* in einer verschachtelten ausländischen Anforderung ersetzt wird.

Variablen werden referenziert, indem der Variablenname (von einem vorangestellten und einem nachfolgenden $ eingeschlossen) an einer beliebigen Stelle in Befehlswerte eingebettet wird. Beispielsweise zwischen dem &#39;=&#39;, das auf den Befehlsnamen folgt, und dem nachfolgenden &#39;&amp;&#39; oder dem Ende der Anfrage. Der Server ersetzt jedes dieser Vorkommen von $ *[!DNL name]*$ durch *[!DNL string]*. Bei Vorkommen von $ *[!DNL name]*$ in Befehlsnamen (vor dem Gleichheitszeichen eines Befehls) und im Pfadabschnitt der Anfrage werden keine Ersetzungen vorgenommen.

Benutzerdefinierte Variablen sind möglicherweise nicht verschachtelt. Jedes Vorkommen von $ *[!DNL name]*$ innerhalb von *[!DNL string]* wird nicht ersetzt. Beispielsweise wird das Anforderungsfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` in `text=my$var2$tree` aufgelöst.

$ ist kein reserviertes Zeichen; kann es andernfalls in der Anfrage auftreten. `src=my$texture$file.tif` ist beispielsweise ein gültiger Befehl (vorausgesetzt, dass ein Materialkatalogeintrag oder eine Texturdatei mit dem Namen [!DNL my$texture$file.tif] vorhanden ist), während `wid=$number$` nicht vorhanden ist, da `wid=` ein numerisches Argument erfordert.
