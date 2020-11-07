---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932737"
---
# <span data-ttu-id="a310a-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a310a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a310a-102">SYNOPSIS</span></span>
<span data-ttu-id="a310a-103">Sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a310a-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="a310a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a310a-104">SYNTAX</span></span>

### <span data-ttu-id="a310a-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a310a-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a310a-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="a310a-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a310a-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="a310a-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a310a-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a310a-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a310a-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="a310a-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a310a-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a310a-110">DESCRIPTION</span></span>
<span data-ttu-id="a310a-111">**Set-AzVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a310a-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="a310a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a310a-112">EXAMPLES</span></span>

### <span data-ttu-id="a310a-113">Örnek 1: sanal ağ geçidinin ASN 'yi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a310a-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="a310a-114">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır $Gateway ve ikinci komut $Gateway değişken bir şekilde depolanan sanal ağ ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a310a-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="a310a-115">Komut ayrıca ASN 'yi 1337 'e ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a310a-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="a310a-116">Örnek 2: sanal ağ ağ geçidine IPSec ilkesi ekleme</span><span class="sxs-lookup"><span data-stu-id="a310a-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="a310a-117">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır ve bu değeri $Gateway ikinci komut, belirtilen IPSec parametreleri için VPN IPSec ilke nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a310a-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="a310a-118">Üçüncü komut, $Gateway değişkeninde depolanan sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a310a-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="a310a-119">Komut ayrıca sanal ağ geçidinde $vpnclientipsecpolicy nesnesinde belirtilen özel VPN IPSec ilkesini de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a310a-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="a310a-120">Örnek 3: var olan sanal ağ ağ geçidine etiket ekleme/güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a310a-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="a310a-121">İlk komut, Gateway01 adında, kaynak grubuna ait ResourceGroup001 adlı bir sanal ağ geçidi alır ve bu değeri $Gateway ikinci komut @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} etiketli sanal ağ geçidi Gateway01 güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a310a-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="a310a-122">Örnek 4: var olan sanal ağ ağ geçidinin VpnClient için AAD kimlik doğrulama yapılandırmasını ekleme/güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a310a-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="a310a-123">İlk komut, Gateway01 adında, kaynak grubuna ait ResourceGroup001 adlı bir sanal ağ geçidi alır ve bu değeri $Gateway ikinci komut, sanal ağ geçidi Gateway01 için AAD kimlik doğrulaması yapılandırma params: aadtenanturi, aadaudienceıd, aadıssuturi, aadaudienceıd, aadıssuturi, aadaudi</span><span class="sxs-lookup"><span data-stu-id="a310a-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="a310a-124">Üçüncü komut, AAD kimlik doğrulama yapılandırmasını sanal ağ geçidinin Vpnistemcisinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a310a-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="a310a-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a310a-125">PARAMETERS</span></span>

