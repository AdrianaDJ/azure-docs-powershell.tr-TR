---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266968"
---
# <span data-ttu-id="94816-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="94816-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="94816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94816-102">SYNOPSIS</span></span>
<span data-ttu-id="94816-103">Kümeleri alma veya listeleme</span><span class="sxs-lookup"><span data-stu-id="94816-103">Get or list clusters</span></span>

## <span data-ttu-id="94816-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94816-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94816-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94816-105">DESCRIPTION</span></span>
<span data-ttu-id="94816-106">"-ClusterName" ve "ResourceGroupName" sağlanmadıysa, "-ClusterName" ve "ResourceGroupName" gibi kümeler</span><span class="sxs-lookup"><span data-stu-id="94816-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="94816-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94816-107">EXAMPLES</span></span>

### <span data-ttu-id="94816-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94816-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="94816-109">Küme al</span><span class="sxs-lookup"><span data-stu-id="94816-109">Get cluster</span></span>

## <span data-ttu-id="94816-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94816-110">PARAMETERS</span></span>

### <span data-ttu-id="94816-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94816-111">-ClusterName</span></span>
<span data-ttu-id="94816-112">Küme adı.</span><span class="sxs-lookup"><span data-stu-id="94816-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94816-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94816-113">-DefaultProfile</span></span>
<span data-ttu-id="94816-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94816-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94816-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94816-115">-ResourceGroupName</span></span>
<span data-ttu-id="94816-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="94816-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94816-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94816-117">CommonParameters</span></span>
<span data-ttu-id="94816-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94816-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94816-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94816-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94816-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94816-120">INPUTS</span></span>

### <span data-ttu-id="94816-121">System. String</span><span class="sxs-lookup"><span data-stu-id="94816-121">System.String</span></span>

## <span data-ttu-id="94816-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94816-122">OUTPUTS</span></span>

### <span data-ttu-id="94816-123">Microsoft. Azure. Commands. Operationalınsights. model. PSCluster</span><span class="sxs-lookup"><span data-stu-id="94816-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="94816-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94816-124">NOTES</span></span>

## <span data-ttu-id="94816-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94816-125">RELATED LINKS</span></span>
