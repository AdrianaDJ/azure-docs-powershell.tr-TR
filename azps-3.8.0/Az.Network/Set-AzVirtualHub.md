---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938456"
---
# <span data-ttu-id="69658-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="69658-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="69658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69658-102">SYNOPSIS</span></span>
<span data-ttu-id="69658-103">Sanal hub 'ı değiştirir ve buna sanal hub yol tablosu ekler.</span><span class="sxs-lookup"><span data-stu-id="69658-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="69658-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69658-104">SYNTAX</span></span>

### <span data-ttu-id="69658-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69658-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69658-106">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="69658-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69658-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="69658-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69658-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="69658-108">DESCRIPTION</span></span>
<span data-ttu-id="69658-109">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="69658-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="69658-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69658-110">EXAMPLES</span></span>

### <span data-ttu-id="69658-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="69658-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="69658-112">İlk önce bir sanal hub yol nesnesi oluşturun ve sanal hub yol tablosu kaynağı oluşturmak için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="69658-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="69658-113">Ardından, Set-AzVirtualHub komutunu kullanarak bu yol tablosu kaynağını sanal hub olarak ayarladık.</span><span class="sxs-lookup"><span data-stu-id="69658-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="69658-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69658-114">PARAMETERS</span></span>

### <span data-ttu-id="69658-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="69658-115">-AsJob</span></span>
<span data-ttu-id="69658-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="69658-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69658-117">-DefaultProfile</span></span>
<span data-ttu-id="69658-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69658-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69658-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69658-119">-InputObject</span></span>
<span data-ttu-id="69658-120">Değiştirilecek sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="69658-120">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69658-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="69658-121">-Name</span></span>
<span data-ttu-id="69658-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="69658-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69658-123">-ResourceGroupName</span></span>
<span data-ttu-id="69658-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="69658-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="69658-125">-ResourceId</span></span>
<span data-ttu-id="69658-126">Değiştirilecek sanal hub 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="69658-126">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69658-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="69658-127">-RouteTable</span></span>
<span data-ttu-id="69658-128">Bu sanal hub ile ilişkilendirilmiş yol tabloları.</span><span class="sxs-lookup"><span data-stu-id="69658-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="69658-129">-Tag</span></span>
<span data-ttu-id="69658-130">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="69658-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="69658-131">-Confirm</span></span>
<span data-ttu-id="69658-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69658-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69658-133">-WhatIf</span></span>
<span data-ttu-id="69658-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69658-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69658-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69658-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69658-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69658-136">CommonParameters</span></span>
<span data-ttu-id="69658-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69658-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69658-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69658-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69658-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69658-139">INPUTS</span></span>

### <span data-ttu-id="69658-140">System. String</span><span class="sxs-lookup"><span data-stu-id="69658-140">System.String</span></span>

### <span data-ttu-id="69658-141">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="69658-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="69658-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69658-142">OUTPUTS</span></span>

### <span data-ttu-id="69658-143">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="69658-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="69658-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69658-144">NOTES</span></span>

## <span data-ttu-id="69658-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69658-145">RELATED LINKS</span></span>
