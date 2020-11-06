---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
ms.openlocfilehash: 635b8e1524f6123aa6ddde4ed7a64768d6c3d791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572485"
---
# Set-AzureStorageCORSRule

## SYNOPSIS
Bir depolama hizmeti türü için CORS kurallarını ayarlar.

## INDEKI

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Tanım
**Set-AzureStorageCORSRule** cmdlet 'i, bir Azure depolama hizmeti türünün çapraz kaynak PAYLAŞıMı (CORS) kurallarını ayarlar.
Bu cmdlet için depolama hizmetleri türleri blob, tablo, kuyruk ve dosyadır.
Bu cmdlet var olan kuralların üzerine yazılır.
Geçerli kuralları görmek için Get-AzureStorageCORSRule cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: blob hizmetine CORS kuralları atama
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

İlk komut $CorsRules değişkenine bir dizi kural atar.
Bu komut, bu kod bloğundaki birkaç satırın yerine standart extends kullanır.

İkinci komut $CorsRules kuralları blob hizmet türüne atar.

### Örnek 2: blob hizmeti için CORS kuralının özelliklerini değiştirme
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

İlk komut, **Get-AzureStorageCORSRule** cmdlet 'Ini kullanarak blob türünün geçerli CORS kurallarını alır.
Komut, kuralları $CorsRules dizi değişkeninde depolar.

İkinci ve üçüncü komutlar $CorsRules ilk kuralı değiştirir.

Son komut $CorsRules kuralları blob hizmet türüne atar.
Gözden geçirilmiş kurallar geçerli CORS kurallarının üzerine yazılır.

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
Bağlam almak için New-AzureStorageContext cmdlet 'ini kullanın.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -CorsRules
CORS kuralları dizisi belirtir.
Get-AzureStorageCORSRule cmdlet 'ini kullanarak var olan kuralları alabilirsiniz.

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'in işlemin başarısını yansıtan bir Boole değeri döndürdüğü anlamına gelir.
Varsayılan olarak, bu cmdlet değer döndürmez.

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

### -ServiceType
Bu cmdlet 'in kuralları atadığı Azure depolama hizmeti türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- 'Unu 
- Tablo 
- Kuyruğ 
- Dosyasý

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageCORSRule](./Get-AzureStorageCORSRule.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Remove-AzureStorageCORSRule](./Remove-AzureStorageCORSRule.md)


