---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: d103a2bc3d23ff37857592ed9496e625302ed144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938527"
---
# <span data-ttu-id="dce8d-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="dce8d-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="dce8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce8d-102">SYNOPSIS</span></span>
<span data-ttu-id="dce8d-103">Küme yapılandırma nesnesine bir komut dosyası eylemi ekler.</span><span class="sxs-lookup"><span data-stu-id="dce8d-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="dce8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dce8d-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce8d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dce8d-105">DESCRIPTION</span></span>
<span data-ttu-id="dce8d-106">**Add-AzHDInsightScriptAction** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet tarafından oluşturulan HDInsight yapılandırma nesnesine betik eylemleri ekler.</span><span class="sxs-lookup"><span data-stu-id="dce8d-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="dce8d-107">Komut dosyası eylemleri, Windows PowerShell veya bash betiklerini (sırasıyla Windows veya Linux kümeleri için) kullanarak bir Hadoop kümesinde çalışan uygulamaların yapılandırmalarını değiştirmek veya ek yazılım yüklemek için kullanılan işlevleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="dce8d-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="dce8d-108">Bir betik eylemi, HDInsight kümeleri dağıtıldığında küme düğümlerinde çalışır ve kümenin tamamlanma HDInsight yapılandırmasındaki düğümlerden sonra çalışırlar.</span><span class="sxs-lookup"><span data-stu-id="dce8d-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="dce8d-109">Komut dosyası eylemi sistem yöneticisi hesap ayrıcalıklarıyla çalışır ve küme düğümlerine tam erişim hakları sağlar.</span><span class="sxs-lookup"><span data-stu-id="dce8d-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="dce8d-110">Belirli bir sırada çalışacak bir komut dosyası eylemleri listesi içeren her kümeyi sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dce8d-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="dce8d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dce8d-111">EXAMPLES</span></span>

### <span data-ttu-id="dce8d-112">Örnek 1: küme yapılandırma nesnesine bir komut dosyası eylemi ekleme</span><span class="sxs-lookup"><span data-stu-id="dce8d-112">Example 1: Add a script action to the cluster configuration object</span></span>
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

<span data-ttu-id="dce8d-113">Bu komut,-Hadoop-001 kümenizin baş ve çalışan düğümlerine yönelik bir komut dosyası eylemi ekleyerek küme oluşturmanın sonunda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="dce8d-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="dce8d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dce8d-114">PARAMETERS</span></span>

### <span data-ttu-id="dce8d-115">-Config</span><span class="sxs-lookup"><span data-stu-id="dce8d-115">-Config</span></span>
<span data-ttu-id="dce8d-116">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dce8d-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="dce8d-117">Bu nesne, **New-AzHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dce8d-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="dce8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce8d-118">-DefaultProfile</span></span>
<span data-ttu-id="dce8d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dce8d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dce8d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dce8d-120">-Name</span></span>
<span data-ttu-id="dce8d-121">Betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dce8d-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="dce8d-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="dce8d-122">-NodeType</span></span>
<span data-ttu-id="dce8d-123">Betik eyleminin çalıştırılacağı düğüm türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dce8d-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="dce8d-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dce8d-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dce8d-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="dce8d-125">HeadNode</span></span>
- <span data-ttu-id="dce8d-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="dce8d-126">WorkerNode</span></span>
- <span data-ttu-id="dce8d-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="dce8d-127">ZookeeperNode</span></span>

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

### <span data-ttu-id="dce8d-128">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="dce8d-128">-Parameters</span></span>
<span data-ttu-id="dce8d-129">Betik eyleminin parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dce8d-129">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="dce8d-130">-URI</span><span class="sxs-lookup"><span data-stu-id="dce8d-130">-Uri</span></span>
<span data-ttu-id="dce8d-131">Betik eyleminin Genel URI 'sini (PowerShell veya bash betiği) belirtir.</span><span class="sxs-lookup"><span data-stu-id="dce8d-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="dce8d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce8d-132">CommonParameters</span></span>
<span data-ttu-id="dce8d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dce8d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce8d-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce8d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce8d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dce8d-135">INPUTS</span></span>

### <span data-ttu-id="dce8d-136">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="dce8d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="dce8d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dce8d-137">OUTPUTS</span></span>

### <span data-ttu-id="dce8d-138">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="dce8d-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="dce8d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dce8d-139">NOTES</span></span>

## <span data-ttu-id="dce8d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dce8d-140">RELATED LINKS</span></span>

[<span data-ttu-id="dce8d-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="dce8d-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

