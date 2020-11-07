---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751440"
---
# <span data-ttu-id="1a14e-101">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1a14e-101">Remove-AzMlOpCluster</span></span>

## <span data-ttu-id="1a14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a14e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a14e-103">Bir operationalization kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a14e-103">Removes an operationalization cluster.</span></span>

## <span data-ttu-id="1a14e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a14e-104">SYNTAX</span></span>

### <span data-ttu-id="1a14e-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a14e-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a14e-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a14e-106">RemoveByInputObject</span></span>
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a14e-107">Removebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1a14e-107">RemoveByResourceId</span></span>
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a14e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a14e-108">DESCRIPTION</span></span>
<span data-ttu-id="1a14e-109">Bir operationalization kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a14e-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="1a14e-110">Kümeyle ilişkili bazı kaynakların tümü kaldırılmayabilir.</span><span class="sxs-lookup"><span data-stu-id="1a14e-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="1a14e-111">Örneğin, Azure Kapsayıcı Hizmeti kaldırılır, ancak ilişkili VM 'Ler çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a14e-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="1a14e-112">Tanılama bilgileri için depolama hesabı, kapsayıcı kayıt defteri ve Application Insights kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="1a14e-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="1a14e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a14e-113">EXAMPLES</span></span>

### <span data-ttu-id="1a14e-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1a14e-114">Example 1</span></span>
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="1a14e-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1a14e-115">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## <span data-ttu-id="1a14e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a14e-116">PARAMETERS</span></span>

### <span data-ttu-id="1a14e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a14e-117">-DefaultProfile</span></span>
<span data-ttu-id="1a14e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a14e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a14e-119">-Includeallresources</span><span class="sxs-lookup"><span data-stu-id="1a14e-119">-IncludeAllResources</span></span>
<span data-ttu-id="1a14e-120">Kümeyle oluşturulan tüm kaynakları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a14e-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="1a14e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a14e-121">-InputObject</span></span>
<span data-ttu-id="1a14e-122">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1a14e-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a14e-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a14e-123">-Name</span></span>
<span data-ttu-id="1a14e-124">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="1a14e-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a14e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a14e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a14e-126">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a14e-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a14e-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1a14e-127">-ResourceId</span></span>
<span data-ttu-id="1a14e-128">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1a14e-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a14e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a14e-129">-Confirm</span></span>
<span data-ttu-id="1a14e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a14e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a14e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a14e-131">-WhatIf</span></span>
<span data-ttu-id="1a14e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a14e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a14e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a14e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a14e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a14e-134">CommonParameters</span></span>
<span data-ttu-id="1a14e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a14e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a14e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a14e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a14e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a14e-137">INPUTS</span></span>

### <span data-ttu-id="1a14e-138">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="1a14e-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="1a14e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1a14e-139">System.String</span></span>

## <span data-ttu-id="1a14e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a14e-140">OUTPUTS</span></span>

### <span data-ttu-id="1a14e-141">System. void</span><span class="sxs-lookup"><span data-stu-id="1a14e-141">System.Void</span></span>

## <span data-ttu-id="1a14e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a14e-142">NOTES</span></span>

## <span data-ttu-id="1a14e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a14e-143">RELATED LINKS</span></span>
