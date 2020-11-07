---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: f829486dfa2ae1654678597ff79c730a49454275
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751448"
---
# <span data-ttu-id="f93a3-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f93a3-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="f93a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f93a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f93a3-103">Yeni bir taahhüt planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f93a3-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="f93a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f93a3-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f93a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f93a3-105">DESCRIPTION</span></span>
<span data-ttu-id="f93a3-106">Var olan bir kaynak grubunda bir Azure makine öğrenme taahhüdü planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f93a3-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="f93a3-107">Kaynak grubunda aynı ada sahip bir taahhüt planı varsa, çağrı bir güncelleştirme işlemi olarak çalışır ve var olan taahhüt planının üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="f93a3-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="f93a3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f93a3-108">EXAMPLES</span></span>

### <span data-ttu-id="f93a3-109">Örnek 1: yeni bir taahhüt planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f93a3-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="f93a3-110">"MyResourceGroup" grubundaki "MyCommitmentPlanName" adlı yeni bir Azure makine öğrenme taahhüt planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f93a3-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="f93a3-111">Bu örnekte, SKU Devtesti/standart kullanılır; Yani, taahhüt planı tarafından sağlanan kaynaklar, DevTest/Standard sınırlarına göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f93a3-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="f93a3-112">Bu örnekteki Skukapasitesi 1 ' dir, Yani planın maliyeti, DevTest maliyeti olarak ve planın içerdiği kaynaklar için hangi Devtestin sağladığı.</span><span class="sxs-lookup"><span data-stu-id="f93a3-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="f93a3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f93a3-113">PARAMETERS</span></span>

### <span data-ttu-id="f93a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93a3-114">-DefaultProfile</span></span>
<span data-ttu-id="f93a3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f93a3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f93a3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f93a3-116">-Force</span></span>
<span data-ttu-id="f93a3-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="f93a3-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f93a3-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="f93a3-118">-Location</span></span>
<span data-ttu-id="f93a3-119">Azure ML taahhüt planının konumu.</span><span class="sxs-lookup"><span data-stu-id="f93a3-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f93a3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f93a3-120">-Name</span></span>
<span data-ttu-id="f93a3-121">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="f93a3-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f93a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="f93a3-123">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f93a3-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f93a3-124">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="f93a3-124">-SkuCapacity</span></span>
<span data-ttu-id="f93a3-125">Azure ML taahhüt planı sağlanırken kullanılacak SKU 'nun kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="f93a3-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f93a3-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f93a3-126">-SkuName</span></span>
<span data-ttu-id="f93a3-127">Azure ML taahhüt planı sağlanırken kullanılacak SKU adı.</span><span class="sxs-lookup"><span data-stu-id="f93a3-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f93a3-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f93a3-128">-SkuTier</span></span>
<span data-ttu-id="f93a3-129">Azure ML taahhüt planı sağlanırken kullanılacak SKU 'nun katmanı.</span><span class="sxs-lookup"><span data-stu-id="f93a3-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f93a3-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="f93a3-130">-Confirm</span></span>
<span data-ttu-id="f93a3-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f93a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f93a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f93a3-132">-WhatIf</span></span>
<span data-ttu-id="f93a3-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f93a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f93a3-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f93a3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f93a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93a3-135">CommonParameters</span></span>
<span data-ttu-id="f93a3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f93a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93a3-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f93a3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93a3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f93a3-138">INPUTS</span></span>

### <span data-ttu-id="f93a3-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f93a3-139">None</span></span>

## <span data-ttu-id="f93a3-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f93a3-140">OUTPUTS</span></span>

### <span data-ttu-id="f93a3-141">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f93a3-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f93a3-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f93a3-142">NOTES</span></span>
<span data-ttu-id="f93a3-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f93a3-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f93a3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f93a3-144">RELATED LINKS</span></span>
