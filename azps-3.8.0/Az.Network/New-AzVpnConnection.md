---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 870caec4cad2bd4d64c00a2b0bf3423f080b98ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937432"
---
# <span data-ttu-id="9fe5d-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fe5d-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="9fe5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe5d-103">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="9fe5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fe5d-104">SYNTAX</span></span>

### <span data-ttu-id="9fe5d-105">Byvpngatewaynamebyvpnsitenesnesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fe5d-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe5d-106">Byvpngatewaynamebyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="9fe5d-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe5d-107">Byvpngatewayobjectbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="9fe5d-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe5d-108">Byvpngatewayobjectbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="9fe5d-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe5d-109">Byvpngatewayresourceıdbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="9fe5d-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe5d-110">Byvpngatewayresourceıdbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="9fe5d-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe5d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fe5d-111">DESCRIPTION</span></span>
<span data-ttu-id="9fe5d-112">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="9fe5d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fe5d-113">EXAMPLES</span></span>

### <span data-ttu-id="9fe5d-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9fe5d-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="9fe5d-115">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9fe5d-116">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="9fe5d-117">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="9fe5d-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9fe5d-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="9fe5d-119">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'deki 1 VpnSiteLinks 'e sahip bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="9fe5d-120">Sanal hub 'da bir VPN ağ geçidi oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="9fe5d-121">Ağ Geçidi oluşturulduktan sonra, vpnsite için 1 VpnSiteLinkConnections ile New-AzVpnConnection komutu ile VpnSite 'e bağlanır.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="9fe5d-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fe5d-122">PARAMETERS</span></span>

### <span data-ttu-id="9fe5d-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="9fe5d-123">-AsJob</span></span>
<span data-ttu-id="9fe5d-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9fe5d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fe5d-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="9fe5d-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="9fe5d-126">Bu bağlantı tarafından, Mbps cinsinden işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="9fe5d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe5d-127">-DefaultProfile</span></span>
<span data-ttu-id="9fe5d-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe5d-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="9fe5d-129">-EnableBgp</span></span>
<span data-ttu-id="9fe5d-130">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="9fe5d-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="9fe5d-131">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="9fe5d-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="9fe5d-132">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="9fe5d-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="9fe5d-133">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="9fe5d-133">-IpSecPolicy</span></span>
<span data-ttu-id="9fe5d-134">Bu bağlantı tarafından, Mbps cinsinden işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fe5d-135">-Name</span></span>
<span data-ttu-id="9fe5d-136">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9fe5d-137">-ParentObject</span></span>
<span data-ttu-id="9fe5d-138">Bu bağlantı için üst VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-139">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="9fe5d-139">-ParentResourceId</span></span>
<span data-ttu-id="9fe5d-140">Bu bağlantı için üst VpnGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9fe5d-141">-ParentResourceName</span></span>
<span data-ttu-id="9fe5d-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe5d-143">-ResourceGroupName</span></span>
<span data-ttu-id="9fe5d-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9fe5d-145">-SharedKey</span></span>
<span data-ttu-id="9fe5d-146">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-146">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-147">-Uselocalazureıpaddress</span><span class="sxs-lookup"><span data-stu-id="9fe5d-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="9fe5d-148">Bağlantıyı başlatırken yerel Azure IP adresini kaynak adresi olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="9fe5d-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="9fe5d-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="9fe5d-150">Bu bağlantı için ilkeye dayalı trafik seçicileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="9fe5d-151">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="9fe5d-151">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="9fe5d-152">Ağ Geçidi bağlantı protokolü: IKEv1/Ikev2</span><span class="sxs-lookup"><span data-stu-id="9fe5d-152">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-153">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="9fe5d-153">-VpnSite</span></span>
<span data-ttu-id="9fe5d-154">Bu hub sanal ağ bağlantısının bağlı olduğu uzak VPN sitesi.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-154">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-155">-Vpnsitekimliği</span><span class="sxs-lookup"><span data-stu-id="9fe5d-155">-VpnSiteId</span></span>
<span data-ttu-id="9fe5d-156">Bu hub sanal ağ bağlantısının bağlı olduğu uzak VPN sitesi.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-157">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="9fe5d-157">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="9fe5d-158">Bu VpnConnection 'un sahip olduğu VpnSiteLinkConnections listesi.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-158">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe5d-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fe5d-159">-Confirm</span></span>
<span data-ttu-id="9fe5d-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe5d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe5d-161">-WhatIf</span></span>
<span data-ttu-id="9fe5d-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe5d-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe5d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe5d-164">CommonParameters</span></span>
<span data-ttu-id="9fe5d-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe5d-166">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9fe5d-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe5d-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fe5d-167">INPUTS</span></span>

### <span data-ttu-id="9fe5d-168">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9fe5d-168">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9fe5d-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe5d-169">System.String</span></span>

## <span data-ttu-id="9fe5d-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fe5d-170">OUTPUTS</span></span>

### <span data-ttu-id="9fe5d-171">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fe5d-171">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="9fe5d-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fe5d-172">NOTES</span></span>

## <span data-ttu-id="9fe5d-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fe5d-173">RELATED LINKS</span></span>

[<span data-ttu-id="9fe5d-174">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fe5d-174">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="9fe5d-175">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fe5d-175">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="9fe5d-176">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9fe5d-176">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
