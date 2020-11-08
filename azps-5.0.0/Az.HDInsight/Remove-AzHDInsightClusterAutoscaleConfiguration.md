---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277831"
---
# <span data-ttu-id="d7118-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7118-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="d7118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7118-102">SYNOPSIS</span></span>
<span data-ttu-id="d7118-103">HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7118-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="d7118-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7118-104">SYNTAX</span></span>

### <span data-ttu-id="d7118-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7118-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7118-106">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d7118-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7118-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7118-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7118-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7118-108">DESCRIPTION</span></span>
<span data-ttu-id="d7118-109">**Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet 'i HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7118-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="d7118-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7118-110">EXAMPLES</span></span>

### <span data-ttu-id="d7118-111">Örnek 1: HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="d7118-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="d7118-112">Bu komut HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7118-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="d7118-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7118-113">PARAMETERS</span></span>

### <span data-ttu-id="d7118-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d7118-114">-AsJob</span></span>
<span data-ttu-id="d7118-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d7118-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7118-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d7118-116">-ClusterName</span></span>
<span data-ttu-id="d7118-117">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d7118-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7118-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7118-118">-DefaultProfile</span></span>
<span data-ttu-id="d7118-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7118-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7118-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7118-120">-InputObject</span></span>
<span data-ttu-id="d7118-121">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d7118-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7118-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7118-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7118-123">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d7118-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7118-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d7118-124">-ResourceId</span></span>
<span data-ttu-id="d7118-125">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d7118-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7118-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7118-126">-Confirm</span></span>
<span data-ttu-id="d7118-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7118-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7118-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7118-128">-WhatIf</span></span>
<span data-ttu-id="d7118-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7118-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7118-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7118-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7118-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7118-131">CommonParameters</span></span>
<span data-ttu-id="d7118-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7118-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7118-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7118-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7118-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7118-134">INPUTS</span></span>

### <span data-ttu-id="d7118-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d7118-135">System.String</span></span>

### <span data-ttu-id="d7118-136">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d7118-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="d7118-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7118-137">OUTPUTS</span></span>

### <span data-ttu-id="d7118-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7118-138">System.Boolean</span></span>

## <span data-ttu-id="d7118-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7118-139">NOTES</span></span>

## <span data-ttu-id="d7118-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7118-140">RELATED LINKS</span></span>

<span data-ttu-id="d7118-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d7118-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
