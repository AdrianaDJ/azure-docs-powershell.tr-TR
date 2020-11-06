---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594069"
---
# <span data-ttu-id="bce6d-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="bce6d-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="bce6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce6d-102">SYNOPSIS</span></span>
<span data-ttu-id="bce6d-103">Bir veya daha fazla taahhüt ilişkisi için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="bce6d-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bce6d-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bce6d-105">DESCRIPTION</span></span>
<span data-ttu-id="bce6d-106">Taahhüt ilişkisi bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="bce6d-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="bce6d-107">Geçilen paralara bağlı olarak, cmdlet belirtilen taahhüt planı için belirli bir taahhüt ilişkisi veya taahhüt ilişkisi koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="bce6d-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="bce6d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bce6d-108">EXAMPLES</span></span>

### <span data-ttu-id="bce6d-109">--------------------------Örnek 1: belirli bir taahhüt ilişkisi alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="bce6d-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="bce6d-110">--------------------------Örnek 2: belirtilen taahhüt planı için tüm taahhüt ilişkilendirmelerini alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="bce6d-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="bce6d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bce6d-111">PARAMETERS</span></span>

### <span data-ttu-id="bce6d-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="bce6d-112">-CommitmentPlanName</span></span>
<span data-ttu-id="bce6d-113">Bir veya daha fazla taahhüt ilişkisi olan Azure ML taahhüt planının adı.</span><span class="sxs-lookup"><span data-stu-id="bce6d-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="bce6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce6d-114">-DefaultProfile</span></span>
<span data-ttu-id="bce6d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bce6d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bce6d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bce6d-116">-Name</span></span>
<span data-ttu-id="bce6d-117">Azure ML taahhüt ilişkisinin adı.</span><span class="sxs-lookup"><span data-stu-id="bce6d-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="bce6d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce6d-118">-ResourceGroupName</span></span>
<span data-ttu-id="bce6d-119">Azure ML taahhüt ilişkisinin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bce6d-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="bce6d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce6d-120">CommonParameters</span></span>
<span data-ttu-id="bce6d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bce6d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce6d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce6d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce6d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bce6d-123">INPUTS</span></span>

### <span data-ttu-id="bce6d-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bce6d-124">None</span></span>
<span data-ttu-id="bce6d-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bce6d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bce6d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bce6d-126">OUTPUTS</span></span>

### <span data-ttu-id="bce6d-127">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="bce6d-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="bce6d-128">Microsoft. Azure. Management. Machinöğrenim. Commitmentplanlar. modeller. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="bce6d-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="bce6d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bce6d-129">NOTES</span></span>
<span data-ttu-id="bce6d-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="bce6d-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bce6d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bce6d-131">RELATED LINKS</span></span>

