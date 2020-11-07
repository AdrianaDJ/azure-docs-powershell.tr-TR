---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751461"
---
# <span data-ttu-id="788a2-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="788a2-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="788a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="788a2-102">SYNOPSIS</span></span>
<span data-ttu-id="788a2-103">Bir operationalization küme nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="788a2-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="788a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="788a2-104">SYNTAX</span></span>

### <span data-ttu-id="788a2-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="788a2-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="788a2-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="788a2-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="788a2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="788a2-107">DESCRIPTION</span></span>
<span data-ttu-id="788a2-108">Bir operationalization kümesi nesnesini ada göre veya kaynak grubuna göre veya abonelikle alır.</span><span class="sxs-lookup"><span data-stu-id="788a2-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="788a2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="788a2-109">EXAMPLES</span></span>

### <span data-ttu-id="788a2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="788a2-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="788a2-111">Belirli bir operationalization kümesini ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="788a2-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="788a2-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="788a2-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="788a2-113">Kaynak grubundaki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="788a2-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="788a2-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="788a2-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="788a2-115">Bir abonelikteki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="788a2-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="788a2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="788a2-116">PARAMETERS</span></span>

### <span data-ttu-id="788a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788a2-117">-DefaultProfile</span></span>
<span data-ttu-id="788a2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="788a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="788a2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="788a2-119">-Name</span></span>
<span data-ttu-id="788a2-120">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="788a2-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="788a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="788a2-122">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="788a2-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="788a2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788a2-123">CommonParameters</span></span>
<span data-ttu-id="788a2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="788a2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788a2-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788a2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788a2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="788a2-126">INPUTS</span></span>

### <span data-ttu-id="788a2-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="788a2-127">None</span></span>

## <span data-ttu-id="788a2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="788a2-128">OUTPUTS</span></span>

### <span data-ttu-id="788a2-129">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="788a2-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="788a2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="788a2-130">NOTES</span></span>

## <span data-ttu-id="788a2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="788a2-131">RELATED LINKS</span></span>
