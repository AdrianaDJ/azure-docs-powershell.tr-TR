---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751844"
---
# Get-AzHDInsightOperationsManagementSuite

## SYNOPSIS
Kümedeki Operations Management Suite (OMS) yüklemesinin durumunu alır.

## INDEKI

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzHDInsightOperationsManagementSuite** cmdlet 'i, bir Azure HDıNSIGHT kümesindeki OMS yüklemesinin durumunu alır. OMS etkinleştirilirse, ayrıca OMS çalışma alanı kimliği 'ni de döndürür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir. Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği

### Örnek 2
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled özelliği doğru olduğundan kümede Operations Management Suite (OMS) etkinleştirilir. Günlüklerin akışını 1d364e89-bb71-4503-aa3d-a23535aea7bd olan OMS çalışma alanı kimliği

### Örnek 3
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.

### Örnek 4
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

ClusterMonitoringEnabled özelliği yanlış olduğundan kümede Operations Management Suite (OMS) devre dışı bırakıldı.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightOMS

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
