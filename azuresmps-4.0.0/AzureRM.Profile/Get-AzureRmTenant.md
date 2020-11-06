---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571745"
---
# Get-AzureRmTenant

## SYNOPSIS
Geçerli Kullanıcı için yetkilendirilmiş kiracıları alır.

## INDEKI

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## Tanım
Get-AzureRmTenant cmdlet 'i, geçerli kullanıcı için yetkilendirilmiş kiracıları alır.

## ÖRNEKLERDEN

### Örnek 1: Tüm kiracıları alma
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

Bu örnekte, bir Azure hesabının tüm yetkili kiracıları nasıl alabileceğiniz gösterilmektedir.

### Örnek 2: belirli bir kiracı alma
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

Bu örnekte, bir Azure hesabında belirli bir yetkili kiracının nasıl alınacağı gösterilmektedir.

## PARAMETRELERINE

### -Tenantıd
Bu cmdlet 'in aldığı kiracının KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### PSAzureTenant
Bu cmdlet, geçerli hesap için yetkilendirilmiş kiracıları için kiracı KIMLIĞI ve ilişkili etki alanı bilgilerini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

