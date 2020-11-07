---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: d22632f830c40cd992f874d4f09c05b8a3fd9a5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915912"
---
# <span data-ttu-id="4e2e9-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="4e2e9-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="4e2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2e9-103">Bir veya daha fazla taahhüt ilişkisi için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="4e2e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e2e9-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e2e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="4e2e9-106">Taahhüt ilişkisi bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="4e2e9-107">Geçilen paralara bağlı olarak, cmdlet belirtilen taahhüt planı için belirli bir taahhüt ilişkisi veya taahhüt ilişkisi koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="4e2e9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e2e9-108">EXAMPLES</span></span>

### <span data-ttu-id="4e2e9-109">Örnek 1: belirli bir taahhüt ilişkisi alma</span><span class="sxs-lookup"><span data-stu-id="4e2e9-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="4e2e9-110">Örnek 2: belirtilen taahhüt planı için tüm taahhüt ilişkilerini alma</span><span class="sxs-lookup"><span data-stu-id="4e2e9-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="4e2e9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e2e9-111">PARAMETERS</span></span>

### <span data-ttu-id="4e2e9-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="4e2e9-112">-CommitmentPlanName</span></span>
<span data-ttu-id="4e2e9-113">Bir veya daha fazla taahhüt ilişkisi olan Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="4e2e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2e9-114">-DefaultProfile</span></span>
<span data-ttu-id="4e2e9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4e2e9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e2e9-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e2e9-116">-Name</span></span>
<span data-ttu-id="4e2e9-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="4e2e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e2e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="4e2e9-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="4e2e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2e9-120">CommonParameters</span></span>
<span data-ttu-id="4e2e9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e2e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2e9-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e2e9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2e9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e2e9-123">INPUTS</span></span>

### <span data-ttu-id="4e2e9-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e2e9-124">None</span></span>

## <span data-ttu-id="4e2e9-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e2e9-125">OUTPUTS</span></span>

### <span data-ttu-id="4e2e9-126">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4e2e9-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="4e2e9-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e2e9-127">NOTES</span></span>
<span data-ttu-id="4e2e9-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4e2e9-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4e2e9-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e2e9-129">RELATED LINKS</span></span>
