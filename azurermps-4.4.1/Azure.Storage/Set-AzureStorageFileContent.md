---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6f0421c9b442bfc92dc693326542882ba2b0e8d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593872"
---
# Set-AzureStorageFileContent

## SYNOPSIS
Dosyanın içeriğini karşıya yükler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### PaylaşımAdı (varsayılan)
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Paylaş
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Directory
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureStorageFileContent** cmdlet 'i, dosyanın içeriğini belirtilen paylaşımda bir dosyaya yükler.

## ÖRNEKLERDEN

### Örnek 1: geçerli klasöre dosya yükleme
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Bu komut, geçerli klasörde DataFile37 adlı bir dosyayı, Contosoworkingklasöründeki Currentveri dosyası adlı bir dosya olarak yükler.

### Örnek 2: geçerli klasördeki tüm dosyaları yükleme
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

Bu örnekte, geçerli klasördeki tüm dosyaları Container ContosoShare06 kök klasörüne yüklemek için en yaygın Windows PowerShell cmdlet 'leri ve geçerli cmdlet kullanılır.

İlk komut geçerli klasörün adını alır ve $CurrentFolder değişkeninde depolar.

İkinci komut, ContosoShare06 adlı dosya paylaşımını almak için **Get-Azurestoragesshare** cmdlet 'ini kullanır ve $Container değişkeninde depolar.

Final komutu, geçerli klasörün içeriğini alır ve her birini Where-Object cmdlet 'ine aktarır ve ardışık düzen işlecini kullanın.
Bu cmdlet dosyaları olmayan nesneleri filtreler ve dosyaları ForEach-Object cmdlet 'ine geçirir.
Bu cmdlet, kendisi için uygun yolu oluşturan her dosya için bir betik bloğu çalıştırır ve ardından dosyayı karşıya yüklemek için geçerli cmdlet 'i kullanır.
Sonuçta, bu örnekte karşıya yüklenen diğer dosyalarla ilgili olarak aynı ad ve aynı göreli konum aynıdır.
Betik blokları hakkında daha fazla bilgi için, yazın `Get-Help about_Script_Blocks` .

## PARAMETRELERINE

### -ClientTimeoutPerRequest
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.
Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.
Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Maksimum eşzamanlı ağ çağrılarını belirtir.
Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.
Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.
Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.
Varsayılan değer 10 ' dır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure depolama bağlamını belirtir.
Depolama bağlamı edinmek için, [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet 'ini kullanın.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Dizin
Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.
Bu cmdlet, dosyayı bu parametrenin belirttiği klasöre yükler.
Dizin edinmek için New-AzureStorageDirectory cmdlet 'ini kullanın.
Dizin edinmek için Get-AzureStorageFile cmdlet 'ini de kullanabilirsiniz.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Bu cmdlet 'in var olan bir Azure depolama dosyasının üzerine yazabileceğini gösterir.

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

### -Geçiş
Bu cmdlet 'in oluşturduğu veya karşıya yükleyen **Azurestoragefile** nesnesini döndürmediğini belirtir.

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

### -Yol
Bir dosya veya klasörün yolunu belirtir.
Bu cmdlet, içeriği bu parametrenin belirttiği dosyaya veya bu parametrenin belirttiği klasörde karşıya yükler.
Bir klasör belirtirseniz, bu cmdlet kaynak dosyayla aynı ada sahip bir dosya oluşturur.

Varolmayan bir dosyanın yolunu belirtirseniz, bu cmdlet bu dosyayı oluşturur ve içeriği bu dosyaya kaydeder.
Var olan bir dosyayı belirtirseniz ve _Force_ parametresini belirtirseniz, bu cmdlet dosya içeriğinin üzerine yazar.
Var olan bir dosyayı belirtirseniz ve _Force_ belirtmezseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.

Varolmayan bir klasörün yolunu belirtirseniz, bu cmdlet hiçbir değişiklik yapmaz ve hata verir.


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
İsteğin sunucu kısmı için zaman aşımı süresinin uzunluğunu belirtir.

```yaml
Type: Int32
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
Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.
**Cloudfileshare** nesnesi edinmek için Get-AzureStorageShare cmdlet 'ini kullanın.
Bu nesne depolama bağlamını içerir.
Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.

```yaml
Type: CloudFileShare
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
Bu cmdlet, bu parametrenin belirttiği dosya paylaşımındaki bir dosyaya yükler.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kaynak
Bu cmdlet 'in karşıya yükleolduğu kaynak dosyayı belirtir.
Varolmayan bir dosya belirtirseniz, bu cmdlet bir hata döndürür.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
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

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

### CloudFileDirectory

' Directory ' parametresi ardışık düzenin ' CloudFileDirectory ' türünün değerini kabul eder

### CloudFileShare

' Share ' parametresi ardışık düzenin ' CloudFileShare ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[New-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)
