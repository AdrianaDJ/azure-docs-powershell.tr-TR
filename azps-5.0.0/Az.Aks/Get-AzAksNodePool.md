---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277117"
---
# <span data-ttu-id="6a3bc-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="6a3bc-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="6a3bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3bc-103">Belirtilen kümede Not havuzu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="6a3bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-104">SYNTAX</span></span>

### <span data-ttu-id="6a3bc-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a3bc-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a3bc-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="6a3bc-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a3bc-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a3bc-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3bc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a3bc-108">DESCRIPTION</span></span>
<span data-ttu-id="6a3bc-109">Belirtilen kümede Not havuzu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="6a3bc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a3bc-110">EXAMPLES</span></span>

### <span data-ttu-id="6a3bc-111">Belirtilen küme içindeki tüm düğüm havuzlarını alma</span><span class="sxs-lookup"><span data-stu-id="6a3bc-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="6a3bc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a3bc-112">PARAMETERS</span></span>

### <span data-ttu-id="6a3bc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6a3bc-113">-ClusterName</span></span>
<span data-ttu-id="6a3bc-114">Yönetilen küme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="6a3bc-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="6a3bc-115">-ClusterObject</span></span>
<span data-ttu-id="6a3bc-116">Küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-116">The cluster object.</span></span>

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

### <span data-ttu-id="6a3bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3bc-117">-DefaultProfile</span></span>
<span data-ttu-id="6a3bc-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a3bc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="6a3bc-119">-Id</span></span>
<span data-ttu-id="6a3bc-120">Yönetilen Kubernetes kümesindeki bir düğüm havuzunun kimliği</span><span class="sxs-lookup"><span data-stu-id="6a3bc-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6a3bc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a3bc-121">-Name</span></span>
<span data-ttu-id="6a3bc-122">Düğüm havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="6a3bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a3bc-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a3bc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3bc-125">CommonParameters</span></span>
<span data-ttu-id="6a3bc-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3bc-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3bc-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-128">INPUTS</span></span>

### <span data-ttu-id="6a3bc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3bc-129">System.String</span></span>

## <span data-ttu-id="6a3bc-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a3bc-130">OUTPUTS</span></span>

### <span data-ttu-id="6a3bc-131">Microsoft. Azure. Commands. aks. modeller. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="6a3bc-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="6a3bc-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a3bc-132">NOTES</span></span>

## <span data-ttu-id="6a3bc-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a3bc-133">RELATED LINKS</span></span>
