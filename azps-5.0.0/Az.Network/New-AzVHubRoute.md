---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323689"
---
# <span data-ttu-id="e2630-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="e2630-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="e2630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2630-102">SYNOPSIS</span></span>
<span data-ttu-id="e2630-103">New-AzVHubRouteTable komutuna parametre olarak geçirilebilecek VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2630-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="e2630-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2630-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2630-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2630-105">DESCRIPTION</span></span>

<span data-ttu-id="e2630-106">VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2630-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="e2630-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2630-107">EXAMPLES</span></span>

### <span data-ttu-id="e2630-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2630-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="e2630-109">Yukarıdaki komut, belirtilen güvenlik duvarı ile VHubRouteTable kaynağına eklenebilecek bir VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2630-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="e2630-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e2630-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="e2630-111">Yukarıdaki komut, daha sonra bir VHubRouteTable kaynağına eklenebilecek belirtilen hubVnetConnection ile VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2630-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="e2630-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e2630-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="e2630-113">Yukarıdaki komutlar, var olan bir Azvhub yolunun RoutingConfiguration 'ı alır ve ardından bağlantıya statik bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="e2630-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="e2630-114">Alternatif olarak, içinde statik yol ile yeni bir bağlantı oluşturmayı düşünüyorsanız, lütfen burada örnek 1 ' e bakın [.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e2630-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="e2630-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2630-115">PARAMETERS</span></span>

### <span data-ttu-id="e2630-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2630-116">-DefaultProfile</span></span>
<span data-ttu-id="e2630-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2630-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2630-118">-Hedef</span><span class="sxs-lookup"><span data-stu-id="e2630-118">-Destination</span></span>
<span data-ttu-id="e2630-119">Hedef listesi.</span><span class="sxs-lookup"><span data-stu-id="e2630-119">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2630-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="e2630-120">-DestinationType</span></span>
<span data-ttu-id="e2630-121">Hedef türü.</span><span class="sxs-lookup"><span data-stu-id="e2630-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="e2630-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2630-122">-Name</span></span>
<span data-ttu-id="e2630-123">Yol adı.</span><span class="sxs-lookup"><span data-stu-id="e2630-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2630-124">-Sonraki</span><span class="sxs-lookup"><span data-stu-id="e2630-124">-NextHop</span></span>
<span data-ttu-id="e2630-125">Sonraki atlama.</span><span class="sxs-lookup"><span data-stu-id="e2630-125">The next hop.</span></span>

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

### <span data-ttu-id="e2630-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="e2630-126">-NextHopType</span></span>
<span data-ttu-id="e2630-127">Sonraki atlama türü.</span><span class="sxs-lookup"><span data-stu-id="e2630-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="e2630-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2630-128">CommonParameters</span></span>
<span data-ttu-id="e2630-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2630-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2630-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2630-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2630-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2630-131">INPUTS</span></span>

### <span data-ttu-id="e2630-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e2630-132">System.String</span></span>

## <span data-ttu-id="e2630-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2630-133">OUTPUTS</span></span>

### <span data-ttu-id="e2630-134">Microsoft. Azure. Commands. Network. model. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="e2630-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="e2630-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2630-135">NOTES</span></span>

## <span data-ttu-id="e2630-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2630-136">RELATED LINKS</span></span>

[<span data-ttu-id="e2630-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2630-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="e2630-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2630-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="e2630-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2630-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="e2630-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e2630-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)