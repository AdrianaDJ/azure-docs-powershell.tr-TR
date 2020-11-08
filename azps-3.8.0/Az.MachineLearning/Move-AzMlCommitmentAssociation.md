---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104241"
---
# <span data-ttu-id="e46de-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e46de-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="e46de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e46de-102">SYNOPSIS</span></span>
<span data-ttu-id="e46de-103">Taahhüt ilişkisini bir taahhüt planından diğerine taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="e46de-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="e46de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e46de-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e46de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e46de-105">DESCRIPTION</span></span>
<span data-ttu-id="e46de-106">Taahhüt ilişkisi kaynağını üst taahhüt planından başka bir taahhüt planına taşıma.</span><span class="sxs-lookup"><span data-stu-id="e46de-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="e46de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e46de-107">EXAMPLES</span></span>

### <span data-ttu-id="e46de-108">Örnek 1: taahhüt ilişkisini taşıma</span><span class="sxs-lookup"><span data-stu-id="e46de-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="e46de-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e46de-109">PARAMETERS</span></span>

### <span data-ttu-id="e46de-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e46de-110">-CommitmentPlanName</span></span>
<span data-ttu-id="e46de-111">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="e46de-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e46de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46de-112">-DefaultProfile</span></span>
<span data-ttu-id="e46de-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e46de-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e46de-114">-Destinationplanıd</span><span class="sxs-lookup"><span data-stu-id="e46de-114">-DestinationPlanId</span></span>
<span data-ttu-id="e46de-115">Hedef Azure ML taahhüt planının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e46de-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e46de-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e46de-116">-Name</span></span>
<span data-ttu-id="e46de-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="e46de-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e46de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46de-118">-ResourceGroupName</span></span>
<span data-ttu-id="e46de-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e46de-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e46de-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="e46de-120">-Confirm</span></span>
<span data-ttu-id="e46de-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e46de-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46de-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46de-122">-WhatIf</span></span>
<span data-ttu-id="e46de-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e46de-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e46de-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e46de-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46de-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46de-125">CommonParameters</span></span>
<span data-ttu-id="e46de-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e46de-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46de-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e46de-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46de-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e46de-128">INPUTS</span></span>

### <span data-ttu-id="e46de-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e46de-129">None</span></span>

## <span data-ttu-id="e46de-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e46de-130">OUTPUTS</span></span>

### <span data-ttu-id="e46de-131">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e46de-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e46de-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e46de-132">NOTES</span></span>
<span data-ttu-id="e46de-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e46de-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e46de-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e46de-134">RELATED LINKS</span></span>
