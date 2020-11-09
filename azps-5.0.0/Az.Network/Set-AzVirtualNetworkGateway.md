---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325222"
---
# <span data-ttu-id="2b940-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b940-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="2b940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b940-102">SYNOPSIS</span></span>
<span data-ttu-id="2b940-103">Sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b940-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="2b940-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b940-104">SYNTAX</span></span>

### <span data-ttu-id="2b940-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b940-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b940-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="2b940-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b940-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="2b940-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b940-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b940-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b940-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b940-109">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b940-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="2b940-110">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b940-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b940-111">DESCRIPTION</span></span>
<span data-ttu-id="2b940-112">**Set-AzVirtualNetworkGateway** cmdlet 'i sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b940-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="2b940-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b940-113">EXAMPLES</span></span>

### <span data-ttu-id="2b940-114">Örnek 1: sanal ağ geçidinin ASN 'yi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b940-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="2b940-115">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır $Gateway ve ikinci komut $Gateway değişken bir şekilde depolanan sanal ağ ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b940-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="2b940-116">Komut ayrıca ASN 'yi 1337 'e ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2b940-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="2b940-117">Örnek 2: sanal ağ ağ geçidine IPSec ilkesi ekleme</span><span class="sxs-lookup"><span data-stu-id="2b940-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="2b940-118">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır ve bu değeri $Gateway ikinci komut, belirtilen IPSec parametreleri için VPN IPSec ilke nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b940-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="2b940-119">Üçüncü komut, $Gateway değişkeninde depolanan sanal ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b940-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="2b940-120">Komut ayrıca sanal ağ geçidinde $vpnclientipsecpolicy nesnesinde belirtilen özel VPN IPSec ilkesini de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2b940-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="2b940-121">Örnek 3: var olan sanal ağ ağ geçidine etiket ekleme/güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b940-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="2b940-122">İlk komut, Gateway01 adında, kaynak grubuna ait ResourceGroup001 adlı bir sanal ağ geçidi alır ve bu değeri $Gateway ikinci komut @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} etiketli sanal ağ geçidi Gateway01 güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2b940-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="2b940-123">Örnek 4: var olan sanal ağ ağ geçidinin VpnClient için AAD kimlik doğrulama yapılandırmasını ekleme/güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b940-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="2b940-124">İlk komut, Gateway01 adında, kaynak grubuna ait ResourceGroup001 adlı bir sanal ağ geçidi alır ve bu değeri $Gateway ikinci komut, sanal ağ geçidi Gateway01 için AAD kimlik doğrulaması yapılandırma params: aadtenanturi, aadaudienceıd, aadıssuturi, aadaudienceıd, aadıssuturi, aadaudi</span><span class="sxs-lookup"><span data-stu-id="2b940-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="2b940-125">Üçüncü komut, AAD kimlik doğrulama yapılandırmasını sanal ağ geçidinin Vpnistemcisinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2b940-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="2b940-126">Örnek 5: var olan sanal ağ ağ geçidine ıpconfigurationbgppeeringadresleri ekleme/güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b940-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
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
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="2b940-127">İlk komut, Gateway01 adlı bir sanal ağ ağ geçidini kaynak grubuna ait ResourceGroup001 alır ve $Gateway ikinci komut, sanal ağ geçidi Gateway01</span><span class="sxs-lookup"><span data-stu-id="2b940-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="2b940-128">Üçüncü komut addresslist1 adresine bir adres listesi atar.</span><span class="sxs-lookup"><span data-stu-id="2b940-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="2b940-129">Dördüncü komut bir PSIpConfigurationBgpPeeringAddress nesnesi oluşturdu.</span><span class="sxs-lookup"><span data-stu-id="2b940-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="2b940-130">Beşinci komut bu yeni oluşturulan Psıpconfigurationbgppeeringaddress 'yi ıpconfigurationbgppeeringaddresses olarak ayarladı ve ağ geçidini güncelleyebilirim.</span><span class="sxs-lookup"><span data-stu-id="2b940-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="2b940-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b940-131">PARAMETERS</span></span>

