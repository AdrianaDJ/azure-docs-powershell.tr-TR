---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589633"
---
# Get-AzureStorageFileContent

## SYNOPSIS
Dosyanın içeriğini indirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### PaylaşımAdı (varsayılan)
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Paylaş
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Directory
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Dosyasý
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Get-AzureStorageFileContent** cmdlet 'i bir dosyanın içeriğini indirir ve bunu belirttiğiniz bir hedefe kaydeder.
Bu cmdlet dosyanın içeriğini döndürmez.

## ÖRNEKLERDEN

### Örnek 1: klasörden dosya Indirme
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Bu komut, ContosoShare06 dosya paylaşımı klasöründeki GeçerliVeri dosyası adlı dosyayı geçerli klasöre indirir.

### Örnek 2: örnek dosya paylaşımı altındaki dosyaları Indirir
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

Bu örnekte, örnek dosya paylaşımı altındaki dosyalar indirilir

## PARAMETRELERINE

### -CheckMd5
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

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
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

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

### -ConcurrentTaskCount
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

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
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hedef
Hedef yolu belirtir.
Bu cmdlet, dosya içeriğini bu parametrenin belirttiği konuma indirir.
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dizin
Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.
Bu cmdlet, bu parametrenin belirttiği klasördeki bir dosyanın içeriğini alır.
Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.
Dizin edinmek için Get-AzureStorageFile cmdlet 'ini de kullanabilirsiniz.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Dosya
Bir dosyayı **cloudfile** nesnesi olarak belirtir.
Bu cmdlet, bu parametrenin belirttiği dosyayı alır.
**Cloudfile** nesnesi edinmek için Get-AzureStorageFile cmdlet 'ini kullanın.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

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

### -Geçiş
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

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
Dosyanın yolunu belirtir.
Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya alır.
Dosya yoksa, bu cmdlet hata döndürür.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği yeni dosyaya kaydeder.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* parametresini belirtirseniz, cmdlet dosyanın üzerine yazılır.
Var olan bir dosyanın yolunu belirtirseniz ve *Force* belirtmezseniz, cmdlet devam etmeden önce sorar.
Bir klasörün yolunu belirtirseniz, bu cmdlet, Azure depolama dosyasının adını içeren bir dosya oluşturmaya çalışır.

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

### -Paylaşım
Bir **Cloudfileshare** nesnesi belirtir.
Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.
**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.
Bu nesne depolama bağlamını içerir.
Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PaylaşımAdı
Dosya paylaşımının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği paylaşımın dosya içeriğini indirir.

```yaml
Type: System.String
Parameter Sets: ShareName
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazde. Storage. File. CloudFileShare
Parametreler: paylaşma (ByValue)

### Microsoft. Windowsazde. Storage. File. CloudFileDirectory
Parametreler: Dizin (ByValue)

### Microsoft. Windowsazde. Storage. File. CloudFile
Parametreler: FILE (ByValue)

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Windowsazde. Storage. File. CloudFile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


