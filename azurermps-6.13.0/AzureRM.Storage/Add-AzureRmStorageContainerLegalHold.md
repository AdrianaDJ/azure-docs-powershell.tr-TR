---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587124"
---
# Add-AzureRmStorageContainerLegalHold

## SYNOPSIS
Depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekler

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### AccountName (varsayılan)
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccountObject
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContainerObject
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-AzureRmStorageContainerLegalHold** cmdlet 'ı bir depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekler

## ÖRNEKLERDEN

### Örnek 1: depolama alanı adı ve kapsayıcı adı içeren bir depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekleme
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

Bu komut, depolama alanı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısına geçerli ayrı tutma etiketleri ekler.

### Örnek 2: depolama hesabı nesnesi ve kapsayıcı adı bulunan depolama blob kapsayıcısına yasal ayrı tutma etiketleri ekleme
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

Bu komut, depolama hesabı nesnesi ve kapsayıcı adı bulunan bir depolama blob kapsayıcısına geçerli ayrı tutma etiketleri ekler.

### Örnek 3: ardışık düzen ile depolama hesabındaki tüm depolama blob kapsayıcılarına yasal ayrı tutma etiketleri ekleme
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama blob kapsayıcılarına geçerli ayrı tutma etiketleri ekler.

## PARAMETRELERINE

### Kapsayıcı
Depolama kapsayıcısı nesnesi

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Ad
Kapsayıcı adı

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: AccountName
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
Type: PSStorageAccount
Parameter Sets: AccountObject
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
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Container LegalHold etiketleri

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Management. Storage. model. PSLegalHold

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

