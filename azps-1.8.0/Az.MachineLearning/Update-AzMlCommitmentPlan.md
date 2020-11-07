---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: c1aa160d7a0773569255f425f3993de0b47d552a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915844"
---
# <span data-ttu-id="eb883-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="eb883-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="eb883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb883-102">SYNOPSIS</span></span>
<span data-ttu-id="eb883-103">Var olan bir taahhüt planı kaynağının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eb883-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="eb883-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb883-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb883-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb883-105">DESCRIPTION</span></span>
<span data-ttu-id="eb883-106">Var olan bir taahhüt planı kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eb883-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="eb883-107">Taahhüt planı özelliklerinin çoğu sabittir ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="eb883-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="eb883-108">Değiştirilebilen Özellikler (taahhüt planını bir SKU 'dan diğerine veya bir SKU 'dan diğerine geçirmenize olanak tanır) ve Etiketler.</span><span class="sxs-lookup"><span data-stu-id="eb883-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="eb883-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb883-109">EXAMPLES</span></span>

### <span data-ttu-id="eb883-110">Örnek 1: taahhüt planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="eb883-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="eb883-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb883-111">PARAMETERS</span></span>

### <span data-ttu-id="eb883-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb883-112">-DefaultProfile</span></span>
<span data-ttu-id="eb883-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eb883-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb883-114">-Force</span><span class="sxs-lookup"><span data-stu-id="eb883-114">-Force</span></span>
<span data-ttu-id="eb883-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="eb883-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb883-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb883-116">-Name</span></span>
<span data-ttu-id="eb883-117">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="eb883-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eb883-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb883-118">-ResourceGroupName</span></span>
<span data-ttu-id="eb883-119">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="eb883-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eb883-120">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="eb883-120">-SkuCapacity</span></span>
<span data-ttu-id="eb883-121">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="eb883-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eb883-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="eb883-122">-SkuName</span></span>
<span data-ttu-id="eb883-123">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU adı.</span><span class="sxs-lookup"><span data-stu-id="eb883-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eb883-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="eb883-124">-SkuTier</span></span>
<span data-ttu-id="eb883-125">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun katmanı.</span><span class="sxs-lookup"><span data-stu-id="eb883-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="eb883-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="eb883-126">-Tag</span></span>
<span data-ttu-id="eb883-127">Taahhüt planı kaynağının etiketleri.</span><span class="sxs-lookup"><span data-stu-id="eb883-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="eb883-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb883-128">-Confirm</span></span>
<span data-ttu-id="eb883-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb883-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb883-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb883-130">-WhatIf</span></span>
<span data-ttu-id="eb883-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb883-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb883-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb883-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb883-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb883-133">CommonParameters</span></span>
<span data-ttu-id="eb883-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb883-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb883-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb883-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb883-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb883-136">INPUTS</span></span>

### <span data-ttu-id="eb883-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eb883-137">None</span></span>

## <span data-ttu-id="eb883-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb883-138">OUTPUTS</span></span>

### <span data-ttu-id="eb883-139">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="eb883-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="eb883-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb883-140">NOTES</span></span>
<span data-ttu-id="eb883-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="eb883-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="eb883-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb883-142">RELATED LINKS</span></span>