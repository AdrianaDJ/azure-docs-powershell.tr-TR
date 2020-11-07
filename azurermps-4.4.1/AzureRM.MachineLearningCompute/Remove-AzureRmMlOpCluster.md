---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763107"
---
# <span data-ttu-id="32b7b-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="32b7b-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="32b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="32b7b-103">Bir operationalization kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32b7b-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32b7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32b7b-104">SYNTAX</span></span>

### <span data-ttu-id="32b7b-105">Cmdlet Giriş parametrelerinden bir operationalization kümesi kaldırma.</span><span class="sxs-lookup"><span data-stu-id="32b7b-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="32b7b-106">Bir OperationalizationCluster örneği tanımından bir operationalization kümesi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="32b7b-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="32b7b-107">Bir Azure kaynak kimliğinden bir operationalization kümesi kaldırma.</span><span class="sxs-lookup"><span data-stu-id="32b7b-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="32b7b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="32b7b-108">DESCRIPTION</span></span>
<span data-ttu-id="32b7b-109">Bir operationalization kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="32b7b-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="32b7b-110">Kümeyle ilişkili bazı kaynakların tümü kaldırılmayabilir.</span><span class="sxs-lookup"><span data-stu-id="32b7b-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="32b7b-111">Örneğin, Azure Kapsayıcı Hizmeti kaldırılır, ancak ilişkili VM 'Ler çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32b7b-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="32b7b-112">Tanılama bilgileri için depolama hesabı, kapsayıcı kayıt defteri ve Application Insights kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="32b7b-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="32b7b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32b7b-113">EXAMPLES</span></span>

### <span data-ttu-id="32b7b-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="32b7b-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="32b7b-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="32b7b-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="32b7b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32b7b-116">PARAMETERS</span></span>

### <span data-ttu-id="32b7b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32b7b-117">-InputObject</span></span>
<span data-ttu-id="32b7b-118">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="32b7b-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32b7b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="32b7b-119">-Confirm</span></span>
<span data-ttu-id="32b7b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32b7b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="32b7b-121">-Name</span></span>
<span data-ttu-id="32b7b-122">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="32b7b-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="32b7b-124">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="32b7b-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7b-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="32b7b-125">-ResourceId</span></span>
<span data-ttu-id="32b7b-126">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="32b7b-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32b7b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b7b-127">-WhatIf</span></span>
<span data-ttu-id="32b7b-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32b7b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b7b-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32b7b-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="32b7b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32b7b-130">INPUTS</span></span>

### <span data-ttu-id="32b7b-131">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="32b7b-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="32b7b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="32b7b-132">System.String</span></span>


## <span data-ttu-id="32b7b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32b7b-133">OUTPUTS</span></span>

### <span data-ttu-id="32b7b-134">System. void</span><span class="sxs-lookup"><span data-stu-id="32b7b-134">System.Void</span></span>


## <span data-ttu-id="32b7b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32b7b-135">NOTES</span></span>

## <span data-ttu-id="32b7b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32b7b-136">RELATED LINKS</span></span>

