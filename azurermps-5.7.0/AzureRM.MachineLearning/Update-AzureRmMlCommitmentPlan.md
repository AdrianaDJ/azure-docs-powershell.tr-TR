---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 0cda9ee6f6a93a43234835104130ea39782f36d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590451"
---
# <span data-ttu-id="ce591-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ce591-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ce591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce591-102">SYNOPSIS</span></span>
<span data-ttu-id="ce591-103">Var olan bir taahhüt planı kaynağının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ce591-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce591-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce591-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce591-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce591-105">DESCRIPTION</span></span>
<span data-ttu-id="ce591-106">Var olan bir taahhüt planı kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ce591-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="ce591-107">Taahhüt planı özelliklerinin çoğu sabittir ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="ce591-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="ce591-108">Değiştirilebilen Özellikler (taahhüt planını bir SKU 'dan diğerine veya bir SKU 'dan diğerine geçirmenize olanak tanır) ve Etiketler.</span><span class="sxs-lookup"><span data-stu-id="ce591-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="ce591-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce591-109">EXAMPLES</span></span>

### <span data-ttu-id="ce591-110">Örnek 1: taahhüt planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ce591-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="ce591-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce591-111">PARAMETERS</span></span>

### <span data-ttu-id="ce591-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce591-112">-DefaultProfile</span></span>
<span data-ttu-id="ce591-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ce591-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce591-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ce591-114">-Force</span></span>
<span data-ttu-id="ce591-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="ce591-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ce591-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce591-116">-Name</span></span>
<span data-ttu-id="ce591-117">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="ce591-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce591-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce591-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce591-119">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ce591-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce591-120">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="ce591-120">-SkuCapacity</span></span>
<span data-ttu-id="ce591-121">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="ce591-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce591-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ce591-122">-SkuName</span></span>
<span data-ttu-id="ce591-123">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU adı.</span><span class="sxs-lookup"><span data-stu-id="ce591-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce591-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ce591-124">-SkuTier</span></span>
<span data-ttu-id="ce591-125">Azure ML taahhüt planı güncelleştirilirken kullanılacak SKU 'nun katmanı.</span><span class="sxs-lookup"><span data-stu-id="ce591-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce591-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ce591-126">-Tag</span></span>
<span data-ttu-id="ce591-127">Taahhüt planı kaynağının etiketleri.</span><span class="sxs-lookup"><span data-stu-id="ce591-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce591-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce591-128">-Confirm</span></span>
<span data-ttu-id="ce591-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce591-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce591-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce591-130">-WhatIf</span></span>
<span data-ttu-id="ce591-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce591-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce591-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce591-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce591-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce591-133">CommonParameters</span></span>
<span data-ttu-id="ce591-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce591-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce591-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce591-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce591-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce591-136">INPUTS</span></span>

### <span data-ttu-id="ce591-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ce591-137">None</span></span>
<span data-ttu-id="ce591-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ce591-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce591-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce591-139">OUTPUTS</span></span>

### <span data-ttu-id="ce591-140">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ce591-140">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ce591-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce591-141">NOTES</span></span>
<span data-ttu-id="ce591-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ce591-142">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ce591-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce591-143">RELATED LINKS</span></span>
