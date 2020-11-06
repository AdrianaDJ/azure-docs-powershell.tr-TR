---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587666"
---
# Get-AzureRmEnrollmentAccount

## SYNOPSIS
Kayıt hesapları alın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Liste (varsayılan)
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Başına
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmEnrollmentAccount** cmdlet 'i kaydolma hesaplarını alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

Tüm kullanılabilir kayıt hesaplarını edinin.

### Örnek 2
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

Belirtilen nesne kimliğine sahip kayıt hesabını edinin.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectID
Belirli bir kayıt hesabının ObjectID.

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. faturalandırma. modeller. PSEnrollmentAccount, Microsoft. Azure. Commands. Faturalandırma, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. faturalandırma. modeller. PSEnrollmentAccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

