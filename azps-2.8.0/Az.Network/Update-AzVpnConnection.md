---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a0e7775a85196a7a3ba709f284b58e57c46c4cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932686"
---
# <span data-ttu-id="19e34-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="19e34-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="19e34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19e34-102">SYNOPSIS</span></span>
<span data-ttu-id="19e34-103">VPN bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19e34-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="19e34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19e34-104">SYNTAX</span></span>

### <span data-ttu-id="19e34-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19e34-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19e34-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="19e34-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19e34-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="19e34-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19e34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="19e34-108">DESCRIPTION</span></span>
<span data-ttu-id="19e34-109">**Update-AzVpnConnection** cmdlet 'ı bir VPN bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19e34-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="19e34-110">VPN bağlantısı, VPN ağ geçidini Azure 'da VPN sitesi olarak temsil edilen uzak bir şubeye bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19e34-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="19e34-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19e34-111">EXAMPLES</span></span>

### <span data-ttu-id="19e34-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19e34-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="19e34-113">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19e34-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="19e34-114">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="19e34-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="19e34-115">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="19e34-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="19e34-116">Bağlantı daha sonra Set-AzVpnConnection komutu kullanılarak yeni bir Ipsecpolicy olacak şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="19e34-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="19e34-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="19e34-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="19e34-118">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19e34-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="19e34-119">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="19e34-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="19e34-120">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="19e34-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="19e34-121">Bağlantı daha sonra güvenli dize yapısı kullanılarak yeni bir paylaşılan anahtarla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="19e34-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="19e34-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19e34-122">PARAMETERS</span></span>

### <span data-ttu-id="19e34-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="19e34-123">-AsJob</span></span>
<span data-ttu-id="19e34-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="19e34-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19e34-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="19e34-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="19e34-126">Bu bağlantı tarafından, Mbps cinsinden işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="19e34-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="19e34-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e34-127">-DefaultProfile</span></span>
<span data-ttu-id="19e34-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19e34-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e34-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="19e34-129">-EnableBgp</span></span>
<span data-ttu-id="19e34-130">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="19e34-130">Enable BGP for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19e34-131">-InputObject</span></span>
<span data-ttu-id="19e34-132">Güncelleştirilecek VpnConnection nesnesi.</span><span class="sxs-lookup"><span data-stu-id="19e34-132">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-133">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="19e34-133">-IpSecPolicy</span></span>
<span data-ttu-id="19e34-134">Bu bağlantı tarafından, Mbps cinsinden işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="19e34-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="19e34-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="19e34-135">-Name</span></span>
<span data-ttu-id="19e34-136">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="19e34-136">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="19e34-137">-ParentResourceName</span></span>
<span data-ttu-id="19e34-138">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="19e34-138">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e34-139">-ResourceGroupName</span></span>
<span data-ttu-id="19e34-140">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="19e34-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="19e34-141">-ResourceId</span></span>
<span data-ttu-id="19e34-142">Silinecek VpnConnection nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="19e34-142">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="19e34-143">-SharedKey</span></span>
<span data-ttu-id="19e34-144">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="19e34-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="19e34-145">-Uselocalazureıpaddress</span><span class="sxs-lookup"><span data-stu-id="19e34-145">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="19e34-146">Bağlantıyı başlatırken yerel Azure IP adresini kaynak adresi olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="19e34-146">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-147">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="19e34-147">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="19e34-148">Bu bağlantı için ilkeye dayalı trafik seçicileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="19e34-148">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-149">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="19e34-149">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="19e34-150">Bu VpnConnection 'un sahip olduğu VpnSiteLinkConnections 'ın listesi.</span><span class="sxs-lookup"><span data-stu-id="19e34-150">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e34-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="19e34-151">-Confirm</span></span>
<span data-ttu-id="19e34-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19e34-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e34-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e34-153">-WhatIf</span></span>
<span data-ttu-id="19e34-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19e34-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19e34-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19e34-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e34-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e34-156">CommonParameters</span></span>
<span data-ttu-id="19e34-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19e34-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e34-158">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="19e34-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e34-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19e34-159">INPUTS</span></span>

### <span data-ttu-id="19e34-160">System. String</span><span class="sxs-lookup"><span data-stu-id="19e34-160">System.String</span></span>

### <span data-ttu-id="19e34-161">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="19e34-161">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="19e34-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19e34-162">OUTPUTS</span></span>

### <span data-ttu-id="19e34-163">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="19e34-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="19e34-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19e34-164">NOTES</span></span>

## <span data-ttu-id="19e34-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19e34-165">RELATED LINKS</span></span>

[<span data-ttu-id="19e34-166">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="19e34-166">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="19e34-167">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="19e34-167">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="19e34-168">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="19e34-168">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)