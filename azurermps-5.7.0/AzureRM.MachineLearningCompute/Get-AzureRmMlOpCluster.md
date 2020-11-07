---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762640"
---
# <span data-ttu-id="2b12f-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2b12f-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="2b12f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b12f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b12f-103">Bir operationalization küme nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="2b12f-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b12f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b12f-104">SYNTAX</span></span>

### <span data-ttu-id="2b12f-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="2b12f-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b12f-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b12f-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b12f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b12f-107">DESCRIPTION</span></span>
<span data-ttu-id="2b12f-108">Bir operationalization kümesi nesnesini ada göre veya kaynak grubuna göre veya abonelikle alır.</span><span class="sxs-lookup"><span data-stu-id="2b12f-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="2b12f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b12f-109">EXAMPLES</span></span>

### <span data-ttu-id="2b12f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b12f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="2b12f-111">Belirli bir operationalization kümesini ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="2b12f-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="2b12f-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2b12f-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="2b12f-113">Kaynak grubundaki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2b12f-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="2b12f-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2b12f-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="2b12f-115">Bir abonelikteki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2b12f-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="2b12f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b12f-116">PARAMETERS</span></span>

### <span data-ttu-id="2b12f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b12f-117">-DefaultProfile</span></span>
<span data-ttu-id="2b12f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b12f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b12f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b12f-119">-Name</span></span>
<span data-ttu-id="2b12f-120">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="2b12f-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b12f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b12f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b12f-122">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2b12f-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b12f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b12f-123">CommonParameters</span></span>
<span data-ttu-id="2b12f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b12f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b12f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b12f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b12f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b12f-126">INPUTS</span></span>

### <span data-ttu-id="2b12f-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2b12f-127">None</span></span>

## <span data-ttu-id="2b12f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b12f-128">OUTPUTS</span></span>

### <span data-ttu-id="2b12f-129">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2b12f-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="2b12f-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. modeller. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b12f-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b12f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b12f-131">NOTES</span></span>

## <span data-ttu-id="2b12f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b12f-132">RELATED LINKS</span></span>

