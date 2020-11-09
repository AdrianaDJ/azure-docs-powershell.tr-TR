---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323728"
---
# <span data-ttu-id="74eed-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="74eed-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="74eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74eed-102">SYNOPSIS</span></span>
<span data-ttu-id="74eed-103">RoutingConfiguration nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74eed-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="74eed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74eed-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74eed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74eed-105">DESCRIPTION</span></span>
<span data-ttu-id="74eed-106">RoutingConfiguration nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74eed-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="74eed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74eed-107">EXAMPLES</span></span>

### <span data-ttu-id="74eed-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="74eed-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="74eed-109">Yukarıdaki komut, bir bağlantı kaynağına eklenebilecek bir RoutingConfiguration nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74eed-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="74eed-110">Statik yollara yalnızca bir HubVirtualNetworkConnection nesnesi ile izin verilir.</span><span class="sxs-lookup"><span data-stu-id="74eed-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="74eed-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74eed-111">PARAMETERS</span></span>

### <span data-ttu-id="74eed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74eed-112">-DefaultProfile</span></span>
<span data-ttu-id="74eed-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74eed-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74eed-114">-Ilişkili</span><span class="sxs-lookup"><span data-stu-id="74eed-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="74eed-115">Bu yönlendirme yapılandırmasıyla ilişkili hub yol tablosu.</span><span class="sxs-lookup"><span data-stu-id="74eed-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="74eed-116">-ID</span><span class="sxs-lookup"><span data-stu-id="74eed-116">-Id</span></span>
<span data-ttu-id="74eed-117">PropagatedRouteTables özelliğinin yollarını duyuran tüm Hub yol tablolarının kaynak kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="74eed-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="74eed-118">Etiketli</span><span class="sxs-lookup"><span data-stu-id="74eed-118">-Label</span></span>
<span data-ttu-id="74eed-119">PropagatedRouteTables özelliğinin etiket listesi.</span><span class="sxs-lookup"><span data-stu-id="74eed-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eed-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="74eed-120">-StaticRoute</span></span>
<span data-ttu-id="74eed-121">VirtualHub 'dan sanal ağ bağlantısına yönlendirmeyi denetleyen yolların listesi.</span><span class="sxs-lookup"><span data-stu-id="74eed-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74eed-122">CommonParameters</span></span>
<span data-ttu-id="74eed-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74eed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74eed-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74eed-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74eed-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74eed-125">INPUTS</span></span>

### <span data-ttu-id="74eed-126">System. String</span><span class="sxs-lookup"><span data-stu-id="74eed-126">System.String</span></span>

### <span data-ttu-id="74eed-127">Microsoft. Azure. Commands. Network. modeller. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="74eed-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="74eed-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74eed-128">OUTPUTS</span></span>

### <span data-ttu-id="74eed-129">Microsoft. Azure. Commands. Network. model. PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="74eed-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="74eed-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74eed-130">NOTES</span></span>

## <span data-ttu-id="74eed-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74eed-131">RELATED LINKS</span></span>

[<span data-ttu-id="74eed-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="74eed-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="74eed-133">Yeni-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="74eed-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="74eed-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="74eed-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="74eed-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="74eed-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="74eed-136">Güncelleştirme-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="74eed-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="74eed-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="74eed-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="74eed-138">Güncelleştirme-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="74eed-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="74eed-139">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="74eed-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="74eed-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="74eed-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)