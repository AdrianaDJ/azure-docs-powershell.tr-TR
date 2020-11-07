---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 3ccf321a089dbb519293fe6407581aecf32b8157
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918183"
---
# <span data-ttu-id="21dd5-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="21dd5-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="21dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="21dd5-103">Azure sanal hub yol tablosu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21dd5-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="21dd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21dd5-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21dd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="21dd5-106">Azure sanal hub yol tablosu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21dd5-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="21dd5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="21dd5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21dd5-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="21dd5-109">Yukarıdaki, birden çok yoldan oluşan ve yeni bir sanal hub 'a bağlanan bir yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21dd5-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="21dd5-110">Bu, yeni veya var olan bir VirtualHub 'a yönlendirme tablosu eklemek için kullanılabilecek bir bellek içi nesnedir.</span><span class="sxs-lookup"><span data-stu-id="21dd5-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="21dd5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21dd5-111">PARAMETERS</span></span>

### <span data-ttu-id="21dd5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21dd5-112">-DefaultProfile</span></span>
<span data-ttu-id="21dd5-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21dd5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21dd5-114">-Route</span><span class="sxs-lookup"><span data-stu-id="21dd5-114">-Route</span></span>
<span data-ttu-id="21dd5-115">Sanal hub yollarının listesi.</span><span class="sxs-lookup"><span data-stu-id="21dd5-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dd5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21dd5-116">CommonParameters</span></span>
<span data-ttu-id="21dd5-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21dd5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21dd5-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21dd5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21dd5-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21dd5-119">INPUTS</span></span>

### <span data-ttu-id="21dd5-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21dd5-120">None</span></span>

## <span data-ttu-id="21dd5-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21dd5-121">OUTPUTS</span></span>

### <span data-ttu-id="21dd5-122">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="21dd5-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="21dd5-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21dd5-123">NOTES</span></span>

## <span data-ttu-id="21dd5-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21dd5-124">RELATED LINKS</span></span>

[<span data-ttu-id="21dd5-125">Yeni-Azsanalyol</span><span class="sxs-lookup"><span data-stu-id="21dd5-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)