---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594646"
---
# <span data-ttu-id="fd695-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="fd695-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="fd695-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd695-102">SYNOPSIS</span></span>
<span data-ttu-id="fd695-103">Taahhüt ilişkisini bir taahhüt planından diğerine taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="fd695-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd695-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd695-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd695-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd695-105">DESCRIPTION</span></span>
<span data-ttu-id="fd695-106">Taahhüt ilişkisi kaynağını üst taahhüt planından başka bir taahhüt planına taşıma.</span><span class="sxs-lookup"><span data-stu-id="fd695-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="fd695-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd695-107">EXAMPLES</span></span>

### <span data-ttu-id="fd695-108">--------------------------Örnek 1: bir taahhüt ilişkisi--------------------------taşıma</span><span class="sxs-lookup"><span data-stu-id="fd695-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="fd695-109">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="fd695-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="fd695-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd695-110">PARAMETERS</span></span>

### <span data-ttu-id="fd695-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="fd695-111">-CommitmentPlanName</span></span>
<span data-ttu-id="fd695-112">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="fd695-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fd695-113">-Destinationplanıd</span><span class="sxs-lookup"><span data-stu-id="fd695-113">-DestinationPlanId</span></span>
<span data-ttu-id="fd695-114">Hedef Azure ML taahhüt planının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fd695-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fd695-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd695-115">-Name</span></span>
<span data-ttu-id="fd695-116">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="fd695-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="fd695-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd695-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd695-118">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fd695-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="fd695-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd695-119">-Confirm</span></span>
<span data-ttu-id="fd695-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd695-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd695-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd695-121">-WhatIf</span></span>
<span data-ttu-id="fd695-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd695-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd695-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd695-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd695-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd695-124">-DefaultProfile</span></span>
<span data-ttu-id="fd695-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd695-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd695-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd695-126">CommonParameters</span></span>
<span data-ttu-id="fd695-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd695-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd695-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd695-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd695-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd695-129">INPUTS</span></span>

## <span data-ttu-id="fd695-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd695-130">OUTPUTS</span></span>

### <span data-ttu-id="fd695-131">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="fd695-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="fd695-132">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="fd695-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="fd695-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd695-133">NOTES</span></span>
<span data-ttu-id="fd695-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fd695-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fd695-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd695-135">RELATED LINKS</span></span>

