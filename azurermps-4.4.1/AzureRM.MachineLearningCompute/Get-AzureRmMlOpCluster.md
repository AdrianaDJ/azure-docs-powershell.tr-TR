---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592615"
---
# <span data-ttu-id="719df-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="719df-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="719df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="719df-102">SYNOPSIS</span></span>
<span data-ttu-id="719df-103">Bir operationalization küme nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="719df-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="719df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="719df-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="719df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="719df-105">DESCRIPTION</span></span>
<span data-ttu-id="719df-106">Bir operationalization kümesi nesnesini ada göre veya kaynak grubuna göre veya abonelikle alır.</span><span class="sxs-lookup"><span data-stu-id="719df-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="719df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="719df-107">EXAMPLES</span></span>

### <span data-ttu-id="719df-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="719df-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="719df-109">Belirli bir operationalization kümesini ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="719df-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="719df-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="719df-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="719df-111">Kaynak grubundaki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="719df-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="719df-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="719df-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="719df-113">Bir abonelikteki tüm operationalization kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="719df-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="719df-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="719df-114">PARAMETERS</span></span>

### <span data-ttu-id="719df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719df-115">-DefaultProfile</span></span>
<span data-ttu-id="719df-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="719df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="719df-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="719df-117">-Name</span></span>
<span data-ttu-id="719df-118">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="719df-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719df-119">-ResourceGroupName</span></span>
<span data-ttu-id="719df-120">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="719df-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719df-121">CommonParameters</span></span>
<span data-ttu-id="719df-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="719df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719df-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="719df-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719df-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="719df-124">INPUTS</span></span>

### <span data-ttu-id="719df-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="719df-125">None</span></span>

## <span data-ttu-id="719df-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="719df-126">OUTPUTS</span></span>

### <span data-ttu-id="719df-127">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="719df-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="719df-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. modeller. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="719df-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="719df-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="719df-129">NOTES</span></span>

## <span data-ttu-id="719df-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="719df-130">RELATED LINKS</span></span>

