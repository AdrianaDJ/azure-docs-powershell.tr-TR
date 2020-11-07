---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915891"
---
# <span data-ttu-id="83829-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="83829-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="83829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83829-102">SYNOPSIS</span></span>
<span data-ttu-id="83829-103">Bir operationalization kümesiyle ilişkili erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="83829-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="83829-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83829-104">SYNTAX</span></span>

### <span data-ttu-id="83829-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="83829-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83829-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="83829-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83829-107">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="83829-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83829-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="83829-108">DESCRIPTION</span></span>
<span data-ttu-id="83829-109">Küme özellikleri alınırken depolama hesabının, kapsayıcı kayıt defterinin ve operationalization kümesiyle ilişkili diğer hizmetlerin anahtarları döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="83829-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="83829-110">Hassas bilgiler olduğundan anahtarları almak için belirli bir çağrı yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="83829-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="83829-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83829-111">EXAMPLES</span></span>

### <span data-ttu-id="83829-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="83829-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="83829-113">Operationalization kümesiyle ilişkili hizmetler için gizli anahtarları döndürür.</span><span class="sxs-lookup"><span data-stu-id="83829-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="83829-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83829-114">PARAMETERS</span></span>

### <span data-ttu-id="83829-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83829-115">-DefaultProfile</span></span>
<span data-ttu-id="83829-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83829-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83829-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83829-117">-InputObject</span></span>
<span data-ttu-id="83829-118">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="83829-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83829-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="83829-119">-Name</span></span>
<span data-ttu-id="83829-120">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="83829-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83829-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83829-121">-ResourceGroupName</span></span>
<span data-ttu-id="83829-122">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="83829-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83829-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="83829-123">-ResourceId</span></span>
<span data-ttu-id="83829-124">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="83829-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83829-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83829-125">CommonParameters</span></span>
<span data-ttu-id="83829-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83829-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83829-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83829-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83829-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83829-128">INPUTS</span></span>

### <span data-ttu-id="83829-129">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="83829-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="83829-130">System. String</span><span class="sxs-lookup"><span data-stu-id="83829-130">System.String</span></span>

## <span data-ttu-id="83829-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83829-131">OUTPUTS</span></span>

### <span data-ttu-id="83829-132">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="83829-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="83829-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83829-133">NOTES</span></span>

## <span data-ttu-id="83829-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83829-134">RELATED LINKS</span></span>
