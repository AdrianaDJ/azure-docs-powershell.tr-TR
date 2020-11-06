---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587074"
---
# Get-AzureStorageServiceMetricsProperty

## SYNOPSIS
Azure depolama hizmeti için ölçüm özelliklerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti için ölçüm özelliklerini alır.

## ÖRNEKLERDEN

### Örnek 1: blob hizmeti için ölçüm özelliklerini alma
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Bu komut, saat ölçümü türü için BLOB depolama alanının ölçüm özelliklerini alır.

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

### -MetricsType
Ölçüm türünü belirtir.
Bu cmdlet, bu parametrenin belirttiği ölçüm türü için Azure depolama hizmeti ölçümleri özelliklerini alır.
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

### -ServiceType
Depolama hizmeti türünü belirtir.
Bu cmdlet, bu parametrenin belirttiği türün ölçüm özelliklerini alır.
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Windowsazme. Storage. Shared. Protocol. MetricsProperties

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


