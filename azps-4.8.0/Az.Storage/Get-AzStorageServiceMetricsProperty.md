---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108602"
---
# Get-AzStorageServiceMetricsProperty

## SYNOPSIS
Azure depolama hizmeti için ölçüm özelliklerini alır.

## INDEKI

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzStorageServiceMetricsProperty** cmdlet 'ı Azure depolama hizmeti için ölçüm özelliklerini alır.

## ÖRNEKLERDEN

### Örnek 1: blob hizmeti için ölçüm özelliklerini alma
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Bu komut, saat ölçümü türü için BLOB depolama alanının ölçüm özelliklerini alır.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
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

### -MetricsType
Ölçüm türünü belirtir.
Bu cmdlet, bu parametrenin belirttiği ölçüm türü için Azure depolama hizmeti ölçümleri özelliklerini alır.
Bu parametre için kabul edilebilir değerler: Hour ve Minute.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
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
- Dosya dosyanın değeri şu anda desteklenmiyor.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzStorageContext](./New-AzStorageContext.md)

[Set-AzStorageServiceMetricsProperty](./Set-AzStorageServiceMetricsProperty.md)


