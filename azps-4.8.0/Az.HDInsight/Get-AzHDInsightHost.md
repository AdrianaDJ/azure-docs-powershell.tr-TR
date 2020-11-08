---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108255"
---
# <span data-ttu-id="1b2b1-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="1b2b1-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="1b2b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2b1-103">HDInsight kümesinin konaklarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="1b2b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b2b1-104">SYNTAX</span></span>

### <span data-ttu-id="1b2b1-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b2b1-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b2b1-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1b2b1-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b2b1-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b2b1-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b2b1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b2b1-108">DESCRIPTION</span></span>
<span data-ttu-id="1b2b1-109">**Get-AzHDInsightHost** cmdlet 'i HDInsight kümesinin konaklarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="1b2b1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b2b1-110">EXAMPLES</span></span>

### <span data-ttu-id="1b2b1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b2b1-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="1b2b1-112">Bu komut küme adı içeren kümenin ana bilgisayarlarının listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="1b2b1-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1b2b1-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="1b2b1-114">Bu komut kümesinin ardışık düzeni</span><span class="sxs-lookup"><span data-stu-id="1b2b1-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="1b2b1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b2b1-115">PARAMETERS</span></span>

### <span data-ttu-id="1b2b1-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1b2b1-116">-ClusterName</span></span>
<span data-ttu-id="1b2b1-117">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2b1-118">-DefaultProfile</span></span>
<span data-ttu-id="1b2b1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b2b1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b2b1-120">-InputObject</span></span>
<span data-ttu-id="1b2b1-121">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b2b1-123">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2b1-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1b2b1-124">-ResourceId</span></span>
<span data-ttu-id="1b2b1-125">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2b1-126">CommonParameters</span></span>
<span data-ttu-id="1b2b1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2b1-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b2b1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2b1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b2b1-129">INPUTS</span></span>

### <span data-ttu-id="1b2b1-130">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1b2b1-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="1b2b1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b2b1-131">OUTPUTS</span></span>

### <span data-ttu-id="1b2b1-132">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="1b2b1-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="1b2b1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b2b1-133">NOTES</span></span>

## <span data-ttu-id="1b2b1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b2b1-134">RELATED LINKS</span></span>
