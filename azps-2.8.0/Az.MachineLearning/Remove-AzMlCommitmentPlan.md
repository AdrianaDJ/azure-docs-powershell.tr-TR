---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 1c022d8ae97ac9f1e51bbabaff15a9dec61f5d87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751444"
---
# <span data-ttu-id="a391a-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a391a-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a391a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a391a-102">SYNOPSIS</span></span>
<span data-ttu-id="a391a-103">Taahhüt planını siler.</span><span class="sxs-lookup"><span data-stu-id="a391a-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="a391a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a391a-104">SYNTAX</span></span>

### <span data-ttu-id="a391a-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="a391a-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a391a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a391a-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a391a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a391a-107">DESCRIPTION</span></span>
<span data-ttu-id="a391a-108">Bir Azure makine öğrenme taahhüdü planı siler.</span><span class="sxs-lookup"><span data-stu-id="a391a-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="a391a-109">Taahhüt ilişkisi olan taahhüt planlarının silinemediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a391a-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="a391a-110">Taahhüt ilişkilendirmeleri yalnızca hedef kaynakları tarafından silinebilir.</span><span class="sxs-lookup"><span data-stu-id="a391a-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="a391a-111">Örneğin, bir Azure Machine Learning Web hizmetini silerseniz, Web hizmetini bir taahhüt planıyla ilişkilendiren taahhüt ilişkisi de silinir.</span><span class="sxs-lookup"><span data-stu-id="a391a-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="a391a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a391a-112">EXAMPLES</span></span>

### <span data-ttu-id="a391a-113">Örnek 1: taahhüt planını silme</span><span class="sxs-lookup"><span data-stu-id="a391a-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="a391a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a391a-114">PARAMETERS</span></span>

### <span data-ttu-id="a391a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a391a-115">-DefaultProfile</span></span>
<span data-ttu-id="a391a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a391a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a391a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a391a-117">-Force</span></span>
<span data-ttu-id="a391a-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="a391a-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a391a-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a391a-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="a391a-120">Makine Learning Web hizmeti nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a391a-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a391a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a391a-121">-Name</span></span>
<span data-ttu-id="a391a-122">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="a391a-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a391a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a391a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a391a-124">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a391a-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a391a-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a391a-125">-Confirm</span></span>
<span data-ttu-id="a391a-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a391a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a391a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a391a-127">-WhatIf</span></span>
<span data-ttu-id="a391a-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a391a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a391a-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a391a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a391a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a391a-130">CommonParameters</span></span>
<span data-ttu-id="a391a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a391a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a391a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a391a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a391a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a391a-133">INPUTS</span></span>

### <span data-ttu-id="a391a-134">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a391a-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a391a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a391a-135">OUTPUTS</span></span>

### <span data-ttu-id="a391a-136">System. void</span><span class="sxs-lookup"><span data-stu-id="a391a-136">System.Void</span></span>

## <span data-ttu-id="a391a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a391a-137">NOTES</span></span>
<span data-ttu-id="a391a-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a391a-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a391a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a391a-139">RELATED LINKS</span></span>
