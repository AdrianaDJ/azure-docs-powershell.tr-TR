---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: e7c296c74aad7e733659930aea9487cf2a73aef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763108"
---
# <span data-ttu-id="962dd-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="962dd-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="962dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="962dd-102">SYNOPSIS</span></span>
<span data-ttu-id="962dd-103">Var olan bir taahhüt planı kaynağının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="962dd-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="962dd-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tags <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="962dd-105">DESCRIPTION</span></span>
<span data-ttu-id="962dd-106">Var olan bir taahhüt planı kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="962dd-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="962dd-107">Taahhüt planı özelliklerinin çoğu sabittir ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="962dd-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="962dd-108">Değiştirilebilen Özellikler (taahhüt planını bir SKU 'dan diğerine veya bir SKU 'dan diğerine geçirmenize olanak tanır) ve Etiketler.</span><span class="sxs-lookup"><span data-stu-id="962dd-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="962dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="962dd-109">EXAMPLES</span></span>

### <span data-ttu-id="962dd-110">--------------------------Örnek 1: bir taahhüt planı--------------------------</span><span class="sxs-lookup"><span data-stu-id="962dd-110">--------------------------  Example 1: Update a commitment plan  --------------------------</span></span>
<span data-ttu-id="962dd-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="962dd-111">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="962dd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="962dd-112">PARAMETERS</span></span>

### <span data-ttu-id="962dd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="962dd-113">-Force</span></span>
<span data-ttu-id="962dd-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="962dd-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="962dd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="962dd-115">-Name</span></span>
<span data-ttu-id="962dd-116">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="962dd-116">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="962dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="962dd-118">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="962dd-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="962dd-119">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="962dd-119">-SkuCapacity</span></span>
<span data-ttu-id="962dd-120">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="962dd-120">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="962dd-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="962dd-121">-SkuName</span></span>
<span data-ttu-id="962dd-122">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU adı.</span><span class="sxs-lookup"><span data-stu-id="962dd-122">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="962dd-123">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="962dd-123">-SkuTier</span></span>
<span data-ttu-id="962dd-124">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun katmanı.</span><span class="sxs-lookup"><span data-stu-id="962dd-124">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="962dd-125">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="962dd-125">-Tags</span></span>
<span data-ttu-id="962dd-126">Taahhüt planı kaynağının etiketleri.</span><span class="sxs-lookup"><span data-stu-id="962dd-126">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="962dd-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="962dd-127">-Confirm</span></span>
<span data-ttu-id="962dd-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="962dd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962dd-129">-WhatIf</span></span>
<span data-ttu-id="962dd-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="962dd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="962dd-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="962dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962dd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962dd-132">-DefaultProfile</span></span>
<span data-ttu-id="962dd-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="962dd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962dd-134">CommonParameters</span></span>
<span data-ttu-id="962dd-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="962dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962dd-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962dd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962dd-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="962dd-137">INPUTS</span></span>

## <span data-ttu-id="962dd-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="962dd-138">OUTPUTS</span></span>

### <span data-ttu-id="962dd-139">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="962dd-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="962dd-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="962dd-140">NOTES</span></span>
<span data-ttu-id="962dd-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="962dd-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="962dd-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="962dd-142">RELATED LINKS</span></span>
