---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274049"
---
# <span data-ttu-id="52a36-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="52a36-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="52a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a36-102">SYNOPSIS</span></span>
<span data-ttu-id="52a36-103">Ölçeklenebilir bir VPN ağ geçidi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="52a36-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="52a36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52a36-104">SYNTAX</span></span>

### <span data-ttu-id="52a36-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52a36-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a36-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="52a36-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a36-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="52a36-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a36-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52a36-108">DESCRIPTION</span></span>
<span data-ttu-id="52a36-109">**Update-AzVpnGateway** cmdlet 'i ÖLÇEKLENEBILIR bir VPN ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="52a36-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="52a36-110">Azure VPN ağ geçidi, VirtualHub içindeki site bağlantılarına site için tanımlanmış bir yazılımdır.</span><span class="sxs-lookup"><span data-stu-id="52a36-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="52a36-111">Bu ağ geçidi, Kullanıcı tarafından belirtilen ölçek birimine göre yeniden boyutlandırır ve ölçekler.</span><span class="sxs-lookup"><span data-stu-id="52a36-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="52a36-112">VPN sitesi olarak bilinen bir daldan/siteden ölçeklenebilir ağ geçidine bağlantı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="52a36-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="52a36-113">Her bağlantı 2 Active-Active tünelden oluşur</span><span class="sxs-lookup"><span data-stu-id="52a36-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="52a36-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52a36-114">EXAMPLES</span></span>

### <span data-ttu-id="52a36-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52a36-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="52a36-116">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52a36-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="52a36-117">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="52a36-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="52a36-118">Ağ Geçidi oluşturulduktan sonra, ağ geçidini 3 ölçekli birimlere güncellemek için Update-AzVpnGateway kullanır.</span><span class="sxs-lookup"><span data-stu-id="52a36-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="52a36-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="52a36-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="52a36-120">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52a36-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="52a36-121">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="52a36-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="52a36-122">Ağ Geçidi oluşturulduktan sonra, BgpPeeringAddress 'i güncelleştirmek için Set-AzVpnGateway kullanır.</span><span class="sxs-lookup"><span data-stu-id="52a36-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="52a36-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52a36-123">PARAMETERS</span></span>

### <span data-ttu-id="52a36-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="52a36-124">-AsJob</span></span>
<span data-ttu-id="52a36-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="52a36-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52a36-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="52a36-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="52a36-127">Bu VpnGateway 'in BGP eşleme adresleri.</span><span class="sxs-lookup"><span data-stu-id="52a36-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="52a36-128">-Confirm</span></span>
<span data-ttu-id="52a36-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52a36-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a36-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a36-130">-DefaultProfile</span></span>
<span data-ttu-id="52a36-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52a36-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a36-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a36-132">-InputObject</span></span>
<span data-ttu-id="52a36-133">Değiştirilecek VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="52a36-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="52a36-134">-Name</span></span>
<span data-ttu-id="52a36-135">VPN ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="52a36-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a36-136">-ResourceGroupName</span></span>
<span data-ttu-id="52a36-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="52a36-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="52a36-138">-ResourceId</span></span>
<span data-ttu-id="52a36-139">Değiştirilecek Vpnağ geçidinin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="52a36-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="52a36-140">-Tag</span></span>
<span data-ttu-id="52a36-141">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="52a36-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="52a36-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="52a36-142">-VpnConnection</span></span>
<span data-ttu-id="52a36-143">Bu VpnGateway 'in sahip olduğu VpnConnections listesi.</span><span class="sxs-lookup"><span data-stu-id="52a36-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="52a36-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="52a36-145">Bu VpnGateway 'in ölçek birimi.</span><span class="sxs-lookup"><span data-stu-id="52a36-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a36-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a36-146">-WhatIf</span></span>
<span data-ttu-id="52a36-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52a36-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a36-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52a36-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a36-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a36-149">CommonParameters</span></span>
<span data-ttu-id="52a36-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52a36-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a36-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="52a36-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a36-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52a36-152">INPUTS</span></span>

### <span data-ttu-id="52a36-153">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="52a36-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="52a36-154">System. String</span><span class="sxs-lookup"><span data-stu-id="52a36-154">System.String</span></span>

## <span data-ttu-id="52a36-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52a36-155">OUTPUTS</span></span>

### <span data-ttu-id="52a36-156">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="52a36-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="52a36-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52a36-157">NOTES</span></span>

## <span data-ttu-id="52a36-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52a36-158">RELATED LINKS</span></span>
[<span data-ttu-id="52a36-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="52a36-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="52a36-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="52a36-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="52a36-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="52a36-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)