---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 042c857efde915847e8ad809e84c91ddaa103b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590193"
---
# <span data-ttu-id="ef27f-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="ef27f-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="ef27f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef27f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef27f-103">Operationalization kümesinin sistem hizmetlerinde bir güncelleştirme başlatır.</span><span class="sxs-lookup"><span data-stu-id="ef27f-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef27f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef27f-104">SYNTAX</span></span>

### <span data-ttu-id="ef27f-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef27f-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef27f-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="ef27f-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef27f-107">Startupdatewithresourceıd</span><span class="sxs-lookup"><span data-stu-id="ef27f-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef27f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef27f-108">DESCRIPTION</span></span>
<span data-ttu-id="ef27f-109">Sistem Hizmetleri, operationalization kümesinden bağımsız olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ef27f-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="ef27f-110">Sistem hizmetlerinde güncelleştirme başlatmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="ef27f-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="ef27f-111">Güncelleştirme yoksa güncelleştirme yine başlatılır ve başarıyla geri döner.</span><span class="sxs-lookup"><span data-stu-id="ef27f-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="ef27f-112">Güncelleştirme tamamlandıktan sonra, bir kez başlatıldığında, bittiğinde ve başarılı olduysa.</span><span class="sxs-lookup"><span data-stu-id="ef27f-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="ef27f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef27f-113">EXAMPLES</span></span>

### <span data-ttu-id="ef27f-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ef27f-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="ef27f-115">Belirtilen kümede sistem hizmetleri güncelleştirmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ef27f-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="ef27f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef27f-116">PARAMETERS</span></span>

### <span data-ttu-id="ef27f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-117">-DefaultProfile</span></span>
<span data-ttu-id="ef27f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef27f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef27f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef27f-119">-InputObject</span></span>
<span data-ttu-id="ef27f-120">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ef27f-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef27f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef27f-121">-Name</span></span>
<span data-ttu-id="ef27f-122">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="ef27f-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef27f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef27f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef27f-124">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef27f-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef27f-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ef27f-125">-ResourceId</span></span>
<span data-ttu-id="ef27f-126">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ef27f-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef27f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef27f-127">-Confirm</span></span>
<span data-ttu-id="ef27f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef27f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef27f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef27f-129">-WhatIf</span></span>
<span data-ttu-id="ef27f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef27f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef27f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef27f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef27f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef27f-132">CommonParameters</span></span>
<span data-ttu-id="ef27f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef27f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef27f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef27f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef27f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef27f-135">INPUTS</span></span>

### <span data-ttu-id="ef27f-136">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="ef27f-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="ef27f-137">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef27f-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ef27f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ef27f-138">System.String</span></span>

## <span data-ttu-id="ef27f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef27f-139">OUTPUTS</span></span>

### <span data-ttu-id="ef27f-140">Microsoft. Azure. Commands. MachineLearningCompute. model. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="ef27f-140">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="ef27f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef27f-141">NOTES</span></span>

## <span data-ttu-id="ef27f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef27f-142">RELATED LINKS</span></span>
