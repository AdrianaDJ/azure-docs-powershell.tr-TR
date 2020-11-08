---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104511"
---
# <span data-ttu-id="6a4c2-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c2-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="6a4c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a4c2-103">VPN bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="6a4c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a4c2-104">SYNTAX</span></span>

### <span data-ttu-id="6a4c2-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a4c2-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a4c2-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="6a4c2-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a4c2-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6a4c2-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a4c2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a4c2-108">DESCRIPTION</span></span>
<span data-ttu-id="6a4c2-109">**Update-AzVpnConnection** cmdlet 'ı bir VPN bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="6a4c2-110">VPN bağlantısı, VPN ağ geçidini Azure 'da VPN sitesi olarak temsil edilen uzak bir şubeye bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="6a4c2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a4c2-111">EXAMPLES</span></span>

### <span data-ttu-id="6a4c2-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a4c2-112">Example 1</span></span>

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

<span data-ttu-id="6a4c2-113">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6a4c2-114">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6a4c2-115">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="6a4c2-116">Bağlantı daha sonra Set-AzVpnConnection komutu kullanılarak yeni bir Ipsecpolicy olacak şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="6a4c2-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6a4c2-117">Example 2</span></span>

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

<span data-ttu-id="6a4c2-118">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6a4c2-119">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6a4c2-120">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="6a4c2-121">Bağlantı daha sonra güvenli dize yapısı kullanılarak yeni bir paylaşılan anahtarla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="6a4c2-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a4c2-122">PARAMETERS</span></span>

### <span data-ttu-id="6a4c2-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="6a4c2-123">-AsJob</span></span>
<span data-ttu-id="6a4c2-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6a4c2-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a4c2-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="6a4c2-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="6a4c2-126">Bu bağlantı tarafından, Mbps cinsinden işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="6a4c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a4c2-127">-DefaultProfile</span></span>
<span data-ttu-id="6a4c2-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a4c2-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6a4c2-129">-EnableBgp</span></span>
<span data-ttu-id="6a4c2-130">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="6a4c2-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-131">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="6a4c2-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="6a4c2-132">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="6a4c2-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a4c2-133">-InputObject</span></span>
<span data-ttu-id="6a4c2-134">Güncelleştirilecek VpnConnection nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-135">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="6a4c2-135">-IpSecPolicy</span></span>
<span data-ttu-id="6a4c2-136">Bu bağlantı tarafından, Mbps cinsinden işlenmesi gereken bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="6a4c2-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a4c2-137">-Name</span></span>
<span data-ttu-id="6a4c2-138">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6a4c2-139">-ParentResourceName</span></span>
<span data-ttu-id="6a4c2-140">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a4c2-141">-ResourceGroupName</span></span>
<span data-ttu-id="6a4c2-142">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-143">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6a4c2-143">-ResourceId</span></span>
<span data-ttu-id="6a4c2-144">Silinecek VpnConnection nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6a4c2-145">-SharedKey</span></span>
<span data-ttu-id="6a4c2-146">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="6a4c2-147">-Uselocalazureıpaddress</span><span class="sxs-lookup"><span data-stu-id="6a4c2-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="6a4c2-148">Bağlantıyı başlatırken yerel Azure IP adresini kaynak adresi olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-148">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6a4c2-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6a4c2-150">Bu bağlantı için ilkeye dayalı trafik seçicileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-150">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a4c2-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c2-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="6a4c2-152">Bu VpnConnection 'un sahip olduğu VpnSiteLinkConnections 'ın listesi.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="6a4c2-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a4c2-153">-Confirm</span></span>
<span data-ttu-id="6a4c2-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a4c2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a4c2-155">-WhatIf</span></span>
<span data-ttu-id="6a4c2-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a4c2-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a4c2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a4c2-158">CommonParameters</span></span>
<span data-ttu-id="6a4c2-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a4c2-160">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6a4c2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a4c2-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a4c2-161">INPUTS</span></span>

### <span data-ttu-id="6a4c2-162">System. String</span><span class="sxs-lookup"><span data-stu-id="6a4c2-162">System.String</span></span>

### <span data-ttu-id="6a4c2-163">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c2-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="6a4c2-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a4c2-164">OUTPUTS</span></span>

### <span data-ttu-id="6a4c2-165">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c2-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="6a4c2-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a4c2-166">NOTES</span></span>

## <span data-ttu-id="6a4c2-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a4c2-167">RELATED LINKS</span></span>

[<span data-ttu-id="6a4c2-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c2-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="6a4c2-169">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="6a4c2-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="6a4c2-170">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6a4c2-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
