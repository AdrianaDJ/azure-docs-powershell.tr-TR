---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763360"
---
# <span data-ttu-id="e3efd-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="e3efd-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="e3efd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3efd-102">SYNOPSIS</span></span>
<span data-ttu-id="e3efd-103">Bir operationalization kümesiyle ilişkilendirilmiş sistem hizmetleri için güncelleştirmeler olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="e3efd-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3efd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3efd-104">SYNTAX</span></span>

### <span data-ttu-id="e3efd-105">Cmdlet Giriş parametrelerinden güncelleştirme kullanılabilirliği sınaması.</span><span class="sxs-lookup"><span data-stu-id="e3efd-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="e3efd-106">Bir OperationalizationCluster örneği tanımından güncelleştirme kullanılabilirliği sınaması.</span><span class="sxs-lookup"><span data-stu-id="e3efd-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="e3efd-107">Bir Azure kaynak kimliğinden güncelleştirme kullanılabilirliği sınaması.</span><span class="sxs-lookup"><span data-stu-id="e3efd-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="e3efd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3efd-108">DESCRIPTION</span></span>
<span data-ttu-id="e3efd-109">Sistem Hizmetleri, güncelleştirmeleri operationalization kümesinden bağımsız olarak alır.</span><span class="sxs-lookup"><span data-stu-id="e3efd-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="e3efd-110">Bu cmdlet 'i kullanmak kullanıcının Invoke-AzureRmMlOpClusterSystemServicesUpdate 'i kullanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e3efd-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="e3efd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3efd-111">EXAMPLES</span></span>

### <span data-ttu-id="e3efd-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3efd-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="e3efd-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e3efd-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="e3efd-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e3efd-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="e3efd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3efd-115">PARAMETERS</span></span>

### <span data-ttu-id="e3efd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3efd-116">-InputObject</span></span>
<span data-ttu-id="e3efd-117">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e3efd-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3efd-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3efd-118">-Name</span></span>
<span data-ttu-id="e3efd-119">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="e3efd-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3efd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3efd-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3efd-121">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3efd-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3efd-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e3efd-122">-ResourceId</span></span>
<span data-ttu-id="e3efd-123">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="e3efd-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e3efd-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3efd-124">INPUTS</span></span>

### <span data-ttu-id="e3efd-125">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="e3efd-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="e3efd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3efd-126">System.String</span></span>


## <span data-ttu-id="e3efd-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3efd-127">OUTPUTS</span></span>

### <span data-ttu-id="e3efd-128">Microsoft. Azure. Commands. machinelearningcompute. modeller. pschecksystemservicesupdatesavailablerese</span><span class="sxs-lookup"><span data-stu-id="e3efd-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="e3efd-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3efd-129">NOTES</span></span>

## <span data-ttu-id="e3efd-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3efd-130">RELATED LINKS</span></span>

