---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594644"
---
# Update-AzureRmMlOpClusterSystemService

## SYNOPSIS
Operationalization kümesinin sistem hizmetlerinde bir güncelleştirme başlatır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Cmdlet Giriş parametrelerinden bir sistem hizmetleri güncelleştirmesi başlatın.
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### Bir PSOperationalizationCluster örneği tanımından bir sistem hizmetleri güncelleştirmesi başlatın.
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Bir Azure kaynak kimliğinden sistem hizmetleri güncelleştirmesini başlatın.
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## Tanım
Sistem Hizmetleri, operationalization kümesinden bağımsız olarak güncelleştirilebilir. Sistem hizmetlerinde güncelleştirme başlatmak için bu cmdlet 'i kullanın. Güncelleştirme yoksa güncelleştirme yine başlatılır ve başarıyla geri döner. Güncelleştirme tamamlandıktan sonra, bir kez başlatıldığında, bittiğinde ve başarılı olduysa.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

Belirtilen kümede sistem hizmetleri güncelleştirmesini başlatır. 

## PARAMETRELERINE

### -InputObject
Operationalization kümesi nesnesi.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

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

### -Ad
Operationalization kümesi adı.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Operationalization kümesi için kaynak grubunun adı.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Operationalization kümesi için Azure Resource ID.

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster
### System. String


## ÇıKıŞLAR

### Microsoft. Azure. Commands. MachineLearningCompute. model. PSUpdateSystemServicesResponse


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

