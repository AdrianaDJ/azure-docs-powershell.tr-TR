---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267149"
---
# <span data-ttu-id="24ce6-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="24ce6-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="24ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="24ce6-103">Bir veya daha fazla taahhüt planı için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="24ce6-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="24ce6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24ce6-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ce6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="24ce6-106">Taahhüt planı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="24ce6-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="24ce6-107">Geçirilen parametrelere bağlı olarak, cmdlet belirli bir taahhüt planını, geçerli abonelikteki belirli bir kaynak grubuna yönelik bir taahhüt planı koleksiyonu veya geçerli abonelikteki bir taahhüt planı koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="24ce6-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="24ce6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24ce6-108">EXAMPLES</span></span>

### <span data-ttu-id="24ce6-109">Örnek 1: belirli bir taahhüt planı alma</span><span class="sxs-lookup"><span data-stu-id="24ce6-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="24ce6-110">Örnek 2: geçerli abonelikteki tüm taahhüt planı kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="24ce6-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="24ce6-111">Örnek 3: geçerli abonelikteki ve verilen kaynak grubundaki tüm taahhüt planlarını alma</span><span class="sxs-lookup"><span data-stu-id="24ce6-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="24ce6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24ce6-112">PARAMETERS</span></span>

### <span data-ttu-id="24ce6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ce6-113">-DefaultProfile</span></span>
<span data-ttu-id="24ce6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24ce6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24ce6-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="24ce6-115">-Name</span></span>
<span data-ttu-id="24ce6-116">Taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="24ce6-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="24ce6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ce6-117">-ResourceGroupName</span></span>
<span data-ttu-id="24ce6-118">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="24ce6-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="24ce6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ce6-119">CommonParameters</span></span>
<span data-ttu-id="24ce6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24ce6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ce6-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ce6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ce6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24ce6-122">INPUTS</span></span>

### <span data-ttu-id="24ce6-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="24ce6-123">None</span></span>

## <span data-ttu-id="24ce6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24ce6-124">OUTPUTS</span></span>

### <span data-ttu-id="24ce6-125">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="24ce6-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="24ce6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24ce6-126">NOTES</span></span>
<span data-ttu-id="24ce6-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="24ce6-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="24ce6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24ce6-128">RELATED LINKS</span></span>
