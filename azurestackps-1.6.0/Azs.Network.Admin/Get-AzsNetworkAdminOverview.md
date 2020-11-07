---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761776"
---
# Get-AzsNetworkAdminOverview

## SYNOPSIS
Ağ kaynağı sağlayıcısının durumuna genel bakış.

## INDEKI

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## Tanım
Ağ kaynağı sağlayıcısının durumuna genel bakış. Tek tek özellikler, bileşene göre ayrıntılı kaynak kullanımı ve sistem durumu sağlar.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Ağ yöneticisine genel bakış.

### --------------------------ÖRNEK 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Genel IP adresi kullanımını edinin.

## PARAMETRELERINE

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. Network. admin. model. AdminOverview

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

