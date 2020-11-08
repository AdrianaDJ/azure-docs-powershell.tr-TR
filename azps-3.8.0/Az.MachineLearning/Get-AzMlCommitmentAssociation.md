---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098266"
---
# <span data-ttu-id="c69f8-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="c69f8-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="c69f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c69f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c69f8-103">Bir veya daha fazla taahhüt ilişkisi için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="c69f8-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="c69f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c69f8-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c69f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c69f8-105">DESCRIPTION</span></span>
<span data-ttu-id="c69f8-106">Taahhüt ilişkisi bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c69f8-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="c69f8-107">Geçirilen parametrelere bağlı olarak, cmdlet belirtilen taahhüt planı için belirli bir taahhüt ilişkisi veya taahhüt ilişkisi koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="c69f8-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="c69f8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c69f8-108">EXAMPLES</span></span>

### <span data-ttu-id="c69f8-109">Örnek 1: belirli bir taahhüt ilişkisi alma</span><span class="sxs-lookup"><span data-stu-id="c69f8-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="c69f8-110">Örnek 2: belirtilen taahhüt planı için tüm taahhüt ilişkilerini alma</span><span class="sxs-lookup"><span data-stu-id="c69f8-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="c69f8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c69f8-111">PARAMETERS</span></span>

### <span data-ttu-id="c69f8-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="c69f8-112">-CommitmentPlanName</span></span>
<span data-ttu-id="c69f8-113">Bir veya daha fazla taahhüt ilişkisi olan Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="c69f8-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="c69f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69f8-114">-DefaultProfile</span></span>
<span data-ttu-id="c69f8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c69f8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c69f8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c69f8-116">-Name</span></span>
<span data-ttu-id="c69f8-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="c69f8-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="c69f8-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c69f8-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="c69f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69f8-120">CommonParameters</span></span>
<span data-ttu-id="c69f8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c69f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69f8-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69f8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69f8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c69f8-123">INPUTS</span></span>

### <span data-ttu-id="c69f8-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c69f8-124">None</span></span>

## <span data-ttu-id="c69f8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c69f8-125">OUTPUTS</span></span>

### <span data-ttu-id="c69f8-126">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c69f8-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="c69f8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c69f8-127">NOTES</span></span>
<span data-ttu-id="c69f8-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c69f8-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c69f8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c69f8-129">RELATED LINKS</span></span>