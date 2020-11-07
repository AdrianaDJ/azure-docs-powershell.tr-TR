---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765209"
---
# <span data-ttu-id="f1f18-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f1f18-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="f1f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f18-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f18-103">Belirtilen bir taahhüt planı için kullanım geçmişi bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="f1f18-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1f18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1f18-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1f18-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1f18-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f18-106">Belirtilen bir taahhüt planı için kullanım geçmişi bilgilerini (kullanılan kaynaklar ve bu planda kalan kaynaklar dahil) alır.</span><span class="sxs-lookup"><span data-stu-id="f1f18-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="f1f18-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1f18-107">EXAMPLES</span></span>

### <span data-ttu-id="f1f18-108">--------------------------Örnek 1: belirli bir taahhüt planı için kullanım geçmişi alma--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1f18-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="f1f18-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1f18-109">PARAMETERS</span></span>

### <span data-ttu-id="f1f18-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f18-110">-DefaultProfile</span></span>
<span data-ttu-id="f1f18-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f1f18-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1f18-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1f18-112">-Name</span></span>
<span data-ttu-id="f1f18-113">Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="f1f18-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f1f18-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f18-114">-ResourceGroupName</span></span>
<span data-ttu-id="f1f18-115">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1f18-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f1f18-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f18-116">CommonParameters</span></span>
<span data-ttu-id="f1f18-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1f18-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f18-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f18-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f18-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1f18-119">INPUTS</span></span>

### <span data-ttu-id="f1f18-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f1f18-120">None</span></span>
<span data-ttu-id="f1f18-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f1f18-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1f18-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1f18-122">OUTPUTS</span></span>

### <span data-ttu-id="f1f18-123">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. model. Planusage geçmişi []</span><span class="sxs-lookup"><span data-stu-id="f1f18-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="f1f18-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1f18-124">NOTES</span></span>
<span data-ttu-id="f1f18-125">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f1f18-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f1f18-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1f18-126">RELATED LINKS</span></span>