### <span data-ttu-id="2b940-132">-Aadaudienceıd</span><span class="sxs-lookup"><span data-stu-id="2b940-132">-AadAudienceId</span></span>
<span data-ttu-id="2b940-133">P2S AAD kimlik doğrulama seçeneği: Aadaudienceıd.</span><span class="sxs-lookup"><span data-stu-id="2b940-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="2b940-134">-Aadıssueruri</span><span class="sxs-lookup"><span data-stu-id="2b940-134">-AadIssuerUri</span></span>
<span data-ttu-id="2b940-135">P2S AAD kimlik doğrulama seçeneği: Aadıssueruri.</span><span class="sxs-lookup"><span data-stu-id="2b940-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="2b940-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="2b940-136">-AadTenantUri</span></span>
<span data-ttu-id="2b940-137">P2S AAD kimlik doğrulama seçeneği: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="2b940-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="2b940-138">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b940-138">-AsJob</span></span>
<span data-ttu-id="2b940-139">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b940-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b940-140">-ASN</span><span class="sxs-lookup"><span data-stu-id="2b940-140">-Asn</span></span>
<span data-ttu-id="2b940-141">IPSec tünellerinin içinde BGP oturumlarını ayarlamak için kullanılan sanal ağ geçidinin ASN</span><span class="sxs-lookup"><span data-stu-id="2b940-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="2b940-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="2b940-142">-CustomRoute</span></span>
<span data-ttu-id="2b940-143">Müşteri tarafından belirtilen özel rotalar adres havuzu</span><span class="sxs-lookup"><span data-stu-id="2b940-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="2b940-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b940-144">-DefaultProfile</span></span>
<span data-ttu-id="2b940-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b940-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b940-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="2b940-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="2b940-147">Sanal ağ geçidinde etkin etkin özelliği devre dışı bırakma bayrağı</span><span class="sxs-lookup"><span data-stu-id="2b940-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="2b940-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="2b940-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="2b940-149">Sanal ağ geçidinde etkin etkin özelliği etkinleştirme bayrağı</span><span class="sxs-lookup"><span data-stu-id="2b940-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="2b940-150">-Enableprivateıpaddress</span><span class="sxs-lookup"><span data-stu-id="2b940-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="2b940-151">Sanal ağ geçidinde etkin etkin özelliği etkinleştirme bayrağı</span><span class="sxs-lookup"><span data-stu-id="2b940-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="2b940-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2b940-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="2b940-153">Zorlama tünel için kullanılacak varsayılan site.</span><span class="sxs-lookup"><span data-stu-id="2b940-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="2b940-154">Varsayılan bir site belirtilmişse, ağ geçidinin VNET 'den gelen tüm internet trafiği bu siteye yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="2b940-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="2b940-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="2b940-155">-GatewaySku</span></span>
<span data-ttu-id="2b940-156">Sanal ağ geçidi SKU 'SU</span><span class="sxs-lookup"><span data-stu-id="2b940-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="2b940-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="2b940-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="2b940-158">Sanal ağ geçidi bıgpsettings için BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="2b940-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b940-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2b940-159">-PeerWeight</span></span>
<span data-ttu-id="2b940-160">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara yapılan ağırlık</span><span class="sxs-lookup"><span data-stu-id="2b940-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="2b940-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2b940-161">-RadiusServerAddress</span></span>
<span data-ttu-id="2b940-162">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="2b940-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="2b940-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="2b940-163">-RadiusServerList</span></span>
<span data-ttu-id="2b940-164">P2S çoklu RADIUS sunucuları.</span><span class="sxs-lookup"><span data-stu-id="2b940-164">P2S multiple external Radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b940-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2b940-165">-RadiusServerSecret</span></span>
<span data-ttu-id="2b940-166">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="2b940-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="2b940-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="2b940-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="2b940-168">P2S istemcisinin AAD kimlik doğrulamasını sanal ağ ağ geçidinden kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="2b940-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="2b940-169">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2b940-169">-Tag</span></span>
<span data-ttu-id="2b940-170">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="2b940-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="2b940-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b940-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2b940-172">Değişikliklerin temel aldığı sanal ağ geçidi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2b940-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="2b940-173">Bu, Get-AzVirtualNetworkGateway kullanılarak alınabilir</span><span class="sxs-lookup"><span data-stu-id="2b940-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="2b940-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2b940-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="2b940-175">VPN istemcisinin IP adreslerini ayrılacak adres alanı.</span><span class="sxs-lookup"><span data-stu-id="2b940-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="2b940-176">Bu, sanal ağ veya şirket içi aralıklardaki çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b940-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="2b940-177">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="2b940-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="2b940-178">P2S VPN istemcisi tünel protokollerinin IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="2b940-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="2b940-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="2b940-179">-VpnClientProtocol</span></span>
<span data-ttu-id="2b940-180">P2S VPN istemci tünel protokollerinin listesi</span><span class="sxs-lookup"><span data-stu-id="2b940-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="2b940-181">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="2b940-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="2b940-182">İptal edilen VPN istemci sertifikalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="2b940-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="2b940-183">Bunlardan biriyle eşleşen bir sertifika sunan VPN istemcisi, çıkmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="2b940-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="2b940-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="2b940-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="2b940-185">VPN istemci kimlik doğrulaması için kullanılacak VPN istemcisi kök sertifikalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="2b940-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="2b940-186">VPN istemcilerinin bağlanması, bu kök sertifikalardan birinden üretilmiş sertifikaları sunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b940-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="2b940-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b940-187">-Confirm</span></span>
<span data-ttu-id="2b940-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b940-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b940-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b940-189">-WhatIf</span></span>
<span data-ttu-id="2b940-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b940-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b940-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b940-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b940-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b940-192">CommonParameters</span></span>
<span data-ttu-id="2b940-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b940-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b940-194">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b940-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b940-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b940-195">INPUTS</span></span>

### <span data-ttu-id="2b940-196">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b940-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="2b940-197">System. String</span><span class="sxs-lookup"><span data-stu-id="2b940-197">System.String</span></span>

### <span data-ttu-id="2b940-198">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b940-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="2b940-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="2b940-199">System.String[]</span></span>

### <span data-ttu-id="2b940-200">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="2b940-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="2b940-201">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifika []</span><span class="sxs-lookup"><span data-stu-id="2b940-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="2b940-202">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="2b940-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="2b940-203">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2b940-203">System.UInt32</span></span>

### <span data-ttu-id="2b940-204">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2b940-204">System.Int32</span></span>

### <span data-ttu-id="2b940-205">Microsoft. Azure. Commands. Network. model. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="2b940-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="2b940-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="2b940-206">System.Security.SecureString</span></span>

## <span data-ttu-id="2b940-207">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b940-207">OUTPUTS</span></span>

### <span data-ttu-id="2b940-208">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2b940-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2b940-209">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b940-209">NOTES</span></span>

## <span data-ttu-id="2b940-210">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b940-210">RELATED LINKS</span></span>
