---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 4d78d6e6a1b0ae5ea9f8815d537bca1496e24bbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915899"
---
# <span data-ttu-id="b125d-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b125d-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="b125d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b125d-102">SYNOPSIS</span></span>
<span data-ttu-id="b125d-103">Belirtilen bir taahhüt planı için kullanım geçmişi bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="b125d-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="b125d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b125d-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b125d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b125d-105">DESCRIPTION</span></span>
<span data-ttu-id="b125d-106">Belirtilen bir taahhüt planı için kullanım geçmişi bilgilerini (kullanılan kaynaklar ve bu planda kalan kaynaklar dahil) alır.</span><span class="sxs-lookup"><span data-stu-id="b125d-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="b125d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b125d-107">EXAMPLES</span></span>

### <span data-ttu-id="b125d-108">Örnek 1: belirli bir taahhüt planı için kullanım geçmişi alma</span><span class="sxs-lookup"><span data-stu-id="b125d-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="b125d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b125d-109">PARAMETERS</span></span>

### <span data-ttu-id="b125d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b125d-110">-DefaultProfile</span></span>
<span data-ttu-id="b125d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b125d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b125d-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="b125d-112">-Name</span></span>
<span data-ttu-id="b125d-113">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="b125d-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b125d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b125d-114">-ResourceGroupName</span></span>
<span data-ttu-id="b125d-115">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b125d-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b125d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b125d-116">CommonParameters</span></span>
<span data-ttu-id="b125d-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b125d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b125d-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b125d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b125d-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b125d-119">INPUTS</span></span>

### <span data-ttu-id="b125d-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b125d-120">None</span></span>

## <span data-ttu-id="b125d-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b125d-121">OUTPUTS</span></span>

### <span data-ttu-id="b125d-122">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. Planusage geçmişi</span><span class="sxs-lookup"><span data-stu-id="b125d-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="b125d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b125d-123">NOTES</span></span>
<span data-ttu-id="b125d-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b125d-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b125d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b125d-125">RELATED LINKS</span></span>
