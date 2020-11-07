---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 792ca76f7259058991b8c181b383bdeffd7db290
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916675"
---
# <span data-ttu-id="cf221-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="cf221-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="cf221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf221-102">SYNOPSIS</span></span>
<span data-ttu-id="cf221-103">Kümede çalışan bir hizmetin bir kopyasını küme yapılandırma nesnesine ekler.</span><span class="sxs-lookup"><span data-stu-id="cf221-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="cf221-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf221-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf221-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf221-105">DESCRIPTION</span></span>
<span data-ttu-id="cf221-106">Add-AzHDInsightComponentVersion cmdlet, kümede çalışan bir hizmetin sürümünü, New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight yapılandırma nesnesine ekler.</span><span class="sxs-lookup"><span data-stu-id="cf221-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="cf221-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf221-107">EXAMPLES</span></span>

### <span data-ttu-id="cf221-108">Örnek 1: küme yapılandırma nesnesine Spark için bir sürüm ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cf221-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="cf221-109">Bu komut, Spark 'in sürümünü ' Spark-Spark-001 ' adlı HDInsight kümesine ekler.</span><span class="sxs-lookup"><span data-stu-id="cf221-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="cf221-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf221-110">PARAMETERS</span></span>

### <span data-ttu-id="cf221-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="cf221-111">-ComponentName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf221-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="cf221-112">-ComponentVersion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf221-113">-Config</span><span class="sxs-lookup"><span data-stu-id="cf221-113">-Config</span></span>
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

### <span data-ttu-id="cf221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf221-114">-DefaultProfile</span></span>
<span data-ttu-id="cf221-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cf221-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf221-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf221-116">-Confirm</span></span>
<span data-ttu-id="cf221-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf221-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf221-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf221-118">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf221-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf221-119">CommonParameters</span></span>
<span data-ttu-id="cf221-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf221-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf221-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf221-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf221-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf221-122">INPUTS</span></span>

### <span data-ttu-id="cf221-123">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cf221-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cf221-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf221-124">OUTPUTS</span></span>

### <span data-ttu-id="cf221-125">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cf221-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cf221-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf221-126">NOTES</span></span>

## <span data-ttu-id="cf221-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf221-127">RELATED LINKS</span></span>