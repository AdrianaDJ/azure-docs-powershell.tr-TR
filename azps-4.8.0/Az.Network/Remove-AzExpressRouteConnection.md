---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274094"
---
# <span data-ttu-id="cb409-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb409-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="cb409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb409-102">SYNOPSIS</span></span>
<span data-ttu-id="cb409-103">ExpressRouteConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb409-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="cb409-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb409-104">SYNTAX</span></span>

### <span data-ttu-id="cb409-105">ByExpressRouteConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb409-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb409-106">Byexpressrouteconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="cb409-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb409-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="cb409-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb409-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb409-108">DESCRIPTION</span></span>
<span data-ttu-id="cb409-109">ExpressRouteConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb409-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="cb409-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb409-110">EXAMPLES</span></span>

### <span data-ttu-id="cb409-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb409-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="cb409-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb409-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cb409-113">Daha sonra 2 ölçekli birim içeren sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cb409-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cb409-114">Ağ Geçidi oluşturulduktan sonra, New-AzExpressRouteConnection komutunu kullanarak ExpressRouteSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="cb409-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="cb409-115">Ardından bağlantı adını kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb409-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="cb409-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cb409-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="cb409-117">Örnek 1 ile aynıdır, ancak artık Get-AzExpressRouteConnection 'dan Piped nesnesini kullanarak bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb409-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="cb409-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb409-118">PARAMETERS</span></span>

### <span data-ttu-id="cb409-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb409-119">-DefaultProfile</span></span>
<span data-ttu-id="cb409-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb409-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb409-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="cb409-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="cb409-122">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cb409-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cb409-123">-Force</span></span>
<span data-ttu-id="cb409-124">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="cb409-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb409-125">-InputObject</span></span>
<span data-ttu-id="cb409-126">Güncelleştirilecek ExpressRouteConnection nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cb409-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb409-127">-Name</span></span>
<span data-ttu-id="cb409-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cb409-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb409-129">-PassThru</span></span>
<span data-ttu-id="cb409-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb409-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb409-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cb409-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb409-132">-ResourceGroupName</span></span>
<span data-ttu-id="cb409-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cb409-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cb409-134">-ResourceId</span></span>
<span data-ttu-id="cb409-135">Silinecek ExpressRouteConnection nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cb409-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb409-136">-Confirm</span></span>
<span data-ttu-id="cb409-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb409-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb409-138">-WhatIf</span></span>
<span data-ttu-id="cb409-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb409-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb409-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb409-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb409-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb409-141">CommonParameters</span></span>
<span data-ttu-id="cb409-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb409-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb409-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb409-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb409-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb409-144">INPUTS</span></span>

### <span data-ttu-id="cb409-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cb409-145">System.String</span></span>

### <span data-ttu-id="cb409-146">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb409-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="cb409-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb409-147">OUTPUTS</span></span>

### <span data-ttu-id="cb409-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb409-148">System.Boolean</span></span>

## <span data-ttu-id="cb409-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb409-149">NOTES</span></span>

## <span data-ttu-id="cb409-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb409-150">RELATED LINKS</span></span>
