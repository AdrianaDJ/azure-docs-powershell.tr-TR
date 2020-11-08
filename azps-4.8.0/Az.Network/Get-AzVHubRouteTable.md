---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266526"
---
# <span data-ttu-id="6bec0-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bec0-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="6bec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bec0-102">SYNOPSIS</span></span>
<span data-ttu-id="6bec0-103">VirtualHub ile ilişkilendirilmiş bir hub yol tablosu kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="6bec0-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="6bec0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bec0-104">SYNTAX</span></span>

### <span data-ttu-id="6bec0-105">ByVHubRouteTableName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bec0-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bec0-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6bec0-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bec0-107">Byvhubroutetableresourceıd</span><span class="sxs-lookup"><span data-stu-id="6bec0-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bec0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bec0-108">DESCRIPTION</span></span>
<span data-ttu-id="6bec0-109">Belirtilen hub yol tablosunu belirtilen sanal hub ile ilişkili olarak alır.</span><span class="sxs-lookup"><span data-stu-id="6bec0-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="6bec0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bec0-110">EXAMPLES</span></span>

### <span data-ttu-id="6bec0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bec0-111">Example 1</span></span>

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

<span data-ttu-id="6bec0-112">Bu komut, sanal hub 'ın hub yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="6bec0-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="6bec0-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6bec0-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="6bec0-114">Bu komut, belirtilen VirtualHub 'daki tüm Hub yol tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6bec0-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="6bec0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bec0-115">PARAMETERS</span></span>

### <span data-ttu-id="6bec0-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="6bec0-116">-AsJob</span></span>
<span data-ttu-id="6bec0-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6bec0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bec0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bec0-118">-DefaultProfile</span></span>
<span data-ttu-id="6bec0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bec0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bec0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bec0-120">-Name</span></span>
<span data-ttu-id="6bec0-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6bec0-121">The resource name.</span></span>

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

### <span data-ttu-id="6bec0-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6bec0-122">-ParentObject</span></span>
<span data-ttu-id="6bec0-123">Bu kaynağın üst sanal hub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6bec0-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="6bec0-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6bec0-124">-ParentResourceName</span></span>
<span data-ttu-id="6bec0-125">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6bec0-125">The parent resource name.</span></span>

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

### <span data-ttu-id="6bec0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bec0-126">-ResourceGroupName</span></span>
<span data-ttu-id="6bec0-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6bec0-127">The resource group name.</span></span>

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

### <span data-ttu-id="6bec0-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6bec0-128">-ResourceId</span></span>
<span data-ttu-id="6bec0-129">Alınacak vhubroutetable kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6bec0-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="6bec0-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bec0-130">-Confirm</span></span>
<span data-ttu-id="6bec0-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bec0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bec0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bec0-132">-WhatIf</span></span>
<span data-ttu-id="6bec0-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bec0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bec0-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bec0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bec0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bec0-135">CommonParameters</span></span>
<span data-ttu-id="6bec0-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bec0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bec0-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6bec0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bec0-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bec0-138">INPUTS</span></span>

### <span data-ttu-id="6bec0-139">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6bec0-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6bec0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6bec0-140">System.String</span></span>

## <span data-ttu-id="6bec0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bec0-141">OUTPUTS</span></span>

### <span data-ttu-id="6bec0-142">Microsoft. Azure. Commands. Network. model. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bec0-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="6bec0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bec0-143">NOTES</span></span>

## <span data-ttu-id="6bec0-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bec0-144">RELATED LINKS</span></span>

[<span data-ttu-id="6bec0-145">Yeni-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="6bec0-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="6bec0-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bec0-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="6bec0-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bec0-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="6bec0-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bec0-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)