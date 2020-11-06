---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592204"
---
# <span data-ttu-id="b665e-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b665e-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="b665e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b665e-102">SYNOPSIS</span></span>
<span data-ttu-id="b665e-103">Bir veya daha fazla taahhüt planı için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="b665e-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b665e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b665e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b665e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b665e-105">DESCRIPTION</span></span>
<span data-ttu-id="b665e-106">Taahhüt planı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b665e-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="b665e-107">Geçilen paralara bağlı olarak, cmdlet belirli bir taahhüt planını, geçerli abonelikteki belirli bir kaynak grubuna yönelik bir taahhüt planı koleksiyonu veya geçerli abonelikteki bir taahhüt planı koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="b665e-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="b665e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b665e-108">EXAMPLES</span></span>

### <span data-ttu-id="b665e-109">--------------------------Örnek 1: belirli bir taahhüt planı alma--------------------------</span><span class="sxs-lookup"><span data-stu-id="b665e-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="b665e-110">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b665e-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="b665e-111">--------------------------Örnek 2: geçerli abonelikteki tüm taahhüt planı kaynaklarını edinin--------------------------</span><span class="sxs-lookup"><span data-stu-id="b665e-111">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
<span data-ttu-id="b665e-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b665e-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="b665e-113">--------------------------Örnek 3: geçerli abonelikteki ve verilen kaynak grubundaki tüm taahhüt planlarını alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="b665e-113">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="b665e-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b665e-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="b665e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b665e-115">PARAMETERS</span></span>

### <span data-ttu-id="b665e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b665e-116">-Name</span></span>
<span data-ttu-id="b665e-117">Taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="b665e-117">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="b665e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b665e-118">-ResourceGroupName</span></span>
<span data-ttu-id="b665e-119">Azure ML için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b665e-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b665e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b665e-120">-DefaultProfile</span></span>
<span data-ttu-id="b665e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b665e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b665e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b665e-122">CommonParameters</span></span>
<span data-ttu-id="b665e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b665e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b665e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b665e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b665e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b665e-125">INPUTS</span></span>

## <span data-ttu-id="b665e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b665e-126">OUTPUTS</span></span>

### <span data-ttu-id="b665e-127">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b665e-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="b665e-128">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="b665e-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="b665e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b665e-129">NOTES</span></span>
<span data-ttu-id="b665e-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b665e-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b665e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b665e-131">RELATED LINKS</span></span>

