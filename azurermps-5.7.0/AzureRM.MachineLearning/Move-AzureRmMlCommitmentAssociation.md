---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594948"
---
# <span data-ttu-id="fa3fa-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="fa3fa-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="fa3fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3fa-103">Taahhüt ilişkisini bir taahhüt planından diğerine taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa3fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa3fa-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa3fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa3fa-105">DESCRIPTION</span></span>
<span data-ttu-id="fa3fa-106">Taahhüt ilişkisi kaynağını üst taahhüt planından başka bir taahhüt planına taşıma.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="fa3fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa3fa-107">EXAMPLES</span></span>

### <span data-ttu-id="fa3fa-108">--------------------------Örnek 1: bir taahhüt ilişkisi--------------------------taşıma</span><span class="sxs-lookup"><span data-stu-id="fa3fa-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="fa3fa-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa3fa-109">PARAMETERS</span></span>

### <span data-ttu-id="fa3fa-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="fa3fa-110">-CommitmentPlanName</span></span>
<span data-ttu-id="fa3fa-111">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fa3fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3fa-112">-DefaultProfile</span></span>
<span data-ttu-id="fa3fa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa3fa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa3fa-114">-Destinationplanıd</span><span class="sxs-lookup"><span data-stu-id="fa3fa-114">-DestinationPlanId</span></span>
<span data-ttu-id="fa3fa-115">Hedef Azure ML taahhüt planının Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fa3fa-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa3fa-116">-Name</span></span>
<span data-ttu-id="fa3fa-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="fa3fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa3fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="fa3fa-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="fa3fa-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa3fa-120">-Confirm</span></span>
<span data-ttu-id="fa3fa-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa3fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa3fa-122">-WhatIf</span></span>
<span data-ttu-id="fa3fa-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa3fa-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa3fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3fa-125">CommonParameters</span></span>
<span data-ttu-id="fa3fa-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3fa-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa3fa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3fa-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa3fa-128">INPUTS</span></span>

### <span data-ttu-id="fa3fa-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fa3fa-129">None</span></span>
<span data-ttu-id="fa3fa-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fa3fa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa3fa-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa3fa-131">OUTPUTS</span></span>

### <span data-ttu-id="fa3fa-132">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="fa3fa-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="fa3fa-133">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="fa3fa-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="fa3fa-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa3fa-134">NOTES</span></span>
<span data-ttu-id="fa3fa-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fa3fa-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fa3fa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa3fa-136">RELATED LINKS</span></span>

