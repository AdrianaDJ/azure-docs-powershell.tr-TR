---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593088"
---
# Get-AzureRmMlOpClusterKey

## SYNOPSIS
Bir operationalization kümesiyle ilişkili erişim tuşlarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Cmdlet Giriş parametrelerinden operationalization kümesinin anahtarlarını alın.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### OperationalizationCluster örneğinin tanımını alma.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Azure kaynak kimliğinden operationalization kümesinin anahtarlarını alın.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## Tanım
Küme özellikleri alınırken depolama hesabının, kapsayıcı kayıt defterinin ve operationalization kümesiyle ilişkili diğer hizmetlerin anahtarları döndürülmez. Hassas bilgiler olduğundan anahtarları almak için belirli bir çağrı yapılmalıdır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Operationalization kümesiyle ilişkili hizmetler için gizli anahtarları döndürür.

## PARAMETRELERINE

### -InputObject
Operationalization kümesi nesnesi.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Operationalization kümesi adı.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster
System. String


## ÇıKıŞLAR

### Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationClusterCredentials


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

