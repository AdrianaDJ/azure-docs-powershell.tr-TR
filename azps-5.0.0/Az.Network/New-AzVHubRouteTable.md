---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278539"
---
# <span data-ttu-id="31b97-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31b97-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="31b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b97-102">SYNOPSIS</span></span>
<span data-ttu-id="31b97-103">VirtualHub ile ilişkilendirilmiş bir hub yol tablosu kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31b97-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="31b97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31b97-104">SYNTAX</span></span>

### <span data-ttu-id="31b97-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31b97-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b97-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="31b97-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b97-107">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="31b97-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b97-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="31b97-108">DESCRIPTION</span></span>
<span data-ttu-id="31b97-109">Belirtilen yollar ve etiketlerle belirtilen sanal hub ile ilişkilendirilmiş belirtilen yol tablosunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31b97-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="31b97-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31b97-110">EXAMPLES</span></span>

### <span data-ttu-id="31b97-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31b97-111">Example 1</span></span>

```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="31b97-112">Bu komut sanal hub 'ın hub yol tablosunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31b97-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="31b97-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31b97-113">PARAMETERS</span></span>

### <span data-ttu-id="31b97-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="31b97-114">-AsJob</span></span>
<span data-ttu-id="31b97-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="31b97-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31b97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b97-116">-DefaultProfile</span></span>
<span data-ttu-id="31b97-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31b97-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b97-118">Etiketli</span><span class="sxs-lookup"><span data-stu-id="31b97-118">-Label</span></span>
<span data-ttu-id="31b97-119">Etiket listesi.</span><span class="sxs-lookup"><span data-stu-id="31b97-119">The list of labels.</span></span>

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

### <span data-ttu-id="31b97-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="31b97-120">-Name</span></span>
<span data-ttu-id="31b97-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="31b97-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b97-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="31b97-122">-ParentObject</span></span>
<span data-ttu-id="31b97-123">Bu kaynağın üst sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="31b97-123">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b97-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="31b97-124">-ParentResourceName</span></span>
<span data-ttu-id="31b97-125">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="31b97-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b97-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b97-126">-ResourceGroupName</span></span>
<span data-ttu-id="31b97-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="31b97-127">The resource group name.</span></span>

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

### <span data-ttu-id="31b97-128">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="31b97-128">-ParentResourceId</span></span>
<span data-ttu-id="31b97-129">Sanal hub kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="31b97-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b97-130">-Route</span><span class="sxs-lookup"><span data-stu-id="31b97-130">-Route</span></span>
<span data-ttu-id="31b97-131">Bu yol tablosundaki yolların listesi.</span><span class="sxs-lookup"><span data-stu-id="31b97-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b97-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="31b97-132">-Confirm</span></span>
<span data-ttu-id="31b97-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31b97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b97-134">-WhatIf</span></span>
<span data-ttu-id="31b97-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31b97-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b97-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31b97-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b97-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b97-137">CommonParameters</span></span>
<span data-ttu-id="31b97-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31b97-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b97-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="31b97-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b97-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31b97-140">INPUTS</span></span>

### <span data-ttu-id="31b97-141">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="31b97-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="31b97-142">Microsoft. Azure. Commands. Network. model. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31b97-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="31b97-143">System. String</span><span class="sxs-lookup"><span data-stu-id="31b97-143">System.String</span></span>

## <span data-ttu-id="31b97-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31b97-144">OUTPUTS</span></span>

### <span data-ttu-id="31b97-145">Microsoft. Azure. Commands. Network. model. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31b97-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="31b97-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31b97-146">NOTES</span></span>

## <span data-ttu-id="31b97-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31b97-147">RELATED LINKS</span></span>

[<span data-ttu-id="31b97-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31b97-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="31b97-149">Yeni-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="31b97-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="31b97-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31b97-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="31b97-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31b97-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
