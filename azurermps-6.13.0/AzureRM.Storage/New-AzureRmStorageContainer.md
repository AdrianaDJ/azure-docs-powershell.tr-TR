---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587123"
---
# New-AzureRmStorageContainer

## SYNOPSIS
Depolama blob kapsayıcısı oluşturur

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### AccountName (varsayılan)
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AccountObject
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmStorageContainer** cmdlet 'ı bir depolama blob kapsayıcısı oluşturur

## ÖRNEKLERDEN

### Örnek 1: meta veri içeren depolama hesabı adı ve kapsayıcı adıyla depolama blob kapsayıcısı oluşturma
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

Bu komut meta veri ile depolama hesabı adı ve kapsayıcı adı olan bir depolama blob kapsayıcısı oluşturur.

### Örnek 2: blob olarak Genel erişimli depolama hesabı nesnesi ve kapsayıcı adıyla bir depolama blob kapsayıcısı oluşturma
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

Bu komut, blob olarak Genel erişimli depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı oluşturur.

## PARAMETRELERINE

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

### -Metadata
Kapsayıcı meta verileri

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

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
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PublicAccess
Kapsayıcı yayımlanabilir

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. Management. Storage. model. PSContainer

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

