---
description: Direkten Zugriff auf pfadbasierte Assets zulassen.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Direkten Zugriff auf pfadbasierte Assets zulassen.

Wenn dieses Attribut definiert ist, ist der pfadbasierte Zugriff für die angegebenen Objektarten zulässig oder eingeschränkt, je nachdem, ob das Schlüsselwort `include` oder `exclude` verwendet wird.

>[!NOTE]
>
>Wenn das Attribut `AllowDirectAccess` nicht angegeben ist, ist der Standardwert `exclude`.

* `include` ermöglicht den Zugriff auf die angegebenen Objekttypen und beschränkt den Zugriff auf alle anderen.
* `exclude` beschränkt den Zugriff für die angegebenen Objektarten und ermöglicht den Zugriff für alle anderen.

Wenn weder `include` noch `exclude` angegeben ist, wird `include` angenommen.

Die folgenden Typen können gesteuert werden:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Beispiele {#section-4c3765ebaa4245a799b454fc196f9237}

* Direkten Zugriff nur für die Objekttypen `IS` und `STATIC` zulassen

  `AllowDirectAccess=include:IS,STATIC`

* Direkten Zugriff für alle Objekttypen mit Ausnahme von `IS` und `STATIC``AllowDirectAccess=exclude:IS,STATIC` zulassen

* Direkten Zugriff für *no* -Objekttypen zulassen (d. h. keine einschließen)

  `AllowDirectAccess=include:`

* Direkten Zugriff für *alle* Objekttypen zulassen (d. h. keine ausschließen)

  `AllowDirectAccess=exclude:`

* Entspricht `include:IS,STATIC` (wenn `include`/ `exclude` nicht vorhanden ist, wird `include` angenommen.)

  `AllowDirectAccess=IS,STATIC`

  Beachten Sie, dass der Standardwert verwendet wird, wenn das Attribut `AllowDirectAccess` nicht für dieses Unternehmen angegeben ist.

* Keine einschließen, entspricht `include:` (wenn `include`/ `exclude` nicht vorhanden ist, wird `include` angenommen)

  `AllowDirectAccess=`
