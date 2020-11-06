---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593088"
---
# <span data-ttu-id="95949-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="95949-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="95949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95949-102">SYNOPSIS</span></span>
<span data-ttu-id="95949-103">Bir operationalization kümesiyle ilişkili erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="95949-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95949-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95949-104">SYNTAX</span></span>

### <span data-ttu-id="95949-105">Cmdlet Giriş parametrelerinden operationalization kümesinin anahtarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="95949-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="95949-106">OperationalizationCluster örneğinin tanımını alma.</span><span class="sxs-lookup"><span data-stu-id="95949-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="95949-107">Azure kaynak kimliğinden operationalization kümesinin anahtarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="95949-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="95949-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95949-108">DESCRIPTION</span></span>
<span data-ttu-id="95949-109">Küme özellikleri alınırken depolama hesabının, kapsayıcı kayıt defterinin ve operationalization kümesiyle ilişkili diğer hizmetlerin anahtarları döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="95949-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="95949-110">Hassas bilgiler olduğundan anahtarları almak için belirli bir çağrı yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="95949-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="95949-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95949-111">EXAMPLES</span></span>

### <span data-ttu-id="95949-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95949-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="95949-113">Operationalization kümesiyle ilişkili hizmetler için gizli anahtarları döndürür.</span><span class="sxs-lookup"><span data-stu-id="95949-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="95949-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95949-114">PARAMETERS</span></span>

### <span data-ttu-id="95949-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95949-115">-InputObject</span></span>
<span data-ttu-id="95949-116">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="95949-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95949-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="95949-117">-Name</span></span>
<span data-ttu-id="95949-118">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="95949-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95949-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95949-119">-ResourceGroupName</span></span>
<span data-ttu-id="95949-120">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="95949-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95949-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="95949-121">-ResourceId</span></span>
<span data-ttu-id="95949-122">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="95949-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="95949-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95949-123">INPUTS</span></span>

### <span data-ttu-id="95949-124">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="95949-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="95949-125">System. String</span><span class="sxs-lookup"><span data-stu-id="95949-125">System.String</span></span>


## <span data-ttu-id="95949-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95949-126">OUTPUTS</span></span>

### <span data-ttu-id="95949-127">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="95949-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="95949-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95949-128">NOTES</span></span>

## <span data-ttu-id="95949-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95949-129">RELATED LINKS</span></span>

