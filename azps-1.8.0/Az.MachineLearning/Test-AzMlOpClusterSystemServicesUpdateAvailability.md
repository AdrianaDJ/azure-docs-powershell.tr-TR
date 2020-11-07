---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915847"
---
# <span data-ttu-id="9ca4a-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="9ca4a-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="9ca4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca4a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca4a-103">Bir operationalization kümesiyle ilişkilendirilmiş sistem hizmetleri için güncelleştirmeler olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="9ca4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ca4a-104">SYNTAX</span></span>

### <span data-ttu-id="9ca4a-105">Testbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="9ca4a-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca4a-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ca4a-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca4a-107">Testbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9ca4a-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ca4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ca4a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca4a-109">Sistem Hizmetleri, güncelleştirmeleri operationalization kümesinden bağımsız olarak alır.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="9ca4a-110">Bu cmdlet 'i kullanmak, kullanıcının Invoke-AzMlOpClusterSystemServicesUpdate 'i kullanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="9ca4a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ca4a-111">EXAMPLES</span></span>

### <span data-ttu-id="9ca4a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ca4a-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="9ca4a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9ca4a-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="9ca4a-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9ca4a-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="9ca4a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ca4a-115">PARAMETERS</span></span>

### <span data-ttu-id="9ca4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca4a-116">-DefaultProfile</span></span>
<span data-ttu-id="9ca4a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ca4a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca4a-118">-InputObject</span></span>
<span data-ttu-id="9ca4a-119">Operationalization kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-119">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="9ca4a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ca4a-120">-Name</span></span>
<span data-ttu-id="9ca4a-121">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-121">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="9ca4a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca4a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ca4a-123">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-123">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="9ca4a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9ca4a-124">-ResourceId</span></span>
<span data-ttu-id="9ca4a-125">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-125">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="9ca4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca4a-126">CommonParameters</span></span>
<span data-ttu-id="9ca4a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca4a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca4a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca4a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ca4a-129">INPUTS</span></span>

### <span data-ttu-id="9ca4a-130">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="9ca4a-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="9ca4a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9ca4a-131">System.String</span></span>

## <span data-ttu-id="9ca4a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ca4a-132">OUTPUTS</span></span>

### <span data-ttu-id="9ca4a-133">Microsoft. Azure. Commands. machinelearningcompute. modeller. pschecksystemservicesupdatesavailablerese</span><span class="sxs-lookup"><span data-stu-id="9ca4a-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="9ca4a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ca4a-134">NOTES</span></span>

## <span data-ttu-id="9ca4a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ca4a-135">RELATED LINKS</span></span>
