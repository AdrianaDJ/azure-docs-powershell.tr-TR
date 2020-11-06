---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571750"
---
# Get-AzureRmContext

## SYNOPSIS
Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.

## INDEKI

```
Get-AzureRmContext [<CommonParameters>]
```

## Tanım
Get-AzureRmContext cmdlet 'i, Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan geçerli meta verileri alır.

Bu cmdlet Active Directory hesabını, Active Directory kiracısı, Azure aboneliğini ve hedeflenen Azure ortamını alır.
Azure Resource Manager cmdlet 'leri Azure Resource Manager istekleri yaparken varsayılan olarak bu ayarları kullanın.

## ÖRNEKLERDEN

### Örnek 1: geçerli bağlamı alma
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Bu örnekte, Add-AzureRmAccount kullanarak bir Azure aboneliğiyle hesabınıza oturum açıyoruz ve ardından Get-AzureRmContext ' i çağırarak geçerli oturumun bağlamını alıyoruz.

## PARAMETRELERINE

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### PSAzureContext
Bu cmdlet, Azure Resource Manager cmdlet 'lerinin kullandığı hesap, kiracı ve aboneliği döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRMContext]()

