---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9832faaaaf1097f53aff841f8a455680b2a40a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590194"
---
# <span data-ttu-id="d851e-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="d851e-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="d851e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d851e-102">SYNOPSIS</span></span>
<span data-ttu-id="d851e-103">Bir operationalization kümesiyle ilişkilendirilmiş sistem hizmetleri için güncelleştirmeler olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d851e-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d851e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d851e-104">SYNTAX</span></span>

### <span data-ttu-id="d851e-105">Testbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="d851e-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d851e-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="d851e-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d851e-107">Testbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d851e-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d851e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d851e-108">DESCRIPTION</span></span>
<span data-ttu-id="d851e-109">Sistem Hizmetleri, güncelleştirmeleri operationalization kümesinden bağımsız olarak alır.</span><span class="sxs-lookup"><span data-stu-id="d851e-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="d851e-110">Bu cmdlet 'i kullanmak kullanıcının Invoke-AzureRmMlOpClusterSystemServicesUpdate 'i kullanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d851e-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="d851e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d851e-111">EXAMPLES</span></span>

### <span data-ttu-id="d851e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d851e-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="d851e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d851e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="d851e-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d851e-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="d851e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d851e-115">PARAMETERS</span></span>

### <span data-ttu-id="d851e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d851e-116">-DefaultProfile</span></span>
<span data-ttu-id="d851e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d851e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d851e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d851e-118">-InputObject</span></span>
<span data-ttu-id="d851e-119">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d851e-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d851e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d851e-120">-Name</span></span>
<span data-ttu-id="d851e-121">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="d851e-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d851e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d851e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d851e-123">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d851e-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d851e-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d851e-124">-ResourceId</span></span>
<span data-ttu-id="d851e-125">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d851e-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d851e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d851e-126">CommonParameters</span></span>
<span data-ttu-id="d851e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d851e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d851e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d851e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d851e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d851e-129">INPUTS</span></span>

### <span data-ttu-id="d851e-130">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d851e-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="d851e-131">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d851e-131">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d851e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d851e-132">System.String</span></span>

## <span data-ttu-id="d851e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d851e-133">OUTPUTS</span></span>

### <span data-ttu-id="d851e-134">Microsoft. Azure. Commands. machinelearningcompute. modeller. pschecksystemservicesupdatesavailablerese</span><span class="sxs-lookup"><span data-stu-id="d851e-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="d851e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d851e-135">NOTES</span></span>

## <span data-ttu-id="d851e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d851e-136">RELATED LINKS</span></span>
