---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764789"
---
# Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem

## SYNOPSIS
Azure Site Recovery çoğaltması korumalı öğe için çoğaltmayı durdurur/devre dışı bırakır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermrecoveryservicesasrreplicationkorunabilir** , belirtilen Azure Site Recovery çoğaltma korumalı öğesinin çoğaltılmasını devre dışı bırakır.
Bu işlem, korumalı öğe için çoğaltmanın durmasına neden olur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

Belirtilen çoğaltma korumalı öğe için çoğaltmayı devre dışı bırak işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

## PARAMETRELERINE

### -Force
Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.

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

### -InputObject
Cmdlet 'e giriş nesnesi: çoğaltmanın devre dışı bırakıldığı çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WaitForCompletion
Cmdlet 'in işlemin tamamlanmasını beklemesi gerektiğini belirtir.

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

### -Onay
Onayın gerekli olup olmadığını belirtin. Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.

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
Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.

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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermrecoveryservicesasrreplicationkorunabilir.](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[New-Azurermrecoveryservicesasrreplicationkorunabilir.](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Set-Azurermrecoveryservicesasrreplicationkorunabilir.](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
