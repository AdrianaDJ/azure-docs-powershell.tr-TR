---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592615"
---
# Get-AzureRmMlOpCluster

## SYNOPSIS
Bir operationalization küme nesnesi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Bir operationalization kümesi nesnesini ada göre veya kaynak grubuna göre veya abonelikle alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

Belirli bir operationalization kümesini ada göre alır.

### Örnek 2
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

Kaynak grubundaki tüm operationalization kümelerini alır.

### Örnek 3
```
PS C:\> Get-AzureRmMlOpCluster
```

Bir abonelikteki tüm operationalization kümelerini alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Operationalization kümesi için kaynak grubunun adı.

```yaml
Type: String
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

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. modeller. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

