---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594888"
---
# <span data-ttu-id="39136-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="39136-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="39136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39136-102">SYNOPSIS</span></span>
<span data-ttu-id="39136-103">Belirtilen bir taahhüt planı için kullanım geçmişi bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="39136-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39136-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39136-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39136-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39136-105">DESCRIPTION</span></span>
<span data-ttu-id="39136-106">Belirtilen bir taahhüt planı için kullanım geçmişi bilgilerini (kullanılan kaynaklar ve bu planda kalan kaynaklar dahil) alır.</span><span class="sxs-lookup"><span data-stu-id="39136-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="39136-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39136-107">EXAMPLES</span></span>

### <span data-ttu-id="39136-108">Örnek 1: belirli bir taahhüt planı için kullanım geçmişi alma</span><span class="sxs-lookup"><span data-stu-id="39136-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="39136-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39136-109">PARAMETERS</span></span>

### <span data-ttu-id="39136-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39136-110">-DefaultProfile</span></span>
<span data-ttu-id="39136-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="39136-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39136-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="39136-112">-Name</span></span>
<span data-ttu-id="39136-113">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="39136-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="39136-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39136-114">-ResourceGroupName</span></span>
<span data-ttu-id="39136-115">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="39136-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="39136-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39136-116">CommonParameters</span></span>
<span data-ttu-id="39136-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39136-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39136-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39136-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39136-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39136-119">INPUTS</span></span>

### <span data-ttu-id="39136-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="39136-120">None</span></span>

## <span data-ttu-id="39136-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39136-121">OUTPUTS</span></span>

### <span data-ttu-id="39136-122">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. Planusage geçmişi</span><span class="sxs-lookup"><span data-stu-id="39136-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="39136-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39136-123">NOTES</span></span>
<span data-ttu-id="39136-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="39136-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="39136-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39136-125">RELATED LINKS</span></span>
