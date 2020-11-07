---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 750af3bf948345a22c7cb7a86b09e07d4e266f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760242"
---
# <span data-ttu-id="b4612-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4612-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="b4612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4612-102">SYNOPSIS</span></span>
<span data-ttu-id="b4612-103">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4612-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="b4612-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4612-104">SYNTAX</span></span>

### <span data-ttu-id="b4612-105">Byvpngatewaynamebyvpnsitenesnesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4612-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4612-106">Byvpngatewaynamebyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4612-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4612-107">Byvpngatewayobjectbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="b4612-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4612-108">Byvpngatewayobjectbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4612-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4612-109">Byvpngatewayresourceıdbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="b4612-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4612-110">Byvpngatewayresourceıdbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4612-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4612-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4612-111">DESCRIPTION</span></span>
<span data-ttu-id="b4612-112">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4612-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="b4612-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4612-113">EXAMPLES</span></span>

### <span data-ttu-id="b4612-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4612-114">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="b4612-115">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4612-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b4612-116">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4612-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b4612-117">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="b4612-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="b4612-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4612-118">PARAMETERS</span></span>

### <span data-ttu-id="b4612-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="b4612-119">-AsJob</span></span>
<span data-ttu-id="b4612-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b4612-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4612-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b4612-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="b4612-122">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="b4612-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="b4612-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4612-123">-DefaultProfile</span></span>
<span data-ttu-id="b4612-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4612-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4612-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b4612-125">-EnableBgp</span></span>
<span data-ttu-id="b4612-126">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="b4612-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="b4612-127">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="b4612-127">-IpSecPolicy</span></span>
<span data-ttu-id="b4612-128">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="b4612-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4612-129">-Name</span></span>
<span data-ttu-id="b4612-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b4612-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4612-131">-ParentObject</span></span>
<span data-ttu-id="b4612-132">Bu bağlantı için üst VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b4612-132">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-133">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4612-133">-ParentResourceId</span></span>
<span data-ttu-id="b4612-134">Bu bağlantı için üst VpnGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b4612-134">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b4612-135">-ParentResourceName</span></span>
<span data-ttu-id="b4612-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4612-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4612-137">-ResourceGroupName</span></span>
<span data-ttu-id="b4612-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4612-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b4612-139">-SharedKey</span></span>
<span data-ttu-id="b4612-140">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="b4612-140">The shared key required to set this connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="b4612-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="b4612-142">Ağ Geçidi bağlantı protokolü: IKEv1/Ikev2</span><span class="sxs-lookup"><span data-stu-id="b4612-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b4612-143">-VpnSite</span></span>
<span data-ttu-id="b4612-144">Bu hub sanal ağ bağlantısının bağlı olduğu uzak VPN sitesi.</span><span class="sxs-lookup"><span data-stu-id="b4612-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-145">-Vpnsitekimliği</span><span class="sxs-lookup"><span data-stu-id="b4612-145">-VpnSiteId</span></span>
<span data-ttu-id="b4612-146">Bu hub sanal ağ bağlantısının bağlı olduğu uzak VPN sitesi.</span><span class="sxs-lookup"><span data-stu-id="b4612-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4612-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4612-147">-Confirm</span></span>
<span data-ttu-id="b4612-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4612-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4612-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4612-149">-WhatIf</span></span>
<span data-ttu-id="b4612-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4612-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4612-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4612-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4612-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4612-152">CommonParameters</span></span>
<span data-ttu-id="b4612-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4612-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4612-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4612-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4612-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4612-155">INPUTS</span></span>

### <span data-ttu-id="b4612-156">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b4612-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="b4612-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b4612-157">System.String</span></span>

## <span data-ttu-id="b4612-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4612-158">OUTPUTS</span></span>

### <span data-ttu-id="b4612-159">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4612-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="b4612-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4612-160">NOTES</span></span>

## <span data-ttu-id="b4612-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4612-161">RELATED LINKS</span></span>

[<span data-ttu-id="b4612-162">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4612-162">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="b4612-163">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4612-163">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="b4612-164">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b4612-164">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
