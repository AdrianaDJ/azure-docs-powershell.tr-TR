---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 25a77e0e34e741273618ab4c434168b796595737
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590884"
---
# <span data-ttu-id="ab453-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="ab453-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="ab453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab453-102">SYNOPSIS</span></span>
<span data-ttu-id="ab453-103">Taahhüt ilişkisini bir taahhüt planından diğerine taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="ab453-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab453-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab453-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab453-105">DESCRIPTION</span></span>
<span data-ttu-id="ab453-106">Taahhüt ilişkisi kaynağını üst taahhüt planından başka bir taahhüt planına taşıma.</span><span class="sxs-lookup"><span data-stu-id="ab453-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="ab453-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab453-107">EXAMPLES</span></span>

### <span data-ttu-id="ab453-108">Örnek 1: taahhüt ilişkisini taşıma</span><span class="sxs-lookup"><span data-stu-id="ab453-108">Example 1: Move a commitment association</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="ab453-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab453-109">PARAMETERS</span></span>

### <span data-ttu-id="ab453-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="ab453-110">-CommitmentPlanName</span></span>
<span data-ttu-id="ab453-111">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="ab453-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab453-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab453-112">-DefaultProfile</span></span>
<span data-ttu-id="ab453-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ab453-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab453-114">-Destinationplanıd</span><span class="sxs-lookup"><span data-stu-id="ab453-114">-DestinationPlanId</span></span>
<span data-ttu-id="ab453-115">Hedef Azure ML taahhüt planının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ab453-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab453-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab453-116">-Name</span></span>
<span data-ttu-id="ab453-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="ab453-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="ab453-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab453-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab453-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ab453-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="ab453-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab453-120">-Confirm</span></span>
<span data-ttu-id="ab453-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab453-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab453-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab453-122">-WhatIf</span></span>
<span data-ttu-id="ab453-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab453-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab453-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab453-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab453-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab453-125">CommonParameters</span></span>
<span data-ttu-id="ab453-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab453-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab453-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab453-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab453-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab453-128">INPUTS</span></span>

### <span data-ttu-id="ab453-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ab453-129">None</span></span>

## <span data-ttu-id="ab453-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab453-130">OUTPUTS</span></span>

### <span data-ttu-id="ab453-131">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab453-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ab453-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab453-132">NOTES</span></span>
<span data-ttu-id="ab453-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ab453-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ab453-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab453-134">RELATED LINKS</span></span>
