---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: cdf8c04a3d3b3b9fc50e571642bc14352d976b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592472"
---
# <span data-ttu-id="09fd1-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="09fd1-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="09fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="09fd1-103">Bir operationalization kümesiyle ilişkili erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="09fd1-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09fd1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09fd1-104">SYNTAX</span></span>

### <span data-ttu-id="09fd1-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="09fd1-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09fd1-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="09fd1-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09fd1-107">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="09fd1-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09fd1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="09fd1-108">DESCRIPTION</span></span>
<span data-ttu-id="09fd1-109">Küme özellikleri alınırken depolama hesabının, kapsayıcı kayıt defterinin ve operationalization kümesiyle ilişkili diğer hizmetlerin anahtarları döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="09fd1-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="09fd1-110">Hassas bilgiler olduğundan anahtarları almak için belirli bir çağrı yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="09fd1-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="09fd1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09fd1-111">EXAMPLES</span></span>

### <span data-ttu-id="09fd1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="09fd1-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="09fd1-113">Operationalization kümesiyle ilişkili hizmetler için gizli anahtarları döndürür.</span><span class="sxs-lookup"><span data-stu-id="09fd1-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="09fd1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09fd1-114">PARAMETERS</span></span>

### <span data-ttu-id="09fd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fd1-115">-DefaultProfile</span></span>
<span data-ttu-id="09fd1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09fd1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09fd1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09fd1-117">-InputObject</span></span>
<span data-ttu-id="09fd1-118">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="09fd1-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09fd1-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="09fd1-119">-Name</span></span>
<span data-ttu-id="09fd1-120">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="09fd1-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="09fd1-122">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="09fd1-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fd1-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="09fd1-123">-ResourceId</span></span>
<span data-ttu-id="09fd1-124">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="09fd1-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09fd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fd1-125">CommonParameters</span></span>
<span data-ttu-id="09fd1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09fd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fd1-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fd1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fd1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09fd1-128">INPUTS</span></span>

### <span data-ttu-id="09fd1-129">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="09fd1-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="09fd1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09fd1-130">System.String</span></span>

## <span data-ttu-id="09fd1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09fd1-131">OUTPUTS</span></span>

### <span data-ttu-id="09fd1-132">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="09fd1-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="09fd1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09fd1-133">NOTES</span></span>

## <span data-ttu-id="09fd1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09fd1-134">RELATED LINKS</span></span>

