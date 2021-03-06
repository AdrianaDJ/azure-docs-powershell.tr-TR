---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 0777c24aa5cb9b505ffc3495c9a9220da912f055
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758659"
---
# Get-AzStorageFileContent

## SYNOPSIS
Dosyanın içeriğini indirir.

## INDEKI

### PaylaşımAdı (varsayılan)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Paylaş
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Directory
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Dosyasý
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Get-AzStorageFileContent** cmdlet 'inin içeriğini indirir ve bunu belirttiğiniz bir hedefe kaydeder.
Bu cmdlet dosyanın içeriğini döndürmez.

## ÖRNEKLERDEN

### Örnek 1: klasörden dosya Indirme
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Bu komut, ContosoShare06 dosya paylaşımı klasöründeki GeçerliVeri dosyası adlı dosyayı geçerli klasöre indirir.

### Örnek 2: örnek dosya paylaşımı altındaki dosyaları Indirir
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

Bu örnekte, örnek dosya paylaşımı altındaki dosyalar indirilir

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın.

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

### -CheckMd5
İndirilen dosyanın MD5 toplamının olup olmadığını belirtir.

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
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir. Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener. Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

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
Maksimum eşzamanlı ağ çağrılarını belirtir. Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz. Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı. Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye. Varsayılan değer 10 ' dır.

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
Azure depolama bağlamını belirtir. Bağlam almak için New-AzStorageContext cmdlet 'ini kullanın.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
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
Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.
Dizin edinmek için Get-AzStorageFile cmdlet 'ini de kullanabilirsiniz.

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
**Cloudfile** nesnesi edinmek için Get-AzStorageFile cmdlet 'ini kullanın.

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
Bu cmdlet 'in indiren **Ragefıle** nesnesini geri aldığını gösterir.

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
İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir. Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.

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
**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.
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

### Microsoft. Windowsazde. Storage. File. CloudFileDirectory

### Microsoft. Windowsazde. Storage. File. CloudFile

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Windowsazde. Storage. File. CloudFile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


