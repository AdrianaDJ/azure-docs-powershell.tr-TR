---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764850"
---
# Get-AzureRmHDInsightOperationsManagementSuite

## SYNOPSIS
Kümedeki Operations Management Suite (OMS) yüklemesinin durumunu alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmHDInsightOperationsManagementSuite** cmdlet 'i, bir Azure HDıNSIGHT kümesindeki OMS yüklemesinin durumunu alır. OMS etkinleştirilirse, ayrıca OMS çalışma alanı kimliği 'ni de döndürür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir. Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği

### Örnek 2
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir. Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği

### Örnek 3
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.

### Örnek 4
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.

## PARAMETRELERINE

### -Ad
Işlem yönetim paketinin (OMS) durumunu almak için kümenin adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Kümenin kaynak grubu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightOMS

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

