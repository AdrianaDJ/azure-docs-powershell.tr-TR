---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274045"
---
# <span data-ttu-id="02b97-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="02b97-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="02b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b97-102">SYNOPSIS</span></span>
<span data-ttu-id="02b97-103">VirtualHub ile ilişkili bir hub yol tablosu kaynağını silme.</span><span class="sxs-lookup"><span data-stu-id="02b97-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="02b97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02b97-104">SYNTAX</span></span>

### <span data-ttu-id="02b97-105">ByVHubRouteTableName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02b97-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b97-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="02b97-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b97-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="02b97-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b97-108">Byvhubroutetableresourceıd</span><span class="sxs-lookup"><span data-stu-id="02b97-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b97-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="02b97-109">DESCRIPTION</span></span>
<span data-ttu-id="02b97-110">Belirtilen yol veya etiketlerle belirtilen sanal hub ile ilişkilendirilmiş belirtilen yol tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02b97-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="02b97-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02b97-111">EXAMPLES</span></span>

### <span data-ttu-id="02b97-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02b97-112">Example 1</span></span>
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
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="02b97-113">Bu komut sanal hub 'ın hub yol tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="02b97-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="02b97-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02b97-114">PARAMETERS</span></span>

### <span data-ttu-id="02b97-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="02b97-115">-AsJob</span></span>
<span data-ttu-id="02b97-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02b97-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02b97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b97-117">-DefaultProfile</span></span>
<span data-ttu-id="02b97-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02b97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02b97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02b97-119">-InputObject</span></span>
<span data-ttu-id="02b97-120">Güncelleştirilecek vhubroutetable kaynağı.</span><span class="sxs-lookup"><span data-stu-id="02b97-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="02b97-121">-Label</span></span>
<span data-ttu-id="02b97-122">Etiket listesi.</span><span class="sxs-lookup"><span data-stu-id="02b97-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="02b97-123">-Name</span></span>
<span data-ttu-id="02b97-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="02b97-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02b97-125">-ParentObject</span></span>
<span data-ttu-id="02b97-126">Bu kaynağın üst sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02b97-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="02b97-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="02b97-127">-ParentResourceName</span></span>
<span data-ttu-id="02b97-128">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="02b97-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b97-129">-ResourceGroupName</span></span>
<span data-ttu-id="02b97-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02b97-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02b97-131">-ResourceId</span></span>
<span data-ttu-id="02b97-132">Güncelleştirilecek vhubroutetable kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="02b97-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-133">-Route</span><span class="sxs-lookup"><span data-stu-id="02b97-133">-Route</span></span>
<span data-ttu-id="02b97-134">Bu yol tablosundaki yolların listesi.</span><span class="sxs-lookup"><span data-stu-id="02b97-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b97-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="02b97-135">-Confirm</span></span>
<span data-ttu-id="02b97-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02b97-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02b97-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b97-137">-WhatIf</span></span>
<span data-ttu-id="02b97-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02b97-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b97-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02b97-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b97-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b97-140">CommonParameters</span></span>
<span data-ttu-id="02b97-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02b97-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b97-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02b97-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b97-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02b97-143">INPUTS</span></span>

### <span data-ttu-id="02b97-144">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="02b97-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="02b97-145">Microsoft. Azure. Commands. Network. model. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="02b97-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="02b97-146">System. String</span><span class="sxs-lookup"><span data-stu-id="02b97-146">System.String</span></span>

## <span data-ttu-id="02b97-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02b97-147">OUTPUTS</span></span>

### <span data-ttu-id="02b97-148">Microsoft. Azure. Commands. Network. model. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="02b97-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="02b97-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02b97-149">NOTES</span></span>

## <span data-ttu-id="02b97-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02b97-150">RELATED LINKS</span></span>

[<span data-ttu-id="02b97-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="02b97-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="02b97-152">Yeni-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="02b97-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="02b97-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="02b97-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="02b97-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="02b97-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)