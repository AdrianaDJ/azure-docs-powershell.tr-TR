---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322274"
---
# Close-AzStorageFileHandle

## SYNOPSIS
Dosya paylaşımının dosya tanıtıcılarını, dosya dizinini veya dosyayı kapatır.

## INDEKI

### ShareNameCloseAll (varsayılan)
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ShareNameCloseSingle
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ShareCloseAll
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Paylaşım
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DirectoryCloseAll
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FileCloseAll
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Close-AzStorageFileHandle** cmdlet 'i dosya paylaşımının veya dosya dizininin veya dosyanın dosya tutamaçlarını kapatır.

## ÖRNEKLERDEN

### Örnek 1: geçerli depolama hesabının tüm dosya paylaşımlarını listeler ve dosya paylaşımlarının tüm dosya tanıtıcılarını yinelemeli olarak kapatın.
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

Bu komut geçerli depolama hesabının tüm dosya paylaşımlarını listeler ve dosya paylaşımlarının tüm dosya tanıtıcılarını yinelemeli olarak kapatır.

### Örnek 2: dosya dizinindeki tüm dosya tutamaçlarını özyinelemeli olarak kapatma ve kapalı dosya tanıtıcısı sayısını gösterme
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

Bu komut, dosya dizinindeki tüm dosya tanıtıcılarını kapatır ve kapatılan dosya tanıtıcısı sayısını gösterir.

### Örnek 3: dosya dizininde 1 gün önce açılan tüm dosya tutamaçlarını kapatın
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

Bu komut, dosya dizinindeki tüm dosya tanıtıcılarını yinelemeli olarak listeler, 1 gün önce açılan tutamaçları filtreler ve sonra da kapatır.

### Örnek 4: dosyadaki tüm dosya tutamaçlarını kapatma
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

Bu komut, dosyadaki tüm dosya tanıtıcılarını kapatır.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Her isteğin saniye cinsinden istemci tarafı maksimum yürütme süresi.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloseAll
Tüm dosya tutamaçlarını kapatmaya zorlayın.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Eşzamanlı eşzamansız görevlerin toplam miktarı.
Varsayılan değer 10 ' dır.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure depolama bağlamı nesnesi

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
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
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dizin
CloudFileDirectory nesnesi, dosyaların/dizinlerin listelenmekte olduğu temel klasörü belirtti.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Dosya
CloudFile nesnesi, kapatılacak dosyayı belirtti.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FileHandle
Kapatılacak dosya tutamacı.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Geçiş
Kapatılan dosya tanıtıcılarının sayısını döndür.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
Var olan bir dosyanın/dizinin yolu.

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yinelemeli
Liste tutamaçları yinelemeli olarak.
Yalnızca dosya dizininde çalışır.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Her isteğin saniye cinsinden zaman aşımı.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paylaşım
CloudFileShare nesnesi, dosyaların/dizinlerin listelendiği paylaşımı belirtti.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PaylaşımAdı
Dosyaların/dizinlerin listelendiği dosya paylaşımının adı.

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
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

### Microsoft. Azure. Storage. File. CloudFileShare

### Microsoft. Azure. Storage. File. CloudFileDirectory

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Azure. Storage. File. CloseFileHandleResultSegment

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
