---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592205"
---
# <span data-ttu-id="044b2-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="044b2-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="044b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044b2-102">SYNOPSIS</span></span>
<span data-ttu-id="044b2-103">Bir veya daha fazla taahhüt ilişkisi için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="044b2-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="044b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="044b2-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="044b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="044b2-105">DESCRIPTION</span></span>
<span data-ttu-id="044b2-106">Taahhüt ilişkisi bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="044b2-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="044b2-107">Geçilen paralara bağlı olarak, cmdlet belirtilen taahhüt planı için belirli bir taahhüt ilişkisi veya taahhüt ilişkisi koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="044b2-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="044b2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="044b2-108">EXAMPLES</span></span>

### <span data-ttu-id="044b2-109">--------------------------Örnek 1: belirli bir taahhüt ilişkisi alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="044b2-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="044b2-110">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="044b2-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="044b2-111">--------------------------Örnek 2: belirtilen taahhüt planı için tüm taahhüt ilişkilendirmelerini alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="044b2-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="044b2-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="044b2-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="044b2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="044b2-113">PARAMETERS</span></span>

### <span data-ttu-id="044b2-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="044b2-114">-CommitmentPlanName</span></span>
<span data-ttu-id="044b2-115">Bir veya daha fazla taahhüt ilişkisi olan Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="044b2-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="044b2-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="044b2-116">-Name</span></span>
<span data-ttu-id="044b2-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="044b2-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="044b2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044b2-118">-ResourceGroupName</span></span>
<span data-ttu-id="044b2-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="044b2-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="044b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044b2-120">-DefaultProfile</span></span>
<span data-ttu-id="044b2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="044b2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="044b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044b2-122">CommonParameters</span></span>
<span data-ttu-id="044b2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="044b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044b2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044b2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="044b2-125">INPUTS</span></span>

## <span data-ttu-id="044b2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="044b2-126">OUTPUTS</span></span>

### <span data-ttu-id="044b2-127">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="044b2-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="044b2-128">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="044b2-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="044b2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="044b2-129">NOTES</span></span>
<span data-ttu-id="044b2-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="044b2-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="044b2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="044b2-131">RELATED LINKS</span></span>

