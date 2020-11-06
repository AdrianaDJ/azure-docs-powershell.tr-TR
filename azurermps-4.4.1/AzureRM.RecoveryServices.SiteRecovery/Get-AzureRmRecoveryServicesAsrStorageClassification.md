---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594191"
---
# Get-AzureRmRecoveryServicesAsrStorageClassification

## SYNOPSIS
Kurtarma Hizmetleri kasasındaki kullanılabilir (keşfedilen) ASR depolama sınıflandırmalarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFabricObject (varsayılan)
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## Tanım
**Get-Azurermrecoveryservicesasrstorageclassıfist** cmdlet 'ı, kurtarma hizmetleri KASASıNDAKI bulunan ASR depolama sınıflandırmalarını ayrıntılarını alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

Belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmalarını listeleyin. 

## PARAMETRELERINE

### -Kumaş
ASR Fabric nesnesini belirtir. Cmdlet, belirtilen ASR dokusunda belirtilen bulunan depolama sınıflandırmaları ayrıntılarını alır. 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
Alınacak depolama sınıflandırması nesnesinin kolay adını belirtir.

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak depolama sınıflandırması nesnesinin adını belirtir.

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Services. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

