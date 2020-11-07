---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759922"
---
# <span data-ttu-id="4bdf6-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bdf6-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="4bdf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bdf6-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdf6-103">VPN bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="4bdf6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bdf6-104">SYNTAX</span></span>

### <span data-ttu-id="4bdf6-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bdf6-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bdf6-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="4bdf6-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdf6-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4bdf6-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdf6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bdf6-108">DESCRIPTION</span></span>
<span data-ttu-id="4bdf6-109">**Update-AzVpnConnection** cmdlet 'ı bir VPN bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="4bdf6-110">VPN bağlantısı, VPN ağ geçidini Azure 'da VPN sitesi olarak temsil edilen uzak bir şubeye bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="4bdf6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bdf6-111">EXAMPLES</span></span>

### <span data-ttu-id="4bdf6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bdf6-112">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="4bdf6-113">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4bdf6-114">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4bdf6-115">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="4bdf6-116">Bağlantı daha sonra Set-AzVpnConnection komutu kullanılarak yeni bir Ipsecpolicy olacak şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="4bdf6-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4bdf6-117">Example 2</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="4bdf6-118">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4bdf6-119">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4bdf6-120">Ağ Geçidi oluşturulduktan sonra, New-AzVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="4bdf6-121">Bağlantı daha sonra güvenli dize yapısı kullanılarak yeni bir paylaşılan anahtarla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="4bdf6-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bdf6-122">PARAMETERS</span></span>

### <span data-ttu-id="4bdf6-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="4bdf6-123">-AsJob</span></span>
<span data-ttu-id="4bdf6-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4bdf6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bdf6-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="4bdf6-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="4bdf6-126">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="4bdf6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdf6-127">-DefaultProfile</span></span>
<span data-ttu-id="4bdf6-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdf6-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="4bdf6-129">-EnableBgp</span></span>
<span data-ttu-id="4bdf6-130">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4bdf6-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="4bdf6-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bdf6-131">-InputObject</span></span>
<span data-ttu-id="4bdf6-132">Güncelleştirilecek VpnConenction nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-132">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="4bdf6-133">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="4bdf6-133">-IpSecPolicy</span></span>
<span data-ttu-id="4bdf6-134">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="4bdf6-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bdf6-135">-Name</span></span>
<span data-ttu-id="4bdf6-136">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-136">The resource name.</span></span>

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

### <span data-ttu-id="4bdf6-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4bdf6-137">-ParentResourceName</span></span>
<span data-ttu-id="4bdf6-138">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-138">The parent resource name.</span></span>

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

### <span data-ttu-id="4bdf6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdf6-139">-ResourceGroupName</span></span>
<span data-ttu-id="4bdf6-140">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-140">The resource group name.</span></span>

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

### <span data-ttu-id="4bdf6-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4bdf6-141">-ResourceId</span></span>
<span data-ttu-id="4bdf6-142">Silinecek VpnConenction nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-142">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="4bdf6-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4bdf6-143">-SharedKey</span></span>
<span data-ttu-id="4bdf6-144">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="4bdf6-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bdf6-145">-Confirm</span></span>
<span data-ttu-id="4bdf6-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bdf6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdf6-147">-WhatIf</span></span>
<span data-ttu-id="4bdf6-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bdf6-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bdf6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdf6-150">CommonParameters</span></span>
<span data-ttu-id="4bdf6-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bdf6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdf6-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bdf6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdf6-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bdf6-153">INPUTS</span></span>

### <span data-ttu-id="4bdf6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4bdf6-154">System.String</span></span>

### <span data-ttu-id="4bdf6-155">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bdf6-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="4bdf6-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bdf6-156">OUTPUTS</span></span>

### <span data-ttu-id="4bdf6-157">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bdf6-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="4bdf6-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bdf6-158">NOTES</span></span>

## <span data-ttu-id="4bdf6-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bdf6-159">RELATED LINKS</span></span>

[<span data-ttu-id="4bdf6-160">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bdf6-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="4bdf6-161">Yeni-Azvpnbağlantısı</span><span class="sxs-lookup"><span data-stu-id="4bdf6-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="4bdf6-162">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bdf6-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)