---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: b34fbf01196f5e25cb62ed7d9ecb0ba78aafa17f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751860"
---
# Add-AzHDInsightScriptAction

## SYNOPSIS
Küme yapılandırma nesnesine bir komut dosyası eylemi ekler.

## INDEKI

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzHDInsightScriptAction** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet tarafından oluşturulan HDInsight yapılandırma nesnesine betik eylemleri ekler.
Komut dosyası eylemleri, Windows PowerShell veya bash betiklerini (sırasıyla Windows veya Linux kümeleri için) kullanarak bir Hadoop kümesinde çalışan uygulamaların yapılandırmalarını değiştirmek veya ek yazılım yüklemek için kullanılan işlevleri sağlar.
Bir betik eylemi, HDInsight kümeleri dağıtıldığında küme düğümlerinde çalışır ve kümenin tamamlanma HDInsight yapılandırmasındaki düğümlerden sonra çalışırlar.
Komut dosyası eylemi sistem yöneticisi hesap ayrıcalıklarıyla çalışır ve küme düğümlerine tam erişim hakları sağlar.
Belirli bir sırada çalışacak bir komut dosyası eylemleri listesi içeren her kümeyi sağlayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: küme yapılandırma nesnesine bir komut dosyası eylemi ekleme
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

Bu komut,-Hadoop-001 kümenizin baş ve çalışan düğümlerine yönelik bir komut dosyası eylemi ekleyerek küme oluşturmanın sonunda da çalışır.

## PARAMETRELERINE

### -Config
Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.
Bu nesne, **New-AzHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Betik eyleminin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeType
Betik eyleminin çalıştırılacağı düğüm türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- HeadNode
- WorkerNode
- ZookeeperNode

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parametreler
Betik eyleminin parametrelerini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Betik eyleminin Genel URI 'sini (PowerShell veya bash betiği) belirtir.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig

## ÇıKıŞLAR

### Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzHDInsightClusterConfig](./New-AzHDInsightClusterConfig.md)


