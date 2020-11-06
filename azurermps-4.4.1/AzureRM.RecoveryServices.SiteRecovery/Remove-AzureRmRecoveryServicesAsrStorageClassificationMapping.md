---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593039"
---
# Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping

## SYNOPSIS
Belirtilen ASR depolama sınıflandırması eşlemesini siler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı belirtilen Azure Site Recovery depolama sınıflandırması eşlemesini siler.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

Belirtilen depolama sınıflandırması eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

## PARAMETRELERINE

### -InputObject
Cmdlet 'e giriş nesnesi: ASR depolama sınıflandırması eşlemesine, ASR depolama sınıflandırması eşleme nesnesi silinecektir.

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermrecoveryservicesasrstorageclassıficationmapping](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[New-Azurermrecoveryservicesasrstorageclassıficationmapping](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
