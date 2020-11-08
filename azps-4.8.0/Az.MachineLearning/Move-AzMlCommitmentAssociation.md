---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108193"
---
# <span data-ttu-id="3098d-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="3098d-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="3098d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3098d-102">SYNOPSIS</span></span>
<span data-ttu-id="3098d-103">Taahhüt ilişkisini bir taahhüt planından diğerine taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="3098d-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="3098d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3098d-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3098d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3098d-105">DESCRIPTION</span></span>
<span data-ttu-id="3098d-106">Taahhüt ilişkisi kaynağını üst taahhüt planından başka bir taahhüt planına taşıma.</span><span class="sxs-lookup"><span data-stu-id="3098d-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="3098d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3098d-107">EXAMPLES</span></span>

### <span data-ttu-id="3098d-108">Örnek 1: taahhüt ilişkisini taşıma</span><span class="sxs-lookup"><span data-stu-id="3098d-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="3098d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3098d-109">PARAMETERS</span></span>

### <span data-ttu-id="3098d-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="3098d-110">-CommitmentPlanName</span></span>
<span data-ttu-id="3098d-111">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="3098d-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3098d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3098d-112">-DefaultProfile</span></span>
<span data-ttu-id="3098d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3098d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3098d-114">-Destinationplanıd</span><span class="sxs-lookup"><span data-stu-id="3098d-114">-DestinationPlanId</span></span>
<span data-ttu-id="3098d-115">Hedef Azure ML taahhüt planının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3098d-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3098d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3098d-116">-Name</span></span>
<span data-ttu-id="3098d-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="3098d-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="3098d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3098d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3098d-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3098d-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="3098d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="3098d-120">-Confirm</span></span>
<span data-ttu-id="3098d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3098d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3098d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3098d-122">-WhatIf</span></span>
<span data-ttu-id="3098d-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3098d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3098d-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3098d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3098d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3098d-125">CommonParameters</span></span>
<span data-ttu-id="3098d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3098d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3098d-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3098d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3098d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3098d-128">INPUTS</span></span>

### <span data-ttu-id="3098d-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3098d-129">None</span></span>

## <span data-ttu-id="3098d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3098d-130">OUTPUTS</span></span>

### <span data-ttu-id="3098d-131">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3098d-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3098d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3098d-132">NOTES</span></span>
<span data-ttu-id="3098d-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3098d-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3098d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3098d-134">RELATED LINKS</span></span>
