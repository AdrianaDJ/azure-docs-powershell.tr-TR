---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 6aabba5154e14f3af0ccfff20569c0cdc51a2578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760349"
---
# <span data-ttu-id="7ea5c-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7ea5c-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="7ea5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea5c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea5c-103">Ölçeklenebilir ExpressRoute ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="7ea5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ea5c-104">SYNTAX</span></span>

### <span data-ttu-id="7ea5c-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ea5c-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea5c-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7ea5c-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea5c-107">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="7ea5c-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea5c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ea5c-108">DESCRIPTION</span></span>

<span data-ttu-id="7ea5c-109">New-AzExpressRouteGateway ölçeklenebilir ExpressRoute ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="7ea5c-110">Bu, VirtualHub içindeki Azure ile şirket içi için tanımlanmış bir yazılımdır.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="7ea5c-111">Bu ağ geçidi, bu veya Set-AzExpressRouteGateway cmdlet 'inde belirtilen ölçek birimine göre ölçeklendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="7ea5c-112">Bir bağlantı Şirket içi ExpressRoute devresi ile ölçeklenebilir ağ geçidine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="7ea5c-113">ExpressRouteGateway, başvurulan VirtualHub ile aynı konumda olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="7ea5c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ea5c-114">EXAMPLES</span></span>

### <span data-ttu-id="7ea5c-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ea5c-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7ea5c-116">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7ea5c-117">Daha sonra 2 ölçekli birim içeren sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="7ea5c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ea5c-118">PARAMETERS</span></span>

### <span data-ttu-id="7ea5c-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="7ea5c-119">-AsJob</span></span>
<span data-ttu-id="7ea5c-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7ea5c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ea5c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea5c-121">-DefaultProfile</span></span>
<span data-ttu-id="7ea5c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ea5c-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7ea5c-123">-MaxScaleUnits</span></span>
<span data-ttu-id="7ea5c-124">Bu ExpressRouteGateway için en yüksek ölçek birimi sayısı.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7ea5c-125">Geçerli Aralık > 2</span><span class="sxs-lookup"><span data-stu-id="7ea5c-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7ea5c-126">-MinScaleUnits</span></span>
<span data-ttu-id="7ea5c-127">Bu ExpressRouteGateway için en az ölçek birimi sayısı.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7ea5c-128">Geçerli Aralık > 2</span><span class="sxs-lookup"><span data-stu-id="7ea5c-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ea5c-129">-Name</span></span>
<span data-ttu-id="7ea5c-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea5c-131">-ResourceGroupName</span></span>
<span data-ttu-id="7ea5c-132">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7ea5c-133">-Tag</span></span>
<span data-ttu-id="7ea5c-134">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7ea5c-135">-VirtualHub</span></span>
<span data-ttu-id="7ea5c-136">Bu VpnGateway 'in VirtualHub 'ı ile ilişkilendirilmesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-137">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="7ea5c-137">-VirtualHubId</span></span>
<span data-ttu-id="7ea5c-138">Bu VpnGateway 'in ilişkilendirildiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="7ea5c-139">-VirtualHubName</span></span>
<span data-ttu-id="7ea5c-140">Bu VpnGateway 'in ilişkilendirildiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea5c-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ea5c-141">-Confirm</span></span>
<span data-ttu-id="7ea5c-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea5c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea5c-143">-WhatIf</span></span>
<span data-ttu-id="7ea5c-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea5c-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea5c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea5c-146">CommonParameters</span></span>
<span data-ttu-id="7ea5c-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea5c-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea5c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea5c-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ea5c-149">INPUTS</span></span>

### <span data-ttu-id="7ea5c-150">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7ea5c-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7ea5c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea5c-151">System.String</span></span>

## <span data-ttu-id="7ea5c-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ea5c-152">OUTPUTS</span></span>

### <span data-ttu-id="7ea5c-153">Microsoft. Azure. Commands. Network. model. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7ea5c-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="7ea5c-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ea5c-154">NOTES</span></span>

## <span data-ttu-id="7ea5c-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ea5c-155">RELATED LINKS</span></span>
