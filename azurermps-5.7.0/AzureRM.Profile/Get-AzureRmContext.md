---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593468"
---
# Get-AzureRmContext

## SYNOPSIS
Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### GetSingleContext (varsayılan)
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### Listallbağlamları
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzureRmContext cmdlet 'i, Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan geçerli meta verileri alır.

Bu cmdlet Active Directory hesabını, Active Directory kiracısı, Azure aboneliğini ve hedeflenen Azure ortamını alır.
Azure Resource Manager cmdlet 'leri Azure Resource Manager istekleri yaparken varsayılan olarak bu ayarları kullanın.

## ÖRNEKLERDEN

### Örnek 1: geçerli bağlamı alma
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Bu örnekte, Connect-AzureRmAccount kullanarak bir Azure aboneliğiyle hesabınıza oturum açıyor ve ardından Get-AzureRmContext 'i çağırarak geçerli oturumun bağlamını alıyoruz.

### Örnek 2: kullanılabilir tüm bağlamların listelenmesi
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

Bu örnekte, kullanılabilen tüm içerikler görüntülenir.  Kullanıcı, select-AzureRmContext kullanarak bu bağlamların birini seçebilir.

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

### -ListAvailable
Geçerli oturumdaki kullanılabilir tüm içeriği listeler.

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
İçeriğin adı

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### PSAzureContext
Bu cmdlet, Azure Resource Manager cmdlet 'lerinin kullandığı hesap, kiracı ve aboneliği döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRMContext](./Set-AzureRMContext.md)

