---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593466"
---
# Get-AzureRmSubscription

## SYNOPSIS
Geçerli hesabın erişebileceği abonelikleri alın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Listın (varsayılan)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listbynamei
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzureRmSubscription cmdlet 'i, geçerli hesabın erişebileceği abonelikler için abonelik KIMLIĞI, abonelik adı ve ev kiracısını alır.

## ÖRNEKLERDEN

### Örnek 1: Tüm kiracıları tüm abonelikleri al
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

Bu komut, geçerli hesap için yetkilendirilmiş tüm kiracıları tüm abonelikleri alır.

### Örnek 2: belirli bir kiracıya yönelik tüm abonelikleri alma
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

Belirtilen Kiracıdaki geçerli hesap için yetkilendirilmiş tüm abonelikleri listeler.

### Örnek 3: geçerli Kiracıdaki tüm abonelikleri alma
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

Bu komut geçerli Kiracıdaki geçerli kullanıcı için yetkilendirilmiş tüm abonelikleri alır.

### Örnek 4: belirli bir aboneliği kullanmak için geçerli bağlamı değiştirme
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

Bu komut belirtilen aboneliği alır ve geçerli bağlamı kullanacak şekilde ayarlar. Bu oturumdaki sonraki tüm cmdlet 'ler yeni aboneliği (contoso aboneliği 1) varsayılan olarak kullanır.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik

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

### -SubscriptionID
Alınacak aboneliğin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Alınacak aboneliğin adını belirtir.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tenantıd
Alınacak abonelikleri içeren kiracının KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Psazuyeniden gönderme komut dosyası

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

