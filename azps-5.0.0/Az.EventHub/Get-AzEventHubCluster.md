---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278698"
---
# <span data-ttu-id="5e54b-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="5e54b-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="5e54b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e54b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e54b-103">Tek bir olay hub kümesinin ayrıntılarını alır veya Olay Hub kümelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="5e54b-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="5e54b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e54b-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e54b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e54b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e54b-106">Get-AzEventHubCluster cmdlet 'i, bir olay hub kümesinin ayrıntılarını veya verilen kaynak grubundaki tüm olay hub kümelerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e54b-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="5e54b-107">Küme adı sağlanmışsa, tek bir kümenin ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="5e54b-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="5e54b-108">Bir küme adı sağlanmazsa, belirtilen kaynak grubundaki tüm kümelerin listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="5e54b-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="5e54b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e54b-109">EXAMPLES</span></span>

### <span data-ttu-id="5e54b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e54b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="5e54b-111">', ' Eventhub-Cluster-5557 ' kümesinin ' RSG-Cluster27651 ' kaynak grubundan geri türlerini döndürür</span><span class="sxs-lookup"><span data-stu-id="5e54b-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="5e54b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e54b-112">PARAMETERS</span></span>

### <span data-ttu-id="5e54b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e54b-113">-DefaultProfile</span></span>
<span data-ttu-id="5e54b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e54b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e54b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e54b-115">-Name</span></span>
<span data-ttu-id="5e54b-116">Küme adı</span><span class="sxs-lookup"><span data-stu-id="5e54b-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e54b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e54b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e54b-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5e54b-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e54b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e54b-119">CommonParameters</span></span>
<span data-ttu-id="5e54b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e54b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e54b-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e54b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e54b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e54b-122">INPUTS</span></span>

### <span data-ttu-id="5e54b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5e54b-123">System.String</span></span>

## <span data-ttu-id="5e54b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e54b-124">OUTPUTS</span></span>

### <span data-ttu-id="5e54b-125">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="5e54b-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="5e54b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e54b-126">NOTES</span></span>

## <span data-ttu-id="5e54b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e54b-127">RELATED LINKS</span></span>
