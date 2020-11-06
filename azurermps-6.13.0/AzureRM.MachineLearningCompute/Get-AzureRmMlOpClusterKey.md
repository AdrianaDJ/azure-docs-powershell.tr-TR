---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 6b5797d67b709e9c44756dad018a47eb416ed174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590198"
---
# <span data-ttu-id="a5a74-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a5a74-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="a5a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a74-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a74-103">Bir operationalization kümesiyle ilişkili erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a5a74-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5a74-104">SYNTAX</span></span>

### <span data-ttu-id="a5a74-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="a5a74-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a74-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5a74-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a74-107">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="a5a74-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a74-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5a74-108">DESCRIPTION</span></span>
<span data-ttu-id="a5a74-109">Küme özellikleri alınırken depolama hesabının, kapsayıcı kayıt defterinin ve operationalization kümesiyle ilişkili diğer hizmetlerin anahtarları döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="a5a74-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="a5a74-110">Hassas bilgiler olduğundan anahtarları almak için belirli bir çağrı yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a5a74-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="a5a74-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5a74-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a74-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5a74-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="a5a74-113">Operationalization kümesiyle ilişkili hizmetler için gizli anahtarları döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5a74-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="a5a74-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5a74-114">PARAMETERS</span></span>

### <span data-ttu-id="a5a74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a74-115">-DefaultProfile</span></span>
<span data-ttu-id="a5a74-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5a74-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5a74-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a74-117">-InputObject</span></span>
<span data-ttu-id="a5a74-118">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a5a74-118">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="a5a74-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5a74-119">-Name</span></span>
<span data-ttu-id="a5a74-120">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="a5a74-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="a5a74-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a74-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5a74-122">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a5a74-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a5a74-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5a74-123">-ResourceId</span></span>
<span data-ttu-id="a5a74-124">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="a5a74-124">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a5a74-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a74-125">CommonParameters</span></span>
<span data-ttu-id="a5a74-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5a74-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a74-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a74-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a74-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5a74-128">INPUTS</span></span>

### <span data-ttu-id="a5a74-129">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a5a74-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="a5a74-130">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5a74-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a5a74-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a74-131">System.String</span></span>

## <span data-ttu-id="a5a74-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5a74-132">OUTPUTS</span></span>

### <span data-ttu-id="a5a74-133">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="a5a74-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="a5a74-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5a74-134">NOTES</span></span>

## <span data-ttu-id="a5a74-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5a74-135">RELATED LINKS</span></span>
