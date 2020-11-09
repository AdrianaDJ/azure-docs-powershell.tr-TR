---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321465"
---
# <span data-ttu-id="246a9-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="246a9-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="246a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="246a9-102">SYNOPSIS</span></span>
<span data-ttu-id="246a9-103">Yeni bir CosmosDB VirtualNetworkRule nesnesi (PSVirtualNetworkRule) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="246a9-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="246a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="246a9-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="246a9-105">DESCRIPTION</span></span>
<span data-ttu-id="246a9-106">Yeni bir CosmosDB VirtualNetworkRule nesnesi (PSVirtualNetworkRule) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="246a9-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="246a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="246a9-107">EXAMPLES</span></span>

### <span data-ttu-id="246a9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="246a9-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="246a9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="246a9-109">PARAMETERS</span></span>

### <span data-ttu-id="246a9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246a9-110">-DefaultProfile</span></span>
<span data-ttu-id="246a9-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="246a9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="246a9-112">-ID</span><span class="sxs-lookup"><span data-stu-id="246a9-112">-Id</span></span>
<span data-ttu-id="246a9-113">Alt ağın kaynak KIMLIĞI; örneğin:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="246a9-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246a9-114">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="246a9-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="246a9-115">Sanal ağın VNET hizmeti uç noktası etkinleştirilmeden önce güvenlik duvarı oluşturup oluşturmamı belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="246a9-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246a9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246a9-116">CommonParameters</span></span>
<span data-ttu-id="246a9-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="246a9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246a9-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="246a9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246a9-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="246a9-119">INPUTS</span></span>

### <span data-ttu-id="246a9-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="246a9-120">None</span></span>

## <span data-ttu-id="246a9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="246a9-121">OUTPUTS</span></span>

### <span data-ttu-id="246a9-122">Microsoft. Azure. Commands. CosmosDB. modeller. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="246a9-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="246a9-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="246a9-123">NOTES</span></span>

## <span data-ttu-id="246a9-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="246a9-124">RELATED LINKS</span></span>
