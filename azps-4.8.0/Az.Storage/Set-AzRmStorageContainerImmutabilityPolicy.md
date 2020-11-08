---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273789"
---
# Set-AzRmStorageContainerImmutabilityPolicy

## SYNOPSIS
Depolama blob kapsayıcılarının

## INDEKI

### AccountName (varsayılan)
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExtendAccountName
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExtendAccountObject
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContainerObject
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Extenvseçcontainerobject
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Sandeğiştirici Bilitypolicyobject
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Extendimdeğiştirici Bilitypolicyobject
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-Azrmstoragecontainerımdeğiştirici bilitypolicy** cmdlet 'i, bir depolama blob kapsayıcılarının sandeğiştirici bir ilkesini oluşturur veya güncelleştirir

## ÖRNEKLERDEN

### Örnek 1: depolama alanı adı ve kapsayıcı adıyla birlikte depolama blob kapsayıcısının
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

Bu komut, depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini oluşturur veya güncelleştirir.

### Örnek 2: depolama alanı bir blob kapsayıcısının
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

Bu komut, depolama hesabı nesnesiyle bir depolama blob kapsayıcısının Sandeğiştirici Ilkelerini genişletir. Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.

### Örnek 3: bir depolama blob kapsayıcısının Claimdeğiştirici Ilkelerini güncelleştirme
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

Bu komut, depolama kapsayıcısı nesnesi 3 kez olan bir depolama blob kapsayıcısının ımdeğiştirici Ilkesini güncelleştirir: Ilk olarak, en az ETag olmadan, Arial dönemi 12 gün içinde olacak şekilde

### Örnek 4: bir depolama blob kapsayıcısının, Sandeğiştirici Ilke nesnesiyle
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

Bu komut, bir depolama blob kapsayıcısının sandeğiştirici, Genişletme ve Bilitypolicy yalnızca Sandeğiştirici Bilitypolicy kilitlendikten sonra çalışabilir.

## PARAMETRELERINE

### -AllowProtectedAppendWrite
Bu özellik yalnızca kilitlenmemiş süre tabanlı bekletme ilkeleri için değiştirilebilir. Bu özellik etkinleştirildiğinde, yeni bloklar, bir ekleme bloğuyla bir ekleme Yalnızca yeni bloklar eklenebilir ve var olan bloklar değiştirilemez veya silinemez.

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Kapsayıcı
Depolama kapsayıcısı nesnesi

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Kapsayıcıadı
Kapsayıcı adı

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ETag
İlke ETag 'i If-Extenvseçpolicy belirtilmezse, ETag isteğe bağlıdır; başka ETag gereklidir.

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Extenvseçpolicy
Var olan bir Sanval Bilitypolicy 'yi uzatmak için Extenvseçpolicy 'i belirtin.  Sandeğiştirici Bilitypolicy kilitlendikten sonra yalnızca uzatılaştırabilirsiniz. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sandeğiştirici
Gün içinde oluşturma işleminden itibaren kullanılabilirlik süresi

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Kapsayıcı adı

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
Depolama hesabı nesnesi

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Depolama hesabı adı.

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount

### Microsoft. Azure. Commands. Management. Storage. model. PSContainer

### Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Management. Storage. model. Psıdeğiştirici Bilitypolicy

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
