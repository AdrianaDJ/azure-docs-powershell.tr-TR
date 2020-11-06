---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 746dde8dd3460add5eb6a20e4a9b771873dac0e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590199"
---
# <span data-ttu-id="76e4c-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="76e4c-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="76e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="76e4c-103">Bir operationalization küme nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="76e4c-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76e4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76e4c-104">SYNTAX</span></span>

### <span data-ttu-id="76e4c-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="76e4c-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76e4c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="76e4c-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76e4c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76e4c-107">DESCRIPTION</span></span>
<span data-ttu-id="76e4c-108">Bir operationalization kümesi nesnesini ada göre veya kaynak grubuna göre veya abonelikle alır.</span><span class="sxs-lookup"><span data-stu-id="76e4c-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="76e4c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76e4c-109">EXAMPLES</span></span>

### <span data-ttu-id="76e4c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76e4c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="76e4c-111">Belirli bir operationalization kümesini ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="76e4c-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="76e4c-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76e4c-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="76e4c-113">Kaynak grubundaki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="76e4c-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="76e4c-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="76e4c-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="76e4c-115">Bir abonelikteki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="76e4c-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="76e4c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76e4c-116">PARAMETERS</span></span>

### <span data-ttu-id="76e4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e4c-117">-DefaultProfile</span></span>
<span data-ttu-id="76e4c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76e4c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e4c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="76e4c-119">-Name</span></span>
<span data-ttu-id="76e4c-120">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="76e4c-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="76e4c-122">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="76e4c-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e4c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e4c-123">CommonParameters</span></span>
<span data-ttu-id="76e4c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76e4c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e4c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e4c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e4c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76e4c-126">INPUTS</span></span>

### <span data-ttu-id="76e4c-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76e4c-127">None</span></span>

## <span data-ttu-id="76e4c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76e4c-128">OUTPUTS</span></span>

### <span data-ttu-id="76e4c-129">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="76e4c-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="76e4c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76e4c-130">NOTES</span></span>

## <span data-ttu-id="76e4c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76e4c-131">RELATED LINKS</span></span>
