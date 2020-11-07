---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765208"
---
# <span data-ttu-id="8f5e4-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8f5e4-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="8f5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5e4-103">Bir operationalization kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f5e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f5e4-104">SYNTAX</span></span>

### <span data-ttu-id="8f5e4-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="8f5e4-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f5e4-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f5e4-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f5e4-107">Removebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8f5e4-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f5e4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f5e4-108">DESCRIPTION</span></span>
<span data-ttu-id="8f5e4-109">Bir operationalization kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="8f5e4-110">Kümeyle ilişkili bazı kaynakların tümü kaldırılmayabilir.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="8f5e4-111">Örneğin, Azure Kapsayıcı Hizmeti kaldırılır, ancak ilişkili VM 'Ler çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="8f5e4-112">Tanılama bilgileri için depolama hesabı, kapsayıcı kayıt defteri ve Application Insights kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="8f5e4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f5e4-113">EXAMPLES</span></span>

### <span data-ttu-id="8f5e4-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f5e4-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="8f5e4-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8f5e4-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="8f5e4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f5e4-116">PARAMETERS</span></span>

### <span data-ttu-id="8f5e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5e4-117">-DefaultProfile</span></span>
<span data-ttu-id="8f5e4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f5e4-119">-Includeallresources</span><span class="sxs-lookup"><span data-stu-id="8f5e4-119">-IncludeAllResources</span></span>
<span data-ttu-id="8f5e4-120">Kümeyle oluşturulan tüm kaynakları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5e4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f5e4-121">-InputObject</span></span>
<span data-ttu-id="8f5e4-122">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f5e4-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f5e4-123">-Name</span></span>
<span data-ttu-id="8f5e4-124">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f5e4-126">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5e4-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f5e4-127">-ResourceId</span></span>
<span data-ttu-id="8f5e4-128">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f5e4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f5e4-129">-Confirm</span></span>
<span data-ttu-id="8f5e4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5e4-131">-WhatIf</span></span>
<span data-ttu-id="8f5e4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5e4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5e4-134">CommonParameters</span></span>
<span data-ttu-id="8f5e4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f5e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5e4-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5e4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f5e4-137">INPUTS</span></span>

### <span data-ttu-id="8f5e4-138">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="8f5e4-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="8f5e4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8f5e4-139">System.String</span></span>

## <span data-ttu-id="8f5e4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f5e4-140">OUTPUTS</span></span>

### <span data-ttu-id="8f5e4-141">System. void</span><span class="sxs-lookup"><span data-stu-id="8f5e4-141">System.Void</span></span>

## <span data-ttu-id="8f5e4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f5e4-142">NOTES</span></span>

## <span data-ttu-id="8f5e4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f5e4-143">RELATED LINKS</span></span>

