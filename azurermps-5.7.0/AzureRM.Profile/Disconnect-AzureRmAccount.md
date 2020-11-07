---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764018"
---
# Disconnect-AzureRmAccount

## SYNOPSIS
Bağlı bir Azure hesabının bağlantısını keser ve bu hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ContextName (varsayılan)
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Desteklenmeyen
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipal
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContextObject
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Disconnect-AzureRmAccount cmdlet 'i bağlı bir Azure hesabının bağlantısını keser ve bu Firmayla ilişkili tüm kimlik bilgilerini ve bağlamları (abonelik ve kiracı bilgileri) kaldırır.

Bu cmdlet 'i çalıştırdıktan sonra Connect-AzureRmAccount kullanarak yeniden oturum açmanız gerekir.

## ÖRNEKLERDEN

### Geçerli hesabın oturumunu kapatma
```
PS C:\> Disconnect-AzureRmAccount
```

Geçerli içerikle ilişkili Azure hesabından oturum açar.

### Belirli bir içerikle ilişkili hesabın oturumu kapatma
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

Verilen içerikle ilişkili hesabı (' çalışma ' adlı) günlüğe kaydeder. Bu, ' CurrentUser ' kapsamını kullandığı için tüm kimlik bilgileri ve bağlamlar kalıcı olarak silinecektir.

### Belirli bir kullanıcının oturumunu kapatma
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

' user1@contoso.org ' Kullanıcıyı-tüm kimlik bilgilerini ve bu kullanıcıyla ilişkili tüm bağlamları günlüğe kaydeder.

## PARAMETRELERINE

### -ApplicationId
ServicePrincipal ID (genel benzersiz kimlik)

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContext
Dan

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ContextName
Oturumu kapatma bağlamının adı

```yaml
Type: String
Parameter Sets: ContextName
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

### -InputObject
Kaldırılacak hesap nesnesi

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapsam
Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenantıd
Kiracı kimliği (genel benzersiz kimlik)

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kullanıcı adı
' ' Formunun Kullanıcı adı user@contoso.org

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet yürütülmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount

### Microsoft. Azure. Commands. Profile. modeller. PSAzureContext

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Profile. modeller. PSAzureRmAccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
