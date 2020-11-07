---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 5404cf82308c63a5ba6fe07ef4ac01101f44c48c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764444"
---
# <span data-ttu-id="31aea-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="31aea-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="31aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31aea-102">SYNOPSIS</span></span>
<span data-ttu-id="31aea-103">Bir veya daha fazla taahhüt planı için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="31aea-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31aea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31aea-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31aea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31aea-105">DESCRIPTION</span></span>
<span data-ttu-id="31aea-106">Taahhüt planı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="31aea-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="31aea-107">Geçilen paralara bağlı olarak, cmdlet belirli bir taahhüt planını, geçerli abonelikteki belirli bir kaynak grubuna yönelik bir taahhüt planı koleksiyonu veya geçerli abonelikteki bir taahhüt planı koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="31aea-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="31aea-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31aea-108">EXAMPLES</span></span>

### <span data-ttu-id="31aea-109">--------------------------Örnek 1: belirli bir taahhüt planı alma--------------------------</span><span class="sxs-lookup"><span data-stu-id="31aea-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="31aea-110">--------------------------Örnek 2: geçerli abonelikteki tüm taahhüt planı kaynaklarını edinin--------------------------</span><span class="sxs-lookup"><span data-stu-id="31aea-110">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="31aea-111">--------------------------Örnek 3: geçerli abonelikteki ve verilen kaynak grubundaki tüm taahhüt planlarını alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="31aea-111">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="31aea-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31aea-112">PARAMETERS</span></span>

### <span data-ttu-id="31aea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31aea-113">-DefaultProfile</span></span>
<span data-ttu-id="31aea-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="31aea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31aea-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="31aea-115">-Name</span></span>
<span data-ttu-id="31aea-116">Taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="31aea-116">The name of the commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31aea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31aea-117">-ResourceGroupName</span></span>
<span data-ttu-id="31aea-118">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="31aea-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31aea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aea-119">CommonParameters</span></span>
<span data-ttu-id="31aea-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31aea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aea-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31aea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aea-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31aea-122">INPUTS</span></span>

### <span data-ttu-id="31aea-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="31aea-123">None</span></span>
<span data-ttu-id="31aea-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="31aea-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31aea-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31aea-125">OUTPUTS</span></span>

### <span data-ttu-id="31aea-126">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="31aea-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="31aea-127">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="31aea-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="31aea-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31aea-128">NOTES</span></span>
<span data-ttu-id="31aea-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="31aea-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="31aea-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31aea-130">RELATED LINKS</span></span>

