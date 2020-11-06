---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594193"
---
# Get-AzureRmRecoveryServicesAsrProtectionContainerMapping

## SYNOPSIS
Azure Site Recovery koruma kapsayıcısı eşleştirmelerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByObject (varsayılan)
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## Tanım
**Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'ı belirtilen ASR koruma kapsayıcısının kasasındaki çoğaltma ilkesi eşlemeleri (ilişkilendirme) hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

Belirtilen koruma kapsayıcısının tüm koruma kapsayıcısı eşlemelerini alır.

## PARAMETRELERINE

### -Ad
Alınacak koruma kapsayıcısı eşlemesinin adını belirtir.

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

### -ProtectionContainer
Belirtilen ASR koruma kapsayıcısı nesnesine karşılık gelen koruma kapsayıcısı eşlemelerini alın.

```yaml
Type: ASRProtectionContainer
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmRecoveryServicesAsrProtectionContainerMapping](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
