---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764797"
---
# Get-AzureRmRecoveryServicesAsrNetworkMapping

## SYNOPSIS
Geçerli kasa için site kurtarma ağ eşlemeleri hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByObject (varsayılan)
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## Tanım
**Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı, kurtarma hizmetleri Kasası Için Azure Site Recovery ağ eşlemeleri hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

Geçirilen ağın tüm ağ eşlemelerini alır.

## PARAMETRELERINE

### -Ad
Alınacak ASR ağ eşleme nesnesinin adı.

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

### -Ağ
Belirtilen ağ ASR nesnesine karşılık gelen ASR ağ eşleştirmelerini edinin.

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices., Services. Siterecomappmapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmRecoveryServicesAsrNetworkMapping](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[Remove-AzureRmRecoveryServicesAsrNetworkMapping](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
