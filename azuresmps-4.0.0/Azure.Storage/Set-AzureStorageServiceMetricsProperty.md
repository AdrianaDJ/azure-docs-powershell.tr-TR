---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572473"
---
# Set-AzureStorageServiceMetricsProperty

## SYNOPSIS
Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.

## INDEKI

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Tanım
**Set-AzureStorageServiceMetricsProperty** cmdlet 'ı, Azure depolama hizmeti 'nin ölçüm özelliklerini değiştirir.

## ÖRNEKLERDEN

### Örnek 1: blob hizmeti için ölçüm özelliklerini değiştirme
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

Bu komut, BLOB depolama için sürüm 1,0 ölçümlerini bir hizmet düzeyine değiştirir.
Azure depolama hizmeti ölçümleri 10 günlük girişleri korur.
Bu komut *passin* parametresini belirttiğinden, komut değiştirilmiş ölçüler özelliklerini görüntüler.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.

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

### -MetricsLevel
Azure Storage 'un hizmet için kullandığı ölçü düzeyini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yabilirsiniz
- Hizmetinin
- ServiceAndApi

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsType
Ölçüm türünü belirtir.
Bu cmldet, Azure depolama hizmeti ölçümleri türünü bu parametrenin belirttiği değere ayarlar.
Bu parametre için kabul edilebilir değerler: Hour ve Minute.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'lerin güncelleştirilmiş ölçüm özelliklerini döndürmediğini belirtir.
Bu parametreyi belirtmezseniz, bu cmdlet bir değer döndürmez.

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

### -RetentionDays
Azure depolama hizmeti 'nin ölçüm bilgilerini koruduğu gün sayısını belirtir.

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
Depolama hizmeti türünü belirtir.
Bu cmdlet, bu parametrenin belirttiği hizmet türünün ölçüm özelliklerini değiştirir.
Bu parametre için kabul edilebilir değerler şunlardır:

- 'Unu 
- Tablo
- Kuyruğ
- Dosyasý

Dosya değeri şu anda desteklenmiyor.

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

### -Version
Azure depolama alanı ölçümlerinin sürümünü belirtir.
Varsayılan değer 1,0 ' dır.

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-AzureStorageServiceMetricsProperty](./Get-AzureStorageServiceMetricsProperty.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


