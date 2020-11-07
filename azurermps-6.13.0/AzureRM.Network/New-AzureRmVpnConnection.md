---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
ms.openlocfilehash: 8b7d0845e6a8fce2d6c496573a493dfd187c34af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764339"
---
# <span data-ttu-id="c18d4-101">New-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c18d4-101">New-AzureRmVpnConnection</span></span>

## <span data-ttu-id="c18d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c18d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c18d4-103">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c18d4-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c18d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c18d4-104">SYNTAX</span></span>

### <span data-ttu-id="c18d4-105">Byvpngatewaynamebyvpnsitenesnesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c18d4-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c18d4-106">Byvpngatewaynamebyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="c18d4-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSiteId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c18d4-107">Byvpngatewayobjectbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="c18d4-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c18d4-108">Byvpngatewayobjectbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="c18d4-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c18d4-109">Byvpngatewayresourceıdbyvpnsitenesnesi</span><span class="sxs-lookup"><span data-stu-id="c18d4-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c18d4-110">Byvpngatewayresourceıdbyvpnsiteresourceıd</span><span class="sxs-lookup"><span data-stu-id="c18d4-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c18d4-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c18d4-111">DESCRIPTION</span></span>
<span data-ttu-id="c18d4-112">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c18d4-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="c18d4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c18d4-113">EXAMPLES</span></span>

### <span data-ttu-id="c18d4-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c18d4-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

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

<span data-ttu-id="c18d4-115">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c18d4-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c18d4-116">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c18d4-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c18d4-117">Ağ Geçidi oluşturulduktan sonra, New-AzureRmVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="c18d4-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="c18d4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c18d4-118">PARAMETERS</span></span>

### <span data-ttu-id="c18d4-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="c18d4-119">-AsJob</span></span>
<span data-ttu-id="c18d4-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c18d4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c18d4-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="c18d4-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="c18d4-122">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="c18d4-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="c18d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18d4-123">-DefaultProfile</span></span>
<span data-ttu-id="c18d4-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c18d4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c18d4-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c18d4-125">-EnableBgp</span></span>
<span data-ttu-id="c18d4-126">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="c18d4-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="c18d4-127">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="c18d4-127">-IpSecPolicy</span></span>
<span data-ttu-id="c18d4-128">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="c18d4-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="c18d4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="c18d4-129">-Name</span></span>
<span data-ttu-id="c18d4-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c18d4-130">The resource name.</span></span>

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

### <span data-ttu-id="c18d4-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c18d4-131">-ParentObject</span></span>
<span data-ttu-id="c18d4-132">Bu bağlantı için üst VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c18d4-132">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="c18d4-133">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="c18d4-133">-ParentResourceId</span></span>
<span data-ttu-id="c18d4-134">Bu bağlantı için üst VpnGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c18d4-134">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="c18d4-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c18d4-135">-ParentResourceName</span></span>
<span data-ttu-id="c18d4-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c18d4-136">The resource group name.</span></span>

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

### <span data-ttu-id="c18d4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c18d4-137">-ResourceGroupName</span></span>
<span data-ttu-id="c18d4-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c18d4-138">The resource group name.</span></span>

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

### <span data-ttu-id="c18d4-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c18d4-139">-SharedKey</span></span>
<span data-ttu-id="c18d4-140">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="c18d4-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="c18d4-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="c18d4-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="c18d4-142">Ağ Geçidi bağlantı protokolü: IKEv1/Ikev2</span><span class="sxs-lookup"><span data-stu-id="c18d4-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="c18d4-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c18d4-143">-VpnSite</span></span>
<span data-ttu-id="c18d4-144">Bu hub sanal ağ bağlantısının bağlı olduğu uzak VPN sitesi.</span><span class="sxs-lookup"><span data-stu-id="c18d4-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="c18d4-145">-Vpnsitekimliği</span><span class="sxs-lookup"><span data-stu-id="c18d4-145">-VpnSiteId</span></span>
<span data-ttu-id="c18d4-146">Bu hub sanal ağ bağlantısının bağlı olduğu uzak VPN sitesi.</span><span class="sxs-lookup"><span data-stu-id="c18d4-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="c18d4-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="c18d4-147">-Confirm</span></span>
<span data-ttu-id="c18d4-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c18d4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c18d4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c18d4-149">-WhatIf</span></span>
<span data-ttu-id="c18d4-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c18d4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c18d4-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c18d4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c18d4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18d4-152">CommonParameters</span></span>
<span data-ttu-id="c18d4-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c18d4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18d4-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c18d4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18d4-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c18d4-155">INPUTS</span></span>

### <span data-ttu-id="c18d4-156">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c18d4-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c18d4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c18d4-157">System.String</span></span>

## <span data-ttu-id="c18d4-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c18d4-158">OUTPUTS</span></span>

### <span data-ttu-id="c18d4-159">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c18d4-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c18d4-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c18d4-160">NOTES</span></span>

## <span data-ttu-id="c18d4-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c18d4-161">RELATED LINKS</span></span>
