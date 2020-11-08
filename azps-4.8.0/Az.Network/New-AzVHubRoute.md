---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265982"
---
# <span data-ttu-id="1a140-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="1a140-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="1a140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a140-102">SYNOPSIS</span></span>
<span data-ttu-id="1a140-103">New-AzVHubRouteTable komutuna parametre olarak geçirilebilecek VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a140-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="1a140-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a140-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a140-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a140-105">DESCRIPTION</span></span>

<span data-ttu-id="1a140-106">VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a140-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="1a140-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a140-107">EXAMPLES</span></span>

### <span data-ttu-id="1a140-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1a140-108">Example 1</span></span>

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

<span data-ttu-id="1a140-109">Yukarıdaki komut, belirtilen güvenlik duvarı ile VHubRouteTable kaynağına eklenebilecek bir VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a140-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="1a140-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1a140-110">Example 2</span></span>

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

<span data-ttu-id="1a140-111">Yukarıdaki komut, daha sonra bir VHubRouteTable kaynağına eklenebilecek belirtilen hubVnetConnection ile VHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a140-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="1a140-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a140-112">PARAMETERS</span></span>

### <span data-ttu-id="1a140-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a140-113">-DefaultProfile</span></span>
<span data-ttu-id="1a140-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a140-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a140-115">-Hedef</span><span class="sxs-lookup"><span data-stu-id="1a140-115">-Destination</span></span>
<span data-ttu-id="1a140-116">Hedef listesi.</span><span class="sxs-lookup"><span data-stu-id="1a140-116">List of Destinations.</span></span>

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

### <span data-ttu-id="1a140-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="1a140-117">-DestinationType</span></span>
<span data-ttu-id="1a140-118">Hedef türü.</span><span class="sxs-lookup"><span data-stu-id="1a140-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="1a140-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a140-119">-Name</span></span>
<span data-ttu-id="1a140-120">Yol adı.</span><span class="sxs-lookup"><span data-stu-id="1a140-120">The route name.</span></span>

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

### <span data-ttu-id="1a140-121">-Sonraki</span><span class="sxs-lookup"><span data-stu-id="1a140-121">-NextHop</span></span>
<span data-ttu-id="1a140-122">Sonraki atlama.</span><span class="sxs-lookup"><span data-stu-id="1a140-122">The next hop.</span></span>

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

### <span data-ttu-id="1a140-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="1a140-123">-NextHopType</span></span>
<span data-ttu-id="1a140-124">Sonraki atlama türü.</span><span class="sxs-lookup"><span data-stu-id="1a140-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="1a140-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a140-125">CommonParameters</span></span>
<span data-ttu-id="1a140-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a140-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a140-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1a140-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a140-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a140-128">INPUTS</span></span>

### <span data-ttu-id="1a140-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1a140-129">System.String</span></span>

## <span data-ttu-id="1a140-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a140-130">OUTPUTS</span></span>

### <span data-ttu-id="1a140-131">Microsoft. Azure. Commands. Network. model. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="1a140-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="1a140-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a140-132">NOTES</span></span>

## <span data-ttu-id="1a140-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a140-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a140-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a140-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="1a140-135">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a140-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="1a140-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a140-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="1a140-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a140-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)