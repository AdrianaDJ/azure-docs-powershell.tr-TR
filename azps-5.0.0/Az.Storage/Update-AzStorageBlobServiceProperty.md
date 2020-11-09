---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323557"
---
# Update-AzStorageBlobServiceProperty

## SYNOPSIS
Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.

## INDEKI

### AccountName (varsayılan)
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Blobservicepropertiesresourceıd
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Update-AzStorageBlobServiceProperty** cmdlet 'ı, Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.

## ÖRNEKLERDEN

### Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2018-03-28 olarak ayarlama
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

Bu komut, Blob hizmetinin Defaultservicesürümünü 2018-03-28 olarak ayarlar.

### Örnek 2: depolama hesabının blob hizmetinde changefeed 'i etkinleştirme
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

Bu komut bir depolama hesabının blob hizmetinde changefeed 'i etkinleştirirse, herhangi bir blob düzeyi oluşturma, değiştirme veya silme etkinliği Ardından, depolama hesabındaki $blobchangefeed kapsayıcısında depolanan BLOB 'lar için sıralı olayların günlüğünü verir. Serileştirilmiş değişiklikler Apache avro dosyası olarak kalıcıdır ve zaman uyumsuz ve artımlı olarak işlenebilir.

### Örnek 3: depolama hesabının blob hizmetinde sürüm oluşturmayı etkinleştirme
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

Bu komut, depolama hesabının blob hizmetinde sürüm oluşturmayı olanaklı kılar

## PARAMETRELERINE

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

### -DefaultServiceVersion
Ayarlanacak varsayılan hizmet sürümü

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableChangeFeed
Depolama hesabı için günlük kaydını Değiştir 'i $true olarak ayarlayarak, $false olarak ayarlayarak akış günlüğünü Değiştir 'i devre dışı bırakın.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Isversioningenabled
Doğru olarak ayarlandığında sürüm oluşturma özelliği etkin olur veya ayarlanır.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
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
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Depolama hesabı adı.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
