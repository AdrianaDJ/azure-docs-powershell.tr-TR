---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268891"
---
# <span data-ttu-id="837ee-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="837ee-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="837ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="837ee-102">SYNOPSIS</span></span>
<span data-ttu-id="837ee-103">Belirtilen kümede Not havuzu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="837ee-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="837ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="837ee-104">SYNTAX</span></span>

### <span data-ttu-id="837ee-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="837ee-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="837ee-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="837ee-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="837ee-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="837ee-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="837ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="837ee-108">DESCRIPTION</span></span>
<span data-ttu-id="837ee-109">Belirtilen kümede Not havuzu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="837ee-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="837ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="837ee-110">EXAMPLES</span></span>

### <span data-ttu-id="837ee-111">Belirtilen küme içindeki tüm düğüm havuzlarını alma</span><span class="sxs-lookup"><span data-stu-id="837ee-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="837ee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="837ee-112">PARAMETERS</span></span>

### <span data-ttu-id="837ee-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="837ee-113">-ClusterName</span></span>
<span data-ttu-id="837ee-114">Yönetilen küme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="837ee-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837ee-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="837ee-115">-ClusterObject</span></span>
<span data-ttu-id="837ee-116">Küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="837ee-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="837ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837ee-117">-DefaultProfile</span></span>
<span data-ttu-id="837ee-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="837ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="837ee-119">-ID</span><span class="sxs-lookup"><span data-stu-id="837ee-119">-Id</span></span>
<span data-ttu-id="837ee-120">Yönetilen Kubernetes kümesindeki bir düğüm havuzunun kimliği</span><span class="sxs-lookup"><span data-stu-id="837ee-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837ee-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="837ee-121">-Name</span></span>
<span data-ttu-id="837ee-122">Düğüm havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="837ee-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="837ee-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="837ee-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837ee-125">CommonParameters</span></span>
<span data-ttu-id="837ee-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="837ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837ee-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="837ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837ee-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="837ee-128">INPUTS</span></span>

### <span data-ttu-id="837ee-129">System. String</span><span class="sxs-lookup"><span data-stu-id="837ee-129">System.String</span></span>

## <span data-ttu-id="837ee-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="837ee-130">OUTPUTS</span></span>

### <span data-ttu-id="837ee-131">Microsoft. Azure. Commands. aks. modeller. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="837ee-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="837ee-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="837ee-132">NOTES</span></span>

## <span data-ttu-id="837ee-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="837ee-133">RELATED LINKS</span></span>