### <span data-ttu-id="a310a-126">-Aadaudienceıd</span><span class="sxs-lookup"><span data-stu-id="a310a-126">-AadAudienceId</span></span>
<span data-ttu-id="a310a-127">P2S AAD kimlik doğrulama seçeneği: Aadaudienceıd.</span><span class="sxs-lookup"><span data-stu-id="a310a-127">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-128">-Aadıssueruri</span><span class="sxs-lookup"><span data-stu-id="a310a-128">-AadIssuerUri</span></span>
<span data-ttu-id="a310a-129">P2S AAD kimlik doğrulama seçeneği: Aadıssueruri.</span><span class="sxs-lookup"><span data-stu-id="a310a-129">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="a310a-130">-AadTenantUri</span></span>
<span data-ttu-id="a310a-131">P2S AAD kimlik doğrulama seçeneği: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="a310a-131">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-132">-Iş</span><span class="sxs-lookup"><span data-stu-id="a310a-132">-AsJob</span></span>
<span data-ttu-id="a310a-133">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a310a-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a310a-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="a310a-134">-Asn</span></span>
<span data-ttu-id="a310a-135">IPSec tünellerinin içindeki Sınır Ağ Geçidi Protokolü (BGP) oturumlarını ayarlamak için kullanılan sanal ağ geçidi otonom sistem numarasını (ASN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="a310a-136">-CustomRoute</span></span>
<span data-ttu-id="a310a-137">Müşteri tarafından belirtilen özel rotalar adres havuzu</span><span class="sxs-lookup"><span data-stu-id="a310a-137">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a310a-138">-DefaultProfile</span></span>
<span data-ttu-id="a310a-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a310a-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a310a-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a310a-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="a310a-141">Etkin özelliği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a310a-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="a310a-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a310a-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="a310a-143">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="a310a-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="a310a-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a310a-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="a310a-145">Zorla tünel için kullanılacak varsayılan siteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="a310a-146">Varsayılan bir site belirtilmişse, ağ geçidinin sanal özel ağından (VPN) tüm internet trafiği bu siteye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="a310a-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a310a-147">-GatewaySku</span></span>
<span data-ttu-id="a310a-148">Sanal ağ geçidi 'nin hisse senedi birimini (SKU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="a310a-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a310a-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a310a-150">Ana</span><span class="sxs-lookup"><span data-stu-id="a310a-150">Basic</span></span>
- <span data-ttu-id="a310a-151">Ardından</span><span class="sxs-lookup"><span data-stu-id="a310a-151">Standard</span></span>
- <span data-ttu-id="a310a-152">Üst performans</span><span class="sxs-lookup"><span data-stu-id="a310a-152">HighPerformance</span></span>
- <span data-ttu-id="a310a-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="a310a-153">VpnGw1</span></span>
- <span data-ttu-id="a310a-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="a310a-154">VpnGw2</span></span>
- <span data-ttu-id="a310a-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="a310a-155">VpnGw3</span></span>
- <span data-ttu-id="a310a-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="a310a-156">VpnGw1AZ</span></span>
- <span data-ttu-id="a310a-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="a310a-157">VpnGw2AZ</span></span>
- <span data-ttu-id="a310a-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="a310a-158">VpnGw3AZ</span></span>
- <span data-ttu-id="a310a-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="a310a-159">ErGw1AZ</span></span>
- <span data-ttu-id="a310a-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="a310a-160">ErGw2AZ</span></span>
- <span data-ttu-id="a310a-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="a310a-161">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a310a-162">-PeerWeight</span></span>
<span data-ttu-id="a310a-163">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara eklenecek ağırlığı belirtir</span><span class="sxs-lookup"><span data-stu-id="a310a-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a310a-164">-RadiusServerAddress</span></span>
<span data-ttu-id="a310a-165">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="a310a-165">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a310a-166">-RadiusServerSecret</span></span>
<span data-ttu-id="a310a-167">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="a310a-167">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a310a-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="a310a-169">P2S istemcisinin AAD kimlik doğrulamasını sanal ağ ağ geçidinden kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="a310a-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="a310a-170">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a310a-170">-Tag</span></span>
<span data-ttu-id="a310a-171">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="a310a-171">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a310a-173">Değişikliklerin temel aldığı sanal ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="a310a-174">Sanal ağ geçidi nesnesini almak için Get-AzVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a310a-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a310a-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="a310a-176">Bu cmdlet 'in VPN istemci IP adreslerini ayırmak için kullandığı adres alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="a310a-177">Bu, sanal ağ veya şirket içi aralıklardaki çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a310a-177">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-178">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="a310a-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a310a-179">P2S VPN istemcisi tünel protokollerinin IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="a310a-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="a310a-180">-VpnClientProtocol</span></span>
<span data-ttu-id="a310a-181">P2S VPN istemci tünel protokollerinin listesi</span><span class="sxs-lookup"><span data-stu-id="a310a-181">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-182">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="a310a-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="a310a-183">İptal edilen VPN istemci sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="a310a-184">Bunlardan biriyle eşleşen bir sertifika sunan VPN istemcisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a310a-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="a310a-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="a310a-186">VPN istemci kimlik doğrulaması için kullanılacak VPN istemcisi kök sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a310a-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="a310a-187">VPN istemcilerinin bağlanması, bu kök sertifikalardan birinden üretilmiş sertifikaları sunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a310a-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a310a-188">-Onay</span><span class="sxs-lookup"><span data-stu-id="a310a-188">-Confirm</span></span>
<span data-ttu-id="a310a-189">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a310a-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a310a-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a310a-190">-WhatIf</span></span>
<span data-ttu-id="a310a-191">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a310a-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a310a-192">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a310a-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a310a-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a310a-193">CommonParameters</span></span>
<span data-ttu-id="a310a-194">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a310a-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a310a-195">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a310a-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a310a-196">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a310a-196">INPUTS</span></span>

### <span data-ttu-id="a310a-197">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a310a-198">System. String</span><span class="sxs-lookup"><span data-stu-id="a310a-198">System.String</span></span>

### <span data-ttu-id="a310a-199">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="a310a-200">System. String []</span><span class="sxs-lookup"><span data-stu-id="a310a-200">System.String[]</span></span>

### <span data-ttu-id="a310a-201">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="a310a-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="a310a-202">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifika []</span><span class="sxs-lookup"><span data-stu-id="a310a-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="a310a-203">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a310a-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="a310a-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="a310a-204">System.UInt32</span></span>

### <span data-ttu-id="a310a-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a310a-205">System.Int32</span></span>

### <span data-ttu-id="a310a-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a310a-206">System.Security.SecureString</span></span>

## <span data-ttu-id="a310a-207">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a310a-207">OUTPUTS</span></span>

### <span data-ttu-id="a310a-208">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a310a-209">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a310a-209">NOTES</span></span>
* <span data-ttu-id="a310a-210">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="a310a-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a310a-211">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a310a-211">RELATED LINKS</span></span>

[<span data-ttu-id="a310a-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a310a-213">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a310a-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a310a-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a310a-216">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a310a-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
