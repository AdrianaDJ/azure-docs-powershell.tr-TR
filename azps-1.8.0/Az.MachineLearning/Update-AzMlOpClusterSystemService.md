---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915839"
---
# <span data-ttu-id="1e9f4-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="1e9f4-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="1e9f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9f4-103">Operationalization kümesinin sistem hizmetlerinde bir güncelleştirme başlatır.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="1e9f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e9f4-104">SYNTAX</span></span>

### <span data-ttu-id="1e9f4-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e9f4-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9f4-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="1e9f4-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9f4-107">Startupdatewithresourceıd</span><span class="sxs-lookup"><span data-stu-id="1e9f4-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e9f4-108">DESCRIPTION</span></span>
<span data-ttu-id="1e9f4-109">Sistem Hizmetleri, operationalization kümesinden bağımsız olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="1e9f4-110">Sistem hizmetlerinde güncelleştirme başlatmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="1e9f4-111">Güncelleştirme yoksa güncelleştirme yine başlatılır ve başarıyla geri döner.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="1e9f4-112">Güncelleştirme tamamlandıktan sonra, bir kez başlatıldığında, bittiğinde ve başarılı olduysa.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="1e9f4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e9f4-113">EXAMPLES</span></span>

### <span data-ttu-id="1e9f4-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e9f4-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="1e9f4-115">Belirtilen kümede sistem hizmetleri güncelleştirmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="1e9f4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e9f4-116">PARAMETERS</span></span>

### <span data-ttu-id="1e9f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9f4-117">-DefaultProfile</span></span>
<span data-ttu-id="1e9f4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e9f4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e9f4-119">-InputObject</span></span>
<span data-ttu-id="1e9f4-120">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-120">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="1e9f4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e9f4-121">-Name</span></span>
<span data-ttu-id="1e9f4-122">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-122">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="1e9f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e9f4-124">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-124">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="1e9f4-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1e9f4-125">-ResourceId</span></span>
<span data-ttu-id="1e9f4-126">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-126">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="1e9f4-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e9f4-127">-Confirm</span></span>
<span data-ttu-id="1e9f4-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9f4-129">-WhatIf</span></span>
<span data-ttu-id="1e9f4-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9f4-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9f4-132">CommonParameters</span></span>
<span data-ttu-id="1e9f4-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9f4-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e9f4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9f4-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e9f4-135">INPUTS</span></span>

### <span data-ttu-id="1e9f4-136">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="1e9f4-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="1e9f4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9f4-137">System.String</span></span>

## <span data-ttu-id="1e9f4-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e9f4-138">OUTPUTS</span></span>

### <span data-ttu-id="1e9f4-139">Microsoft. Azure. Commands. MachineLearningCompute. model. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="1e9f4-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="1e9f4-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e9f4-140">NOTES</span></span>

## <span data-ttu-id="1e9f4-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e9f4-141">RELATED LINKS</span></span>
