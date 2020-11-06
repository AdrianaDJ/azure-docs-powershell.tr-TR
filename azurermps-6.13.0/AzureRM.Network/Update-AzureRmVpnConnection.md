---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590124"
---
# <span data-ttu-id="1107f-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1107f-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="1107f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1107f-102">SYNOPSIS</span></span>
<span data-ttu-id="1107f-103">Bir VpnConnection nesnesini hedef duruma güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1107f-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1107f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1107f-104">SYNTAX</span></span>

### <span data-ttu-id="1107f-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1107f-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1107f-106">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="1107f-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1107f-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="1107f-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1107f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1107f-108">DESCRIPTION</span></span>
<span data-ttu-id="1107f-109">Bir VpnGateway 'i bir VpnSite olarak RM 'de gösterilen bir uzak müşteri dalında bağlayan bir IPSec bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1107f-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="1107f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1107f-110">EXAMPLES</span></span>

### <span data-ttu-id="1107f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1107f-111">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="1107f-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1107f-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1107f-113">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1107f-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="1107f-114">Ağ Geçidi oluşturulduktan sonra, New-AzureRmVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="1107f-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="1107f-115">Bağlantı daha sonra Set-AzureRmVpnConnection komutu kullanılarak yeni bir Ipsecpolicy olacak şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1107f-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="1107f-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1107f-116">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="1107f-117">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir VpnSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1107f-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1107f-118">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1107f-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="1107f-119">Ağ Geçidi oluşturulduktan sonra, New-AzureRmVpnConnection komutunu kullanarak VpnSite 'ye bağlanır.</span><span class="sxs-lookup"><span data-stu-id="1107f-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="1107f-120">Bağlantı daha sonra güvenli dize yapısı kullanılarak yeni bir paylaşılan anahtarla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1107f-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="1107f-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1107f-121">PARAMETERS</span></span>

### <span data-ttu-id="1107f-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="1107f-122">-AsJob</span></span>
<span data-ttu-id="1107f-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1107f-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1107f-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="1107f-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="1107f-125">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="1107f-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="1107f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1107f-126">-DefaultProfile</span></span>
<span data-ttu-id="1107f-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1107f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1107f-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="1107f-128">-EnableBgp</span></span>
<span data-ttu-id="1107f-129">Bu bağlantı için BGP 'yi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="1107f-129">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="1107f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1107f-130">-InputObject</span></span>
<span data-ttu-id="1107f-131">Güncelleştirilecek VpnConenction nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1107f-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="1107f-132">-Ipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="1107f-132">-IpSecPolicy</span></span>
<span data-ttu-id="1107f-133">Bu bağlantı tarafından, Mbps 'de işlenmesi gereken bant.</span><span class="sxs-lookup"><span data-stu-id="1107f-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="1107f-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="1107f-134">-Name</span></span>
<span data-ttu-id="1107f-135">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1107f-135">The resource name.</span></span>

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

### <span data-ttu-id="1107f-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="1107f-136">-ParentResourceName</span></span>
<span data-ttu-id="1107f-137">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1107f-137">The parent resource name.</span></span>

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

### <span data-ttu-id="1107f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1107f-138">-ResourceGroupName</span></span>
<span data-ttu-id="1107f-139">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1107f-139">The resource group name.</span></span>

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

### <span data-ttu-id="1107f-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1107f-140">-ResourceId</span></span>
<span data-ttu-id="1107f-141">Silinecek VpnConenction nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1107f-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="1107f-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1107f-142">-SharedKey</span></span>
<span data-ttu-id="1107f-143">Bu bağlantıyı ayarlamak için paylaşılan anahtar.</span><span class="sxs-lookup"><span data-stu-id="1107f-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="1107f-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="1107f-144">-Confirm</span></span>
<span data-ttu-id="1107f-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1107f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1107f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1107f-146">-WhatIf</span></span>
<span data-ttu-id="1107f-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1107f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1107f-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1107f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1107f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1107f-149">CommonParameters</span></span>
<span data-ttu-id="1107f-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1107f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1107f-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1107f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1107f-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1107f-152">INPUTS</span></span>

### <span data-ttu-id="1107f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1107f-153">System.String</span></span>

### <span data-ttu-id="1107f-154">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1107f-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="1107f-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1107f-155">OUTPUTS</span></span>

### <span data-ttu-id="1107f-156">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1107f-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="1107f-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1107f-157">NOTES</span></span>

## <span data-ttu-id="1107f-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1107f-158">RELATED LINKS</span></span>
