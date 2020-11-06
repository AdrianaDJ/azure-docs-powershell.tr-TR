---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 38228cd8f7618d3dfeec1836621d2eeffc5ecb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590883"
---
# <span data-ttu-id="5fd43-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5fd43-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="5fd43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fd43-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd43-103">Var olan bir taahhüt planı kaynağının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5fd43-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fd43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fd43-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fd43-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd43-106">Var olan bir taahhüt planı kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5fd43-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="5fd43-107">Taahhüt planı özelliklerinin çoğu sabittir ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="5fd43-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="5fd43-108">Değiştirilebilen Özellikler (taahhüt planını bir SKU 'dan diğerine veya bir SKU 'dan diğerine geçirmenize olanak tanır) ve Etiketler.</span><span class="sxs-lookup"><span data-stu-id="5fd43-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="5fd43-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fd43-109">EXAMPLES</span></span>

### <span data-ttu-id="5fd43-110">Örnek 1: taahhüt planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5fd43-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="5fd43-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fd43-111">PARAMETERS</span></span>

### <span data-ttu-id="5fd43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd43-112">-DefaultProfile</span></span>
<span data-ttu-id="5fd43-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5fd43-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fd43-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5fd43-114">-Force</span></span>
<span data-ttu-id="5fd43-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5fd43-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5fd43-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="5fd43-116">-Name</span></span>
<span data-ttu-id="5fd43-117">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="5fd43-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd43-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd43-118">-ResourceGroupName</span></span>
<span data-ttu-id="5fd43-119">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5fd43-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd43-120">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="5fd43-120">-SkuCapacity</span></span>
<span data-ttu-id="5fd43-121">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="5fd43-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd43-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5fd43-122">-SkuName</span></span>
<span data-ttu-id="5fd43-123">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU adı.</span><span class="sxs-lookup"><span data-stu-id="5fd43-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd43-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5fd43-124">-SkuTier</span></span>
<span data-ttu-id="5fd43-125">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun katmanı.</span><span class="sxs-lookup"><span data-stu-id="5fd43-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd43-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5fd43-126">-Tag</span></span>
<span data-ttu-id="5fd43-127">Taahhüt planı kaynağının etiketleri.</span><span class="sxs-lookup"><span data-stu-id="5fd43-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd43-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fd43-128">-Confirm</span></span>
<span data-ttu-id="5fd43-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fd43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd43-130">-WhatIf</span></span>
<span data-ttu-id="5fd43-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fd43-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fd43-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5fd43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd43-133">CommonParameters</span></span>
<span data-ttu-id="5fd43-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fd43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd43-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd43-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fd43-136">INPUTS</span></span>

### <span data-ttu-id="5fd43-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5fd43-137">None</span></span>

## <span data-ttu-id="5fd43-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fd43-138">OUTPUTS</span></span>

### <span data-ttu-id="5fd43-139">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5fd43-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="5fd43-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fd43-140">NOTES</span></span>
<span data-ttu-id="5fd43-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5fd43-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5fd43-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fd43-142">RELATED LINKS</span></span>
